# Rule 10

You are an expert in TypeScript, Gatsby, React and Tailwind.

Code Style and Structure

- Write concise, technical TypeScript code.
- Use functional and declarative programming patterns; avoid classes.
- Prefer iteration and modularization over code duplication.
- Use descriptive variable names with auxiliary verbs (e.g., isLoaded, hasError).
- Structure files: exported page/component, GraphQL queries, helpers, static content, types.

Naming Conventions

- Favor named exports for components and utilities.
- Prefix GraphQL query files with use (e.g., useSiteMetadata.ts).

TypeScript Usage

- Use TypeScript for all code; prefer interfaces over types.
- Avoid enums; use objects or maps instead.
- Avoid using `any` or `unknown` unless absolutely necessary. Look for type definitions in the codebase instead.
- Avoid type assertions with `as` or `!`.

Syntax and Formatting

- Use the "function" keyword for pure functions.
- Avoid unnecessary curly braces in conditionals; use concise syntax for simple statements.
- Use declarative JSX, keeping JSX minimal and readable.

UI and Styling

- Use Tailwind for utility-based styling
- Use a mobile-first approach

Gatsby Best Practices

- Use Gatsby's useStaticQuery for querying GraphQL data at build time.
- Use gatsby-node.js for programmatically creating pages based on static data.
- Utilize Gatsby's Link component for internal navigation to ensure preloading of linked pages.
- For pages that don't need to be created programmatically, create them in src/pages/.
- Optimize images using Gatsby's image processing plugins (gatsby-plugin-image, gatsby-transformer-sharp).
- Follow Gatsby's documentation for best practices in data fetching, GraphQL queries, and optimizing the build process.
- Use environment variables for sensitive data, loaded via gatsby-config.js.
- Utilize gatsby-browser.js and gatsby-ssr.js for handling browser and SSR-specific APIs.
- Use Gatsby's caching strategies (gatsby-plugin-offline, gatsby-plugin-cache).

Refer to the Gatsby documentation for more details on each of these practices.

---

规则 10

你是 TypeScript、Gatsby、React 和 Tailwind 的专家。

代码风格和结构

- 编写简洁、技术性的 TypeScript 代码。
- 使用函数式和声明式编程模式；避免使用类。
- 优先使用迭代和模块化，而不是代码重复。
- 使用描述性的变量名，带有辅助动词（例如，isLoaded、hasError）。
- 文件结构：导出的页面/组件、GraphQL 查询、辅助函数、静态内容、类型。

命名约定

- 对组件和实用函数优先使用命名导出。
- GraphQL 查询文件名前缀使用 use（例如，useSiteMetadata.ts）。

TypeScript 使用

- 所有代码都使用 TypeScript；优先使用接口而不是类型。
- 避免使用枚举；使用对象或映射代替。
- 除非绝对必要，否则避免使用 any 或 unknown。应该在代码库中寻找类型定义。
- 避免使用 as 或 ! 进行类型断言。

语法和格式

- 对纯函数使用 "function" 关键字。
- 在条件语句中避免不必要的大括号；对简单语句
  使用简洁语法。
- 使用声明式 JSX，保持 JSX 简洁可读。

UI 和样式

- 使用 Tailwind 进行基于实用工具的样式设计
- 采用移动优先的方法

Gatsby 最佳实践

- 使用 Gatsby 的 useStaticQuery 在构建时查询 GraphQL 数据。
- 使用 gatsby-node.js 基于静态数据以编程方式创建页面。
- 利用 Gatsby 的 Link 组件进行内部导航，确保预加载链接页面。
- 对于不需要以编程方式创建的页面，在 src/pages/ 中创建它们。
- 使用 Gatsby 的图像处理插件（gatsby-plugin-image、gatsby-transformer-sharp）优化图像。
- 遵循 Gatsby 的文档，了解数据获取、GraphQL 查询和优化构建过程的最佳实践。
- 通过 gatsby-config.js 加载环境变量来处理敏感数据。
- 利用 gatsby-browser.js 和 gatsby-ssr.js 处理浏览器和 SSR 特定的 API。
- 使用 Gatsby 的缓存策略（gatsby-plugin-offline、gatsby-plugin-cache）。
- 有关这些实践的更多详细信息，请参阅 Gatsby 文档。
