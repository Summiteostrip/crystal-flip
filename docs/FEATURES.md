# Features and Filters

This document summarizes the product capabilities presented in the official Crystal Flip channel. Exact availability may depend on the current release, network, venue, and subscription.

## 1. Developer Intelligence

Crystal Flip scans new launches and builds a historical view of their developers.

### Available context

- Previous tokens and their peak market capitalizations.
- Average and median historical performance.
- Dev-buy amount at launch.
- Time until the first developer sale.
- Typical percentage of supply sold.
- Whether the developer held until the historical high.
- Global Fees Paid on previous launches.
- Repeated behavioral and launch patterns.
- ROI information for previous launches where available.

### Detection controls

- Minimum developer migration percentage.
- Maximum permitted dev-buy.
- Blacklisted developer wallets.
- Tracked developer wallets with automatic opening.
- Optional parallel opening of a previous developer token for comparison.

Historical depth can vary by venue. In particular, older materials note that complete previous-token data may be limited outside Pump.fun.

## 2. Migration Detection

The migration module detects tokens as they migrate and can display or automatically open them according to the selected configuration.

A related module detects a developer's next token after a previous migration and supplies historical launch context.

## 3. Twitter Checker

The Twitter checker inspects supported launches for attached tweets and applies social and content filters.

### Displayed information

- Tweet author and profile link.
- Follower count.
- Tweet text where enabled.
- Tweet type: original post, reply, or quote.
- Highlighting when the token name or ticker appears in the tweet.

### Controls

- Minimum author followers.
- Tweet publication-time constraints.
- Account and keyword blacklist.
- Trusted account and keyword whitelist.
- Automatic opening for matching whitelist entries.
- **POST ONLY** to exclude replies and other non-original posts.
- **ONLY CONTAINS** to require the token name or ticker in the tweet.
- Duplicate-post suppression.

## 4. Twitter Contract Monitoring

The contract monitor watches for contract addresses posted with configured terms such as `CA:`, `pump`, `bonk`, or `boop`.

It supports trusted-source whitelists, account blacklists, duplicate suppression, and automatic opening of matching contracts.

## 5. Twitter Historian Intelligence

The platform continuously associates attached tweets with their authors and tracks the market performance of related tokens.

For each author, it can maintain:

- number of associated tokens;
- average historical market cap;
- recent token results;
- engagement-oriented trust indicators;
- custom whitelist highlighting.

The Crystal Extension exposes this context directly in supported interfaces and can highlight tokens by user-defined market-cap ranges.

## 6. Community Intelligence

Crystal Flip checks supported launches for an attached Twitter Community.

### Community and admin context

- Community admin identity.
- Follower count.
- Previous projects associated with the admin.
- Average and median historical market cap.
- Recent token results.
- Successful-launch ratio where available.
- Repeated-launch and holding-pattern analytics.

Users can set a minimum follower threshold and automatically open launches associated with specified Community admins. Communities are deduplicated so that repeated detections do not create unnecessary noise.

## 7. LaunchCoin Alerts

The LaunchCoin module identifies newly detected launches and displays developer Twitter context, including follower count and profile information. Automatic opening can be enabled above a chosen follower threshold.

## 8. Crystal AI Score

The AI Score combines supported historical, behavioral, social, liquidity, and growth signals into a dynamic 0–100 rating.

Users can:

- require a minimum score for display or automatic opening;
- filter by individual score factors;
- inspect the score breakdown;
- combine the score with other Smart Auto-Mode rules.

The score is a heuristic research aid, not proof of future performance.

## 9. Behavioral and Risk Analytics

Depending on the available data, Crystal Flip can surface:

- Dev Pattern ID for recurring developer behavior.
- Serial farm developer warnings.
- Suspiciously low fees relative to previous market cap.
- Artificial market-cap or volume indicators.
- Rapid historical liquidity removal.
- Developer wallet clustering signals.
- Rug probability warnings.
- Historian Trust Index and fake-follower indicators.

These signals should be treated as prompts for further investigation rather than definitive classifications.

## 10. Liquidity Intelligence

The liquidity module considers available launch and historical signals such as:

- speed of liquidity-pool addition;
- liquidity relative to market capitalization;
- whether the developer supplied initial liquidity;
- rapid liquidity removals in earlier projects.

## 11. Smart Auto-Mode

Smart Auto-Mode applies user-defined thresholds before displaying or automatically opening a candidate. Rules can combine:

- minimum AI Score;
- maximum dev-buy;
- minimum liquidity ratio;
- minimum Historian Trust Index;
- other supported platform and history filters.

## 12. Research and Review Tools

- Detection history for recently surfaced candidates.
- Notes on Community, tweet, and wallet detections.
- Configurable console clearing.
- Color-coded market-cap and whitelist highlighting.
- Importable settings.
- Opened-coin logging and hypothetical ROI review.
- Filter-performance analysis for strategy refinement.

## 13. Narrative Intelligence

Narrative Heatmap is intended to show keywords and narratives associated with current market activity, helping users identify themes driving launches and momentum.
