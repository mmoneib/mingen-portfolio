# Minimalist Generated Portfolio
## Description
A minimalist, flow-oriented, easily generated portfolio of hierarchical sections, each containing its stream of items, each item having its own type, which influence how it is displayed.
## Core Principles of Design
1. **Compactness:** As minimal branching and artefacts as possible to allow a streamlined process of adding new content. Necessity dictates complexity level.
1. **Configurability:**  A rigid structure with guided customizability through CSS and classification of sections and items.
1. **Centralization:** Limitless number of pages withing a single page, updated through a push-to-publish mechanism.
## Stack
* Only standard stack is used to disallow any needless dependencies.
* Intentional design and minimalism objectives mandate no usage of AI in code generation.
* CSS is separated from the single-page HTML to allow for changeability of the design.
* JavaScript is included in the single-page HTML as an incentive to keep it minimal.
* JSON along with AJAX are used to maintainn the dynamic views within the single page by defining their contents and their interrelations.
* Markdown is used to define and design content.
## Structure
* Building Blocks: Sections, Items, and Content.
* Relations: Section is subset of Single Page; Section can be subset of Section; Items are subset of Sections.
* Linkage: Each view constitutes a section with buttons linking to its direct descendents as defined in the sections.json file.
* Sections: Along with the buttons, each view shows a description, content, and a list of items.
* Items: Each item shows a title, content, and a description.
* Content: Each content can be configured through types, which dictate how they should be displayed.
### Content Format 
* The supported content types are as follows:
| Type | Description | Allowed Formats |
| :-- | :-- | :-- |
| text | Text typed inside the JSON file | Plain text |
| image_file | Reference to image file inside the JSON file | As supported by the browser |
| text_file | Reference to a text file. | Plain text |
| md_file | Reference to a markdown file. | Basic Markdown as defined in the table below |
#### Markdown Compatibility
* A stripped sown version of Markdown is currently supported as follows:
| MD Symbol | HTML Equivalent | Description | Notes |
| :-- | :-- | :-- | :-- |
| \*\* | <b> or </b> | Bold text | |
| \* | <i> or </i> | Italic text | |
| \# | <h2> or </h2> | Big heading (title) | |
| \#\# | <h3> or </h3> | Medium heading (title) | |
| \#\#\# | <h2> or </h2> | Small heading (title) | |
| -  | <ul> <li> | List item within an unordered list | List closes with any new line without the starting symbol. |
| 1  | <ol> <li> | List item within an ordered list | List closes with any new line without the starting symbol, which can also be any other digit up to 9. |  
