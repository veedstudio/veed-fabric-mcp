# Make Setup

Connect VEED Fabric to Make (formerly Integromat) to generate AI talking head videos in your scenarios.

## Setup

1. Log in to [make.com](https://www.make.com) and open a scenario
2. Add the **MCP Client** module to your scenario
3. Click **Create a connection**
4. In the **MCP Server** field, select **+ New MCP Server**
5. Enter connection details:
   - **URL:** `https://www.veed.io/api/v1/mcp`
6. If prompted for an OAuth redirect URI, add: `https://www.make.com/oauth/cb/mcp`
7. Click **Save** and authenticate with your VEED account
8. Authorize Make to access your workspace

## What You Get

Once connected, Make automatically discovers all VEED Fabric tools:

- **create_fabric_video** - Create talking head videos
- **confirm_fabric_video** - Confirmation widget for parameters
- **get_generation_status** - Check video generation progress
- **list_voices** - Browse available voices
- **list_workspaces** - List your workspaces
- **get_credit_balance** - Check your AI credits

## Usage

Use the **Call a Tool** module to explicitly invoke any VEED Fabric tool by name. Select the tool from the list and map your scenario data to its input fields.

Make also offers an **Execute an Action with AI** module, which uses AI to automatically select and run the right tool based on a prompt. This can be useful for more dynamic scenarios where you want AI-driven tool selection.

Example prompts for the AI module:

- "Make a talking head video introducing our new product"
- "Create a video in Spanish about our company"
- "How many AI credits do I have left?"

See [Authentication](./authentication) for more details.

## Costs

- **Make:** Each MCP tool call consumes operations on your Make plan. Check [Make pricing](https://www.make.com/en/pricing) for details.
- **VEED:** AI Playground credits (per video generation)

## Troubleshooting

### Connection Issues

If you can't connect to the MCP server:

- Verify the URL: `https://www.veed.io/api/v1/mcp`
- Make sure you selected **+ New MCP Server** (not a pre-existing server)
- Try removing and re-adding the MCP Client module

### Authentication Errors

If OAuth fails:

- Clear browser cookies and try again
- Make sure you're using a VEED account with an active workspace
- Check that your VEED account has AI Playground credits

### Tool Discovery

If tools don't appear:

- Disconnect and reconnect the MCP server connection
- Verify your VEED account is authenticated
- Re-open the module settings to refresh the tool list

Need help? Contact support at hello@veed.io
