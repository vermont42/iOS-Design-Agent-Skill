Marketplace Submission Instructions
====================================

This file contains instructions for listing the iOS Design Agent Skill on the Claude Code plugin marketplace and the Cursor marketplace. These steps require interactive access and cannot be automated.

## Claude Code Plugin Marketplace

### Prerequisites
- Claude Code CLI installed and authenticated
- The repository must be public on GitHub

### Steps

1. Open a terminal and run Claude Code.

2. Add your repository as a marketplace source:
   ```
   /plugin marketplace add https://github.com/vermont42/iOS-Design-Agent-Skill
   ```

3. Verify the plugin is recognized:
   ```
   /plugin marketplace list
   ```
   You should see `ios-design-agent-skill` in the output.

4. Test installing your own plugin to confirm it works:
   ```
   /plugin install ios-design-agent-skill
   ```

5. Verify the skill loads correctly:
   ```
   /plugin list
   ```

Once registered, other users can install the skill by adding your marketplace source and running `/plugin install ios-design-agent-skill`.

### Troubleshooting
- If the marketplace command is not recognized, ensure you are running a recent version of Claude Code that supports plugins.
- The `.claude-plugin/marketplace.json` in this repo defines the plugin metadata. If you change the skill name or description, update that file as well.

## Cursor Marketplace

### Prerequisites
- A Cursor account
- The repository must be public on GitHub

### Steps

1. Go to the [Cursor plugin submission page](https://cursor.com/plugins) (or check Cursor's latest documentation for the current submission URL).

2. Submit your repository URL:
   ```
   https://github.com/vermont42/iOS-Design-Agent-Skill
   ```

3. Fill in the required metadata:
   - **Name:** iOS Design Agent Skill
   - **Description:** Audit and improve iOS/SwiftUI app aesthetics — typography, color, spatial composition, motion, and atmospheric depth.
   - **Category:** Development / Design
   - **Keywords:** ios, swiftui, design, ui, audit

4. Cursor reviews submissions before listing them. Antoine's SwiftUI Expert Skill notes that Cursor approval is "pending" — expect a review period.

5. To prepare for Cursor, you may optionally create a `.cursor-plugin/` directory in this repo. Antoine's repo uses this structure, though the exact format may evolve. A minimal setup:

   ```
   .cursor-plugin/
   └── plugin.json
   ```

   With contents mirroring the Claude plugin manifest:
   ```json
   {
     "name": "ios-design-agent-skill",
     "version": "1.0.0",
     "description": "Audit and improve iOS/SwiftUI app aesthetics — typography, color, spatial composition, motion, and depth.",
     "author": {
       "name": "Josh Adams"
     },
     "repository": "https://github.com/vermont42/iOS-Design-Agent-Skill",
     "license": "MIT",
     "skills": [
       "./ios-design-agent-skill"
     ]
   }
   ```

### Notes
- The Cursor marketplace submission process is newer and may change. Check Cursor's official documentation for the latest instructions.
- Both marketplaces ultimately point back to this GitHub repository. Keeping the repo public and the `SKILL.md` / `marketplace.json` files up to date is what matters most.
