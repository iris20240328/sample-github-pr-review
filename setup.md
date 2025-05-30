
✅ Step 1: Update GitHub Webhook
1. Go to your GitHub repo (e.g., `https://github.com/your-user/sample-github-pr-review`)

2. Navigate to:
    `Settings > Webhooks > Add webhook`

3. Fill in the details:
    * Payload URL:
      `http://localhost:5678/webhook/github-pr`
    * Content type: `application/json`
    * Secret: (optional)
    * Events: Choose `Let me select individual events` and check **Pull requests**
    * Click **Add webhook**

✅ Step 2: Create/Update Credentials in n8n
🔐 **GitHub Token**
1. In n8n, go to **Credentials**
2. Create a Generic Credential for GitHub:
    * Name: `GitHub Token`
    * Type: `HTTP Basic Auth`
    * Username: `x-access-token`
    * Password: (your GitHub personal access token with `repo` scope)

🔐 **OpenAI Key**
1. Create another HTTP Basic Auth Credential:
   * Name: `OpenAI API Key`
   * Username: `Bearer`
   * Password: (your OpenAI API key)


