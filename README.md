# Fullstack Features 全栈开发核心功能与技术

## 📚 A collection of language agnostic core fullstack features for almost every application

### 👶 When I first began learning to code, I often hear people tell me to learn xxx technology, as if it's a magic pill. But no, there is no magic pill, there's also not a single language or framework that guarantees you a job in the field if you only grasp the basics of it.

记得我刚开始学编程的时候，周围大部分人都跟我说要学某样技术，什么 Java 啦，.NET 啦, SQL 啦，Python 啦，好像学会这些就能找到工作似的，实则不然。只会技术本身没有 Diao 用，关键是你会用这门技术能不能做出用户能用的功能，做出来产品用户喜不喜欢用。

### 💊 Users don't give a sh-t whether your app uses `Redux` or `Zustand` for state management, `REST` or `GraphQL` for APIs, nor do they care about which buttons you clicked in `AWS` console to deploy your infrastructure. All they care about, is whether your software is solving the problem(s) you promised them it'll solve.

### 🤷 So, why does it have anything to do with fullstack features?

### 🧑‍🤝‍🧑 Well, your code, your infrastructures and your databases are all built FOR EACH OTHER, they're rather useless on their own.

### 📜 Reading documentations and making toy projects alone doesn't teach you as much. The concepts of `refetchQueries` and `Reactive Variables` in Apollo GraphQL were jibberish to me until I had to save AWS bills by reducing duplicated API queries using `InMemoryCache`.

### 🎥 I could list out a ton lot more examples of how I learnt things, and I can be 100% sure with you that none of them came from following YT tutorials or reading documentations alone.

### 🍹 Most applications (in web 2 at least) are essentially fancy spreadsheets doing CRUD operations on the cloud. Different languages and frameworks simply do things in different ways, and some companies prefer certain frameworks over others, but the underlying core features remain the same: fancy CRUD operations.

### ⬇️ Below is a list of features that almost every application has, which we, as people trying to learn to code better be aware of during our learning process

| Feature                                                 | How it roughly works                                                                                                                                                                                                                                                                                                                                                                                               |
| ------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| ✅ New user sign up flow                                | New user signs up app using Auth0 or Cognito, auth service triggers event that adds new user to own DB                                                                                                                                                                                                                                                                                                             |
| ✅ Upload / update user profile picture                 | UI posts file into server, server posts file into cloud storage service (E.g, AWS S3) then return the server an URL of the uploaded image, the server then adds the returned URL into own DB for each record, UI then fetches image URL to partially update the page where profile picture should be shown                                                                                                         |
| ✅ Download CSV files from filterable data tables on UI | User sets up filters (date range or other columns) on the data table from the UI, then hit download, server receives req with filter parameters, retrieves all data from DB following that filtering parameter and forms a CSV file buffer (or xslx, etc) and sends that buffer to the client, the client then receives the buffer payload which allows it to actually download the file into user's local machine |
