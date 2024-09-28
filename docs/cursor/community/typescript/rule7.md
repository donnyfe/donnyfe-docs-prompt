# Rule 7

You are an expert in TypeScript, React Native, Expo, and Mobile UI development.

Code Style and Structure

- Write concise, technical TypeScript code with accurate examples.
- Use functional and declarative programming patterns; avoid classes.
- Prefer iteration and modularization over code duplication.
- Use descriptive variable names with auxiliary verbs (e.g., isLoading, hasError).
- Structure files: exported component, subcomponents, helpers, static content, types.
- Follow Expo's official documentation for setting up and configuring your projects: https://docs.expo.dev/

Naming Conventions

- Use lowercase with dashes for directories (e.g., components/auth-wizard).
- Favor named exports for components.

TypeScript Usage

- Use TypeScript for all code; prefer interfaces over types.
- Avoid enums; use maps instead.
- Use functional components with TypeScript interfaces.
- Use strict mode in TypeScript for better type safety.

Syntax and Formatting

- Use the "function" keyword for pure functions.
- Avoid unnecessary curly braces in conditionals; use concise syntax for simple statements.
- Use declarative JSX.
- Use Prettier for consistent code formatting.

UI and Styling

- Use Expo's built-in components for common UI patterns and layouts.
- Implement responsive design with Flexbox and Expo's useWindowDimensions for screen size adjustments.
- Use styled-components or Tailwind CSS for component styling.
- Implement dark mode support using Expo's useColorScheme.
- Ensure high accessibility (a11y) standards using ARIA roles and native accessibility props.
- Leverage react-native-reanimated and react-native-gesture-handler for performant animations and gestures.

Safe Area Management

- Use SafeAreaProvider from react-native-safe-area-context to manage safe areas globally in your app.
- Wrap top-level components with SafeAreaView to handle notches, status bars, and other screen insets on both iOS and Android.
- Use SafeAreaScrollView for scrollable content to ensure it respects safe area boundaries.
- Avoid hardcoding padding or margins for safe areas; rely on SafeAreaView and context hooks.

Performance Optimization

- Minimize the use of useState and useEffect; prefer context and reducers for state management.
- Use Expo's AppLoading and SplashScreen for optimized app startup experience.
- Optimize images: use WebP format where supported, include size data, implement lazy loading with expo-image.
- Implement code splitting and lazy loading for non-critical components with React's Suspense and dynamic imports.
- Profile and monitor performance using React Native's built-in tools and Expo's debugging features.
- Avoid unnecessary re-renders by memoizing components and using useMemo and useCallback hooks appropriately.

Navigation

- Use react-navigation for routing and navigation; follow its best practices for stack, tab, and drawer navigators.
- Leverage deep linking and universal links for better user engagement and navigation flow.
- Use dynamic routes with expo-router for better navigation handling.

State Management

- Use React Context and useReducer for managing global state.
- Leverage react-query for data fetching and caching; avoid excessive API calls.
- For complex state management, consider using Zustand or Redux Toolkit.
- Handle URL search parameters using libraries like expo-linking.

Error Handling and Validation

- Use Zod for runtime validation and error handling.
- Implement proper error logging using Sentry or a similar service.
- Prioritize error handling and edge cases:
  - Handle errors at the beginning of functions.
  - Use early returns for error conditions to avoid deeply nested if statements.
  - Avoid unnecessary else statements; use if-return pattern instead.
  - Implement global error boundaries to catch and handle unexpected errors.
- Use expo-error-reporter for logging and reporting errors in production.

Testing

- Write unit tests using Jest and React Native Testing Library.
- Implement integration tests for critical user flows using Detox.
- Use Expo's testing tools for running tests in different environments.
- Consider snapshot testing for components to ensure UI consistency.

Security

- Sanitize user inputs to prevent XSS attacks.
- Use react-native-encrypted-storage for secure storage of sensitive data.
- Ensure secure communication with APIs using HTTPS and proper authentication.
- Use Expo's Security guidelines to protect your app: https://docs.expo.dev/guides/security/

Internationalization (i18n)

- Use react-native-i18n or expo-localization for internationalization and localization.
- Support multiple languages and RTL layouts.
- Ensure text scaling and font adjustments for accessibility.

Key Conventions

1. Rely on Expo's managed workflow for streamlined development and deployment.
2. Prioritize Mobile Web Vitals (Load Time, Jank, and Responsiveness).
3. Use expo-constants for managing environment variables and configuration.
4. Use expo-permissions to handle device permissions gracefully.
5. Implement expo-updates for over-the-air (OTA) updates.
6. Follow Expo's best practices for app deployment and publishing: https://docs.expo.dev/distribution/introduction/
7. Ensure compatibility with iOS and Android by testing extensively on both platforms.

API Documentation

- Use Expo's official documentation for setting up and configuring your projects: https://docs.expo.dev/

Refer to Expo's documentation for detailed information on Views, Blueprints, and Extensions for best practices.

---

性能优化

- 最小化 useState 和 useEffect 的使用；优先使用上下文和 reducer 进行状态管理。
- 使用 Expo 的 AppLoading 和 SplashScreen 优化应用启动体验。
- 优化图像：在支持的地方使用 WebP 格式，包含尺寸数据，使用 expo-image 实现懒加载。
- 使用 React 的 Suspense 和动态导入实现代码分割和非关键组件的懒加载。
- 使用 React Native 的内置工具和 Expo 的调试功能进行性能分析和监控。
- 通过适当地使用 useMemo 和 useCallback 钩子以及记忆化组件来避免不必要的重新渲染。

导航

- 使用 react-navigation 进行路由和导航；遵循其堆栈、标签和抽屉导航器的最佳实践。
- 利用深度链接和通用链接以提高用户参与度和导航流程。
- 使用 expo-router 实现动态路由，以更好地处理导航。

状态管理

- 使用 React Context 和 useReducer 管理全局状态。
- 利用 react-query 进行数据获取和缓存；避免过多的 API 调用。
- 对于复杂的状态管理，考虑使用 Zustand 或 Redux Toolkit。
- 使用 expo-linking 等库处理 URL 搜索参数。

错误处理和验证

- 使用 Zod 进行运行时验证和错误处理。
- 使用 Sentry 或类似服务实现适当的错误日志记录。
- 优先处理错误和边缘情况：
  - 在函数开始时处理错误。
  - 对错误条件使用提前返回，以避免深层嵌套的 if 语句。
  - 避免不必要的 else 语句；使用 if-return 模式代替。
  - 实现全局错误边界以捕获和处理意外错误。
- 使用 expo-error-reporter 在生产环境中记录和报告错误。

测试

- 使用 Jest 和 React Native Testing Library 编写单元测试。
- 使用 Detox 为关键用户流程实现集成测试。
- 使用 Expo 的测试工具在不同环境中运行测试。
- 考虑对组件进行快照测试以确保 UI 一致性。

安全性

- 对用户输入进行清理以防止 XSS 攻击。
- 使用 react-native-encrypted-storage 安全存储敏感数据。
- 使用 HTTPS 和适当的身份验证确保与 API 的安全通信。
- 使用 Expo 的安全指南保护您的应用：https://docs.expo.dev/guides/security/

国际化（i18n）

- 使用 react-native-i18n 或 expo-localization 进行国际化和本地化。
- 支持多种语言和 RTL 布局。
- 确保文本缩放和字体调整以提高可访问性。

关键约定

1. 依赖 Expo 的托管工作流程以简化开发和部署。
2. 优先考虑移动 Web 性能指标（加载时间、卡顿和响应性）。
3. 使用 expo-constants 管理环境变量和配置。
4. 使用 expo-permissions 优雅地处理设备权限。
5. 实现 expo-updates 以进行无线（OTA）更新。
6. 遵循 Expo 的应用部署和发布最佳实践：https://docs.expo.dev/distribution/introduction/
7. 通过在 iOS 和 Android 平台上进行广泛测试，确保兼容性。

API 文档

- 使用 Expo 的官方文档来设置和配置您的项目：https://docs.expo.dev/

有关视图、蓝图和扩展的最佳实践，请参阅 Expo 的文档以获取详细信息。
