**GETTING STARTED**
# **REGISTRATION AND SETUP**

---

## **i. WHAT YOU WILL CONFIGURE**

![type:video](./_videos/Registration and Setup [Bob Regulated L3].mp4)
!!! note ""
    Christopher Bienko *(AI Enablement GTM Product Manager)* provides an overview of the *Registration and Setup* module for the hands-on enablement. **<a href="https://ibm.seismic.com/Link/Content/DCWJcf9cTHgD4G9B8PPDX7b33BB3" target="_blank">[2 min]</a>**

Before beginning [Module 1 | Analyze](1-1.md){:target="_blank"} of the hands-on lab, three components must be in place.

!!! success "PREREQUISITES"
    1. The **IBM Bob IDE**, installed and registered on your local machine.
    2. The **lab workspace**, downloaded from IBM Seismic and extracted locally.
    3. An **authenticated Bob session** inside that workspace.

Installation and registration of the Bob IDE are covered in the <a href="https://ibm.github.io/bob-l3/setup/" target="_blank">Setup chapter of *Climbing the AI Maturity Curve*</a>, which you completed as the prerequisite to this course. This page covers the remaining two components.

---

## **ii. DOWNLOADING THE LAB WORKSPACE**

The lab is delivered as a single `.zip` archive containing the starter project files. Inside are the GFM Bank codebase and the offline Carbon references, along with helper scripts and the pre-configured `.bob` workspace settings.

---

### **Download the workspace archive**

1. Navigate to the IBM Seismic page that hosts the lab materials. It opens to the **IBM Bob Regulated Industry** content item.

    !!! warning "IBM SEISMIC CONTENT ITEM"
        **URL: <a href="https://ibm.seismic.com/Link/Content/DCTCG7pcP7p8dG7WD7jBBX39mJQ8" target="_blank">https://ibm.seismic.com/Link/Content/DCTCG7pcP7p8dG7WD7jBBX39mJQ8</a>**

    <p align="left">
    <img src="https://colony-recorder.s3.us-west-1.amazonaws.com/files/org_c5a86d7505634b408ffed7c02e1a91dc/team_1e16acc894ad4e0eba6e176fd42bdcc1/document_5c11ed2e1ddf4b89837d732997cd74b8/steps/step_dadfaec74ba942f3976e806e1252f76d_bef6b801af19407ebe7abca2fd5ede3b_ba9909dbd6dd4d13984b531c0d78ffb6_text_export.jpeg" alt="" width="600" />
    </p>

2. Click **Download** to retrieve the **IBM Bob Regulated Industry** `.zip` file.

    <p align="left">
    <img src="https://colony-recorder.s3.us-west-1.amazonaws.com/files/org_c5a86d7505634b408ffed7c02e1a91dc/team_1e16acc894ad4e0eba6e176fd42bdcc1/document_5c11ed2e1ddf4b89837d732997cd74b8/steps/step_bd8c3222e4294fda917b5c4589f76747_0cebb618f12f4142861552f312407d6e_eeed3405e4bb42aa94581eb48d5c183d_text_export.jpeg" alt="" width="600" />
    </p>

---

### **Extract the archive**

3. Once the download completes, open your operating system's file manager and navigate to the location where the `.zip` file was saved — typically your **Downloads** folder.

    - The **Show in folder** icon in your browser's download bar is a quick shortcut.
    - The archive must be extracted before Bob can open it.

    <p align="left">
    <img src="https://colony-recorder.s3.us-west-1.amazonaws.com/files/org_c5a86d7505634b408ffed7c02e1a91dc/team_1e16acc894ad4e0eba6e176fd42bdcc1/document_5c11ed2e1ddf4b89837d732997cd74b8/steps/step_74c1089ee7f240f79d21178843d1de49_daa092fe79864fb08cdd5c2680f139a3_00716081182d4a91a389dd62c40093a0_text_export.jpeg" alt="" width="600" />
    </p>

4. Select the downloaded **IBM Bob Regulated Industry** zip file and click **Extract all**. Extracting it produces the workspace folder that Bob will open in the next section.

    <p align="left">
    <img src="https://colony-recorder.s3.us-west-1.amazonaws.com/files/org_c5a86d7505634b408ffed7c02e1a91dc/team_1e16acc894ad4e0eba6e176fd42bdcc1/document_5c11ed2e1ddf4b89837d732997cd74b8/steps/step_77d279ba820b459f8a70aa97c0ed4ede_c16cb1657a464501a5f36df9bc3ab474_39a0aef9a5904e9a8e85b3335818285d_text_export.jpeg" alt="" width="600" />
    </p>

    ??? warning "RUNNING macOS?"
        The screenshots in this section show Windows. On macOS, double-click the archive in Finder to extract it in place; the remaining steps are the same.

5. In the **Extract Compressed (Zipped) Folders** dialog, the destination path is pre-filled as `C:\Users\...\Downloads\IBM Bob Regulated Industry`.

    - You can leave this as-is or use **Browse...** to choose a different location.
    - Tick **Show extracted files when complete** so the extracted folder opens automatically
    - Finally, click **Extract** to continue

    <p align="left">
    <img src="https://colony-recorder.s3.us-west-1.amazonaws.com/files/org_c5a86d7505634b408ffed7c02e1a91dc/team_1e16acc894ad4e0eba6e176fd42bdcc1/document_5c11ed2e1ddf4b89837d732997cd74b8/steps/step_2229f9f10cfc43679fcdd094444e2ebc_31573f7e125f44b3ab4ae32a261000a8_739658d6663f451885d3285b56ada25a_text_export.jpeg" alt="" width="600" />
    </p>

6. Windows Explorer opens the extracted **IBM Bob Regulated Industry** folder. Confirm that all four folders are present before proceeding:

    !!! success "CHECKLIST"
        - **`.bob`** — Bob's workspace configuration directory. It contains the custom Modes and Skills pre-configured for this lab, along with its rules
        - **`bob-banking-lab`** — the GFM Bank demo application codebase and lab assets
        - **`carbon-offline-reference`** — offline copies of IBM Carbon Design System component definitions (TypeScript `.d.ts` files), which Bob reads to generate accurate Carbon component code without needing API keys
        - **`scripts`** — helper scripts used to set up the lab environment

    <p align="left">
    <img src="https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-09-04/54920ca9-7c58-4f32-a246-7a1bd10b8780/screenshot_cbae3bfd7f0948c1ba04288165800f37_text_export.jpeg" alt="" width="600" />
    </p>

---

## **iii. OPENING THE WORKSPACE IN BOB IDE**

Bob picks up the lab's pre-configured settings from the `.bob` folder the moment the workspace is opened, so it is important to open the extracted folder itself rather than one of its sub-folders.

---

### **Open the folder**

1. Launch IBM Bob. Under the **Start** section on the left, click **Open Folder…** to open a file-picker dialog.

    <p align="left">
    <img src="https://colony-recorder.s3.us-west-1.amazonaws.com/files/org_c5a86d7505634b408ffed7c02e1a91dc/team_1e16acc894ad4e0eba6e176fd42bdcc1/document_5c11ed2e1ddf4b89837d732997cd74b8/steps/step_ebe8125797164d3195d3981ddce3295b_0ea2e758e8f34da2b380bf7b9b93713a_5308b43c650840858243408f07f74f25_text_export.jpeg" alt="" width="600" />
    </p>

2. In the **Open Folder** dialog, navigate to **Downloads** in the left panel — or wherever you chose to extract the `.zip` file.

    <p align="left">
    <img src="https://colony-recorder.s3.us-west-1.amazonaws.com/files/org_c5a86d7505634b408ffed7c02e1a91dc/team_1e16acc894ad4e0eba6e176fd42bdcc1/document_5c11ed2e1ddf4b89837d732997cd74b8/steps/step_9b777058690b4c5a96252af7e83ee867_bc52c74e674f4b9e9eeee10f2bfd9bb4_256f0365c46e4ec8adc2ff5c04986455_text_export.jpeg" alt="" width="600" />
    </p>

3. Click once on the **IBM Bob Regulated Industry** folder to select it (it highlights and its name appears in the **Folder:** field at the bottom of the dialog), then click **Select Folder**. Bob loads this folder as the active workspace, picking up the pre-configured `.bob` settings contained within it.

    <p align="left">
    <img src="https://colony-recorder.s3.us-west-1.amazonaws.com/files/org_c5a86d7505634b408ffed7c02e1a91dc/team_1e16acc894ad4e0eba6e176fd42bdcc1/document_5c11ed2e1ddf4b89837d732997cd74b8/steps/step_0b3f3bf4a039483696573b7e31ed50f9_3d23ddecfefe42c1987c9be81d4a70b1_427973544fd7443ca89c3553cd92924c_text_export.jpeg" alt="" width="600" />
    </p>

4. The workspace is now open. The **Explorer** panel on the left shows **IBM BOB REGULATED INDUSTRY** as the root, with the same four folders you confirmed in section ii inside it.

    <p align="left">
    <img src="https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-09-04/f0682cc6-4166-46a0-9427-386b7acc84ee/user_cropped_screenshot_fa7b1a3d8daf4d04a3e6a863578517ac_text_export.jpeg" alt="" width="600" />
    </p>

---

## **iv. SIGNING IN TO IBM BOB**

With the workspace open, the remaining step is to authenticate the Bob extension so the Agentic Sidebar is ready to accept prompts.

---

### **Start the authentication flow**

1. Click the **Open Bob** button (the Bob robot-head icon in the top-right toolbar of the IDE) to open the Agentic Sidebar — the panel where you will type prompts and interact with Bob throughout this lab.

    <p align="left">
    <img src="https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-09-03/f3d16277-65ed-448e-ba13-6a72ed598318/user_cropped_screenshot_3f6194d6236d4ba188500f6c6af829b4_text_export.jpeg" alt="" width="600" />
    </p>

2. The sidebar opens on the right and shows Bob's welcome screen. Click **Log in to Bob** to begin the authentication flow.

    <p align="left">
    <img src="https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-09-03/6bbf8d54-e115-43c5-88a4-40acb50586d7/user_cropped_screenshot_f622f64dd20942fe94a25db157db39f7_text_export.jpeg" alt="" width="600" />
    </p>

3. A permission dialog appears: *"The extension 'IBM Bob' wants to sign in using Bob."*

    - Click **Allow** to grant the extension permission to open your browser and complete the sign-in.
    - This is a standard security check and is required to proceed.

    <p align="left">
    <img src="https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-09-03/9f91aa97-4ddf-4fa4-a1ed-440d850d1df2/user_cropped_screenshot_b666c7f0b7fe4c46916ea95e63adb94d_text_export.jpeg" alt="" width="600" />
    </p>

4. A second dialog appears: *"Do you want IBM Bob to open the external website?"*, showing the IBM Verify authentication URL.

    - Click **Open** to launch the IBM Verify sign-in page in your default browser.
    - *"Signing in to Bob…"* appears at the bottom of the sidebar, confirming that the authentication handshake has started.

    <p align="left">
    <img src="https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-09-03/732cf37e-7124-4771-a14c-06ada6112bac/user_cropped_screenshot_ffdb8806471d41d2b00bbde8f7a3d938_text_export.jpeg" alt="" width="600" />
    </p>

---

### **Complete the sign-in and return to Bob**

5. Your browser opens the IBM Security Verify **Log in to IBM** page. Enter your IBMid email address in the **IBMid** field (or confirm it is already filled in), click **Continue**, and complete the authentication flow as usual.

    <p align="left">
    <img src="https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-09-03/26386526-9902-45e1-9152-a0ff83542dde/user_cropped_screenshot_5c49e42f65084d0b8e646cefa327c67e_text_export.jpeg" alt="" width="600" />
    </p>

6. After signing in, the browser displays a callback page with the message *"This site is trying to open IBM Bob."*

    - This is the authentication handoff, returning your sign-in token to the Bob IDE running locally.
    - Click **Open** to complete it.

    <p align="left">
    <img src="https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-09-03/60210d06-e85c-49f3-b816-c80ef42aa890/user_cropped_screenshot_9dc65fd97bbb451bb7103b0fa25f6299_text_export.jpeg" alt="" width="600" />
    </p>

7. Return to IBM Bob; you may not be redirected automatically. One final confirmation dialog appears: *"Allow 'IBM Bob' extension to open this URI?"*

    - Click **Open**
    - Notice that the sidebar behind it has already updated: the prompt input now reads *"Build Anything, @ for context, / for commands"*, and the **Agent** mode selector and **Permissions** button are visible at the bottom

    <p align="left">
    <img src="https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-09-03/b219c381-e402-4885-bc3a-4d055b48511d/user_cropped_screenshot_f488f425529b4c74bcddadf25b5a3b2d_text_export.jpeg" alt="" width="600" />
    </p>

8. Bob is now fully authenticated. The Agentic Sidebar displays *"Hi, I'm Bob — Ask me questions or let me code for you."*

    <p align="left">
    <img src="https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-09-03/995d537c-68ad-4dcf-a108-7e3d93699d58/user_cropped_screenshot_6e20849f14ad460ab139925c1a10112f_text_export.jpeg" alt="" width="600" />
    </p>

---

## **v. READY TO PROCEED**

Setup is complete: the lab workspace is open in the Bob IDE and Bob is authenticated. Before proceeding to [Module 1 | Analyze](1-1.md){:target="_blank"}, verify all items below:

!!! success "CHECKLIST"
    - Bob IDE installed and registered
    - **IBM Bob Regulated Industry** archive downloaded and extracted
    - All four workspace folders present:
        - `.bob`
        - `bob-banking-lab`
        - `carbon-offline-reference`
        - `scripts`
    - The extracted folder (rather than a sub-folder) open as the workspace root
    - Bob signed in, with the **Agent** mode selector and **Permissions** button visible in the Agentic Sidebar

Onward now to [Module 1 | Analyze](1-1.md){:target="_blank"}, where you direct Bob through a read-only analysis of the GFM Bank codebase.

---