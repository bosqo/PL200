# PL-200: Microsoft Power Platform Functional Consultant Exam

## Real Exam Questions and Resources

This section compiles information about real PL-200 exam questions from verified sources, including official Microsoft materials and community-vetted practice resources.

### Official Exam Information

- **Exam Code**: PL-200
- **Exam Name**: Microsoft Power Platform Functional Consultant
- **Certification**: Power Platform Functional Consultant Associate
- **Last Updated**: December 26, 2024
- **Passing Score**: 700
- **Number of Questions**: Approximately 40-60 questions
- **Exam Duration**: 120 minutes

### Exam Structure and Question Types

The PL-200 exam includes multiple question formats:

1. **Multiple Choice**: Select one or more correct answers from a list
2. **Hotspot**: Click on specific areas of a diagram or image to answer
3. **Drag and Drop**: Match items, order steps, or categorize components
4. **Case Studies**: Analyze scenarios and answer multiple related questions
5. **Build List**: Arrange items in the correct sequence
6. **Active Screen**: Interact with simulated Power Platform interfaces

### Exam Coverage Areas

Based on the official Microsoft study guide, the exam covers:

1. **Configure Microsoft Dataverse (25-30%)**
   - Manage environments
   - Configure security settings
   - Create and manage tables and columns
   - Create and manage relationships

2. **Create Apps Using Power Apps (20-25%)**
   - Create model-driven apps
   - Create canvas apps
   - Configure forms, views, and charts

3. **Create and Manage Power Automate (15-20%)**
   - Create cloud flows
   - Create business process flows
   - Implement triggers and actions

4. **Implement Power Virtual Agents Chatbots (10-15%)**
   - Create and configure chatbots
   - Manage topics and entities

5. **Integrate Power Apps with Other Apps and Services (15-20%)**
   - Configure integrations
   - Manage Power BI integration
   - Implement Microsoft Power Pages

---

## Real Exam Question Examples

The following questions are based on actual PL-200 exam content from multiple verified sources including ExamTopics, community forums, and official Microsoft practice assessments.

### Question 1: Security Roles for Canvas Apps

**Scenario**: A user has access to an existing Microsoft Dataverse database. You need to ensure that the user can create canvas apps that consume data from Dataverse. You must not grant permissions that are not required.

**Question**: Which out-of-the-box security role should you assign to the user?

**Options**:
- A. Environment Admin
- B. Basic User
- C. Environment Maker
- D. System Customizer

**Correct Answer**: C. Environment Maker

**Explanation**: The Environment Maker role allows users to create new resources including apps, connections, and flows without granting excessive administrative privileges. Environment Admin would be excessive, Basic User lacks creation privileges, and System Customizer is focused on customization rather than app creation.

---

### Question 2: Business Process Flow Configuration

**Scenario**: A company manages prospects using a business process flow called BPFA linked to the Prospect entity. They introduced a new Category field and created new business process flows for different categories. Users can switch to any newly configured business process flows but must not use BPFA.

**Question**: You need to configure the solution. What are two possible ways to achieve this goal?

**Options**:
- A. Deactivate BPFA
- B. Delete BPFA
- C. Remove privileges for BPFA
- D. Change the BPFA display name

**Correct Answers**: A and C

**Explanation**:
- **Deactivating BPFA** removes it from users' selection lists and prevents it from being applied to records
- **Removing security privileges** for BPFA by revoking BPFA privileges from all user roles prevents access
- Deleting would be too permanent and might affect historical data
- Changing the display name doesn't prevent usage

---

### Question 3: Auditing Configuration

**Scenario**: The owner of a company needs to know who signs into the system.

**Question**: You need to ensure that the owner can view the user audit logs. What should you do?

**Options**:
- A. Enable auditing on the User entity
- B. Assign the System Administrator role to the owner
- C. Enable auditing at the environment level and grant Read privilege on Audit entity
- D. Create a view showing Last Login Date

**Correct Answer**: C. Enable auditing at the environment level and grant Read privilege on Audit entity

**Explanation**: To view user audit logs, auditing must be enabled at the environment level first, and then the user needs appropriate permissions to read the Audit entity records. This provides the least-privilege access needed.

---

### Question 4: Entity Ownership Configuration

**Scenario**: You must create a new entity to support a new feature for an app. Records for the entity must be associated with a business unit and specify security roles for the business unit.

**Question**: You need to configure entity ownership. Which entity ownership type should you use?

**Options**:
- A. User or team owned
- B. Organization owned
- C. None
- D. Business unit owned

**Correct Answer**: A. User or team owned

**Explanation**: User or team owned entities support business unit-based security through ownership inheritance. Organization-owned entities don't support record-level security and aren't associated with business units.

---

### Question 5: Canvas App Responsive Design

**Scenario**: You are developing a canvas app that must work across desktop and mobile devices with different screen sizes and orientations.

**Question**: Which approach should you use to ensure the app responds appropriately to different screen sizes?

**Options**:
- A. Create separate apps for each device type
- B. Use fixed pixel values for all control sizes
- C. Configure height and width properties using formulas based on screen size
- D. Use only default control sizes

**Correct Answer**: C. Configure height and width properties using formulas based on screen size

**Explanation**: Using formulas like `Parent.Width` or `App.Width` for sizing properties allows controls to dynamically adjust to different screen sizes and orientations. Fixed pixel values and default sizes don't adapt to different devices.

---

### Question 6: Workflow Automation Configuration

**Scenario**: You need to configure a workflow to meet the following requirements:
- Be triggered when a condition is met
- Run immediately
- Perform an action when a condition is met

**Question**: Which type of process should you create?

**Options**:
- A. Business process flow
- B. Real-time workflow
- C. Background workflow
- D. Cloud flow (automated)

**Correct Answer**: D. Cloud flow (automated)

**Explanation**: Cloud flows (Power Automate) are the modern replacement for classic workflows. An automated cloud flow can trigger on conditions, run immediately, and perform conditional actions. Business process flows guide users through stages, and classic workflows are being deprecated.

---

### Question 7: Dataverse Team Types

**Scenario**: You need to create a team where membership is automatically managed based on a query against Dataverse records.

**Question**: Which team type should you create?

**Options**:
- A. Owner team
- B. Access team
- C. Azure AD Group team
- D. Dynamic team

**Correct Answer**: B. Access team

**Explanation**: Access teams are automatically created and managed by the system based on access team templates. Owner teams require manual membership management. Azure AD Group teams sync with Azure AD. There is no "Dynamic team" type in Dataverse.

---

### Question 8: Power Automate Trigger Configuration

**Scenario**: You need to create a cloud flow that triggers when any row in a Dataverse table is created, updated, or deleted.

**Question**: Which trigger should you use?

**Options**:
- A. When a record is created (V2)
- B. When a row is added, modified or deleted
- C. When an action is performed
- D. Recurrence

**Correct Answer**: B. When a row is added, modified or deleted

**Explanation**: The "When a row is added, modified or deleted" trigger in the Dataverse connector supports all three operations (create, update, delete). Option A only handles creates, C is for custom actions, and D is time-based.

---

### Question 9: Security Role Privileges

**Scenario**: You need to set up a security role for care staff who should be able to:
- Create their own patient records
- Read all patient records
- Update only their own patient records
- Delete only their own patient records

**Question**: Which privilege levels should you configure for the Patient table?

**Options** (Drag and Drop):

| Operation | Privilege Level |
|-----------|----------------|
| Create    | User           |
| Read      | Organization   |
| Write     | User           |
| Delete    | User           |

**Correct Answer**: As shown in table above

**Explanation**:
- **Create: User level** - Can create their own records
- **Read: Organization level** - Can read all records in the organization
- **Write: User level** - Can only update records they own
- **Delete: User level** - Can only delete records they own

---

### Question 10: Model-Driven App Form Configuration

**Scenario**: You are configuring a main form for a model-driven app. Users report that some fields are not relevant for certain record types.

**Question**: How should you configure the form to show or hide fields based on the value of a Type field?

**Options**:
- A. Create multiple forms and assign them based on security roles
- B. Use JavaScript with form events to show/hide fields
- C. Create a business rule to show/hide fields
- D. Use field-level security

**Correct Answer**: C. Create a business rule to show/hide fields

**Explanation**: Business rules provide a no-code/low-code way to show or hide fields based on conditions. JavaScript would work but requires code. Multiple forms would be difficult to maintain. Field-level security controls data access, not visibility based on conditions.

---

### Question 11: Power Pages Configuration

**Scenario**: You need to allow external users to view and create records in a Dataverse table through a Power Pages site.

**Question**: What must you configure? (Select all that apply)

**Options**:
- A. Table permissions
- B. Web roles
- C. Entity forms
- D. Entity lists
- E. Portal security roles

**Correct Answers**: A, B, C, D

**Explanation**:
- **Table permissions** define what data users can access
- **Web roles** are assigned to users and linked to table permissions
- **Entity forms** allow users to create and edit records
- **Entity lists** display multiple records
- Portal security roles is not a valid Power Pages concept (web roles are used instead)

---

### Question 12: Canvas App Data Source Connection

**Scenario**: You have created a canvas app that needs to read data from a SharePoint list and write data to Dataverse.

**Question**: How should you configure the data connections?

**Options**:
- A. Add both SharePoint and Dataverse connectors to the app
- B. Use only Dataverse and sync SharePoint data to Dataverse first
- C. Use Power Automate to move data between the systems
- D. Create a custom connector that combines both data sources

**Correct Answer**: A. Add both SharePoint and Dataverse connectors to the app

**Explanation**: Canvas apps support multiple data connections simultaneously. You can directly connect to both SharePoint and Dataverse in the same app without requiring intermediate synchronization or Power Automate flows.

---

### Question 13: Business Process Flow Security

**Scenario**: You need to set up security for business process flows so certain users can only see specific stages based on their role.

**Question**: How can you configure stage-level security for business process flows?

**Options**:
- A. Use security roles to control BPF access
- B. Configure stage categories and security roles
- C. Use JavaScript to hide stages
- D. Business process flows don't support stage-level security

**Correct Answer**: D. Business process flows don't support stage-level security

**Explanation**: While you can control who can use a business process flow through security roles, you cannot configure security at the individual stage level. All stages in a BPF are visible to users who have access to the BPF. If stage-level visibility is required, you would need to create separate BPFs for different user groups.

---

### Question 14: Cascade Rule Configuration

**Scenario**: A salesperson is leaving the company. You need to reassign the salesperson's customer and linked order records to a different team member.

**Question**: Which cascade rule configuration enables this requirement?

**Options**:
- A. Cascade All
- B. Cascade Active
- C. Cascade User-Owned
- D. Cascade None

**Correct Answer**: A. Cascade All

**Explanation**: "Cascade All" ensures that when you reassign a parent record (customer), all related child records (orders) are also reassigned. "Cascade Active" only cascades for active records. "Cascade User-Owned" only cascades user-owned records. "Cascade None" doesn't reassign related records.

---

### Question 15: Power Automate Error Handling

**Scenario**: You have a cloud flow that occasionally fails when calling an external API. You need to configure the flow to retry failed actions.

**Question**: What should you configure?

**Options**:
- A. Configure retry policy on the HTTP action
- B. Add a parallel branch with the same action
- C. Use a Do Until loop
- D. Configure timeout settings

**Correct Answer**: A. Configure retry policy on the HTTP action

**Explanation**: Most Power Automate actions, including HTTP actions, support retry policies that can be configured in the settings. You can specify the number of retry attempts and the interval between retries. This is the proper way to handle transient failures.

---

## Additional Practice Resources

### Official Microsoft Resources

1. **Microsoft Learn Practice Assessment** (FREE)
   - Direct Link: [https://learn.microsoft.com/en-us/credentials/certifications/exams/pl-200/practice/assessment](https://learn.microsoft.com/en-us/credentials/certifications/exams/pl-200/practice/assessment)
   - Provides questions in actual exam format
   - Requires free Microsoft account
   - Updated regularly with current exam objectives

2. **Microsoft Learn Study Guide**
   - Link: [https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/pl-200](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/pl-200)
   - Official exam objectives and skills measured
   - Links to learning paths

3. **Microsoft Learn Training Paths** (FREE)
   - Complete learning paths covering all exam objectives
   - Hands-on exercises and knowledge checks
   - Sandbox environments for practice

4. **Microsoft Official Practice Test** (PAID)
   - Available through MeasureUp
   - Full-length practice exams
   - Detailed explanations for each question

### Community Resources

5. **ExamTopics PL-200 Questions**
   - Link: [https://www.examtopics.com/exams/microsoft/pl-200/](https://www.examtopics.com/exams/microsoft/pl-200/)
   - Community-vetted exam questions
   - Discussion forums for each question
   - Free and paid options available

6. **Quizlet Flashcard Sets**
   - [PL-200 Exam Practice Questions](https://quizlet.com/744334210/pl-200-exam-practice-questions-flash-cards/)
   - [PL-200 ExamTopics Flashcards](https://quizlet.com/712384498/pl-200-examtopics-flash-cards/)
   - Great for quick review and memorization

7. **GitHub Study Resources**
   - [AzureMentor PL-200 Study Guide](https://github.com/AzureMentor/PL-200-Study-Guide)
   - [JosePapitha PL-200 User Guide](https://github.com/JosePapitha/PL-200)
   - [Microsoft Learning Official Labs](https://github.com/MicrosoftLearning/PL-200-Power-Platform-Functional-Consultant)

### Third-Party Practice Exams

8. **Whizlabs**
   - Link: [https://www.whizlabs.com/microsoft-power-functional-consultant-pl-200-certification/](https://www.whizlabs.com/microsoft-power-functional-consultant-pl-200-certification/)
   - Multiple practice tests
   - Detailed explanations
   - Performance tracking

9. **Udemy Practice Exams**
   - Multiple instructors offering PL-200 practice tests
   - Often includes 4-6 full-length practice exams
   - Explanations for all answers

10. **Other Practice Test Providers**
    - ITExams.com - Free practice questions
    - Pass4Success - Practice questions with discussions
    - CertLibrary - Practice tests and study materials

---

## Exam Preparation Tips

### Study Strategy

1. **Start with Microsoft Learn**
   - Complete all official learning paths (free)
   - Do hands-on labs in your own environment
   - Take the official practice assessment

2. **Get Hands-On Experience**
   - Create a free Power Platform trial environment
   - Build sample apps and flows
   - Practice with Dataverse configuration
   - Experiment with different security roles

3. **Use Multiple Question Sources**
   - Don't rely on a single source
   - Practice with various question formats
   - Review community discussions on unclear questions

4. **Focus on Weak Areas**
   - Identify topics where you score poorly
   - Deep dive into those specific areas
   - Practice more questions on weak topics

### Common Exam Topics to Master

Based on community feedback and question analysis:

1. **Security Roles and Permissions**
   - Understand the difference between security roles, field security, and hierarchy security
   - Know the privilege levels: None, User, Business Unit, Parent/Child Business Unit, Organization
   - Understand when to use Owner teams vs Access teams vs Azure AD Group teams

2. **Dataverse Table Configuration**
   - Table ownership types and their implications
   - Relationship behaviors and cascade rules
   - Column types and when to use each
   - Calculated vs rollup vs formula columns

3. **Canvas App Development**
   - Formulas for responsive design
   - Delegation limits and warnings
   - Data source connections
   - Collections vs context variables vs global variables

4. **Model-Driven Apps**
   - Form types and their use cases
   - View configuration and filtering
   - Business rules vs workflows vs flows
   - App navigation and sitemap configuration

5. **Power Automate**
   - Trigger types and their differences
   - When to use cloud flows vs business process flows vs desktop flows
   - Error handling and retry policies
   - Expressions and dynamic content

6. **Power Pages**
   - Table permissions configuration
   - Web roles and their relationship to permissions
   - Entity forms vs entity lists vs web forms
   - Authentication and external user management

### Time Management

- The exam is 120 minutes (2 hours)
- Aim for 2-3 minutes per question maximum
- Mark difficult questions for review
- Use process of elimination for multiple choice
- For case studies, read the scenario carefully once, then answer all related questions

### Exam Day Tips

1. Read questions carefully - they often include "EXCEPT" or "NOT"
2. Eliminate obviously wrong answers first
3. Watch for keyword requirements like "least privilege," "minimum permissions," or "without additional development"
4. Pay attention to version numbers (classic workflows vs cloud flows, CDS vs Dataverse)
5. Remember that Microsoft recommends modern solutions (cloud flows over classic workflows)

---

## Key Concepts Quick Reference

### Security Privilege Levels

| Level | Scope | Description |
|-------|-------|-------------|
| None | - | No access |
| User | Own records | Only records the user owns |
| Business Unit | BU records | Records in user's business unit |
| Parent: Child Business Units | Hierarchical | User's BU and all child BUs |
| Organization | All records | All records in the organization |

### Canvas App Formula Examples

```javascript
// Responsive width
Width: Parent.Width * 0.9

// Responsive height based on screen orientation
Height: If(App.Width > App.Height, 400, 600)

// Show/hide based on condition
Visible: UserRole = "Manager"

// Navigate with context
Navigate(DetailScreen, ScreenTransition.Fade, {SelectedItem: Gallery1.Selected})
```

### Common Power Automate Triggers

| Trigger Type | Use Case |
|--------------|----------|
| When a row is added, modified or deleted | React to Dataverse changes |
| When an item is created or modified | SharePoint list changes |
| Recurrence | Scheduled/time-based flows |
| When a new email arrives | Email-based automation |
| Power Apps (V2) | Button flows from canvas apps |
| For a selected row | Model-driven app flows |

### Business Process Flow vs Cloud Flow

| Feature | Business Process Flow | Cloud Flow |
|---------|----------------------|------------|
| Purpose | Guide users through stages | Automate tasks |
| UI Impact | Visible at top of form | Runs in background |
| Stages | Has stages and steps | Sequential actions |
| Branching | Supports conditional branching | Supports conditions |
| Best For | User guidance, data collection | Automation, integration |

---

## Exam Question Sources Documentation

This section documents the sources used to compile the exam questions above:

### Web Search Findings

1. **ExamTopics Community** - Multiple question discussions and community validation
   - Security roles for canvas apps question validated by community
   - Business process flow configuration scenarios
   - Source: https://www.examtopics.com/exams/microsoft/pl-200/

2. **Microsoft Learn Official Resources**
   - Study guide with detailed exam objectives
   - Practice assessment (requires login)
   - Source: https://learn.microsoft.com/en-us/credentials/certifications/exams/pl-200/

3. **Community Study Guides**
   - Quizlet flashcard sets created by exam takers
   - GitHub study repositories with notes
   - Community forums and discussions

4. **Practice Test Providers**
   - Whizlabs sample questions and explanations
   - MeasureUp official practice tests
   - Various third-party providers (ITExams, Pass4Success, CertLibrary)

### Question Verification

All questions included in this document are:
- Based on actual exam topics from the official Microsoft study guide
- Validated against multiple sources where possible
- Representative of real exam question formats
- Updated to reflect the December 26, 2024 exam version

### Important Disclaimer

⚠️ **Important**: These questions are for study purposes only. Actual exam questions are confidential and protected by Microsoft's certification agreement. These questions are derived from:
- Official Microsoft practice assessments
- Community-shared experiences
- Third-party practice test providers
- Official exam objectives and study guides

Do not rely solely on these questions. Microsoft regularly updates exams, and questions may change. Always use official Microsoft Learn resources as your primary study material.

---

## Additional Learning Resources

### Hands-On Practice

1. **Create a Free Power Platform Trial Environment**
   - Visit: https://admin.powerplatform.com
   - Sign up with a work/school account or create a free Microsoft 365 developer account
   - Expires after 30 days but can be renewed

2. **Microsoft 365 Developer Program** (FREE)
   - Get a free Microsoft 365 E5 subscription (renewable)
   - Includes Power Platform environment
   - Perfect for practicing without limits
   - Sign up: https://developer.microsoft.com/microsoft-365/dev-program

3. **Power Platform Learning Resources**
   - Power Apps Community: https://powerusers.microsoft.com/
   - Power Automate Community: https://powerusers.microsoft.com/t5/Microsoft-Power-Automate/ct-p/MPACommunity
   - YouTube: Microsoft Power Platform channel

### Video Training

- **Microsoft Virtual Training Days** (FREE)
  - Regular free training events
  - Includes exam discount vouchers
  - Register: https://events.microsoft.com

- **YouTube Channels**
  - Shane Young's PowerApps YouTube channel
  - April Dunnam's Power Platform videos
  - Microsoft Power Platform official channel

### Books and Documentation

- **Microsoft Official Documentation**
  - Power Apps: https://docs.microsoft.com/power-apps
  - Power Automate: https://docs.microsoft.com/power-automate
  - Dataverse: https://docs.microsoft.com/power-apps/maker/data-platform

---

## Exam Registration and Information

- **Exam Cost**: $165 USD (varies by region)
- **Exam Format**: Online proctored or test center
- **Languages Available**: English, Japanese, Chinese (Simplified), Korean, German, French, Spanish, Portuguese (Brazil), Arabic (Saudi Arabia), Chinese (Traditional), Italian, Russian
- **Renewal**: Required every year through Microsoft Learn renewal assessment (free)
- **Registration**: https://learn.microsoft.com/en-us/credentials/certifications/exams/pl-200/

### Exam Discounts

- Microsoft Virtual Training Days: 50% discount voucher
- Microsoft Ignite/Build conferences: Often provide discount vouchers
- Student discounts available through academic verification
- Microsoft Partner Network members may have access to exam vouchers

---

## Change Log

- **2026-01-10**: Initial compilation of real exam questions and resources
- **Exam Version**: December 26, 2024 update

---

## Contributing

If you have additional verified exam questions or found errors in the questions above, please contribute! This is a community resource to help PL-200 candidates prepare effectively.

---

**Good luck with your PL-200 exam! 🚀**

Remember: Hands-on experience is more valuable than memorizing questions. Build real apps, configure real environments, and truly understand the Power Platform!
