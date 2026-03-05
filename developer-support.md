---
layout: page
title: Vasati App - Developer Support & Privacy Policy
permalink: /vasati/
---

<h2>Developer Support</h2>

<p>This page provides support information and the privacy policy for <strong>Vasati</strong>, a mobile application available for Android and iOS devices.</p>

<p><strong>Support:</strong> For questions, feedback, or assistance, contact us at <a href="mailto:sukashi.labs+support@gmail.com">sukashi.labs+support@gmail.com</a>.</p>

<hr />

<h2>Privacy Policy</h2>

<p><em>Last updated: March 2025</em></p>

<h3>1. Application Overview</h3>

<p><strong>Vasati</strong> is an offline-first React Native mobile application (iOS and Android) designed for maintenance staff to manage apartment buildings. It enables:</p>

<ul>
  <li>Building structure setup (floors, units)</li>
  <li>Resident and owner management</li>
  <li>Maintenance fee and payment tracking</li>
  <li>Expenditure logging and categorization</li>
  <li>Notes and todo management</li>
  <li>Utilities consumption tracking</li>
  <li>Photo attachments for notes, todos, expenditures, and payments</li>
</ul>

<p><strong>Target users:</strong> Maintenance personnel working in apartment buildings, often in areas with poor connectivity (basements, parking garages).</p>

<h3>2. Data Storage and Transmission</h3>

<h4>2.1 Offline-First, No Backend</h4>

<ul>
  <li><strong>No server infrastructure:</strong> The app has no backend, APIs, or cloud services.</li>
  <li><strong>No data transmission:</strong> User data is never sent over the internet.</li>
  <li><strong>Full offline operation:</strong> All features work without network connectivity.</li>
  <li><strong>Local-only storage:</strong> All data resides on the user's device.</li>
</ul>

<h4>2.2 Storage Technologies</h4>

<table>
  <thead>
    <tr>
      <th>Storage Type</th>
      <th>Technology</th>
      <th>Purpose</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Secure storage</strong></td>
      <td>Expo SecureStore (encrypted)</td>
      <td>Credentials, session, biometric preference, onboarding state, language preference</td>
    </tr>
    <tr>
      <td><strong>Structured data</strong></td>
      <td>SQLite (expo-sqlite)</td>
      <td>Apartments, residents, owners, payments, expenditures, notes, todos, utilities, photos metadata</td>
    </tr>
    <tr>
      <td><strong>Files</strong></td>
      <td>Device document directory</td>
      <td>Photo attachments (JPEG/PNG)</td>
    </tr>
  </tbody>
</table>

<h3>3. Data Collected and Stored</h3>

<h4>3.1 Account and Authentication Data (SecureStore)</h4>

<table>
  <thead>
    <tr>
      <th>Data</th>
      <th>Purpose</th>
      <th>Retention</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Username</td>
      <td>Account identification</td>
      <td>Until user deletes account</td>
    </tr>
    <tr>
      <td>Hashed password (SHA-256)</td>
      <td>Authentication</td>
      <td>Until user deletes account</td>
    </tr>
    <tr>
      <td>Session (username, timestamp)</td>
      <td>Maintain sign-in state</td>
      <td>Until sign-out</td>
    </tr>
    <tr>
      <td>Biometric enabled flag</td>
      <td>Optional Face ID / fingerprint sign-in</td>
      <td>Until user disables</td>
    </tr>
    <tr>
      <td>Last signed-in username</td>
      <td>Biometric sign-in when no session</td>
      <td>Until sign-out</td>
    </tr>
    <tr>
      <td>Onboarding completed flag</td>
      <td>First-time setup flow</td>
      <td>Persistent</td>
    </tr>
    <tr>
      <td>Language preference</td>
      <td>App UI language (en, hi, ta, te, kn)</td>
      <td>Until user changes</td>
    </tr>
  </tbody>
</table>

<h4>3.2 Building and Management Data (SQLite)</h4>

<table>
  <thead>
    <tr>
      <th>Data Category</th>
      <th>Examples</th>
      <th>Purpose</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Apartments</td>
      <td>Floor, unit number, payment status</td>
      <td>Building structure</td>
    </tr>
    <tr>
      <td>Residents</td>
      <td>Name, phone, email, SPOC flag</td>
      <td>Contact and occupancy</td>
    </tr>
    <tr>
      <td>Owners</td>
      <td>Name, phone, email, occupancy type</td>
      <td>Contact and ownership</td>
    </tr>
    <tr>
      <td>Payments</td>
      <td>Amount, date, status, period</td>
      <td>Fee collection tracking</td>
    </tr>
    <tr>
      <td>Expenditures</td>
      <td>Amount, date, description, category</td>
      <td>Expense logging</td>
    </tr>
    <tr>
      <td>Notes</td>
      <td>Title, content, apartment link</td>
      <td>Issue tracking</td>
    </tr>
    <tr>
      <td>Todos</td>
      <td>Title, description, due date, priority</td>
      <td>Task management</td>
    </tr>
    <tr>
      <td>Utilities</td>
      <td>Consumption values, period, type</td>
      <td>Billing and calculations</td>
    </tr>
    <tr>
      <td>Photos metadata</td>
      <td>File path, entity link</td>
      <td>Attachments reference</td>
    </tr>
  </tbody>
</table>

<h4>3.3 Photo Attachments</h4>

<ul>
  <li><strong>Storage:</strong> App document directory (<code>photos/{entityType}/</code>)</li>
  <li><strong>Format:</strong> JPEG/PNG, compressed before storage</li>
  <li><strong>Scope:</strong> Attached to notes, todos, expenditures, payments</li>
  <li><strong>Lifecycle:</strong> Deleted when parent entity is deleted</li>
</ul>

<h3>4. Device Permissions and Their Use</h3>

<table>
  <thead>
    <tr>
      <th>Permission</th>
      <th>Platform</th>
      <th>Purpose</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Contacts</strong></td>
      <td>iOS, Android</td>
      <td>Populate resident/owner name, phone, email from device contacts (optional, user-initiated)</td>
    </tr>
    <tr>
      <td><strong>Camera</strong></td>
      <td>iOS, Android</td>
      <td>Capture photos for notes, todos, expenditures, payments</td>
    </tr>
    <tr>
      <td><strong>Photo Library</strong></td>
      <td>iOS</td>
      <td>Attach photos from gallery to notes, todos, expenditures, payments</td>
    </tr>
    <tr>
      <td><strong>External Storage</strong></td>
      <td>Android</td>
      <td>Read/write photos for attachments</td>
    </tr>
    <tr>
      <td><strong>Biometrics</strong> (Face ID / Fingerprint)</td>
      <td>iOS, Android</td>
      <td>Optional secure sign-in</td>
    </tr>
  </tbody>
</table>

<h3>5. Privacy Characteristics</h3>

<h4>5.1 Data Location and Control</h4>

<ul>
  <li><strong>All data stays on device:</strong> No cloud sync, no remote servers.</li>
  <li><strong>User controls data:</strong> Data is only accessible to the user on their device.</li>
  <li><strong>No third-party data sharing:</strong> No analytics, advertising, or data brokers.</li>
</ul>

<h4>5.2 Security Measures</h4>

<ul>
  <li><strong>Credential encryption:</strong> Passwords hashed with SHA-256; credentials stored in SecureStore (OS-level encryption).</li>
  <li><strong>Session security:</strong> Session data in SecureStore.</li>
  <li><strong>Biometric option:</strong> Optional Face ID / fingerprint for sign-in.</li>
  <li><strong>No plaintext passwords:</strong> Passwords never stored in readable form.</li>
</ul>

<h4>5.3 Third-Party Services</h4>

<ul>
  <li><strong>No analytics:</strong> No Firebase, Amplitude, Mixpanel, Sentry, or similar.</li>
  <li><strong>No crash reporting:</strong> No automatic crash or error reporting to external services.</li>
  <li><strong>Expo/EAS:</strong> Used for build and OTA updates; no user data sent for app functionality.</li>
</ul>

<h4>5.4 Sensitive Data Categories</h4>

<p>The following data categories are stored locally only and are not transmitted:</p>

<ul>
  <li><strong>Personal data:</strong> Names, phone numbers, email addresses (residents, owners)</li>
  <li><strong>Financial data:</strong> Payment amounts, expenditure amounts</li>
  <li><strong>Photos:</strong> User-captured or selected images</li>
  <li><strong>Credentials:</strong> Username, hashed password</li>
</ul>

<h3>6. Data Lifecycle</h3>

<ul>
  <li><strong>Creation:</strong> User enters data or selects from contacts/photos.</li>
  <li><strong>Storage:</strong> Local SQLite or SecureStore.</li>
  <li><strong>Deletion:</strong> User can delete entities; cascade deletes remove related data (e.g., photos).</li>
  <li><strong>App uninstall:</strong> All local data is removed with the app.</li>
</ul>

<h3>7. Internationalization</h3>

<p><strong>Supported languages:</strong> English (en), Hindi (hi), Tamil (ta), Telugu (te), Kannada (kn).</p>

<p>Language preference is stored in SecureStore; device language is used as default. Translations are bundled in the app; no server calls for language content.</p>

<h3>8. Summary</h3>

<ul>
  <li><strong>Local-only data:</strong> All data is stored on the user's device; nothing is sent to external servers.</li>
  <li><strong>No tracking:</strong> No analytics, advertising, or usage tracking.</li>
  <li><strong>Permissions:</strong> Contacts, Camera, Photo Library, and Biometrics are requested only for the purposes described above.</li>
  <li><strong>Security:</strong> Credential hashing and SecureStore protect sensitive data.</li>
  <li><strong>Data retention:</strong> Data remains until the user deletes it or uninstalls the app.</li>
  <li><strong>No sale of data:</strong> No user data is sold or shared with third parties.</li>
  <li><strong>Offline operation:</strong> The app works fully offline; no network transmission of user data.</li>
</ul>

<hr />

<p><em>For support inquiries, contact us at <a href="mailto:sukashi.labs+support@gmail.com">sukashi.labs+support@gmail.com</a>.</em></p>
