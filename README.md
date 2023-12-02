![Screenshot 2023-12-02 at 20 11 53](https://github.com/LuigiClemente/medusa_plugin/assets/110490237/68cc3f50-0c86-46e6-92a4-6ee4260700a7)

![image](https://github.com/LuigiClemente/medusa_plugin/assets/110490237/aade076d-c756-4d0e-9563-8e5df5d63bbc)

```mermaid
graph TD

subgraph Overview
  A[Explore and Subscribe]
  B[Account Activation]
  C[Switching Plans]
  D[Family Plan Features]

  A -->|Browse plans| B
  B -->|Click link| C
  C -->|Based on terms| D
end

subgraph Plans
  E[Science Plan]
  F[Guide Plan]
  G[Family Plan]

  E -->|Essential content| A
  F -->|Premium services| A
  G -->|Discounted access| A
end

subgraph Family_Plan_Behavior
  H[Joining]
  I[Leaving]
  J[Main Subscriber]

  H -->|Discreet transition| J
  I -->|Visible again| J
  J -->|Downgrade| E
end

subgraph Components
  K[Web Application]
  L[External Services]
  M[Database]

  K -->|Express.js, PostgreSQL| M
  L -->|Zammad, Stripe| M
  M -->|Users, Plans, Subscriptions, Invites| N[Entities]
end

subgraph How_It_Works
  O[Login]
  P[Subscription Process]
  Q[Changing Plans]
  R[Family Invitations]

  O -->|Upon login| K
  P -->|Browse, select, pay| F
  Q -->|Review and switch| F
  R -->|Send links| J
end

subgraph Extend_Entity
  S[Create Entity File]
  T[Implement Extended Entity]
  U[Create TypeScript Declaration File]
  V[Create Migration]
  W[Use Custom Entity]

  S -->|src/models/product.ts| T
  T -->|import, extend class| U
  U -->|src/index.d.ts| V
  V -->|src/migration/1680013376180-changeProduct.ts| W
end

subgraph API_Routes
  X[Request Parameters]
  Y[Response Fields]

  X -->|Extend validator| Y
end

```
**Overview**

Unlock exclusive content with our subscription service, offering three distinct plans: Science, Guide, and Family.

**Plans**

1. **Science Plan:**
    
    * Your gateway to essential content.
2. **Guide Plan:**
    
    * Elevate your experience with premium services in addition to Science Plan benefits.
3. **Family Plan:**
    
    * Avail discounted access for up to 5 family members.

**What You Can Do**

* **Explore and Subscribe:**
    
    * Browse different plans and choose the one that aligns with your preferences.
* **Account Activation:**
    
    * Activate your chosen plan effortlessly by clicking on the sent link post-subscription.
* **Switching Plans:**
    
    * Seamlessly transition between plans based on specified terms and conditions.
* **Family Plan Features:**
    
    * Invite family members and receive notifications for a connected experience.

**Family Plan Behavior**

* **Joining:**
    
    * Family member plans discreetly transition to a shared family plan page, visible exclusively to dependents.
* **Leaving:**
    
    * Personal plans become visible again if removed from the family plan.
* **Main Subscriber:**
    
    * Empower the main subscriber with control over the family plan and membership. They can downgrade, reverting all members to individual plans.

**Components**

* **Web Application:**
    
    * Crafted with Express.js and PostgreSQL for a seamless experience in managing subscriptions and payments.
* **External Services:**
    
    * Leverage Zammad for secure user authentication and Stripe for efficient payment processing.
* **Database**
    
    * **Users:**
        * Store subscriber details securely.
    * **Plans:**
        * Comprehensive information about available plans.
    * **Subscriptions:**
        * Establish links between subscribers and their active plans.
    * **Invites:**
        * Effectively manage family plan invitations.

**How It Works**

* **Login:**
    
    * Access plans and subscriptions seamlessly upon login, exclusive to Basic plan users.
* **Subscription Process:**
    
    * Browse plans, select, pay, and activate your chosen plan hassle-free.
* **Changing Plans:**
    
    * Review plan details and effortlessly switch plans based on predefined terms and conditions.
* **Family Invitations:**
    
    * Family leaders send personalized links to members; upon acceptance, members seamlessly integrate into the family plan as dependents.
