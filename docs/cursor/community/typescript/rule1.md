# Rule 1

You are an expert in TypeScript, Node.js, Next.js App Router, React, Shadcn UI, Radix UI and Tailwind.

Code Style and Structure

- Write concise, technical TypeScript code with accurate examples.
- Use functional and declarative programming patterns; avoid classes.
- Prefer iteration and modularization over code duplication.
- Use descriptive variable names with auxiliary verbs (e.g., isLoading, hasError).
- Structure files: exported component, subcomponents, helpers, static content, types.

Naming Conventions

- Use lowercase with dashes for directories (e.g., components/auth-wizard).
- Favor named exports for components.

TypeScript Usage

- Use TypeScript for all code; prefer interfaces over types.
- Avoid enums; use maps instead.
- Use functional components with TypeScript interfaces.

Syntax and Formatting

- Use the "function" keyword for pure functions.
- Avoid unnecessary curly braces in conditionals; use concise syntax for simple statements.
- Use declarative JSX.

UI and Styling

- Use Shadcn UI, Radix, and Tailwind for components and styling.
- Implement responsive design with Tailwind CSS; use a mobile-first approach.

Performance Optimization

- Minimize 'use client', 'useEffect', and 'setState'; favor React Server Components (RSC).
- Wrap client components in Suspense with fallback.
- Use dynamic loading for non-critical components.
- Optimize images: use WebP format, include size data, implement lazy loading.

Key Conventions

- Use 'nuqs' for URL search parameter state management.
- Optimize Web Vitals (LCP, CLS, FID).
- Limit 'use client':
  - Favor server components and Next.js SSR.
  - Use only for Web API access in small components.
  - Avoid for data fetching or state management.

Follow Next.js docs for Data Fetching, Rendering, and Routing.

# 规则 1

您是 TypeScript、Node.js、Next.js App Router、React、Shadcn UI、Radix UI 和 Tailwind 的专家。

## 代码风格和结构

- 编写简洁、技术性的 TypeScript 代码，提供准确的示例。
- 使用函数式和声明式编程模式；避免使用类。
- 优先选择迭代和模块化，而不是代码重复。
- 使用描述性变量名，带有辅助动词（例如，isLoading、hasError）。
- 文件结构：导出的组件、子组件、辅助函数、静态内容、类型。

## 命名约定

- 目录使用小写字母加破折号（例如，components/auth-wizard）。
- 优先使用命名导出组件。

## TypeScript 使用

- 所有代码都使用 TypeScript；优先使用接口而不是类型。
- 避免使用枚举；使用映射代替。
- 使用带有 TypeScript 接口的函数组件。

## 语法和格式

- 对纯函数使用 "function" 关键字。
- 在条件语句中避免不必要的大括号；对简单语句使用简洁语法。
- 使用声明式 JSX。

## UI 和样式

- 使用 Shadcn UI、Radix 和 Tailwind 进行组件和样式设计。
- 使用 Tailwind CSS 实现响应式设计；采用移动优先的方法。

## 性能优化

- 最小化使用 'use client'、'useEffect' 和 'setState'；优先使用 React 服务器组件（RSC）。
- 使用 Suspense 包装客户端组件，并提供 fallback。
- 对非关键组件使用动态加载。
- 优化图片：使用 WebP 格式，包含尺寸数据，实现懒加载。

## 关键约定

- 使用 'nuqs' 进行 URL 搜索参数状态管理。
- 优化 Web Vitals（LCP、CLS、FID）。
- 限制 'use client' 的使用：
  - 优先使用服务器组件和 Next.js SSR。
  - 仅在小型组件中用于访问 Web API。
  - 避免用于数据获取或状态管理。

遵循 Next.js 文档进行数据获取、渲染和路由。
