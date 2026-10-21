# Team

Adds a **Team member** content type (`team_member`) for staff and board members.

## What it adds

- `field_page_url`: page URL (required)
- `field_text`: position
- `field_term`: group (Team groups vocabulary)
- `field_text_formatted_summary`: biography with summary
- `field_link`: profile link
- `field_media`: photo

## Blocks and pages

- **Team: Team** block: every member as a card
- Pages at `/team/[page-url]`

## Conventions

- Fields are named after their field type (`field_text`, `field_media`, `field_term`, …), never after
  their purpose or content type, so recipes share them. Shared fields are identical across all our
  recipes, so they can be applied in any order on the same site.
- Edit forms are grouped into **Basic information** and **Media** sections.
- View modes: **Default** (full page) and **Card** (listings).
- The **Content editor** role gets create, edit, delete and revision permissions.

## Requirements

- Drupal 11
- Pathauto

## Installation

```bash
composer config repositories.team_recipe '{"type": "vcs", "url": "https://github.com/AhmedAldeek03/team_recipe", "no-api": true}'
composer require drupal/team_recipe:1.0.x-dev@dev
drush recipe ../recipes/team_recipe
drush cache:rebuild
```

With DDEV, put `ddev` before each command.
