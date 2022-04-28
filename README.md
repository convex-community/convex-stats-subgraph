# Convex-subgraph

Subgraph Endpoint: https://api.thegraph.com/subgraphs/id/QmWsJjUFSby26BkR27bTgjYMEvg7C8dvuAXQnmWSMbaxaV

Listen to all `RewardPaid` events to collect and accumulate account rewards information.

Query user stats:

```graphql
query getRewards($user_id: ID!) {
  user(id: $user_id) {
    rewards {
      pool
      stakingToken
      rewardToken
      paidAmountCumulative
    }
  }
}
```

Query platform stats:

```graphql
query getRewards($platform_id: ID!) {
  platform(id: $platform_id) {
    rewards {
      pool
      stakingToken
      rewardToken
      paidAmountCumulative
      addedAmountCumulative
    }
  }
}
```
