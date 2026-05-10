---
layout: page
title: Sanchalan — Samay Sarathi
permalink: /sanchalan/
---

<h2 style="display: flex; gap: 16px; align-items: center; margin-bottom: 1em;">
  <img src="{{ site.baseurl }}/assets/apps/sanchalan/splash-icon.png" alt="Samay Sarathi logo" width="60" height="60" style="vertical-align: middle;" />
Sanchalan — Samay Sarathi</h2>

<p>This page describes <strong>Samay Sarathi</strong> (published under the <strong>Sanchalan</strong> product page), a mobile app for structured, timed session plans on iPhone and Android — offline, on-device, and without an account.</p>

<p><strong>Support:</strong> For questions, feedback, or assistance, contact us at <a href="mailto:sukashi.labs+support@gmail.com">sukashi.labs+support@gmail.com</a>.</p>

<hr />

<h2>What the app does</h2>

<p>Samay Sarathi runs session plans end-to-end on your phone: <strong>plan → run → log → share</strong>. One workflow supports personal routines and facilitated group programs.</p>

<table>
  <thead>
    <tr>
      <th>Pillar</th>
      <th>In practice</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Offline-first</strong></td>
      <td>Primary actions work without a network. No cloud sync, no accounts.</td>
    </tr>
    <tr>
      <td><strong>Privacy-first</strong></td>
      <td>No analytics, telemetry, or crash reporting in the MVP. Participant names never leave the device or appear on shared cards.</td>
    </tr>
    <tr>
      <td><strong>Phone-only</strong></td>
      <td>iOS and Android, portrait orientation — no tablet or web build.</td>
    </tr>
    <tr>
      <td><strong>Background-safe</strong></td>
      <td>Session timing and audio cues continue when the phone is locked or the app is in the background.</td>
    </tr>
  </tbody>
</table>

<h3>Activities</h3>

<ul>
  <li>Create activities with a name and default duration; edit or delete your activities.</li>
  <li>Three seed activities ship on first install (Warm-up, Main activity, Break) so you can run a session immediately.</li>
  <li>Activities are snapshotted into plan steps when you create a plan — editing an activity later does not change plans that already used it.</li>
</ul>

<h3>Plans</h3>

<ul>
  <li>Build a plan by ordering activities or ad-hoc steps; each step has a name and duration; total time is the sum of steps.</li>
  <li>Saved plans are <strong>immutable</strong> — to change a plan, duplicate it and save the duplicate.</li>
  <li>Archive plans to hide them without deleting; plans referenced by session logs cannot be hard-deleted.</li>
</ul>

<h3>Sessions (runner)</h3>

<ul>
  <li>Start any plan to run a full-screen session with a live countdown and next-step preview.</li>
  <li>A short audio cue plays at every step transition, including the end; cues use local notifications with bundled audio so they work when the device is locked.</li>
  <li>Timing is drift-resistant (derived from elapsed wall-clock time). There is no Pause/Resume — use Break steps in the plan instead.</li>
  <li><strong>Skip</strong> advances the current step; <strong>End</strong> stops early. Every completed session creates a log automatically.</li>
</ul>

<h3>Logs &amp; participants</h3>

<ul>
  <li>Each finished session produces a log with an immutable link to the plan and start/end times.</li>
  <li>You can later edit enrichment fields (participant counts or names, minutes-of-meeting notes, custom metadata). Plan reference and timestamps stay fixed.</li>
  <li><strong>Participants:</strong> optional count mode (by category) or name mode (names stay on-device and are never exported).</li>
</ul>

<h3>Share as image</h3>

<ul>
  <li>Generate a minimalist share card from any log via the system share sheet.</li>
  <li>Count-mode logs show category breakdowns; name-mode logs show only <strong>total count</strong> — names never appear on the card.</li>
  <li>Rendering is on-device; nothing is uploaded for sharing.</li>
</ul>

<h3>Security (optional)</h3>

<ul>
  <li>Optional app lock: Face ID, fingerprint, custom PIN, or skip — configurable under Settings.</li>
  <li>Authentication gates app entry only; it does not replace OS protections for stored data.</li>
</ul>

<h3>Platforms</h3>

<ul>
  <li><strong>iOS</strong> (recent major versions) and <strong>Android</strong> (API 30+).</li>
  <li>JavaScript-only fixes may ship via EAS Update; native changes require a new store build.</li>
</ul>

<hr />

<h2>Privacy Policy</h2>

<p><em>Last updated: May 2026</em></p>

<h3>1. Application overview</h3>

<p><strong>Samay Sarathi</strong> is an offline-first mobile app. There is <strong>no user account, no sign-up, and no cloud sync</strong>. Your session data is meant to stay on your phone.</p>

<h3>2. Why there is no “server-side” security risk for your session data</h3>

<p><strong>We do not operate a backend that stores your plans, logs, participant names, or notes.</strong> Because user-generated content is <strong>local only</strong>, there is <strong>no exposure of that data through our servers</strong> — there are no application servers receiving your session or participant information. Security questions common to cloud apps (breaches of a central database holding your data, account takeover against our API) <strong>do not apply</strong> to your app-managed session data in the way they would for a synced service.</p>

<p>Typical risks that remain are those inherent to any app that stores data on a physical device (e.g., device loss, someone unlocking the phone, OS-level issues). Optional app lock and device passcodes help reduce access by others.</p>

<h3>3. Data storage and transmission</h3>

<h4>3.1 Local-first, no sync</h4>

<ul>
  <li><strong>No cloud sync and no shared accounts</strong> — by design.</li>
  <li><strong>No transmission of your plans, logs, participant names, or MoM text</strong> to us for app functionality.</li>
  <li><strong>Primary data</strong> lives in on-device SQLite.</li>
</ul>

<h4>3.2 Network use</h4>

<ul>
  <li>The main outbound network activity described for normal operation is <strong>EAS Update</strong> polling for over-the-air JavaScript updates. That does not send your session content to us.</li>
  <li>When you use the system share sheet, sharing is between your device and the app you choose (Messages, Mail, etc.) — not a dedicated Sarathi upload server for your logs.</li>
</ul>

<h3>4. Data collected and stored (on device)</h3>

<table>
  <thead>
    <tr>
      <th>Category</th>
      <th>Examples</th>
      <th>Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Plans &amp; activities</td>
      <td>Step names, durations, ordering</td>
      <td>Immutable plans once saved</td>
    </tr>
    <tr>
      <td>Session logs</td>
      <td>Plan reference, start/end times</td>
      <td>Core fields immutable after creation</td>
    </tr>
    <tr>
      <td>Participants</td>
      <td>Counts by category; optional names in name mode</td>
      <td>Names are not placed on share cards</td>
    </tr>
    <tr>
      <td>Notes &amp; metadata</td>
      <td>MoM text, custom fields</td>
      <td>Editable enrichments on logs</td>
    </tr>
    <tr>
      <td>Settings</td>
      <td>Security choice, participant categories</td>
      <td>Stored locally</td>
    </tr>
  </tbody>
</table>

<h3>5. Privacy characteristics</h3>

<ul>
  <li><strong>No analytics, no telemetry, no crash reporting</strong> in the MVP (as stated in product documentation).</li>
  <li><strong>Share cards never show participant names</strong> when names were captured — only totals appear for name-mode logs.</li>
  <li><strong>No sale of personal data</strong> — we do not operate an ad or data-broker pipeline for app content.</li>
</ul>

<h3>6. Data lifecycle</h3>

<ul>
  <li>Data remains on the device until you delete it in the app or remove the app.</li>
  <li>Uninstalling the app removes local app data unless the OS provides separate backup behavior outside our control.</li>
</ul>

<h3>7. Summary</h3>

<ul>
  <li><strong>Local session data:</strong> Plans, logs, and optional participant details are stored on your device; we do not sync them to our infrastructure.</li>
  <li><strong>No server-side repository of your session content</strong> — so no breach of “our cloud database” of your sessions.</li>
  <li><strong>Minimal tracking:</strong> No analytics/telemetry/crash reporting as described for the MVP.</li>
  <li><strong>Sharing:</strong> Share cards omit names in name mode; export is rendered on-device.</li>
  <li><strong>Updates:</strong> OTA updates may fetch JS bundles; they are not a channel for uploading your private log content.</li>
</ul>

<hr />

<p><em>For support inquiries, contact us at <a href="mailto:sukashi.labs+support@gmail.com">sukashi.labs+support@gmail.com</a>.</em></p>
