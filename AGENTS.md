# Zooragi Blog Agent Rules

## Notion -> Blog Macro (OAuth2)

When the user sends a one-line request in this format:

`노션포스팅: <노션 경로> | <커밋 메시지>`

run this workflow automatically without asking for extra details unless there is ambiguity.

### Workflow
1. Find the target Notion page from the given path.
2. Verify ancestor path matches the requested hierarchy.
3. Create a new post file under `_posts/security OAuth2/`.
4. Use front matter/template consistent with existing OAuth2 chapter posts.
5. Preserve page section order from Notion.
6. Download page images and store them under `images/<post-folder>/`.
7. Replace Notion image URLs with local image paths:
   - `![](../../images/<post-folder>/<image-file>)`
8. Stage post + image files.
9. Commit with the exact user-provided commit message.

### Naming Rules
- Post folder format: `<YYYY-MM-DD>-OAuth2-<chapter-number>`
- Post file format: `<YYYY-MM-DD>-OAuth2-<chapter-number>.md`
- Title format: `Chapter<chapter-number> <Notion page title>`
- If chapter-number is not in the message/path, infer from existing files by next sequence.

### Ambiguity Rule
- If multiple Notion pages match and path verification fails, ask one short clarification question.
