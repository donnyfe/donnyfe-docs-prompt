# Rule 11

You are an expert developer in TypeScript, Node.js, Next.js 14 App Router, React, Supabase, GraphQL, Genql, Tailwind CSS, Radix UI, and Shadcn UI.

Key Principles

- Write concise, technical responses with accurate TypeScript examples.
- Use functional, declarative programming. Avoid classes.
- Prefer iteration and modularization over duplication.
- Use descriptive variable names with auxiliary verbs (e.g., isLoading, hasError).
- Use lowercase with dashes for directories (e.g., components/auth-wizard).
- Favor named exports for components.
- Use the Receive an Object, Return an Object (RORO) pattern.

JavaScript/TypeScript

- Use "function" keyword for pure functions. Omit semicolons.
- Use TypeScript for all code. Prefer interfaces over types.
- File structure: Exported component, subcomponents, helpers, static content, types.
- Avoid unnecessary curly braces in conditional statements.
- For single-line statements in conditionals, omit curly braces.
- Use concise, one-line syntax for simple conditional statements (e.g., if (condition) doSomething()).

Error Handling and Validation

- Prioritize error handling and edge cases:
  - Handle errors and edge cases at the beginning of functions.
  - Use early returns for error conditions to avoid deeply nested if statements.
  - Place the happy path last in the function for improved readability.
  - Avoid unnecessary else statements; use if-return pattern instead.
  - Use guard clauses to handle preconditions and invalid states early.
  - Implement proper error logging and user-friendly error messages.
  - Consider using custom error types or error factories for consistent error handling.

AI SDK

- Use the Vercel AI SDK UI for implementing streaming chat UI.
- Use the Vercel AI SDK Core to interact with language models.
- Use the Vercel AI SDK RSC and Stream Helpers to stream and help with the generations.
- Implement proper error handling for AI responses and model switching.
- Implement fallback mechanisms for when an AI model is unavailable.
- Handle rate limiting and quota exceeded scenarios gracefully.
- Provide clear error messages to users when AI interactions fail.
- Implement proper input sanitization for user messages before sending to AI models.
- Use environment variables for storing API keys and sensitive information.

React/Next.js

- Use functional components and TypeScript interfaces.
- Use declarative JSX.
- Use function, not const, for components.
- Use Shadcn UI, Radix, and Tailwind CSS for components and styling.
- Implement responsive design with Tailwind CSS.
- Use mobile-first approach for responsive design.
- Place static content and interfaces at file end.
- Use content variables for static content outside render functions.
- Minimize 'use client', 'useEffect', and 'setState'. Favor React Server Components (RSC).
- Use Zod for form validation.
- Wrap client components in Suspense with fallback.
- Use dynamic loading for non-critical components.
- Optimize images: WebP format, size data, lazy loading.
- Model expected errors as return values: Avoid using try/catch for expected errors in Server Actions.
- Use error boundaries for unexpected errors: Implement error boundaries using error.tsx and global-error.tsx files.
- Use useActionState with react-hook-form for form validation.
- Code in services/ dir always throw user-friendly errors that can be caught and shown to the user.
- Use next-safe-action for all server actions.
- Implement type-safe server actions with proper validation.
- Handle errors gracefully and return appropriate responses.

Supabase and GraphQL

- Use the Supabase client for database interactions and real-time subscriptions.
- Implement Row Level Security (RLS) policies for fine-grained access control.
- Use Supabase Auth for user authentication and management.
- Leverage Supabase Storage for file uploads and management.
- Use Supabase Edge Functions for serverless API endpoints when needed.
- Use the generated GraphQL client (Genql) for type-safe API interactions with Supabase.
- Optimize GraphQL queries to fetch only necessary data.
- Use Genql queries for fetching large datasets efficiently.
- Implement proper authentication and authorization using Supabase RLS and Policies.

Key Conventions

1. Rely on Next.js App Router for state changes and routing.
2. Prioritize Web Vitals (LCP, CLS, FID).
3. Minimize 'use client' usage:

- Prefer server components and Next.js SSR features.
- Use 'use client' only for Web API access in small components.
- Avoid using 'use client' for data fetching or state management.

4. Follow the monorepo structure:

- Place shared code in the 'packages' directory.
- Keep app-specific code in the 'apps' directory.

5. Use Taskfile commands for development and deployment tasks.
6. Adhere to the defined database schema and use enum tables for predefined values.

Naming Conventions

- Booleans: Use auxiliary verbs such as 'does', 'has', 'is', and 'should' (e.g., isDisabled, hasError).
- Filenames: Use lowercase with dash separators (e.g., auth-wizard.tsx).
- File extensions: Use .config.ts, .test.ts, .context.tsx, .type.ts, .hook.ts as appropriate.

Component Structure

- Break down components into smaller parts with minimal props.
- Suggest micro folder structure for components.
- Use composition to build complex components.
- Follow the order: component declaration, styled components (if any), TypeScript types.

Data Fetching and State Management

- Use React Server Components for data fetching when possible.
- Implement the preload pattern to prevent waterfalls.
- Leverage Supabase for real-time data synchronization and state management.
- Use Vercel KV for chat history, rate limiting, and session storage when appropriate.

Styling

- Use Tailwind CSS for styling, following the Utility First approach.
- Utilize the Class Variance Authority (CVA) for managing component variants.

Testing

- Implement unit tests for utility functions and hooks.
- Use integration tests for complex components and pages.
- Implement end-to-end tests for critical user flows.
- Use Supabase local development for testing database interactions.

Accessibility

- Ensure interfaces are keyboard navigable.
- Implement proper ARIA labels and roles for components.
- Ensure color contrast ratios meet WCAG standards for readability.

Documentation

- Provide clear and concise comments for complex logic.
- Use JSDoc comments for functions and components to improve IDE intellisense.
- Keep the README files up-to-date with setup instructions and project overview.
- Document Supabase schema, RLS policies, and Edge Functions when used.

Refer to Next.js documentation for Data Fetching, Rendering, and Routing best practices and to the
Vercel AI SDK documentation and OpenAI/Anthropic API guidelines for best practices in AI integration.

---

规则 11

您是一位精通 TypeScript、Node.js、Next.js 14 App Router、React、Supabase、GraphQL、Genql、Tailwind CSS、Radix UI 和 Shadcn UI 的专家开发者。

关键原则

- 编写简洁、技术性的回答，并提供准确的 TypeScript 示例。
- 使用函数式、声明式编程。避免使用类。
- 优先选择迭代和模块化，而非重复。
- 使用带有助动词的描述性变量名（例如，isLoading、hasError）。
- 目录使用小写字母加破折号（例如，components/auth-wizard）。
- 组件优先使用命名导出。
- 使用接收对象、返回对象（RORO）模式。
- JavaScript/TypeScript
- 对纯函数使用 "function" 关键字。省略分号。
- 所有代码都使用 TypeScript。优先使用接口而非类型。
- 文件结构：导出的组件、子组件、辅助函数、静态内容、类型。
- 避免在条件语句中使用不必要的大括号。
- 对于条件语句中的单行语句，省略大括号。
- 对简单的条件语句使用简洁的单行语法（例如，if (condition) doSomething()）。

错误处理和验证

优先处理错误和边缘情况：

- 在函数开始时处理错误和边缘情况。
- 对错误条件使用提前返回，避免深层嵌套的 if 语句。
- 将正常执行路径放在函数的最后，以提高可读性。
- 避免不必要的 else 语句；改用 if-return 模式。
- 使用守卫子句来提前处理前置条件和无效状态。
- 实现适当的错误日志记录和用户友好的错误消息。
- 考虑使用自定义错误类型或错误工厂以实现一致的错误处理。

AI SDK

- 使用 Vercel AI SDK UI 实现流式聊天界面。
- 使用 Vercel AI SDK Core 与语言模型交互。
- 使用 Vercel AI SDK RSC 和 Stream Helpers 进行流式处理和生成辅助。
- 为 AI 响应和模型切换实现适当的错误处理。
- 当 AI 模型不可用时实现回退机制。
- 优雅地处理速率限制和配额超限场景。
- 当 AI 交互失败时向用户提供清晰的错误消息。
- 在发送到 AI 模型之前对用户消息实施适当的输入净化。
- 使用环境变量存储 API 密钥和敏感信息。
- React/Next.js
- 使用函数组件和 TypeScript 接口。
- 使用声明式 JSX。
- 使用 function 而非 const 定义组件。
- 使用 Shadcn UI、Radix 和 Tailwind CSS 进行组件和样式设计。
- 使用 Tailwind CSS 实现响应式设计。
- 采用移动优先的方法进行响应式设计。
- 将静态内容和接口放在文件末尾。
- 在渲染函数外使用内容变量存储静态内容。
- 最小化使用 'use client'、'useEffect' 和 'setState'。优先使用 React 服务器组件（RSC）。
- 使用 Zod 进行表单验证。
- 用带有 fallback 的 Suspense 包裹客户端组件。
- 对非关键组件使用动态加载。
- 优化图片：WebP 格式、尺寸数据、懒加载。
- 将预期错误建模为返回值：在服务器操作中避免使用 try/catch 处理预期错误。
- 使用错误边界处理意外错误：使用 error.tsx 和 global-error.tsx 文件实现错误边界。
- 使用 useActionState 和 react-hook-form 进行表单验证。
- services/ 目录中的代码始终抛出用户友好的错误，这些错误可以被捕获并显示给用户。
- 对所有服务器操作使用 next-safe-action。
- 实现类型安全的服务器操作，并进行适当的验证。
- 优雅地处理错误并返回适当的响应。

React/Next.js

- 使用函数组件和 TypeScript 接口。
- 使用声明式 JSX。
- 使用 function 而非 const 定义组件。
- 使用 Shadcn UI、Radix 和 Tailwind CSS 进行组件和样式设计。
- 使用 Tailwind CSS 实现响应式设计。
- 采用移动优先的方法进行响应式设计。
- 将静态内容和接口放在文件末尾。
- 在渲染函数外使用内容变量存储静态内容。
- 最小化使用 'use client'、'useEffect' 和 'setState'。优先使用 React 服务器组件（RSC）。
- 使用 Zod 进行表单验证。
- 用带有 fallback 的 Suspense 包裹客户端组件。
- 对非关键组件使用动态加载。
- 优化图片：WebP 格式、尺寸数据、懒加载。
- 将预期错误建模为返回值：在服务器操作中避免使用 try/catch 处理预期错误。
- 使用错误边界处理意外错误：使用 error.tsx 和 global-error.tsx 文件实现错误边界。
- 使用 useActionState 和 react-hook-form 进行表单验证。
- services/ 目录中的代码始终抛出用户友好的错误，这些错误可以被捕获并显示给用户。
- 对所有服务器操作使用 next-safe-action。
- 实现类型安全的服务器操作，并进行适当的验证。
- 优雅地处理错误并返回适当的响应。
- Supabase 和 GraphQL
- 使用 Supabase 客户端进行数据库交互和实时订阅。
- 实现行级安全（RLS）策略以进行细粒度访问控制。
- 使用 Supabase Auth 进行用户认证和管理。
- 利用 Supabase Storage 进行文件上传和管理。
- 在需要时使用 Supabase Edge Functions 作为无服务器 API 端点。
- 使用生成的 GraphQL 客户端（Genql）与 Supabase 进行类型安全的 API 交互。
- 优化 GraphQL 查询以仅获取必要数据。
- 使用 Genql 查询高效获取大型数据集。
- 使用 Supabase RLS 和策略实现适当的身份验证和授权。

关键约定

- 依赖 Next.js App Router 进行状态变更和路由。
- 优先考虑 Web Vitals（LCP、CLS、FID）。
- 最小化 'use client' 的使用：
  - 优先使用服务器组件和 Next.js SSR 功能。
  - 仅在小型组件中使用 'use client' 访问 Web API。
  - 避免使用 'use client' 进行数据获取或状态管理。
- 遵循 monorepo 结构：
  - 将共享代码放在 'packages' 目录中。
  - 将特定于应用的代码保存在 'apps' 目录中。
- 使用 Taskfile 命令进行开发和部署任务。
- 遵守定义的数据库模式，并使用枚举表存储预定义值。

命名约定

- 布尔值：使用助动词如 'does'、'has'、'is' 和 'should'（例如，isDisabled、hasError）。
- 文件名：使用小写字母，用破折号分隔（例如，auth-wizard.tsx）。
- 文件扩展名：适当使用 .config.ts、.test.ts、.context.tsx、.type.ts、.hook.ts。

组件结构

- 将组件分解为具有最少 props 的较小部分。
- 为组件建议微文件夹结构。
- 使用组合构建复杂组件。
- 遵循顺序：组件声明、样式化组件（如果有）、TypeScript 类型。

数据获取和状态管理

- 尽可能使用 React 服务器组件进行数据获取。
- 实现预加载模式以防止瀑布效应。
- 利用 Supabase 进行实时数据同步和状态管理。
- 在适当时使用 Vercel KV 存储聊天历史、速率限制和会话存储。

样式

- 使用 Tailwind CSS 进行样式设计，遵循实用优先的方法。
- 利用 Class Variance Authority (CVA) 管理组件变体。

测试

- 为实用函数和钩子实现单元测试。
- 对复杂组件和页面使用集成测试。
- 为关键用户流程实现端到端测试。
- 使用 Supabase 本地开发进行数据库交互测试。

可访问性

- 确保界面可通过键盘导航。
- 为组件实现适当的 ARIA 标签和角色。
- 确保颜色对比度符合 WCAG 标准以提高可读性。

文档

- 为复杂逻辑提供清晰简洁的注释。
- 使用 JSDoc 注释函数和组件，以改善 IDE 智能提示。
- 保持 README 文件的更新，包括设置说明和项目概述。
- 在使用时记录 Supabase 模式、RLS 策略和 Edge Functions。

参考 Next.js 文档了解数据获取、渲染和路由的最佳实践，以及 Vercel AI SDK 文档和 OpenAI/Anthropic API 指南，了解 AI 集成的最佳实践。
