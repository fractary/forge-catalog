# Fractary Forge Catalog

Official catalog of bundles and starters for [Fractary Forge](https://github.com/fractary/forge.fractary.com).

🌐 **Live Catalog**: [https://fractary.github.io/forge-catalog/](https://fractary.github.io/forge-catalog/)

## 🚀 Quick Start

Add this catalog to your Forge CLI:

```bash
forge config add-catalog https://fractary.github.io/forge-catalog/catalog.json --name "Fractary Official"
```

Then browse available assets:

```bash
# List all assets
forge list

# Search for specific assets
forge search auth
forge search --type=bundle engineering
```

## 📦 Available Assets

### Bundles

| Bundle | Description | Install Command |
|--------|-------------|----------------|
| **agents-engineering** | AI-powered engineering agents and development utilities | `forge install fractary/forge-bundle-agents-engineering` |
| **claude-code-notifier** | Notification system for Claude Code sessions | `forge install fractary/forge-bundle-claude-code-notifier` |

### Starters

| Starter | Description | Create Command |
|---------|-------------|----------------|
| **www-astro-blog** | Modern blog built with Astro, TypeScript, and Tailwind | `forge create my-blog --starter fractary/forge-starter-www-astro-blog` |

## 📋 Catalog Structure

The catalog follows the Forge Catalog Specification v1.0:

```json
{
  "version": "1.0.0",
  "name": "Catalog Name",
  "description": "Catalog description",
  "bundles": [...],
  "starters": [...]
}
```

### Bundle Entry

```json
{
  "id": "bundle-id",
  "name": "Bundle Name",
  "description": "Bundle description",
  "repository": "owner/repo-name",
  "version": "1.0.0",
  "tags": ["tag1", "tag2"],
  "private": false
}
```

### Starter Entry

```json
{
  "id": "starter-id",
  "name": "Starter Name",
  "description": "Starter description",
  "repository": "owner/repo-name",
  "version": "1.0.0",
  "framework": "astro",
  "tags": ["tag1", "tag2"],
  "private": false
}
```

## 🔌 API Access

### Direct Catalog Access

The catalog is available via HTTP GET:

```bash
curl https://fractary.github.io/forge-catalog/catalog.json
```

### Using with Forge CLI

```javascript
// Example: Fetching catalog programmatically
const response = await fetch('https://fractary.github.io/forge-catalog/catalog.json');
const catalog = await response.json();

console.log(`Available bundles: ${catalog.bundles.length}`);
console.log(`Available starters: ${catalog.starters.length}`);
```

## 🤝 Contributing

Want to add your bundle or starter to the catalog?

### Requirements

1. **Repository Naming**:
   - Bundles: `forge-bundle-{name}`
   - Starters: `forge-starter-{name}`

2. **Required Files**:
   - Bundles: `bundle.manifest.json`
   - Starters: `starter.manifest.json`

3. **Documentation**:
   - Clear README with usage instructions
   - License file
   - Examples (optional but recommended)

### Submission Process

1. Ensure your bundle/starter meets the requirements
2. Fork this repository
3. Add your entry to `catalog.json`
4. Submit a pull request

### Entry Template

```json
{
  "id": "your-asset-id",
  "name": "Your Asset Name",
  "description": "Clear description of what your asset does",
  "repository": "yourorg/forge-bundle-your-asset",
  "version": "1.0.0",
  "tags": ["relevant", "tags"],
  "keywords": ["search", "keywords"],
  "license": "MIT",
  "homepage": "https://github.com/yourorg/forge-bundle-your-asset",
  "private": false
}
```

## 🔍 Quality Guidelines

To be included in the official catalog, assets should:

1. **Work Out of Box**: Install without errors
2. **Be Well Documented**: Clear README and usage instructions
3. **Follow Best Practices**: Proper file structure and naming
4. **Include Examples**: Show how to use the asset
5. **Specify License**: Clear licensing terms
6. **Use Semantic Versioning**: Tag releases properly

## 🏷️ Metadata Fields

### Required Fields

- `id`: Unique identifier for the asset
- `name`: Human-readable name
- `description`: Clear description
- `repository`: GitHub repository path
- `version`: Current version

### Optional Fields

- `author`: Author information
- `tags`: Array of tags for categorization
- `keywords`: Search keywords
- `categories`: Asset categories
- `license`: License type
- `homepage`: Project homepage
- `demo`: Live demo URL (for starters)
- `private`: Whether private access is required
- `verified`: Verification status
- `official`: Official Fractary asset
- `downloads`: Download count
- `rating`: User rating

## 🛠️ Development

### Local Testing

1. Clone this repository:
```bash
git clone https://github.com/fractary/forge-catalog.git
cd forge-catalog
```

2. Test with local Forge CLI:
```bash
forge config add-catalog file:///path/to/forge-catalog/catalog.json --name "Local Test"
forge list
```

3. Validate catalog structure:
```bash
# Validate JSON syntax
python -m json.tool catalog.json

# Or use jq
jq '.' catalog.json
```

### GitHub Pages Setup

This catalog is automatically published to GitHub Pages:

1. Repository Settings → Pages
2. Source: Deploy from branch
3. Branch: main / root
4. URL: https://fractary.github.io/forge-catalog/

## 📜 License

This catalog is licensed under the MIT License. Individual bundles and starters may have their own licenses.

## 🔗 Links

- [Fractary Forge CLI](https://github.com/fractary/forge.fractary.com)
- [Bundle Creation Guide](https://github.com/fractary/forge.fractary.com/blob/main/docs/guides/forge-bundle-creation-guide.md)
- [GitHub Distribution Guide](https://github.com/fractary/forge.fractary.com/blob/main/docs/guides/github-distribution-guide.md)
- [Fractary Website](https://fractary.com)

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/fractary/forge-catalog/issues)
- **Discussions**: [GitHub Discussions](https://github.com/fractary/forge-catalog/discussions)
- **Email**: forge@fractary.com

---

Built with ❤️ by the Fractary team for the developer community.# forge-catalog
