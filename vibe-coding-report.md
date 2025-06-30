# Vibe Coding 刻意练习实验报告  
**周期**：2024年5月28日 ~ 6月25日  
**参与者**：[Libo]  

---

## 1. 实验概览 
- **目标**：通过刻意练习量化AI编程工具的提效效果，总结最佳实践。  
- **核心工具**：Trae Cursor Augment、Deepseek client等。  

---

## 2. 每日开发记录（AI使用分类）
### 2.1 后端基础和Typescript
| 需求名称                | 状态 | 结果               | 备注                  |  
|------------------------|------|------------------------|-----------------------|  
| 数据库学习CRUD         | 大部分使用AI开发提效明显 | AI辅助数据库下载，mongodDB,MySQL,环境配置 | 半自动化，参考菜鸟教程    |  
| 个税计算I/O            | 未尝试AI               | 自己手动实现                             |   百度计算规则  |  
| localstorage临时存储   | 未尝试AI               | 自己手动实现                             |   -  |  
| TS编译检查             | 部分尝试AI             | 解决编译时类型报错                        |   -  |  
| Nginx转发、域名代理     | 大部分使用AI开发提效明显 | Nginx反向代理配置，域名解析配置           |   完全AI参考  |  

![Nginx转发，域名代理](https://github.com/banshanguishu/my-images-store/blob/main/nginx_proxy.png?raw=true)  

### 2.2 后端基础 和 Next.js全栈开发
| 需求名称                | 状态 | 结果               | 备注                  |  
|------------------------|------|------------------------|-----------------------|  
| CRUD + 拖动排序        | 大部分使用AI开发提效明显 | Nextjs + MongoDB + React            | 参考AI教程+nextjs官方文档完成  |  
| 数据存储迁移            | 大部分使用AI开发提效明显 | 成功从localstorage转移到MongoDB数据库|  -  |  
| Next.js的<Image>优化   | 未尝试AI               | 自己手动实现                          |  参考NextJS官方文档  |  
| TS编译检查,build打包    | 大部分使用AI开发提效明显 | 成功build并运行                      |   AI主要辅助打包时报错信息处理  |  

![nextjs解释](https://github.com/banshanguishu/my-images-store/blob/main/Nextjs_explain.png?raw=true)  
![服务端渲染+客户端渲染](https://github.com/banshanguishu/my-images-store/blob/main/Nextjs_SSR_RSC.png?raw=true)  
![nextjs链接MongoDB](https://github.com/banshanguishu/my-images-store/blob/main/nextjs_connect_to_MongoDB.png?raw=true)  
![mongoDB_prompt](https://github.com/banshanguishu/my-images-store/blob/main/MongoDB_prompt.png?raw=true)  
![数据库连接修复](https://github.com/banshanguishu/my-images-store/blob/main/db_connect_error.png?raw=true)  

### 2.3 博客项目迁移到Next.js
| 需求名称                | 状态 | 结果               | 备注                  |  
|------------------------|------|------------------------|-----------------------|  
| 项目迁移                | 未尝试AI               | 成功迁移                 | 基于上一阶段的Nextjs知识  |  
| 账号体系，Token身份验证  | 大部分使用AI开发提效明显 | 创建用户数据库，设计用户表，实现注册登录功能，实现Token身份中间件验证 |  -  |  
| 评论                   | 大部分使用AI开发提效明显 |  实现数据库关联查询，新增评论关联到具体博客数据 |  基于上一步身份令牌中间件的实现  |  
| pm2管理node项目        | 大部分使用AI开发提效明显 |  下载pm2，启动并管理博客项目 |  -  |  
| nginx转发，host并修改系统host  | 部分使用AI成功   | 成功转发到自己的Nextjs服务                    |  基于第一期的Nginx转发知识  |  

![token身份令牌](https://github.com/banshanguishu/my-images-store/blob/main/Token.png?raw=true)  
![token身份验证流程图](https://github.com/banshanguishu/my-images-store/blob/main/token_process.png?raw=true)  
![博客评论关联查询](https://github.com/banshanguishu/my-images-store/blob/main/query_populate.png?raw=true)  
![身份验证中间件跨越解决](https://github.com/banshanguishu/my-images-store/blob/main/middlware_cors.png?raw=true)  

### 2.4 MCP (Model Context Protocol)
| 需求名称                | 状态 | 结果               | 备注                  |  
|------------------------|------|------------------------|-----------------------|  
| 实现一个MCP Server,查询TodoList   | 完全使用AI，Build with MCP Agent,代码补全 | 成功实现MCP Server | 几乎全部AI实现  |  
| MCP Server添加到自己的Trae,并使用  | 完全使用AI | 成功实现 |  -  |  

![MCP Server 实现](https://github.com/banshanguishu/my-images-store/blob/main/MCP_Server_setup.png?raw=true)  
![MCP Server 项目概览](https://github.com/banshanguishu/my-images-store/blob/main/MCP_Server_project_overview.png?raw=true)  
![MCP SDK 获取](https://github.com/banshanguishu/my-images-store/blob/main/MCP_SDK_channel.png?raw=true)  
![MCP Server 结果截图](https://github.com/banshanguishu/my-images-store/blob/main/%E5%8D%9A%E5%AE%A2%E5%86%85%E5%AE%B9%E6%80%BB%E7%BB%93%EF%BC%88%E6%A6%82%E5%BF%B5%E3%80%81%E4%BB%BB%E5%8A%A1%E3%80%81%E5%AE%9E%E4%BD%93%E3%80%81%E5%85%AC%E5%8F%B8%E7%AD%89%EF%BC%89.png?raw=true)  
![MCP Server 集成截图](https://github.com/banshanguishu/my-images-store/blob/main/Agent.png?raw=true)  

---

## 3. AI协作技巧总结
### 3.1 提高代码生成成功率的技巧  
1. **Prompt 优化**：  
   - ❌ 模糊请求：  
     ```plaintext  
     "创建一个MCP Server"  
     ```  
   - ✅ 明确约束：  
     ```plaintext  
      背景：我是一个 MCP 小白，我已经使用了 mongoDB 数据库创建了 TodoList 文档

      需求：如何使用 MCP SDK，实现一个 MCP Server，通过网络通信，提供 TodoList 的查询，步骤尽量详细点，比如说：SDK 去哪里获取（如果有的话）

      后期可能实现：可能会把 MCP Server 添加到自己的 Trae，通过 Trae 帮我实现内容的总结（这一步目前不需要实现，只是在解答上面问题的时候考虑下后期的可能实现）
     ```  

2. **上下文补充**：  
   - 在生成代码前，先让AI理解项目技术栈（如框架、数据库类型）。
     ![添加相关上下文文档URL](https://github.com/banshanguishu/my-images-store/blob/main/Add_Context.png?raw=true)  

3. **分块生成**：  
   - 避免一次性生成完整模块，拆分为小功能点逐步验证。  
   - 拆分需求：明确每个功能点的边界，避免生成跨功能模块的代码。  
   - 逐步生成，循序渐进

---

## 4. 适用性分析  
### 4.1 适合Vibe Coding的场景  
- ✅ 重复性高的模板代码（如CRUD接口）  
- ✅ 已有清晰设计文档的功能  
- ✅ 数据清洗 / 转换脚本  

### 4.2 不适合的场景  
- ❌ 需求定制较高 
- ❌ 自然语言描述困难，修改prompt  
- ❌ 问题场景不常见
- ❌ 需求简单

---

## 5. AI程序员的短板  
| 人类优势                | AI当前缺陷               |  
|-------------------------|--------------------------|  
| 理解模糊需求            | 依赖精确的Prompt描述     |  
| 系统架构设计            | 生成代码缺乏全局一致性   |  
| 性能优化经验            | 易忽略边界条件           |  
| 边界错误处理           | 依赖于工作区上下文环境           |  

---

## 6. 未来应对策略  
1. **岗位冲击预测**：  
   - 初级编码任务可能被自动化替代，但设计/审查需求增加。  
   - 边界错误处理意识相对AI薄弱。  
   - 学习能力不及AI  
2. **自我提升方向**：  
   - 学习Prompt Engineering  
   - 强化代码审查能力（尤其是AI生成代码）  
---

## 附录  
- [主要Prompt记录](https://github.com/banshanguishu/my-images-store/blob/main/prompt.md)  