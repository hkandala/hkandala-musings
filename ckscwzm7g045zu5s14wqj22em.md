## 100 Things You Should Know as a Software Engineer

### Building Software:

- (1) Premature optimization is the root of all evil. Don't underestimate this statement.
- (2) It is quite rare that you ever need to build something from scratch. There are libraries and dependencies for almost every use case. So hold your keyboards and don't reinvent the wheel.
- (3) Understanding the scope of the problem is the first step you need to do before finding the solution. It is quite common that we miss the first step and jump into the solution directly.
- (4) Don't be too much of a perfectionist. First, make it work then make it clean. Software delivery always has the highest priority.
- (5) Bad programmers worry about the code. Good programmers worry about data structures and their relationships. - Linus Torvalds
- (6) Use code comments to explain why you are doing something, not what you are doing. Don't be overly descriptive and start writing novels in the comments.
- (7) Having meaningful error logs saves a lot of time in debugging issues. Provide all relevant information in the error message instead of just saying "Error occurred in Function X!". And never log any sensitive or personal information.
- (8) 100% line/branch coverage doesn't mean your code is bug-free. Write your tests to covers all functional requirements, not to cover lines/branches.
- (9) If you are fixing a bug, write a corresponding test case, so it doesn't happen in the future. Bugs occur usually because of false assumptions, writing test cases for all those false assumptions will make the application more robust.
- (10) When someone reading your code, they shouldn't need to keep more than 7 things in their head to comprehend it. Well, because our brains are not capable to hold [more than 7 things](https://psycnet.apa.org/doiLanding?doi=10.1037%2F0033-295X.101.2.343) at a time in our short-term memory. And that's one of the reasons why many code linters warn with more than 7 arguments in a function too.
- (11) Don't do something in a specific way just because someone asked you to do it, understand why, if you aren't convinced then challenge the status quo.
- (12) Problem-solving is the most important skill every engineer should be really good at. Your organization has a lot of problems lying around. Start solving them, not all can be solved, not even 20% of them. But in the process of trying to solve you would have learned so much.

### Designing Systems:

- (13) Best system designs are usually the simplest ones. Keep it simple stupid!
- (14) Design patterns and best practices are not some magic potion that applies everywhere. A good engineer knows best practices but a senior engineer knows when to break best practices.
- (15) Understand Abstraction. Unnecessary complexity in the code is introduced usually because of poor abstraction.
- (16) A system is only as strong as its weakest point. Focus on the bottleneck.
- (17) The more steps you get away from the primary source the more corrupted everything gets. Try to minimize hops, this applies in both technical and non-technical contexts.
- (18) No perfect solution exists, just trade-offs. List down pros and cons, and your demands to make the right trade-offs.
- (19) Every technology that you introduce in your project comes with an attached risk. Measure the risk and have plans for mitigation of the risk. Don't jump into an ocean without a life jacket.
- (20) Avoid premature abstraction. Solve the problem you have right now and only that. When you see similar problems coming in and you see a pattern emerging then that's when you should think about building an abstraction around it.
- (21) "There are two ways of constructing a software design: One way is it to make it so simple that there are obviously no deficiencies and the other way is to make it so complicated that there are no obvious deficiencies. The first method is far more difficult. Simplicity is HARD." - Tony Hoare.
- (22) Don't be too biased towards languages or frameworks, If you love some language, stop worshipping it all the time and don't start using it everywhere. If you hate it, don't rant about it all the time too. Every language or framework is designed for a particular use case. As an engineer, it is your job to pick the right tool for the use case.
- (23) If by the time you figure out HOW something works, you’ve forgotten the WHY part then there is a lot of unnecessary abstraction and complexity in the code which needs to be cleaned up.
- (24) Once complexity has accumulated, it is hard to eliminate. Don't assume that a little bit of complexity introduced by your current change is no big deal. If every developer follows the same approach, complexity accumulates exponentially.
- (25) If you have decided to rewrite a component/service always rethink your decision. It is harder to read code than to write it, that's why "I should rewrite it!" is very common in software development.
- (26) Don't hesitate to challenge the designs proposed by your senior engineers or architects, sometimes your design is better. Make valid convincing points and compare objectively. Just don't take this to an extreme by being an overconfident jerk.
- (27) Most of the time, statically typed languages are better than dynamically typed languages despite the overhead that comes with a static type system. And that explains why TypeScript is one of the [most loved languages](https://insights.stackoverflow.com/survey/2021#technology-most-loved-dreaded-and-wanted).

### Miscellaneous Tips:

- (28) Optimize your code for understandability. A boring verbose 20 lines of code is always better than a cleverly written single line of code.
- (29) It is quite common for newbies to develop an emotional connection with the code they write. But in an agile environment, requirements and code keep changing. Get comfortable in modifying and removing your old code.
- (30) Come up with more than one solution for any problem. Trying to find multiple solutions forces you to think differently, and once you have different solutions you can decide by choosing the right trade-offs.
- (31) The more modules you work on, the more domain knowledge you will gain. The more domain knowledge you have, the more meetings you need to join. The more meetings you join, the less code you write. Break the chain by documenting and sharing the domain knowledge so that you ain't the only point of contact. I know it is easier to say this than implementing it.
- (32) When you are stuck at some problem for a quite long time without any progress, rephrase the problem or explain the problem to someone, magically this works most of the time. Why do you think rubber duck 🦆 debugging is so popular.
- (33) You don't need to understand the entire codebase to start working on it. Understand the architecture and lifecycle, and get started with your module. Don't waste your time trying to understand every class written.
- (34) Code is a liability rather than an asset. The more code you have, the more it needs to be read, understood, tested, and maintained. The best code is having no code.
- (35) Learn how to post a question on StackOverflow. It is very rare that you ever need to post a question, but it's a useful skill that will come in handy when you are working on a library/framework which has limited documentation and users.
- (36) If you stumble upon issues or bugs in other modules which you aren't working on, inform the respective developers, or mention it in the scrum. Please don't be like: I am not responsible for other modules.
- (37) The functions that you write should have zero/minimal side effects. This makes the function easily and independently testable.
- (38) For god's sake please don't write your own date formatting/parsing functions. Every programming language has many popular date libraries, just use them. Dates and Time zones are way too complex than you think.

### Security:

- (39) Every developer should know how to write secure code. It is okay to write code with bad design/abstraction but definitely not okay to write code with security vulnerabilities. Read [OWASP Top 10](https://owasp.org/www-project-top-ten/) document to get started.
- (40) Don't use online formatters or validators when you quickly want to format or validate some JSON / XML / YAML data. Especially if you are dealing with some confidential production data, it's a strict no for any online tool. Use any local editor or command-line tools instead. Don't risk yourself by leaking your company's data to some random site. (Recommended Tool: [CyberChef](https://gchq.github.io/CyberChef/) - Download for offline use)
- (41) Never, EVER push any sensitive information in your code repositories. Always double check your code doesn't have email addresses, phone numbers, passwords, authentication tokens, private keys, etc. before commit and push.
- (42) Always validate and sanitize user input. Never assume or expect the user will send certain input in the correct format. And always prefer whitelisting over blacklisting when validating.

### Pull Requests:

- (43) Guess what! you can also give compliments in pull request comments. We always focus on the bad parts while reviewing, a small appreciation can bring a smile to your peer's face. Try it next time.
- (44) Make it a daily practice to read pull requests and understand other developers' comments to get different perspectives on the feature and coding standards.
- (45) Code formatting and other standards should be automated. Build your project development pipeline with code formatters and linters, so that the entire codebase stays consistent and clean. Stop fighting about Tabs vs Spaces in PR comments, please!
- (46) Create short Pull Requests. If you are working on multiple features, separate them into multiple PRs. And give reviewers enough time to review, don't create PR one hour before deployment. 🙄

### Learning:

- (47) As a programmer, you should fundamentally enjoy learning and exploring. If you don't enjoy them, you should seriously consider other career options.
- (48) You don't need to learn every technology that comes to the market. Stay updated on the trends but learn and use them when needed.
- (49) There are so many things to learn from a fresh college intern too. Never limit your learning scope only to the people in higher roles.
- (50) Read source code of different open source projects that you consume to understand and learn the clean code practices and code organization.
- (51) The best way to learn some technology is to build a highly simplified version of it on your own. ([https://github.com/danistefanovic/build-your-own-x](https://github.com/danistefanovic/build-your-own-x))
- (52) It is easy to learn a language in few days. But it takes months or years to understand its ecosystem.
- (53) Explore different programming languages to understand different paradigms. Knowing different programming paradigms will help you in choosing the right language for your use case.
- (54) Learn git. Not just git pull and git commit, understand all the advanced concepts. Irrespective of the technology you use, git is going to stay common.
- (55) Given that most of the developers' work is focused on web/network programming. It is helpful to know underlying protocols in a network system: HTTP, HTTPS, SSL/TLS, DNS, SMTP, IPv4, IPv6, etc.
- (56) Having good expertise in CSS will make you look like a wizard! 🧙‍♂️ If you are a full-stack web developer, spending few days on mastering CSS is going to save hours of 'I don't know what I am doing'.
- (57) It is quite easy to impress people (not referring to domain experts obviously) with an attractive UI design than a robust system architecture. So having good design skills comes in handy when you are working on a proof-of-concept. (Just don't misuse it by hardcoding everything in HTML 😛)

### Productivity:

- (58) Create granular sub-tasks to track your progress especially when you are working on a huge task. It is tough to describe the blissful feeling of checking something as done and which in turn motivates you to stay on track.
- (59) Don't try to work on multiple tasks at the same time. Focus on one task and try to minimize context switching. The cost of context switching is higher than you expect.
- (60) Improve and customize your workflow (IDE, Debugging tools, Productivity tools, CI/CD) so that you can iterate faster.<br/>
The faster you iterate, the faster you fail.<br/> 
The faster you fail, the faster you learn.
- (61) Invest your time in automating routine tasks. If you are doing something more than twice, write a tool to automate it the third time. And at the same time, don't waste hours/days in automating a simple task that barely takes a couple of minutes. Find the right balance!
- (62) Organize your work mail (personal mail too) with folders and labels. A small effort in organizing mails daily will help you to quickly find important documents or conversations when needed.
- (63) &lt;Esc> + :q! + <Enter>  exits Vi editor 🤯! On a serious note, learn basic Vi bindings, even if Vi is not your default editor, you can use Vi bindings in almost every text editor that is available, and trust me your productivity will skyrocket after that.
- (64) Documentation skills are highly underrated in this industry. Learn how to write Design Documents, Change Proposals, etc. Start using note-taking tools to organize and document almost everything - MoMs, Personal Goals, Professional Goals, Random thoughts, Book summaries, and the list goes on. (Recommended Tool: [Notion](https://notion.so/))
- (65) Always keep some buffer time when giving estimates to your task. You never know what monster you will encounter in an unexplored cave.
- (66) Preferably listen to instrumental music or [lo-fi beats](https://www.youtube.com/watch?v=f02mOEt11OQ) or calm sounds instead of music with lyrics. Personally, I feel I am more productive with instrumental music and not so surprisingly [science backs it up too](https://jaxenter.com/music-for-coding-152327.html).

### Self:

- (67) Fix your body posture at the desk RIGHT NOW!
- (68) It's good to have different hobbies outside work. Just because you are a developer you don't need to code 24x7.
- (69) Be kind to everyone! Stay calm all the time! And most importantly, Be Humble!
- (70) Remember to take breaks regularly. Don't burn out yourself.
- (71) Invest in a good workstation setup. Given that you spend most of your time at your desk (especially during these remote working days). It is worth spending a couple of extra pennies on high-quality products.
- (72) Read about different [cognitive biases](https://en.wikipedia.org/wiki/Cognitive_bias). It will not only help you in making better personal decisions but also in making better technical decisions.
- (73) Start investing early in your career. Understand the power of compound interest, trust me it is magical. And at the same time don't overdo your savings, what is the point of saving everything when you are not enjoying the present. That's it, no more financial advice. 🙊

### Interpersonal:

- (74) Interpersonal skills are as important as your technical skills. Practice mentoring, public speaking, leading projects, etc. Developers don't need to follow the socially inept stereotype.
- (75) Not everyone will have the same motivations that you have. Never expect others to get excited and show interest in any topic just because you do. Different people respond to different motivations.
- (76) Don't judge your colleague (in fact anyone) by what they don't know.
- (77) Learn how to market yourself. You might be very skillful at many things, but no one would appreciate it if you aren't presenting those skills on the right platform.
- (78) Help the people around you get better. Teach or share things that you have learned. An act of teaching or writing about something you have learned will make you understand it better.
- (79) Never hesitate to say "I don't know". You might be a very good liar but our brains are amazing at finding if someone is lying or faking. And what makes it worse is faking leads to higher expectations.
- (80) There will be one rockstar developer in your team all the time who can solve almost anything. Don't get intimidated by their skills, rather read their pull requests, have technical chats, and regularly get feedback from them to improve yourself.
- (81) There is a very good chance that you will meet your BFF at work. Don't refrain from opening yourself with your colleagues. (Take this advice at your very own discretion 😅)

### Communication:

- (82) Listen, I repeat Listen!
- (83) It's okay if you don't have any points to make in a meeting, never ramble and waste others' time.
- (84) Don't IM people with just Hi / Hello / Good Morning!, and wait for their reply. Give them the reason why you pinged. No one just wants to hear your greetings or wishes. [https://www.nohello.com/](https://www.nohello.com/)
- (85) Use diagrams wherever possible when explaining your design. A picture is worth a thousand words. And it will be useful for documenting too. (Recommended tool: [draw.io](https://draw.io/))
- (86) Reduce the usage of jargon, when explaining some design or concept to someone. Not everyone might be familiar with all the technical terms. Use them at a proper balance.
- (87) You shouldn't be ashamed to ask a question which you think is trivial or stupid.
- (88) If you want to get the work done in minutes then call. If you want to get the work done in hours then IM. If you never want to get the work done then email (Do people still use email in 2021? 🤔).
- (89) When you seek help on a problem from someone, don't just go around and say "Hey X is not working, can you help me?", rather say "Hey, when I am running X, I am facing error Y, and I have researched and tried the solution Z, but it doesn't seem to work too, can you help me fixing this?". Do your research before taking someone's help, please don't waste others' time because of some typo in your code guys, seriously!
- (90) Don't fall prey to [the Bicycle Shed Effect](https://fs.blog/2020/04/bikeshed-effect/). Give importance to complex/critical items over trivial items in meetings or discussions.

### Career:

- (91) It is okay if you are working on something you don't like but it is not acceptable to work on something you hate.
- (92) When you are early in your career prioritize learning and opportunities over pay, benefits, etc. Invest more time in activities or jobs with a high learning rate. Learning compounds, you have to start early to reap its benefits.
- (93) Your sheer motivation at work should be on adding value to the team and project, not on impressing anyone for higher pay or promotion. If the former one is taken care of, the latter one is just a by-product.
- (94) Spend time on your resume and always keep it up to date. It is recommended to have a portfolio site describing your projects and experiences.
- (95) The problems you solve become more ambiguous and hazy, the higher the role you go. Get comfortable with uncertainty and ambiguity.
- (96) Do ask yourself these questions every six months:
    - Am I learning new skills and widening my areas of expertise?
    - Am I creating an impact in the organization?
    - Am I getting paid well enough for my skill set and experience?

  If your answers are no to all of them, then you MUST think about switching companies or teams. If you have been in the present company for more than 2-3 years and your answers are yes to all of them then you should still think about switching companies or at least be open to it. You will never know what you are missing unless you are looking for it.
- (97) If you pay close attention, programming is very similar to writing. Programming languages are analogous to human languages and programmers are analogous to writers/poets. Anyone can be a writer, but it takes a lot of effort and time to be a good writer.
- (98) Have 1:1 with your manager regularly and seek feedback. Don't wait till your annual reviews to get sudden surprises.
- (99) If your manager is not taking responsibility for your failures and blaming you for them then you are risking your personal and professional growth by working under them.
- (100) Years of experience is just a number. Sometimes you will find junior engineers more skilled than senior engineers. Don't get me wrong, experience teaches you more than just skills, so yes, work experience is important, but that's not the only factor.

### Bonus:

- (101) Remember Pareto Principle (80/20 Rule). It does apply to almost any context in Software Engineering:
  - 80% of work is done by 20% of engineers
  - 80% of the impact is done by 20% of work
  - 80% of bugs are caused by 20% of code
  - 80% of slow performance is caused by 20% of code

  I can go on with innumerable examples.
- (102) Can we give a moment of silence for the developers who had to write code before StackOverflow was a thing? StackOverflow has solutions to 95% of your problems PERIOD. (Just don't start asking about your personal problems 😛)
- (103) Git commit messages should be descriptive enough so that you can easily search for them from thousands of commits. Stop writing messages like: "fixed a bug", "improved performance", "module X changes" etc.