# Setting up Render with an has-a.space Subdomain

This guide will walk you through the process of setting up a Render deployment and pointing your has-a.space subdomain towards it.

## Creating a Render Service

First, create a service on Render. Follow the instructions in the [Render Documentation](https://docs.render.com/).

### Creating the Domain File

Create a JSON file inside the `domains` directory (`domains/subdomain.json`) with the following content and submit a pull request:

```json
{
    "owner": {
        "username": "your-github-username"
    },
    "records": {
        "A": ["216.24.57.1"]
    }
}
```

**Note:** Don't forget to provide a preview of your website in your pull request.

## Configuring Render

- After your pull request is merged, you may need to configure your Render service to use the new subdomain. Go to your Render service's dashboard.
- Navigate to **Settings > Custom Domains** and add `subdomain.has-a.space` in the given field.
- Render will provide a verification step, usually requiring you to add a DNS record. This step should be skipped if your subdomain is already pointing to Render's IP address (`216.24.57.1`).

### Final Steps

- Wait for the DNS changes to propagate. This can take from a few minutes to a couple of hours.
- Your Render service should now be accessible at `subdomain.has-a.space`.
