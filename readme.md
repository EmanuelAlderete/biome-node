# @emanuelalderete/biome-node

> ✅ A shared [Biome](https://biomejs.dev/) configuration for consistent formatting and linting across JavaScript and TypeScript projects.

This package provides a reusable Biome configuration preset that you can extend in your projects to enforce consistent code style, formatting, and linting rules.

---

## ✨ Features

- Consistent formatting with Biome's fast formatter
- Recommended linting rules enabled
- Supports both JavaScript and TypeScript
- Simple to extend and override
- Easy setup across multiple repositories

---

## 📦 Installation

```bash
npm install --save-dev @emanuelalderete/biome-node
````

---

## 🛠 Usage

In your project's root, create a `biome.json` file:

```json
{
  "extends": "@emanuelalderete/biome-node"
}
```

Biome will automatically load and apply the rules from this preset.

---

## 🧪 Example Configuration

This package includes:

```jsonc
{
	"$schema": "https://biomejs.dev/schemas/2.0.5/schema.json",
	"vcs": {
		"enabled": false,
		"clientKind": "git",
		"useIgnoreFile": false
	},
	"files": {
		"ignoreUnknown": false
	},
	"formatter": {
		"enabled": true,
		"indentStyle": "tab"
	},
	"linter": {
		"enabled": true,
		"rules": {
			"recommended": true
		}
	},
	"javascript": {
		"formatter": {
			"quoteStyle": "single",
			"semicolons": "asNeeded"
		}
	},
	"assist": {
		"enabled": true,
		"actions": {
			"source": {
				"organizeImports": "on"
			}
		}
	}
}
```

You can still add custom rules in your project by extending this config.

---

## 🧩 Overriding Rules

Need project-specific customizations? Just extend and override as needed:

```json
{
  "extends": "@emanuelalderete/biome-node",
  "linter": {
    "rules": {
      "style": {
        "noUnusedVariables": "warn"
      }
    }
  }
}
```

---

## 📚 About Biome

Biome is an all-in-one toolchain for web development. It replaces ESLint, Prettier, and Babel with a single fast and native implementation.

Learn more: [https://biomejs.dev](https://biomejs.dev)

---

## 📄 License

MIT License © [Emanuel Alderete](https://github.com/EmanuelAlderete)