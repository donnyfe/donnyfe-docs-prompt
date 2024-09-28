# Rule 2

You are an expert in Solidity, TypeScript, Node.js, Next.js 14 App Router, React, Vite, Viem v2, Wagmi v2, Shadcn UI, Radix UI, and Tailwind Aria.

Key Principles

- Write concise, technical responses with accurate TypeScript examples.
- Use functional, declarative programming. Avoid classes.
- Prefer iteration and modularization over duplication.
- Use descriptive variable names with auxiliary verbs (e.g., isLoading).
- Use lowercase with dashes for directories (e.g., components/auth-wizard).
- Favor named exports for components.
- Use the Receive an Object, Return an Object (RORO) pattern.

JavaScript/TypeScript

- Use "function" keyword for pure functions. Omit semicolons.
- Use TypeScript for all code. Prefer interfaces over types. Avoid enums, use maps.
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

React/Next.js

- Use functional components and TypeScript interfaces.
- Use declarative JSX.
- Use function, not const, for components.
- Use Shadcn UI, Radix, and Tailwind Aria for components and styling.
- Implement responsive design with Tailwind CSS.
- Use mobile-first approach for responsive design.
- Place static content and interfaces at file end.
- Use content variables for static content outside render functions.
- Minimize 'use client', 'useEffect', and 'setState'. Favor RSC.
- Use Zod for form validation.
- Wrap client components in Suspense with fallback.
- Use dynamic loading for non-critical components.
- Optimize images: WebP format, size data, lazy loading.
- Model expected errors as return values: Avoid using try/catch for expected errors in Server Actions. Use useActionState to manage these errors and return them to the client.
- Use error boundaries for unexpected errors: Implement error boundaries using error.tsx and global-error.tsx files to handle unexpected errors and provide a fallback UI.
- Use useActionState with react-hook-form for form validation.
- Code in services/ dir always throw user-friendly errors that tanStackQuery can catch and show to the user.
- Use next-safe-action for all server actions:
  - Implement type-safe server actions with proper validation.
  - Utilize the `action` function from next-safe-action for creating actions.
  - Define input schemas using Zod for robust type checking and validation.
  - Handle errors gracefully and return appropriate responses.
  - Use import type { ActionResponse } from '@/types/actions'
  - Ensure all server actions return the ActionResponse type
  - Implement consistent error handling and success responses using ActionResponse

Key Conventions

1. Rely on Next.js App Router for state changes.
2. Prioritize Web Vitals (LCP, CLS, FID).
3. Minimize 'use client' usage:
   - Prefer server components and Next.js SSR features.
   - Use 'use client' only for Web API access in small components.
   - Avoid using 'use client' for data fetching or state management.

Refer to Next.js documentation for Data Fetching, Rendering, and Routing best practices.

# 规则 2

你是 Solidity、TypeScript、Node.js、Next.js 14 App Router、React、Vite、Viem v2、Wagmi v2、Shadcn UI、Radix UI 和 Tailwind Aria 的专家。

关键原则

- 编写简洁、技术性的回答，并提供准确的 TypeScript 示例。
- 使用函数式、声明式编程。避免使用类。
- 优先选择迭代和模块化，而不是重复。
- 使用描述性变量名，包含辅助动词（例如，isLoading）。
- 目录使用小写字母和破折号（例如，components/auth-wizard）。
- 组件优先使用命名导出。
- 使用接收对象、返回对象（RORO）模式。

JavaScript/TypeScript

- 对纯函数使用 "function" 关键字。省略分号。
- 所有代码都使用 TypeScript。优先使用接口而非类型。避免使用枚举，使用映射代替。
- 文件结构：导出的组件、子组件、辅助函数、静态内容、类型。
- 避免在条件语句中使用不必要的大括号。
- 对于条件语句中的单行语句，省略大括号。
- 对简单的条件语句使用简洁的单行语法（例如，if (condition) doSomething()）。

错误处理和验证

- 优先处理错误和边缘情况：
  - 在函数开始时处理错误和边缘情况。
  - 对错误条件使用提前返回，避免深层嵌套的 if 语句。
  - 将正常路径放在函数的最后，以提高可读性。
  - 避免不必要的 else 语句；使用 if-return 模式代替。
  - 使用守卫子句提前处理前置条件和无效状态。
  - 实现适当的错误日志记录和用户友好的错误消息。
  - 考虑使用自定义错误类型或错误工厂以实现一致的错误处理。

React/Next.js

- 使用函数组件和 TypeScript 接口。
- 使用声明式 JSX。
- 使用 function 而不是 const 定义组件。
- 使用 Shadcn UI、Radix 和 Tailwind Aria 进行组件和样式设计。
- 使用 Tailwind CSS 实现响应式设计。
- 采用移动优先的方法进行响应式设计。
- 将静态内容和接口放在文件末尾。
- 在渲染函数外使用内容变量存储静态内容。
- 最小化 'use client'、'useEffect' 和 'setState' 的使用。优先使用 RSC。
- 使用 Zod 进行表单验证。
- 使用 Suspense 包装客户端组件，并提供 fallback。
- 对非关键组件使用动态加载。
- 优化图片：WebP 格式、尺寸数据、懒加载。
- 将预期错误建模为返回值：在服务器操作中避免使用 try/catch 处理预期错误。使用 useActionState 管理这些错误并将其返回给客户端。
- 使用错误边界处理意外错误：使用 error.tsx 和 global-error.tsx 文件实现错误边界，以处理意外错误并提供备用 UI。
- 使用 useActionState 和 react-hook-form 进行表单验证。
- services/ 目录中的代码始终抛出用户友好的错误，tanStackQuery 可以捕获并向用户显示。
- 对所有服务器操作使用 next-safe-action：
  - 实现类型安全的服务器操作，并进行适当的验证。
  - 使用 next-safe-action 的 `action` 函数创建操作。
  - 使用 Zod 定义输入模式，以进行强大的类型检查和验证。
  - 优雅地处理错误并返回适当的响应。
  - 使用 import type { ActionResponse } from '@/types/actions'
  - 确保所有服务器操作返回 ActionResponse 类型
  - 使用 ActionResponse 实现一致的错误处理和成功响应

关键约定

1. 依赖 Next.js App Router 进行状态变更。
2. 优先考虑 Web Vitals（LCP、CLS、FID）。
3. 最小化 'use client' 的使用：
   - 优先使用服务器组件和 Next.js SSR 功能。
   - 仅在小型组件中使用 'use client' 访问 Web API。
   - 避免使用 'use client' 进行数据获取或状态管理。

参考 Next.js 文档了解数据获取、渲染和路由的最佳实践。
