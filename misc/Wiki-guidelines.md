# Guidelines for editing the wiki
Any changes to this wiki should follow these rules.

*:question: GitLab Wiki documentation [is available here](https://docs.gitlab.com/ee/user/project/wiki/)*

## Markdown style
1. For code blocks, specify the language [[Docs](https://gitlab.fit.cvut.cz/help/user/markdown#code-and-syntax-highlighting)]
2. Mark links explicitly, do not leave it to the GitLab renderer: ~~`https://fit.cvut.cz/`~~ `[FIT](https://fit.cvut.cz/)`

*:question: More information about the GitLab MD flavour can be found [in the docs](https://gitlab.fit.cvut.cz/help/user/markdown#code-and-syntax-highlighting)*


## File structure

1. Each project **iteration** has its own **subfolder**
2. Pages that are related to the general project, **not iteration-specific**, go to the `misc` folder
3. The wiki root is reserved for the Home page and "meta" pages: sidebar, ...
4. Prefer short pages with a single topic to long files with multiple sections
5. For files an images, create a `media` folder in the page's directory

## File naming

1. For pages that need a meaningful order, add a prefix: `01_page.md`
2. Separate prefixes with an underscore, separate words in the title with a hypen: `01_page-title-with-multiple-words`
3. Start the actual page name with a capital letter: ~~`wiki-guidelines.md`~~ `Wiki-guidelines.md`

## Sidebar and table of contents

When adding a new page, make sure to:

1. Add it to the [TOC on out Home page](/Home)
2. Add it to the [sidebar](/_sidebar)

Link pages without the extension: ~~`[My new page](./misc/my-new-page.md)`~~ `[My new page](./misc/my-new-page)`

