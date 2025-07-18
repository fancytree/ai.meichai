# AI Demo Platform

A modern web platform for showcasing AI demos with easy Dify application integration.

## Features

- 🎨 Modern UI design, fully implemented according to provided design specifications
- 📱 Responsive layout supporting desktop and mobile devices
- 🔗 Support for embedding Dify applications
- ⚡ Lightweight, no complex build tools required
- 🎯 Easy to configure and customize

## Quick Start

1. Open the `index.html` file directly in your browser
2. Or use a local server:
   ```bash
   # Using Python
   python3 -m http.server 8000
   
   # Using Node.js
   npx serve .
   ```

## Configuring Dify Integration

Find the `demoConfigs` object in the `index.html` file and replace the URLs with your actual Dify application URLs:

```javascript
const demoConfigs = {
    'chat-assistant': {
        title: 'Smart Chat Assistant',
        description: 'Intelligent conversation system based on large language models',
        difyUrl: 'https://your-dify-domain.com/chatbot/your-chatbot-id' // Replace with actual URL
    },
    // ... other configurations
};
```

### How to Get Dify URL

1. Log in to your Dify console
2. Select the application you want to embed
3. Find the "Embed" or "Share" option in application settings
4. Copy the provided embed URL
5. Paste the URL into the corresponding configuration

## Custom Demos

### Adding New Demos

1. Add a new demo item in the `demos-list` section of HTML:
```html
<div class="demo-item" onclick="selectDemo(this, 'your-demo-id')">
    <div class="demo-icon">🤖</div>
    <div class="demo-name">Your Demo Name</div>
</div>
```

2. Add corresponding configuration in JavaScript `demoConfigs`:
```javascript
'your-demo-id': {
    title: 'Your Demo Title',
    description: 'Your Demo Description',
    difyUrl: 'https://your-dify-url.com'
}
```

### Modifying Styles

All styles are in the `<style>` tag, you can modify as needed:
- Color themes
- Font sizes
- Layout spacing
- Animation effects

## Project Structure

```
ai.meichai/
├── index.html          # Main page file
└── README.md          # Documentation
```

## Browser Compatibility

- Chrome 60+
- Firefox 60+
- Safari 12+
- Edge 79+

## Tech Stack

- HTML5
- CSS3 (Flexbox, Grid)
- Vanilla JavaScript
- Google Fonts (Fredoka, Inter)

## Security Considerations

- iframe embedding uses appropriate sandbox attributes
- Recommend configuring CSP headers in production environment
- Ensure Dify application URLs use HTTPS

## Troubleshooting

### Demo Cannot Load
1. Check if Dify URL is correct
2. Confirm if Dify application is published
3. Check network connection
4. View browser console error messages

### Style Display Issues
1. Confirm network connection is normal (Google Fonts requires network)
2. Check if browser supports CSS Flexbox
3. Clear browser cache

## License

MIT License

## Contact

If you have any questions or suggestions, please contact us through:
- Email: your-email@example.com
- WeChat: your-wechat-id