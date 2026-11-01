---
title: RLRPG Privacy Policy
permalink: /rlrpg/privacy-policy/
---

<!--
  DRAFT. Every [[TODO: ...]] must be filled in or removed before publishing.
  Hosting answers used for sections 6-8: see REPONSES-hebergement-sentry.md at the root of this repo.
  Not legal advice: have it reviewed before launch if you can.
-->

# RLRPG Privacy Policy

**Effective date:** [[TODO: date of publication]]
**Last updated:** [[TODO: date]]

This Privacy Policy explains how Sébastien Dubé ("**we**", "**us**", "**our**") collects, uses, shares and protects your personal information when you use the RLRPG mobile application (the "**App**") and the services behind it, including the RLRPG sign-in pages (together, the "**Service**").

RLRPG is a social app where you post photos of your real life to earn experience in skills (cooking, swimming, camping, etc.), complete quests, connect with other people and send them messages.

By creating an account or using the Service, you acknowledge that you have read this Privacy Policy. If you do not agree with it, please do not use the Service.

---

## 1. Who is responsible for your information

The Service is operated by **Sébastien Dubé**, an individual developer based in Québec, Canada, who is the data controller for your personal information.

Sébastien Dubé is also the **person in charge of the protection of personal information**. For any question, request or complaint about your personal information, write to:

**reallifecorpo@gmail.com**

---

## 2. Information we collect

### 2.1 Information you give us

| Information | Why we collect it |
|---|---|
| **Email address** | To create and secure your account, verify it, let you reset your password, and contact you about your account. |
| **Username** | To identify you to other users. Your username is visible to other users and can be found through user search. |
| **Password** | To sign you in. Your password is handled only by our authentication service and is stored as a one-way hash (bcrypt). We never store it in readable form and the RLRPG application server never sees it. |
| **Two-factor authentication (2FA)** | If you turn on 2FA, the secret used by your authenticator app is stored encrypted (AES-256) so we can check your codes. |
| **Profile picture** | Displayed on your profile and next to your content. If you do not upload one, we generate a default picture for you. |
| **Bio** | Displayed on your profile. |
| **Language and time zone** | To show the App, emails, notifications and content in your language and at the right time. |
| **Photos and captions (posts)** | To show them to the people you allow, to award experience points, and to moderate content (see section 4). |
| **Tags** | When you tag another user in a post or comment, that user is notified. |
| **Comments, likes and shares** | To display your interactions on posts and notify the post's author. |
| **Private messages** | Messages, replies, reactions (emojis), edits, conversation titles and conversation images, so they can be delivered to the participants of the conversation. We also record which message you last read to show read receipts. |
| **Social connections** | Connection requests, the people connected to you and the relationship level you give each of them (see section 5). |
| **Game data** | Skills, levels, experience points, quests and their progress, events, titles, unlocked rewards, themes, fonts and profile picture frames. |
| **Messages you send us** | If you contact us, we keep your message and our answer to handle your request. |

### 2.2 Information collected automatically

| Information | Why we collect it |
|---|---|
| **Sign-in sessions** | Creation date, last use and expiry of your sessions, so you stay signed in and can be signed out. |
| **Push notification token** and device platform (iOS or Android) | To send you notifications (messages, connection requests, tags, quests, events, moderation decisions). |
| **IP address** | To protect the Service against abuse through rate limiting. IP addresses used for rate limiting are kept only for a few minutes. Our hosting and network providers may also keep technical access logs containing IP addresses for a limited time (see section 8). |
| **Technical logs** | When our servers handle a request or encounter an error, technical details (time, request, error type) are written to server logs kept by our hosting provider, so we can fix bugs and investigate abuse. |
| **Moderation data** | For each photo: a moderation status, a reason if it was rejected, and a "perceptual hash" (a short numeric fingerprint of the image used to detect re-uploaded duplicates). If photos are rejected as inappropriate, we keep a record of these "strikes" and of any resulting account suspension. |

### 2.3 Device permissions

The App asks for the following permissions. You can refuse or revoke them at any time in your device settings; some features will then not work.

- **Camera** (and **microphone**, which the camera feature requires on iOS): to take photos for your posts. We do not record or keep audio.
- **Photo library**: to choose existing photos for your posts or profile picture. Only the photos you select are uploaded.
- **Notifications**: to send you push notifications.

We do **not** collect your precise location, your contacts, your advertising identifier, or your activity in other apps.

**Photo metadata:** photos taken with a phone can contain hidden information (metadata) such as the date and the GPS location where they were taken. We remove this metadata from your photos when they are uploaded, before they are stored or shown to anyone.

<!-- [[TODO: only publish the paragraph above once the EXIF removal issue is shipped.]] -->

---

## 3. How we use your information, and our legal bases

We use your information only for the purposes below. Where the law requires a legal basis (for example under the EU and UK General Data Protection Regulation, "GDPR"), the basis is indicated for each purpose.

| Purpose | Legal basis |
|---|---|
| **Provide the Service**: create and manage your account, publish your posts, show your feed, deliver your messages, run quests, skills and rewards, send account emails (verification, password reset). | Performance of our contract with you (the Terms of Use). |
| **Keep the community safe**: automatically review photos, enforce the community rules of our [Terms of Use](/rlrpg/terms-of-use/), and suspend accounts that repeatedly break the rules. | Our legitimate interest in providing a safe service, and our legal obligations regarding illegal content. |
| **Send push notifications.** | Your consent, which you give and can withdraw through your device's notification settings. |
| **Access your camera and photo library.** | Your consent, through your device's permission settings. |
| **Maintain and secure the Service**: fix bugs, monitor errors, prevent abuse, spam and fraud (rate limiting). | Our legitimate interest in keeping the Service working and secure. |
| **Comply with the law** and respond to valid legal requests. | Legal obligation. |

We **do not sell** your personal information, we **do not rent** it, and we **do not use it for advertising**. The App contains no ads. We do **not** send newsletters or promotional emails: we only email you about your account.

---

## 4. Automated photo review

To keep the App safe and make the game fair, every photo you post goes through an automated review before it is published:

1. **On our own servers**, an image-analysis model (CLIP) checks whether the photo is too dark or too blurry, whether it is likely to contain nudity or sexual content, and whether it actually shows the skills you tagged.
2. **When these checks cannot decide**, the photo and the skills you tagged are sent to **Anthropic** (the provider of the Claude AI model) for a second automated review. Anthropic processes the photo only to return a decision to us. [[TODO: check Anthropic's commercial API terms at publication. As of writing, API inputs are not used to train their models and are kept only for a limited period for abuse monitoring. Update this sentence accordingly.]]

Possible outcomes:

- the photo is **published**;
- the photo is published but **does not earn experience** for some of the tagged skills;
- the photo is **rejected** (for example: too blurry, inappropriate, or a duplicate). A rejected photo is never shown to other users and you are notified.

If **3** of your photos are rejected as inappropriate within **30 days**, your account is **automatically suspended**.

These decisions are made by automated processing. You have the right to know the main reasons for a decision, to present your point of view and to **ask for a human review** by writing to **reallifecorpo@gmail.com**.

---

## 5. Who can see your information

**Your profile.** Other users can see your username, profile picture, bio, title, level and skills, and your profile customization (theme, font, frame). They can find you by searching your username.

**Relationship levels.** When you accept someone's connection request, you choose the level at which you place that person, from the most distant to the closest: **Acquaintance**, **Friend** or **Best Friend**. People with no accepted connection are **Strangers**.

**Your posts (personal accounts).** Every time you publish a post, you choose its visibility among **Stranger**, **Acquaintance**, **Friend** and **Best Friend**. A post is visible to the people whose level is the one you chose **or closer**. For example:

- a post set to **Stranger** is visible to all users;
- a post set to **Friend** is visible only to the people you placed at Friend or Best Friend;
- a post set to **Best Friend** is visible only to your Best Friends.

**Creator accounts.** All posts of a creator account are visible to all users.

**Comments and likes** are visible to the people who can see the post.

**Private messages** are visible only to the participants of the conversation. They are encrypted in transit but are **not end-to-end encrypted**, which means they are stored on our servers in a form we could technically access. We only access them when necessary (for example to investigate a report of abuse or to comply with the law).

**Administrators.** Access to account and content data is limited to the operator of the Service and is used only to run the Service, moderate content, handle reports or respond to your requests. Administrators may also send announcements (broadcast notifications) to all users.

---

## 6. Service providers we share information with

We share personal information only with providers that help us run the Service, only to the extent necessary, and under terms that require them to protect it:

| Provider | Purpose | Information involved |
|---|---|---|
| **Railway Corporation** | Hosting of our servers, databases, cache and stored photos, and server logs | All data described in section 2 |
| **Cloudflare, Inc.** | Content delivery network (CDN) and protection of our servers against attacks: all traffic between the App and our servers passes through Cloudflare | Your IP address, basic device information and the content of the requests exchanged with our servers, in transit |
| **Brevo (Sendinblue SAS)** | Sending verification and password reset emails | Email address, username, language, content of the email |
| **Google Firebase Cloud Messaging** (Google LLC) | Delivering push notifications | Push token, notification content (for example sender name, message preview, quest title) |
| **Apple Push Notification service** (Apple Inc.), iOS only | Delivering push notifications on iPhone | Push token, notification content |
| **Anthropic, PBC** | Second-level review of some photos (section 4) | The photo and the tagged skills |
| **Google Fonts** (Google LLC) | Downloading the fonts used by the App | Your IP address and basic device information, as with any web request |

We may also disclose information:

- if required by law, a court order or a valid request from a public authority;
- to protect the rights, safety or property of our users, the public or ourselves (for example to investigate abuse or illegal content);
- if the Service is transferred to another person or company (for example a company created to operate RLRPG), in which case we will notify you before your information becomes subject to a different privacy policy.

---

## 7. International transfers

We are based in Canada, but our servers are not:

- our servers, databases, cache and stored photos are hosted by Railway in the **United States** (California);
- traffic to our servers passes through **Cloudflare**'s global network, which may handle it in a data center close to you;
- our email provider **Brevo** is located in the **European Union** (France);
- our other providers (Google, Apple and Anthropic) process information mainly in the **United States**.

Your information is therefore stored and processed outside your province, state or country, in particular in the United States, where data protection laws may differ from those where you live.

Before transferring personal information outside Québec, we assess whether it will receive adequate protection. For users in the European Economic Area, the United Kingdom or Switzerland, transfers to Canada rely on the adequacy decision recognizing Canada, and transfers to the United States or other countries rely on the European Commission's Standard Contractual Clauses or on the provider's certification under the EU-U.S. Data Privacy Framework, as applicable.

---

## 8. How long we keep your information

| Information | Retention |
|---|---|
| **Posts (photos and captions)** | Automatically deleted **3 days** after publication, together with their comments and likes, **unless you pin them to your profile**. Pinned posts are kept until you unpin or delete them, or delete your account. |
| **Rejected photos** | Deleted within 3 days. The moderation strike (without the photo) is kept as long as your account exists. |
| **Private messages** | Kept until you delete them or delete your account. |
| **Account, profile and game data** | Kept as long as your account exists. |
| **Sign-in sessions** | Until they expire or are revoked. |
| **Push notification tokens** | Until you sign out, the token becomes invalid, or you delete your account. |
| **Rate-limiting IP addresses** | A few minutes. |
| **Server and access logs** (which may contain IP addresses) | Up to **30 days**. |
| **Backups** | We do not currently keep backups of our databases or photos: deleted data is deleted for good. If we start keeping backups, we will update this policy with their retention period. |

---

## 9. Deleting your account

You can delete your account at any time **directly in the App**: go to your **profile**, tap the **Settings** icon (gear), then **Delete my account**.

When you delete your account, we permanently delete your account in our authentication service (email, username, password hash, 2FA secret, sessions), your profile, profile picture, posts and their photos, comments, likes, messages, connections, game data, notification tokens and moderation records.

Some information may remain for a limited time: entries in server logs until they expire (see section 8), and information we must keep to comply with the law or resolve a dispute.

If you can no longer access the App, you can request the deletion of your account on [[TODO: https://real-life-corp.github.io/rlrpg/delete-account/]] or by writing to **reallifecorpo@gmail.com** from the email address associated with your account.

---

## 10. Your rights

Depending on where you live (for example in Québec, elsewhere in Canada, in the European Economic Area, in the United Kingdom or in some U.S. states), you have some or all of the following rights:

- **access** the personal information we hold about you and obtain a copy of it;
- **correct** inaccurate or incomplete information;
- **delete** your information (see section 9);
- **withdraw your consent** at any time, without affecting the processing done before (for example by disabling notifications or camera access);
- **receive your information in a structured, commonly used and machine-readable format**, and have it sent to another service (portability);
- **object to** processing based on our legitimate interests, and **restrict** some processing;
- **not be subject to decisions based solely on automated processing** without the safeguards described in section 4, and ask for a human review;
- **file a complaint** with a data protection authority, for example the Commission d'accès à l'information du Québec, the Office of the Privacy Commissioner of Canada, or the supervisory authority of your country of residence in the EU.

You can edit much of your information directly in the App (bio, profile picture, language). For any other request, write to **reallifecorpo@gmail.com**. We may need to verify your identity before answering. We answer within **30 days** (one month under the GDPR, which may be extended in the cases provided by law). Exercising your rights is free.

We do not sell or "share" personal information as those terms are defined under California law, and we do not use sensitive personal information to infer characteristics about you.

---

## 11. Minimum age

RLRPG is reserved for people who are **16 years of age or older**. We do not knowingly collect personal information from anyone under 16. If you are a parent or guardian and believe that a person under 16 has created an account, contact us at **reallifecorpo@gmail.com** and we will delete it.

---

## 12. Security

We use reasonable technical and organizational measures to protect your information, including:

- encryption of data in transit (HTTPS and secure WebSockets);
- passwords handled only by a separate authentication service and stored as bcrypt hashes;
- optional two-factor authentication, with secrets stored encrypted;
- secure storage of sign-in tokens on your device (iOS Keychain / Android Keystore);
- access control on all private data and restricted administrator access;
- rate limiting to prevent abuse.

No system is completely secure. If a security incident involving your personal information creates a risk of serious harm, we will notify you and the relevant authorities as required by law.

---

## 13. Changes to this policy

We may update this Privacy Policy from time to time. The "Last updated" date at the top shows when it was last changed. If we make significant changes, we will notify you in the App or by email before they take effect.

---

## 14. Contact us

For any question about this Privacy Policy or your personal information:

**Sébastien Dubé**
Québec, Canada
**reallifecorpo@gmail.com**
