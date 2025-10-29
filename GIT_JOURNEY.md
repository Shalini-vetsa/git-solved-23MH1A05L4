# My Git Mastery Challenge Journey

## Student Information
- Name: Vetsa Shalini Mani Chandana Kumari
- Student ID: 23MH1A05L4
- Repository: https://github.com/Shalini-vetsa/git-solved-23MH1A05L4.git
- Date Started: 26-10-2025
- Date Completed: 29-10-2025

## Task Summary
Cloned instructor's repository with pre-built conflicts and resolved all 
merge conflicts across multiple branches using proper Git workflows.

## Commands Used

| Command | Times Used | Purpose |
|---------|------------|----------|
| git clone | 1 | Clone instructor's repository |
| git checkout | 20+ | Switch between branches |
| git branch | 10+ | View and manage branches |
| git merge | 2 | Merge dev and conflict-simulator into main |
| git add | 30+ | Stage resolved conflicts |
| git commit | 15+ | Commit resolved changes |
| git push | 10+ | Push to my repository |
| git fetch | 2 | Fetch updates from instructor |
| git pull | 1 | Pull updates |
| git stash | 2 | Save temporary work |
| git cherry-pick | 1 | Copy specific commit |
| git rebase | 1 | Rebase feature branch |
| git reset | 3 | Undo commits (soft/mixed/hard) |
| git revert | 1 | Safe undo |
| git tag | 2 | Create release tags |
| git status | 50+ | Check repository state |
| git log | 30+ | View history |
| git diff | 20+ | Compare changes |

## Conflicts Resolved

### Merge 1: main + dev (6 files)

#### Conflict 1: config/app-config.yaml
- **Issue**: Production used port 8080, development used 3000
- **Resolution**: Created unified config with environment-based settings
- **Strategy**: Keep production as default, add dev as optional
- **Difficulty**: Medium
- **Time**: 15 minutes

#### Conflict 2: config/database-config.json
- **Issue**: Different database hosts and SSL modes
- **Resolution**: Created separate profiles for production and development
- **Strategy**: Restructured JSON to support both environments
- **Difficulty**: Medium
- **Time**: 10 minutes

#### Conflict 3: scripts/deploy.sh
- **Issue**: Different deployment strategies (production vs docker-compose)
- **Resolution**: Added conditional logic based on DEPLOY_ENV variable
- **Strategy**: Made script handle both environments dynamically
- **Difficulty**: Hard
- **Time**: 20 minutes

#### Conflict 4: scripts/monitor.js
- **Issue**: Different monitoring intervals and log formats
- **Resolution**: Environment-based configuration object
- **Strategy**: Used process.env.NODE_ENV to determine behavior
- **Difficulty**: Medium
- **Time**: 15 minutes

#### Conflict 5: docs/architecture.md
- **Issue**: Different architectural descriptions
- **Resolution**: Merged both descriptions into comprehensive document
- **Strategy**: Created sections for each environment
- **Difficulty**: Easy
- **Time**: 10 minutes

#### Conflict 6: README.md
- **Issue**: Different feature lists and version numbers
- **Resolution**: Combined all features with clear environment labels
- **Strategy**: Organized features by category
- **Difficulty**: Easy
- **Time**: 10 minutes

### Merge 2: main + conflict-simulator (6 files)

#### Conflict 1: config/app-config.yaml
- **Issue**: Experimental service configurations (AI optimizer, distributed caching) conflicted with stable production setup.
- **Resolution**: Retained production configuration as default while commenting out experimental settings.
- **Strategy**: Integrated environment-based keys (production, experimental) to toggle safely.
- **Difficulty**: Medium
- **Time**: 15 minutes

#### Conflict 2: config/database-config.json
- **Issue**: Experimental database setup (replication, AI optimization, monitoring) conflicted with development and production configs.
- **Resolution**: Preserved production and development blocks; added experimental block as commented JSON for reference.
- **Strategy**: Used layered JSON approach — stable configurations remain active, experimental logic isolated.
- **Difficulty**: Medium
- **Time**: 20 minutes

#### Conflict 3: scripts/deploy.sh
- **Issue**: Experimental deployment logic (sandbox builds, test pipeline) conflicted with main deployment flow.
- **Resolution**: Added conditional handling using ENABLE_EXPERIMENTAL_DEPLOY flag.
- **Strategy**: Default to production deploy; experimental path executed only if the flag is enabled.
- **Difficulty**: Hard
- **Time**: 25 minutes

#### Conflict 4: scripts/monitor.js
- **Issue**: Different log collection intervals and AI-based anomaly detection logic.
- **Resolution**: Unified monitoring flow; wrapped experimental monitoring inside feature toggle.
- **Strategy**: Use process.env.EXPERIMENTAL_MONITOR to enable/disable new metrics safely.
- **Difficulty**: Medium
- **Time**: 15 minutes

#### Conflict 5: README.md
- **Issue**: Version mismatch and feature discrepancies between production and experimental branches.
- **Resolution**: Updated README to include both stable and experimental features under separate headers.
- **Strategy**: Highlighted that experimental features are optional and not production-ready.
- **Difficulty**: Easy
- **Time**: 10 minutes
### NOTE: Experimental features are for testing purposes only and not recommended for production use.

### Development Mode: These commands are used for local testing and development
export NODE_ENV=development
npm install
npm run dev


## Most Challenging Parts

1. **Understanding Conflict Markers**: Initially confused by `<<<<<<<`, `=======`, `>>>>>>>` symbols. Learned that HEAD is current branch and the other side is incoming changes.

2. **Deciding What to Keep**: Hardest part was choosing between conflicting code. Learned to read both versions completely before deciding.

3. **Complex Logic Conflicts**: deploy.sh had completely different logic. Had to understand both approaches before combining.

4. **Testing After Resolution**: Making sure resolved code actually worked was crucial.

## Key Learnings

### Technical Skills
- Mastered conflict resolution process
- Understood merge conflict markers
- Learned to use git diff effectively
- Practiced all major Git commands

### Best Practices
- Always read both sides of conflict before resolving
- Test resolved code before committing
- Write detailed merge commit messages
- Use git status frequently
- Commit atomically

### Git Workflow Insights
- Conflicts are normal, not errors
- Take time to understand both changes
- When in doubt, ask for clarification
- Document your resolution strategy
- Keep calm and read carefully

## Reflection
This challenge taught me that merge conflicts aren't scary - they're 
just Git asking "which version do you want?". The key is understanding 
what each side is trying to do before combining them. I now feel 
confident handling conflicts in real projects.

The hands-on practice with all Git commands (especially rebase and 
cherry-pick) was invaluable. I understand the difference between merge 
and rebase, and when to use each. Most importantly, I learned that 
git reflog is a lifesaver!
