# SpendWise-AI

<h1>1. Repository Overview & Team Introduction</h1> 
<p>In this repository we introduce you SpendWise AI, the money tracker app that helps you develop a good saving habit. SpendWise AI is built by Vege Birds, consists four members: Soo Zi San, Lee Yong Heng, Lai Qian Hui and Leong Zi Qi.</p>

<h1>2. Project Overview</h1>
<h2>Problem Statement</h2>
<p>According to the Financial Capability and Inclusion Demand Side (FCI) Survey 2024 by Bank Negara Malaysia, declines were seen in the financial behaviour score of Malaysians. The dramatic increase in the usage of digital financial products and services (DBS), from 74% in 2021 to 92% in 2024 as well as Buy Now Pay Later (BNPL) facilities has made online spending more convenient but also heightened the risk of overspending and debt accumulation among Malaysians. Without adequate financial literacy and responsible money management skills, Malaysians may face long-term financial instability, undermining economic resilience and sustainable growth.

Although there are budgeting apps in the market for individuals to take down their spending and Large Language Models (LLMs) like ChatGPT, DeepSeek and Gemini for advice seeking, there has been no sight of solutions that actually combine the two to give the advice based on the user’s background and the spending habit of Malaysians.

This issue aligns with SDG-4, Quality Education, for improving financial literacy and promoting sustainable lifestyles through responsible money management and culturally aware advice, and SDG-8, Decent Work and Economic Growth, for encouraging Malaysians to be financially stable and develop responsible economic behaviour.
</p>
<h2>SDG Alignment</h2>
<p>We chose SDG 4 (Quality Education) and SDG 8 (Decent Work and Economic Growth) because the root cause of the problem we are solving is not a lack of money — it is a lack of financial knowledge and the tools to act on it. According to Bank Negara Malaysia, 7 out of 10 Malaysians live paycheck to paycheck, and a 2022 report by AKPK found that a significant portion of young Malaysians aged 20 to 30 struggle with debt due to poor budgeting habits — not low income. This tells us the problem is behavioural and educational, which is exactly what SDG 4 targets. At the same time, individuals who cannot manage their personal finances are less economically productive and more financially vulnerable, which directly undermines the goals of SDG 8 around decent work and sustainable economic growth at the individual and national level.
  
SpendWise AI addresses this by embedding financial education directly into the user's daily habits through our AI chatbot. Every time a user asks the chatbot a question — whether it's "how much did I spend this week?" or "am I on track with my budget?" — they are not just getting an answer, they are passively learning how to think about money. Over time this builds genuine financial literacy, which is what SDG 4 calls for — education that is practical, accessible, and lifelong. This is something a static budgeting app with charts can never achieve because it puts the burden of interpretation on the user, whereas we guide them through it conversationally.

On the SDG 8 side, SpendWise AI supports digital financial inclusion and long-term economic sustainability at the individual level. By helping users track spending, stay within budgets, and make informed financial decisions, we are directly building the kind of financially responsible behaviour that leads to savings, reduced debt, and greater economic stability over time. We also encourage entrepreneurial thinking by helping users identify where their money is going and where they could redirect it — whether that's saving for a small business, reducing unnecessary expenses, or setting financial goals. The impact is that users become more economically empowered individuals, and at scale, that contributes to a more financially resilient population — which is exactly the kind of inclusive and sustainable economic growth SDG 8 envisions.
</p>
<h2>Solution Description</h2>
<p>SpendWise AI is a smart personal finance app designed to help users take control of their financial health. It enables seamless tracking of daily expenses and income, offering clear visual insights through interactive pie charts that break down spending and earning patterns. Users can set personalized savings goals and monitor their progress over time — all within a single, intuitive platform. Powered by an integrated AI chatbot, SpendWise AI also provides on-demand financial advice, making it easier than ever to make informed money decisions and build better financial habits.</p>
<h1>3. Key Features</h1>
<p>Unlike most personal finance applications that limit users to basic expense and income tracking with chart visualizations, SpendWise AI goes a step further by offering a more complete and intelligent financial management experience.
  
At its core, SpendWise AI provides comprehensive expense and income tracking, giving users a clear picture of where their money comes from and where it goes. This is complemented by interactive pie charts that visually break down spending and earning patterns, making financial data easy to understand at a glance.
What truly sets SpendWise AI apart is its AI Chatbot Assistant, which provides personalized, on-demand financial and savings advice — acting as a pocket financial advisor available anytime the user needs guidance. Paired with this is the Savings Goals feature, which allows users to define specific financial targets and work towards them with purpose, rather than saving without direction.

Together, these features make SpendWise AI not just a tracker, but a complete financial companion built to help users save smarter and spend wiser.</p>
<h1>4. Overview of Technologies Used</h1>
<p>
  
* **Android Studio**
  
The application is developed in Android Studio using Kotlin for native Android performance and a smooth user experience. 

* **Firebase**

On the backend, Firebase is used for user authentication, secure data storage with Firestore, and real-time synchronization. 

* **Google AI Studio**

Google AI Studio is integrated to generate AI-powered financial insights and personalized recommendations based on users’ spending behaviour.
</p>
<h1>5. Implementation Details and Innovation</h1>
<h2>System Architecture</h2>
<p>Our app is built with three main components — a Kotlin Android frontend, Firebase as our backend, and Gemini as our AI layer. On the frontend, users interact with screens for sign-up and login, expense and income input, a budget overview dashboard, and an AI chatbot, with the Android app communicating directly with Firebase services. For the backend, we rely entirely on Firebase — Firebase Authentication handles user registration, login, and session management, while Firebase Realtime Database stores all transaction records, budget thresholds, and user data, giving us instant real-time updates on the dashboard without any extra setup. For the AI component, when a user asks a question in the chatbot, the app first fetches the user's relevant transaction data from Firebase, summarises it, and sends it together with the user's question to the Gemini API, which then returns budgeting suggestions, spending insights, and overspending predictions back to the user. The overall data flow is straightforward — user input goes into Firebase Auth and the Realtime Database, that data is then pulled and sent to Gemini for analysis, and the AI's response is displayed back to the user in real time. Every component is connected through the Android app acting as the central coordinator — it handles authentication, reads and writes to the database, and makes API calls to Gemini, keeping the architecture simple and easy to manage within our team's capacity.</p>
<h2>Workflow</h2>
<p>The user begins by logging their income and expenses, recording the amounts along with their respective sources and categories. Once the data is entered, the user can view the pie charts to gain a visual breakdown of how much they earn and spend across different sources and categories, giving them a clearer picture of their financial standing.
  
With this insight, the user can then create a savings goal, setting a specific financial target they wish to achieve. The app will subsequently calculate and display how much the user can spend without compromising their ability to reach that goal, helping them stay on track and make smarter spending decisions.
Finally, if the user needs further guidance or has financial concerns, they can consult the AI Chatbot Assistant for personalized financial advice tailored to their situation.</p>
<h1>6. Challenges Faced</h1>
<p>
<h2>1. AI Chatbot Switching to Malay Unexpectedly</h2>
  
During testing, it was observed that the AI chatbot would occasionally switch from English to Malay mid-conversation, even when the user was communicating in English. This occurred because the base prompt identified Malaysians as the target audience, which caused the AI to associate the Malaysian context with the Malay language and default to it automatically.

To resolve this, an explicit instruction — "Try your best to speak in English" — was added to the base prompt. This small but targeted addition was sufficient to override the AI's assumption and ensure responses remained consistently in English, without removing the Malaysian financial context the chatbot was built around. This experience highlighted how a single sentence in a prompt can significantly influence the behavior of an AI model, reinforcing the importance of being specific and explicit in prompt engineering.

<h2>2. Incorrect Monthly Savings Calculation for Goals</h2>

During test mode, two savings goals were created to verify that monthly savings amounts were being correctly distributed. It was expected that Goal 1 (RM1000 over 10 months) would allocate RM100 per month, and Goal 2 (RM1000 over 13 months) would allocate RM77 per month. However, the app returned RM112 and RM66 respectively, indicating that the duration was being undercounted by one month for each goal.

The root cause was identified in the month difference formula, where the start or end month was being treated as exclusive, effectively reducing the total duration by one month. This was resolved by adding + 1 to the calculation, ensuring both the start and end months are treated as inclusive. This challenge highlighted the importance of boundary condition testing, where the edges of a date range need to be carefully handled to ensure accurate results.</p>

<h1>7. Installation & Setup</h1> 
<p>Step 1: Download this repository into your laptop. 

Step 2: Open the file in Android Studio.

Step 3: Run the file in your emulator.

If you want the application to be on your own device, continue with the steps below:

Step 4: Go to your phone's Settings and search for About Phone/About Device. Press the Version/Build number for 7 times until your phone tells you that you are now a developer.

Step 5: In your settings search for Developer Options, turn on Wireless debugging and choose Pair Device with QR Code.

Step 6: In the android studio, open the pairing dialog and choose Pair Using Wi-Fi. Choose Pair using QR Code. Scan the QR Code using your phone.

Once successful, the device name will appear in Android Studio's list of available devices, and you can deploy SpendWise AI  in your phone by clicking the Run button.</p>

<h1>8. Future Roadmap</h1>
<p>
  
  * **Open Banking Integration** — Auto-sync with bank accounts and e-wallets
  (Touch 'n Go, GrabPay) to eliminate manual transaction entry, improving
  daily active usage and retention

* **Expanded Target Audience** — Scale beyond students to young working adults,
  families, and small business owners who need simple, guided financial
  management without professional consultation

* **Localised AI Model** — Train a specialised model on anonymised Malaysian
  spending data, factoring in festive spending patterns, state-level cost of
  living differences, and ringgit-specific budgeting habits

* **Strategic Partnerships** — Collaborate with Malaysian financial institutions,
  universities, and government programmes like AKPK to position SpendWise AI
  as an educational tool supporting national financial literacy efforts (SDG 4 & SDG 8)

  </p>

* **Southeast Asian Expansion** — Grow from a Malaysian student budgeting tool
  into a mainstream personal finance platform serving the broader Southeast
  Asian market
