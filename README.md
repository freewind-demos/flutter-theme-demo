# Flutter 主题（ThemeData）

## 简介

在 `MaterialApp` 上传入 **`ThemeData`**：`primarySwatch: Colors.blue` 与 `brightness: Brightness.dark`，整页随之使用深色 Material 配色。

## 快速开始

### 环境要求

Flutter SDK。

### 运行

```bash
flutter pub get
flutter run
```

## 概念讲解

### 第一部分：`ThemeData` 与组件默认值

`AppBar`、`Button` 等会读取主题里的颜色、`textTheme`。只改少数字段时，也可用 `ThemeData(...).copyWith`。

### 第二部分：明暗与 `ColorScheme`

新版 Material 3 推荐更多使用 `colorScheme`；`primarySwatch` 仍常见于旧文档与快原型。

## 完整示例

见 `lib/main.dart`：`MaterialApp(theme: ThemeData(...))`。

## 注意事项

- 亮暗切换通常配合 `theme` 与 `darkTheme` 以及 `themeMode`。
- 设计系统很大时，可把 Token 放扩展 `ThemeExtension`。

## 完整讲解（中文）

主题解决的是 **一批组件的默认长相**。与其每个 `Text` 手写颜色，不如在 `ThemeData` 定规则。Demo 用深色 + 蓝色主色，让你肉眼看到「一处配置，处处生效」。产品要求换肤时，改主题比改散落的 `Color(0xFF...)` 安全得多。
