# RSpec action

This action configures [actions/stale](https://github.com/actions/stale)

## Inputs

  - issue-staled-period:
  description: 'Days before issue is marked as stale'
  required: false
  default: '45'
- issue-closed-period:
  description: 'Days before staled issue is closed'
  required: false
  default: '10'
  - pr-staled-period:
  description: 'Days before PR is marked as stale'
  required: false
  default: '30'
  - pr-closed-period:
  description: 'Days before staled PR is closed'
  required: false
  default: '7'
  - stale-pr-label:
  description: 'Staled PR label'
  required: false
  default: 'staled'
  - stale-issue-label:
  description: 'Staled Issue label'
  required: false
  default: 'staled'

## Example usage

```yaml
- name: Stale bot Action
  uses: OpenSourcePolitics/staled-bot@master
```

To configure stale bot, you can use the following inputs:

```yaml
- name: Run RSpec
  uses: OpenSourcePolitics/rspec-action@master
  with:
    issue-staled-period: 45
    issue-closed-period: 10
    pr-staled-period: 30
    pr-closed-period: 7
    stale-pr-label: staled
    stale-issue-label: staled
```
