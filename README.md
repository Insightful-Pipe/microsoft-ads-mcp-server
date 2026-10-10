# Microsoft Ads MCP Server (Bing Ads) by Insightful Pipe

[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-blue)](https://insightfulpipe.com/mcp-servers/microsoft-ads)
[![Insightful Pipe](https://img.shields.io/badge/Insightful_Pipe-MCP_Servers-purple)](https://insightfulpipe.com/mcp-servers)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Connect Microsoft Ads to AI assistants for Bing search advertising analytics and campaign optimization.**

Part of the [Insightful Pipe MCP Server Collection](https://insightfulpipe.com/mcp-servers) — The Microsoft Ads MCP server enables Claude, ChatGPT, Cursor, and other AI assistants to analyze your Microsoft Advertising campaigns. Reach users on Bing, Yahoo, and Microsoft properties with AI-powered insights.

[![Explore All MCP Servers](https://img.shields.io/badge/Explore_All-MCP_Servers-blue?style=for-the-badge)](https://insightfulpipe.com/mcp-servers)

![Microsoft Ads MCP Server](https://insightfulpipe.com/images/microsoft-ads-icon.svg)

## MCP Server URL

```
https://microsoft-ads.insightfulmcp.com/
```

## What is Microsoft Ads MCP?

Microsoft Ads MCP is a **remote Model Context Protocol server** that connects your Microsoft Advertising account to AI assistants. This search advertising integration allows you to:

- Query Bing Ads performance using natural language
- Analyze keyword and audience performance
- Generate detailed performance reports
- Track ROAS across Microsoft Search Network
- Get AI recommendations for campaign optimization

## Installation

### Claude

1. Copy the MCP Server URL: `https://microsoft-ads.insightfulmcp.com/`
2. Open [Claude Connectors Settings](https://claude.ai/settings/connectors)
3. Scroll to the bottom and click **Add custom connector**
4. Paste the URL and click **Add**
5. Click **Connect** and sign in to InsightfulPipe if asked. Claude then lists the connector as connected.

### ChatGPT

Custom MCP servers are added through ChatGPT's **Developer mode**. Availability depends on your ChatGPT plan, and workspace admins may need to allow it.

1. Turn on **Developer mode** in ChatGPT settings
2. Create a new app for a remote MCP server and paste the URL: `https://microsoft-ads.insightfulmcp.com/`
3. Sign in to InsightfulPipe if asked. The connection finishes as soon as you are signed in.

See OpenAI's guide: [Developer mode and MCP apps in ChatGPT](https://help.openai.com/en/articles/12584461-developer-mode-and-mcp-apps-in-chatgpt)

### Claude Code

```bash
claude mcp add --transport http microsoft-ads https://microsoft-ads.insightfulmcp.com/
```

### Cursor

Add the server to `~/.cursor/mcp.json` (all projects) or `.cursor/mcp.json` (one project):

```json
{
  "mcpServers": {
    "microsoft-ads": {
      "url": "https://microsoft-ads.insightfulmcp.com/"
    }
  }
}
```

When Cursor shows **Needs authentication**, click **Connect** and sign in to InsightfulPipe if asked.

## Available Actions

90 actions: 34 read, 56 write.

### Read Actions (34)

<details>
<summary>Show all 34 read actions</summary>

| Action | Description |
|--------|-------------|
| `get_ad_extension_associations` | Get ad extension associations for specific entities |
| `get_ad_extensions` | Get ad extensions for an account by type |
| `get_ad_group_criterions` | Get targeting criteria for an ad group |
| `get_ad_groups` | Get ad groups for a campaign |
| `get_ads` | Get ads for an ad group |
| `get_asset_groups` | Get asset groups for a Performance Max campaign |
| `get_audiences` | Get audience lists for an account |
| `get_bid_strategies` | Get portfolio bid strategies for an account |
| `get_budgets` | Get shared budgets for an account |
| `get_campaign_criterions` | Get targeting criteria for a campaign |
| `get_campaigns` | Get campaigns for an account |
| `get_conversion_goals` | Get conversion goals for an account |
| `get_experiments` | Get campaign experiments for an account |
| `get_keywords` | Get keywords for an ad group |
| `get_label_associations` | Get label associations for specific entities |
| `get_labels` | Get labels for an account |
| `get_negative_keywords_by_entity_ids` | Get negative keywords associated with campaigns or ad groups |
| `get_shared_entities` | Get shared negative keyword lists for an account |
| `get_shared_entity_associations` | Get associations between shared entities and campaigns |
| `get_shared_list_items` | Get items (negative keywords) in a shared list |
| `get_uet_tags` | Get Universal Event Tracking tags for an account |
| `poll_report_status` | Poll for report generation status and fetch data when ready |
| `search_accounts` | Search for advertising accounts the user has access to |
| `submit_account_performance_report` | Submit an account performance report request |
| `submit_ad_group_performance_report` | Submit an ad group performance report request |
| `submit_ad_performance_report` | Submit an ad performance report request |
| `submit_age_gender_audience_report` | Submit an age and gender audience report request |
| `submit_audience_performance_report` | Submit an audience performance report request |
| `submit_campaign_performance_report` | Submit a campaign performance report request |
| `submit_geographic_performance_report` | Submit a geographic performance report request |
| `submit_goals_and_funnels_report` | Submit a goals and funnels report request |
| `submit_keyword_performance_report` | Submit a keyword performance report request |
| `submit_search_query_performance_report` | Submit a search query performance report request |
| `submit_user_location_performance_report` | Submit a user location performance report request |

</details>

### Write Actions (56)

<details>
<summary>Show all 56 write actions</summary>

| Action | Description |
|--------|-------------|
| `add_ad_extensions` | Create ad extensions in an account |
| `add_ad_group_criterions` | Add targeting criteria to ad groups (location, device, demographics, audience, etc.) |
| `add_ad_groups` | Create new ad groups in a campaign |
| `add_ads` | Create new ads in an ad group |
| `add_asset_groups` | Create asset groups for Performance Max campaigns |
| `add_audience_groups` | Create audience groups for targeting |
| `add_audiences` | Create audience lists (remarketing, customer match, etc.) |
| `add_bid_strategies` | Create portfolio bid strategies |
| `add_budgets` | Create new shared budgets in an account |
| `add_campaign_conversion_goals` | Associate conversion goals with campaigns |
| `add_campaign_criterions` | Add targeting criteria to campaigns (location, device, demographics, etc.) |
| `add_campaigns` | Create new campaigns in an account |
| `add_conversion_goals` | Create conversion goals for tracking |
| `add_conversion_value_rules` | Create conversion value rules for adjusting conversion values |
| `add_data_exclusions` | Create data exclusions to exclude time periods from bid strategy learning |
| `add_experiments` | Create campaign experiments for A/B testing |
| `add_keywords` | Create new keywords in an ad group |
| `add_labels` | Create new labels in an account |
| `add_list_items_to_shared_list` | Add negative keywords to an existing shared list |
| `add_negative_keywords_to_entities` | Add negative keywords to campaigns or ad groups |
| `add_seasonality_adjustments` | Create seasonality adjustments to inform bid strategies of expected conversion rate changes |
| `add_shared_entity` | Create a shared negative keyword list |
| `add_uet_tags` | Create Universal Event Tracking tags for conversion tracking |
| `apply_customer_list_items` | Add or remove items from a customer list audience |
| `apply_hotel_group_actions` | Apply add/update/delete actions to hotel group nodes |
| `apply_offline_conversion_adjustments` | Adjust previously submitted offline conversions |
| `apply_offline_conversions` | Submit offline conversion data |
| `apply_product_partition_actions` | Apply add/update/delete actions to product partition nodes in a Shopping campaign |
| `delete_keywords` | Delete keywords from an ad group |
| `delete_list_items_from_shared_list` | Remove individual negative keywords, by list item id, from a shared list without touching the list or its associations |
| `delete_negative_keywords_from_entities` | Remove specific negative keywords, by id, from campaigns or ad groups |
| `set_account_properties` | Set account-level properties (auto-tagging, tracking templates, etc.) |
| `set_ad_extension_associations` | Associate ad extensions with campaigns or ad groups |
| `set_label_associations` | Associate labels with campaigns, ad groups, ads, or keywords |
| `set_negative_sites_to_ad_groups` | Set negative site URLs for ad groups (replaces existing) |
| `set_negative_sites_to_campaigns` | Set negative site URLs for campaigns (replaces existing) |
| `set_shared_entity_associations` | Associate shared negative keyword lists with campaigns |
| `update_ad_extensions` | Update existing ad extensions |
| `update_ad_group_criterions` | Update targeting criteria on ad groups |
| `update_ad_groups` | Update existing ad groups |
| `update_ads` | Update existing ads |
| `update_asset_groups` | Update existing asset groups |
| `update_audience_groups` | Update existing audience groups |
| `update_audiences` | Update existing audience lists |
| `update_bid_strategies` | Update existing portfolio bid strategies |
| `update_budgets` | Update existing shared budgets |
| `update_campaign_criterions` | Update targeting criteria on campaigns |
| `update_campaigns` | Update existing campaigns |
| `update_conversion_goals` | Update existing conversion goals |
| `update_conversion_value_rules` | Update existing conversion value rules |
| `update_data_exclusions` | Update existing data exclusions |
| `update_experiments` | Update existing experiments |
| `update_keywords` | Update existing keywords |
| `update_labels` | Update existing labels |
| `update_seasonality_adjustments` | Update existing seasonality adjustments |
| `update_uet_tags` | Update existing UET tags |

</details>

## Control What Your AI Can Do

You decide what AI agents can do with each connected account:

- **Turn individual actions on or off** for every connected account, so agents only see the actions you allow.
- **Connect as Read-only or Read & Write.** A read-only connection can only enable read actions.
- **Destructive actions stay off by default.** Actions such as deletes are disabled until an admin enables them.
- **Team access per account.** Restricted team members only use the accounts they are granted, with the read actions enabled on them.

## Usage Examples

### Campaign Performance

```
"How are my Microsoft Ads campaigns performing this month?"
```

### Keyword Analysis

```
"What are my top converting keywords on Bing?"
```

### Generate Reports

```
"Generate a keyword performance report for the last 30 days"
```

### Audience Performance

```
"Show me performance by age and gender demographics"
```

### Geographic Analysis

```
"Which locations have the best ROAS?"
```

## Supported Metrics

| Metric | Description |
|--------|-------------|
| Impressions | Total ad impressions |
| Clicks | Total ad clicks |
| CTR | Click-through rate |
| CPC | Cost per click |
| Conversions | Tracked conversions |
| ROAS | Return on ad spend |
| Quality Score | Keyword quality rating |
| Impression Share | Share of available impressions |

## Why Microsoft Ads MCP?

### For Search Marketers
- **Bing insights** - Often overlooked search channel
- **Lower CPCs** - Typically cheaper than Google
- **Comprehensive reports** - 10+ report types available

### For B2B Marketers
- **LinkedIn targeting** - Professional audience data
- **Decision makers** - Job title and company targeting
- **Enterprise reach** - Windows and Office users

### For Agencies
- **Multi-account management** - Handle client portfolios
- **Automated reporting** - Generate any report type
- **Cross-platform comparison** - Bing vs Google insights

## Security & Privacy

- **Official Microsoft Advertising API** - Direct integration with Microsoft's API
- **OAuth 2.0** - Secure Microsoft authentication

## Pricing

The Microsoft Ads MCP server is included in every InsightfulPipe plan, together with all other MCP servers and the CLI. Plans start at $29.99/month, and you can try it for 7 days. See [insightfulpipe.com/pricing](https://insightfulpipe.com/pricing) for current plans.

## Explore More MCP Servers by Insightful Pipe

Visit **[insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)** to discover our full collection of MCP servers for marketing and analytics.

### Search Advertising MCP Servers
- [Google Ads MCP](https://insightfulpipe.com/mcp-servers/google-ads) - Google search advertising
- [Google Search Console MCP](https://insightfulpipe.com/mcp-servers/google-search-console) - SEO analytics

### B2B & Analytics MCP Servers
- [LinkedIn Ads MCP](https://insightfulpipe.com/mcp-servers/linkedin-ads) - B2B advertising
- [Google Analytics MCP](https://insightfulpipe.com/mcp-servers/google-analytics) - Website analytics

**[View All MCP Servers →](https://insightfulpipe.com/mcp-servers)**

## Resources

- [Documentation](https://insightfulpipe.com/docs/connectors-microsoft-ads)
- [Video Tutorial](https://www.youtube.com/playlist?list=PLJNzvjxzI5Xwe__BJJLAelSF0ewO3mEFk)
- [InsightfulPipe Blog](https://insightfulpipe.com/blog)

## Support

- **Documentation**: [insightfulpipe.com/docs](https://insightfulpipe.com/docs)
- **All MCP Servers**: [insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)
- **Email**: support@insightfulpipe.com

---

**[Insightful Pipe](https://insightfulpipe.com)** — AI-powered marketing analytics through MCP servers. [Explore all integrations →](https://insightfulpipe.com/mcp-servers)

## License

MIT License - see [LICENSE](LICENSE) for details.
