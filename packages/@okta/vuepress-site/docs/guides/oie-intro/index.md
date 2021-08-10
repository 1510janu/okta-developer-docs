---
title: Okta Identity Engine
meta:
  - name: description
    content: Okta Identity Engine offers customizable building blocks that can support dynamic, app-based user journeys. Find out more about Okta Identity Engine, why you would use it, and how to upgrade your org.
---

# Identity Engine

<ApiLifecycle access="ie" /><br>
<ApiLifecycle access="Limited GA" />

## About Okta Identity Engine

The Okta Identity Engine is a platform service that powers flexible and customizable access experiences, which allows enterprises to build access experiences tailored to their organizational needs. Just one of the many goals of Okta Identity Engine is to no longer bind customers to any one way of identifying, authorizing, enrolling, and issuing access to users. Instead, they can customize and extend each of these steps, which delivers more flexible and customizable access experiences for Okta's access management products &mdash; Authentication (Customer Identity), Single Sign-On, and Multifactor Authentication.




To take advantage of these new features and for a better development experience, use the Okta Identity Engine SDKs to manage authentication in your apps. These new SDKs are recommended for orgs using Okta Identity Engine.

Experiment with sample apps that showcase Okta Identity Engine using the following authentication approaches:

- Redirect: These sample apps demonstrate how to redirect users to an Okta-hosted sign-in page, and then receive users redirected back from Okta after users sign in. This approach is recommended for most developers, as it is easier to build and maintain.

- Embedded: These sample apps demonstrate how to embed the Okta Sign-In Widget in an app as a package dependency.

Learn how to implement each approach with these Okta Identity Engine SDKs and sample apps in the Redirect authentication guide, Embedded authentication with SDK guide, and Embedded authentication with Sign-In Widget guide.

Orgs using Okta Identity Engine can also continue to use current SDKs and tools. You can find those SDKs for your stack from the Languages & SDKs overview.












## Why use Identity Engine?

Okta Identity Engine provides:

* Passwordless authentication

  Admins can enable the email authenticator now with the addition of a magic link in the email notification sent to end users. When policies are configured to include non-password authenticators, end users may sign in to their account using factors that don't require the use of a password. See [Configure passwordless authentication with email magic link](https://help.okta.com/en/oie/Content/Topics/identity-engine/procedures/configure-passwordless-auth.htm).

* Progressive profiling

  Update an existing user's profile by prompting them for additional sign-in information when they advance to designated points. See [Create a Profile Enrollment policy for progressive profiling](https://help.okta.com/en/oie/okta_help_CSH.htm#ext-create-profile-enrollment).

* App-level policies

  App sign-on policies define the full requirements for an app. Admins can configure Okta Sign-On Policies to use App-level policies instead &mdash; making it easier to manage your apps. See [App sign-on policies](https://help.okta.com/en/oie/Content/Topics/identity-engine/policies/about-app-sign-on-policies.htm).

* MFA enrollment policies

  With MFA enrollment policies, you can create and enforce policies and rules for specific MFA factors and assign groups accordingly. Sign-on policies determine the types of authentication challenges end users experience when they sign in to their account. MFA enrollment policies are based on a variety of factors, such as location, group definitions, and authentication type. See [Create an MFA enrollment policy](https://help.okta.com/en/oie/Content/Topics/identity-engine/policies/create-mfa-policy.htm).

## New concepts and terminology

Okta Identity Engine introduces new concepts and terminology.

* Assurance

  Assurance is the degree of confidence that an end user signing in to an application is the same end user who previously signed in to the application, and the use of one or more authenticators (see below) and its characteristics determine an assurance level. For example, an end user who authenticates with a knowledge factor and a possession factor has a higher assurance level than one who can only authenticate with one factor.

  Assurance is enforced by sign-on policies. Okta Identity Engine requires that the assurance specified in the Okta and app sign-on policies are satisfied before it allows the end user to access an app. This is a change from the traditional model of authentication, which evaluates one policy depending on whether the user signs in to the org or directly through the app.

* Authenticators

  Authenticators are credentials owned or controlled by an end user that can be verified by an application or service. Passwords, answers to security questions, phones (SMS or voice), and authentication apps like Okta Verify are examples of authenticators.

* Factor types

  Okta is changing its definition of authenticators and factors to provide an industry-standard differentiation:

  * Factors are different categories that define how authentication takes place and the means in which they are controlled by end users.
  * Authenticators are used to verify one or more multiple factors such as Knowledge (for example, passwords and security questions), Possession (for example, Email, SMS, Okta Verify, and hardware tokens), and Inherence/Biometrics (for example, fingerprints and facial recognition).
  * A sign-on policy with two-factor authentication requires two distinct factors. Two authenticators of the same factor (Knowledge, Possession, or Inherence) isn't accepted.

* Okta Sign-On Policies

  Okta Sign-On Policies are globally applied to all applications in the tenant, and specify actions to take, such as allowing access, prompting for a challenge, setting the time before prompting for another challenge, and expiring a session. See [Okta Sign-On Policies](https://help.okta.com/en/oie/Content/Topics/identity-engine/policies/about-okta-sign-on-policies.htm).

* App sign-on policies

  App sign-on policies enforce authentication when an end user attempts to access an application. Each application is assigned one app sign-on policy (with multiple rules that you can order). See [App sign-on policies](https://help.okta.com/en/oie/Content/Topics/identity-engine/policies/about-app-sign-on-policies.htm).

## Enable Okta Identity Engine for your organization

To upgrade to Okta Identity Engine, reach out to your account manager. If you don't have an account manager, reach out to oie@okta.com for more information.

* The v1 API continues to work as before until you're ready to use new Okta Identity Engine functionality.
* The existing Okta-hosted widget continues to work after upgrading your org.
* Upgrade your SDK as you would normally do with other SDK updates.
