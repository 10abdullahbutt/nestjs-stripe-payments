# NestJS Stripe Payments

A modular and reusable **NestJS + MongoDB** boilerplate for managing Stripe plans, subscriptions, and payments — ideal for SaaS applications.

## 🔧 Features

- 🧾 Create & manage subscription plans
- 💳 Stripe checkout session integration
- 📬 Webhook handling (subscription lifecycle)
- 👤 Customer mapping with MongoDB
- ⚙️ Configurable via environment variables
- ♻️ Clean modular structure with NestJS best practices

---

## 📁 Folder Structure

src/
├── config/ # App/Stripe/MongoDB config
├── modules/
│ ├── plans/ # Create plans (monthly, yearly)
│ ├── payments/ # Stripe checkout session
│ ├── users/ # Basic user model
│ └── webhooks/ # Handle Stripe events
├── common/ # Shared utilities
└── main.ts # App entry point




---|


**2. Install Dependencies**
npm install

**3. Setup Environment Variables**
cp .env.sample .env

**4. Run the App**
npm run start:dev


**Environment Variables**

| Variable                | Description                       |
| ----------------------- | --------------------------------- |
| `PORT`                  | App port (default 3000)           |
| `MONGO_URI`             | MongoDB connection string         |
| `STRIPE_SECRET_KEY`     | Stripe secret key                 |
| `STRIPE_WEBHOOK_SECRET` | Stripe webhook signing secret     |
| `FRONTEND_URL`          | Where Stripe redirects (optional) |


**Scripts**

| Command             | Description               |
| ------------------- | ------------------------- |
| `npm run start:dev` | Start app in dev mode     |
| `npm run build`     | Compile TypeScript code   |
| `npm run lint`      | Run ESLint code check     |
| `npm run test`      | Run unit tests using Jest |




**Stripe Webhooks Supported**
* checkout.session.completed
* invoice.paid
* customer.subscription.updated
* customer.subscription.deleted

 Use ngrok to expose your localhost and test webhooks in development.
