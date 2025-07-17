# FreshRSS Self-hosted RSS Reader

## Introduction

FreshRSS is a powerful, easy-to-use self-hosted RSS reader that allows you to effortlessly keep track of updates from your favorite websites. It features a clean and tidy interface, supports multiple users, and offers robust filtering capabilities. This template enables you to deploy FreshRSS on the ClawCloud platform with a single click.

## Features

- 🔄 Easily import/export OPML subscription files
- 🌐 Multi-language interface support
- 👥 Multi-user capability
- 🔍 Powerful article filtering and search functions
- 📱 Responsive design suitable for mobile devices
- 🔌 Extensible plugin system
- 🔒 Secure and reliable, safeguarding your reading privacy

## Deployment Instructions

### Resource Requirements

- CPU: Minimum 100m, Maximum 1000m
- Memory: Minimum 102Mi, Maximum 1024Mi
- Storage: Default 1Gi (customizable during deployment)

### Configuration Parameters

You can customize the following parameter during deployment:

- **volume_size**: Data storage size (default 1Gi)

### Environment Variables

The template comes with the following predefined environment variables:

- `TZ`: Asia/Shanghai - Set timezone
- `PUID`: 1000 - Process user ID
- `PGID`: 1000 - Process group ID

### Storage Volumes

The template creates the following storage volumes:

- `/config`: Main configuration data storage

### Network Configuration

- Publicly exposed port: 80
- DNS servers: 8.8.8.8 and 8.8.4.4

## First-time Use

1. After successful deployment, visit the provided URL
2. Follow the setup wizard to configure the admin account and basic settings
3. Add your favorite RSS feeds
4. Start enjoying your personalized news reading experience!

## Adding RSS Feeds

1. After logging in, click "Feed Management" in the left menu
2. Click the "New Feed" button
3. Enter the URL of the RSS feed
4. Optionally assign a category to the feed
5. Click "Subscribe" to complete the addition

## Usage Tips

- Use keyboard shortcuts (j/k) to navigate through articles
- Create filters to avoid information overload
- Use the tag system to organize and categorize articles
- Customize your reading view (compact, standard, or reading mode)
- Try installing community-developed extensions for enhanced functionality

## Frequently Asked Questions

**Q: How do I update FreshRSS?**  
A: When a new version is released, redeploy this template to get the latest version. Your data and configurations will be preserved.

**Q: How do I back up my data?**  
A: All FreshRSS data is stored in the `/config` directory. Ensure this directory is backed up regularly.

**Q: How do I add extension plugins?**  
A: Log in as an admin and navigate to "Extension Management" to install official or third-party extensions, and your Extension will be stored in the `/config/app/www/extensions`.

## Support and Feedback

- Official Documentation: [FreshRSS Documentation](https://freshrss.github.io/FreshRSS/en/)
- Project Repository: [GitHub](https://github.com/FreshRSS/FreshRSS)
- Feedback: [GitHub Issues](https://github.com/FreshRSS/FreshRSS/issues)

---

Enjoy your experience!
