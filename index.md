---
layout: default
title: The Button Heist
description: Make the iOS accessibility contract programmable.
---

# The Button Heist

Make the iOS accessibility contract programmable.

The accessibility interface is the closest thing an iOS app has to a CLI. The Button Heist runs inside your app, exposes the live accessibility hierarchy and interaction surface, and lets agents, tests, and scripts drive it with a durable DSL.

Every heist waits for the interface to settle, snapshots the accessibility contract, performs a declared action, waits for the next settled state, and returns the semantic diff as evidence.

Every heist is also an accessibility audit: it verifies that real product workflows remain reachable and operable through the live iOS accessibility tree.
