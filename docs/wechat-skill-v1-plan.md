# WeChat Skill Group V1-alpha Plan

## Skill list

```text
wechat-brand-context
wechat-content-polisher
wechat-title-generator
wechat-html-css-layout
wechat-cover-generator
wechat-geo-summary
wechat-fact-checker
wechat-publish-checker
```

## Architecture

V1-alpha uses platform-specific, manually callable Skills. There is no orchestration Skill in this version.

Each Skill can be called independently according to the article's current stage.

## Image status

Column ending images and cover reference images are currently placeholders.

After real images are uploaded, update:

- `assets/wechat/ending-images/`
- `assets/wechat/cover-examples/`
- `wechat/wechat-cover-generator/references/wechat-cover-context.md`
- `wechat/wechat-html-css-layout/references/ending-image-rules.md`

## Current source material

- WeChat one-page brand document
- Existing HTML/CSS layout sample
- Skill architecture discussion
