# LumiPluginSettingView

📖 English | [中文版](README_zh.md)

PluginSettingView is the settings view plugin: it renders the settings page shell and sidebar entry, replacing the kernel's default settings Provider.

## Features

- macOS: `AppSettingsSidebarShell` sidebar + detail two-column layout
- iOS: compact-width stacked navigation / regular-width two-column navigation
- Preserves settings entries and selection state registered before the plugin boots
- UI copy is localized via `Localizable.xcstrings` (en / zh-Hans / zh-Hant / zh-HK / zh-TW), looked up at runtime by LumiLocalization

## Dependencies

- [LumiKernel](https://github.com/CofficLab/LumiKernel) — `KernelCore`
- [LumiLocalization](https://github.com/CofficLab/LumiLocalization) — `LumiLocalizationKit` runtime localization
- [LumiSettings](https://github.com/CofficLab/LumiSettings) — `ProviderSettingView`
- [LumiUI](https://github.com/CofficLab/LumiUI) — settings page components

## Usage

```swift
import PluginSettingView

// Register the plugin in the Factory
kernel.boot(PluginSettingView())
```

## Tests

```bash
swift test
```
