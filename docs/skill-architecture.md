# Skill Architecture

## Architecture decision

This project uses a platform-specific Skill matrix.

Instead of building one general content production Skill or one orchestration Skill, each platform has its own Skill group. The creator manually calls the appropriate Skill according to the content's current stage.

## Why no orchestration Skill in V1

The current workflow is exploratory and non-linear. A single article may need title optimization first, then fact-checking, then layout, then another round of polishing.

Therefore, V1 prioritizes independent, callable Skills over a fixed workflow.

## WeChat Official Account Skill Group V1

```text
wechat/
├── wechat-brand-context/
├── wechat-content-polisher/
├── wechat-title-generator/
├── wechat-html-css-layout/
├── wechat-cover-generator/
├── wechat-geo-summary/
├── wechat-fact-checker/
└── wechat-publish-checker/
```

## Skill dependency principle

Skills should not strongly depend on runtime access to other Skills.

Recommended implementation:

1. Keep a master brand context Skill for each platform.
2. Extract task-specific context snippets into each specialized Skill.
3. Make every specialized Skill independently usable.
4. Use a publish checker Skill for final cross-module review.

## Future extension

Each new platform should follow the same pattern:

```text
platform/
├── platform-brand-context/
├── platform-content-skill-a/
├── platform-content-skill-b/
└── platform-publish-checker/
```
