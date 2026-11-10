<!-- toc-page -->
<style>
  /* Hide the ToC on its own standalone site page (screen), but keep it
     visible inside the combined print page (#print-site-page) so it can
     render into the PDF. Never touches .md-main__inner or the site chrome. */
  @media screen {
    .toc-page { display: none; }
    #print-site-page .toc-page { display: block; }
  }
  /* Keep the ToC's own group headers flowing on one page in print,
     without re-paginating h2 headings anywhere else in the document. */
  @media print {
    .toc-page h2 { page-break-before: auto !important; }
  }
</style>

<div class="toc-page" markdown>

# **Table of Contents**

## [Introduction](index.md)

- [1. Regulated industries raise the bar for AI-assisted engineering](index.md#i-regulated-industries-raise-the-bar-for-ai-assisted-engineering)
- [2. What is IBM Bob?](index.md#ii-what-is-ibm-bob)
- [3. Environment: the GFM Bank demo application](index.md#iii-environment-the-gfm-bank-demo-application)
- [4. The lab journey](index.md#iv-the-lab-journey)
- [5. What you will build](index.md#v-what-you-will-build)
- [6. Next steps](index.md#vi-next-steps)

## [Registration and Setup](setup.md)

- [1. What you will configure](setup.md#i-what-you-will-configure)
- [2. Downloading the lab workspace](setup.md#ii-downloading-the-lab-workspace)
- [3. Opening the workspace in Bob IDE](setup.md#iii-opening-the-workspace-in-bob-ide)
- [4. Signing in to IBM Bob](setup.md#iv-signing-in-to-ibm-bob)
- [5. Ready to proceed](setup.md#v-ready-to-proceed)

## [Analyze - Understanding the Core Banking Codebase](1-1.md)

- [1. What you will analyze](1-1.md#i-what-you-will-analyze)
- [2. Why this matters](1-1.md#ii-why-this-matters)
- [3. Hands-on: analyzing the codebase](1-1.md#iii-hands-on-analyzing-the-codebase)
- [4. Key takeaways](1-1.md#iv-key-takeaways)

## [Build - Building the Carbon Teller Front-End](2-1.md)

- [1. What you will build](2-1.md#i-what-you-will-build)
- [2. Why this matters](2-1.md#ii-why-this-matters)
- [3. Hands-on: proving the backend connection](2-1.md#iii-hands-on-proving-the-backend-connection)
- [4. Hands-on: generating the teller portal](2-1.md#iv-hands-on-generating-the-teller-portal)
- [5. Key takeaways](2-1.md#v-key-takeaways)

## [Build - Running, Debugging, and Iterating](2-2.md)

- [1. What you will do](2-2.md#i-what-you-will-do)
- [2. Why this matters](2-2.md#ii-why-this-matters)
- [3. Hands-on: starting the application](2-2.md#iii-hands-on-starting-the-application)
- [4. Hands-on: the debug loop](2-2.md#iv-hands-on-the-debug-loop)
- [5. Hands-on: completing the teller task](2-2.md#v-hands-on-completing-the-teller-task)
- [6. Key takeaways](2-2.md#vi-key-takeaways)

## [Secure - Security Analysis and Remediation](3-1.md)

- [1. What you will secure](3-1.md#i-what-you-will-secure)
- [2. Why this matters](3-1.md#ii-why-this-matters)
- [3. Hands-on: scanning for vulnerabilities](3-1.md#iii-hands-on-scanning-for-vulnerabilities)
- [4. Hands-on: documenting the findings](3-1.md#iv-hands-on-documenting-the-findings)
- [5. Hands-on: remediating and verifying](3-1.md#v-hands-on-remediating-and-verifying)
- [6. Hands-on: confirming the application still works](3-1.md#vi-hands-on-confirming-the-application-still-works)
- [7. Key takeaways](3-1.md#vii-key-takeaways)
- [8. Earn accreditation](3-1.md#viii-earn-accreditation)

</div>
