# Basic-DNS-Setup
https://roadmap.sh/projects/basic-dns

https://github.com/CPSmoke/gh-deployment-workflow
Step 1: Obtain a Domain Name

If you don't have a domain name yet, you can purchase one from any domain registrar such as Cloudflare, Namecheap, or GoDaddy. After purchasing the domain, you will gain access to your domain's DNS settings.

Step 2: Configure DNS Records

Log into your domain registrar account.

Go to the DNS management section for your domain.

Add the following records:

A records to point to GitHub Pages IP addresses:

    @   185.199.108.153
    @   185.199.109.153
    @   185.199.110.153
    @   185.199.111.153

CNAME record to point to your GitHub Pages:

    www   <your_username>.github.io.

  Replace <your_username> with your GitHub username.

Step 3: Setup GitHub Pages to Use the Custom Domain

Go to your repository settings on GitHub.

Find the GitHub Pages section.

Enter your new domain name in the "Custom domain" field and click "Save."

Step 4: Change Records in hugo.toml

    baseURL = 'yourdomain'  
    languageCode = 'en-us'  
    title = 'My New Hugo Site'
 
Step 5: Verify Configuration

Wait for a while (usually from a few minutes to an hour) for the DNS records to update.

Visit your domain in a browser to check if it is working correctly and redirecting to your GitHub Pages site.

Step 6: HTTPS (optional)

Once you confirm that your domain is working correctly, you can enable HTTPS:

Check the "Enforce HTTPS" box in the GitHub Pages settings if it is available.

https://github.com/CPSmoke/Static-Site-Server
