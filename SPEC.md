# 间隔复习系统 · SPEC

上线地址：https://sran995.github.io/spaced-repetition/

## 概述
基于艾宾浩斯遗忘曲线的复习系统，支持概念理解和精确记忆两种模式，多账号（PIN保护），自由创建模块。

## 技术栈
- 单一 HTML 文件，纯前端，零依赖
- 数据存储：浏览器 localStorage（5MB）
- AI 翻译/判断：可选，浏览器直调 DeepSeek/Claude API
- 部署：GitHub Pages

## 核心功能
- 艾宾浩斯间隔复习（1-2-4-7-15-30 天）
- 三种掌握等级（记得/勉强/忘了），连续勉强 5 天自动降级
- 英语模块：双向互译（中→英精确比对，英→中语义判断）
- 概念理解：左右对照式（左定义、右回答），支持 AI 自动判断（需 API Key）
- 语音输入（浏览器 Web Speech API）
- 数据导出/导入（JSON 备份恢复）

## 账号体系
- 应用内部多账号（账号名 + 4 位 PIN）
- 数据在 localStorage 中按账号隔离（不同浏览器天然隔离）

## 维护
修改 `index.html` → commit → push → GitHub Pages 自动更新
