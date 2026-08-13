# Changelog

All notable changes to the Varbase News Base recipe are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.0.0-alpha2] - 2026-08-13
### Fixed
- Correct invalid `card-featured` prop values so the news featured cards render. All five
  `canvas.content_template.node.news.featured_card_*` templates shipped prop values the
  `card-featured` component does not allow — `content_vertical_alignment:
  justify-content-center`, which is not in the `align-items-start` / `align-items-center` /
  `align-items-end` enumeration, and `columns_sm_size: 0408` instead of `'04_08'` — so every
  featured-card view mode rendered a Twig error instead of a card.
### Changed
- Match the Figma design in the `featured_card_medium` template: the date moves above the title,
  the title uses `text_size: h5`, and the date uses `size: fs-6` with `text_color: text-muted`.
- Switch the Varbase functional testing suite to Varbase E2E.
- Update the version badge to `1.0.0-alpha2` in `README.md`.

## [1.0.0-alpha1] - 2026-08-09
### Added
- Initial release of the Varbase News Base recipe: a News content type (Title, Description,
  Featured Image, Content, Tags, News Categories), SEO fields (SEO Title/Description/Image, Yoast
  SEO analysis), a News views listing with Better Exposed Filters (All News Posts, Latest News
  Posts block, Related News Posts block, RSS feed), Card/Default view modes, Drupal Canvas
  templates, pathauto URL patterns, and editorial workflow integration.
- Add a `/news` listing page to the News view: a Views `page_1` page display at path `news`, based
  on the `All news posts` block, that renders the news cards grid, the Search-by-keyword / Type /
  Industry exposed filters inline (`exposed_block: false`) and the full 12-per-page pager. The
  listing is now available out of the box and functionally testable, without a site template
  having to place the listing block on a page.
### Changed
- Update Drupal Core to `~11.4.0`.
- Pin the `drupal/varbase_components`, `drupal/varbase_content_base`, `drupal/varbase_media_base`,
  `drupal/varbase_seo_base`, and `drupal/varbase_workflow_base` dependencies to real released
  constraints (`~4.0.0` / `~1.0.0`).
- Update the version badge to `1.0.0-alpha1` in `README.md`.

[Unreleased]: https://git.drupalcode.org/project/varbase_news_base/-/compare/1.0.0-alpha2...1.0.x
[1.0.0-alpha2]: https://git.drupalcode.org/project/varbase_news_base/-/compare/1.0.0-alpha1...1.0.0-alpha2
[1.0.0-alpha1]: https://git.drupalcode.org/project/varbase_news_base/-/tags/1.0.0-alpha1
