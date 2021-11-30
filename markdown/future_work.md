
## Future Work

These are the features we didn't quite get to

### Additional Functionality
- The "Edit" interface does not currently support changing the item's image. This could easily be added.
- Sorting the home-page by most-recent items first
  - This could easily be added with a simple search filter. Probably. We aren't sure what metadata GCP Datastore stores with entities (does it keep track of date created/modified?). Although we could add those fields ourselves, and then sort the results
  - In the same vein, pagination (if the website ever grew to thousands of items, only loading the first ~20 or so per-page would help with loading times).

### Security Functionality

- *Actually* verifying whether users had valid GT emails / GTID numbers
  - Obviously we can't check GTID numbers, but it would have been doable to verify emails. We could have sent an email to their address with a unique link, and then we would add a controller to read that link, which would activate the user account associated with that link. However, this would have taken more time to implement, so we didn't.
- HTTPS for the web server
  - This would have taken more time to implement, as we would have to use something like Let's Encrypt to get a CA certificate. Additionally, we would need our own domain name.
  - Although, we could have achieved this if we had deployed through a hosting provider that supports SSL and subdomains. Instead, we just hosted it on a random AWS Lightsail server one of us had lying around.

### Maintenance

- Automated unit tests would be useful in catching regression errors. Especially with merge conflicts, it is very easy to make mistakes. Automated tests and/or Continuous Integration would help us catch those errors more quickly (preferrably before pull-requests are completed) to ensure that we don't mess up each others' features.