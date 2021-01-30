---
title: macOS Handbook - Bing Jeung
description: macOS Handbook
keywords: Bing Jeung, macOS, handbook
---

Change macOS screenshot saving location
```bash
defaults write com.apple.screencapture location ~/Downloads/
```


Font Smoothing
```bash
defaults write -g CGFontRenderingFontSmoothingDisabled -bool NO
defaults -currentHost write -globalDomain AppleFontSmoothing -int 2

defaults read -g CGFontRenderingFontSmoothingDisabled
defaults -currentHost read -globalDomain AppleFontSmoothing
```


Delete `.DS_Store`
```bash
find . -name '.DS_Store' -type f -delete
```
