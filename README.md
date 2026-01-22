# GoatCounter Analytics for TRMNL

Display your [Goatcounter](https://goatcounter.com) web analytics on your TRMNL e-ink device. 
GoatCounter is an open-source, privacy-conscious web analytics platform that provides meaningful statistics without tracking personal data or using cookies—making it the perfect companion for a minimalist e-ink display.

<img width="1392" height="856" alt="image" src="https://github.com/user-attachments/assets/52742907-2e24-4910-beae-a0d7f8d16e68" />


## Features

* Line chart of daily visits over the current cycle
* Dual customizable sidebar slots for top pages, referrers, countries, or systems
* Selectable header metric for today's visits or top system/browser/country
* High-contrast design optimized for e-ink readability
* Robust JavaScript implementation compatible with TRMNL mashups

## Setup

### 1. Get Your GoatCounter API Token

* Sign in to your GoatCounter account.
* Navigate to Settings > API.
* Create a new API token with "Read" permissions for statistics.
* Note your site code (the subdomain of your dashboard).

### 2. Install the Plugin

Add the plugin manually to your TRMNL dashboard using the provided YAML and Liquid files in this repository.

### 3. Configure

* **Site Code**: Enter your GoatCounter site identifier.
* **API Token**: Paste your generated API token.
* **Top Right Stat**: Choose between Today's Visits, Top Country, Top System, or Top Browser.
* **Right Section Slots**: Use the dropdowns to select which two metrics (Pages, Referrers, Countries, etc.) to prioritize in the sidebar.

## Local Development

1. Copy the example configuration:
   `cp trmnlp.yml.example .trmnlp.yml`

2. Edit `.trmnlp.yml` with your test credentials and preferences:
   ```yaml
   custom_fields:
     site: "your-site-code"
     api_token: "your-api-token"
     top_stat_display: "today"
     right_section_1: "pages"
     right_section_2: "referrers"

3. Run the development server:

```bash
docker run \
  --publish 8001:4567 \
  --volume "$(pwd):/plugin" \
```


## Support

If you find this plugin useful, consider supporting my work: [r1l.in/s](https://r1l.in/s)

**Need a custom TRMNL plugin for your business?** I'm available for contract work. Reach out at hello@rishikeshs.com.

## License

MIT
