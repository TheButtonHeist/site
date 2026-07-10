---
layout: default
title: The Button Heist
description: Make the iOS accessibility contract programmable.
---

<header class="site-header">
  <a class="brand" href="/" aria-label="The Button Heist home">
    <span class="brand-mark" aria-hidden="true"></span>
    <span>The Button Heist</span>
  </a>
  <nav aria-label="Primary navigation">
    <a href="https://github.com/RoyalPineapple/TheButtonHeist/tree/main/docs">Docs</a>
    <a href="https://github.com/TheButtonHeist">GitHub</a>
  </nav>
</header>

<main>
  <section class="hero" aria-labelledby="hero-title">
    <div class="hero-copy">
      <h1 id="hero-title">Your iOS app already has a CLI.</h1>
      <p class="hero-subhead">It's called accessibility.</p>
      <p class="hero-text">The Button Heist runs inside your app and makes the live accessibility contract programmable: state, actions, waits, diffs, receipts.</p>
    </div>
    <div class="hero-atmosphere" aria-hidden="true"></div>
  </section>

  <section class="contract-flow" aria-label="The Button Heist execution model">
    <article class="panel screen-panel">
      <h2>Settled screen</h2>
      <div class="screen-state" aria-label="Accessible elements and actions">
        <div class="screen-row">
          <span class="element-kind">button</span>
          <strong>Pay</strong>
          <span class="action-chip">activate</span>
        </div>
        <div class="screen-row">
          <span class="element-kind">static text</span>
          <strong>Total</strong>
          <span class="value-chip">$49.00</span>
        </div>
        <div class="screen-row">
          <span class="element-kind">text field</span>
          <strong>Email</strong>
          <span class="action-chip">type text</span>
        </div>
        <div class="screen-row">
          <span class="element-kind">adjustable</span>
          <strong>Quantity</strong>
          <span class="action-chip">increment</span>
        </div>
      </div>
    </article>

    <div class="action-step" aria-label="Action against a specific accessibility element">
      <span>action on element</span>
      <code>Activate(.label("Pay"))</code>
    </div>

    <article class="panel diff-panel">
      <h2>Semantic diff</h2>
      <dl class="diff-list">
        <div>
          <dt>appeared</dt>
          <dd>Payment Complete</dd>
        </div>
        <div>
          <dt>updated</dt>
          <dd>Total</dd>
        </div>
      </dl>
    </article>

    <article class="panel expectation-panel">
      <h2>Expectation</h2>
      <dl class="expectation-list">
        <div>
          <dt>expect</dt>
          <dd>appeared</dd>
        </div>
        <div>
          <dt>target</dt>
          <dd>label("Payment Complete")</dd>
        </div>
        <div>
          <dt>evidence</dt>
          <dd>matched diff</dd>
        </div>
        <div>
          <dt>result</dt>
          <dd>expectation held</dd>
        </div>
      </dl>
    </article>
  </section>

  <section class="code-proof" aria-label="Button Heist DSL example">
    <pre><code>Activate(.label("Pay"))
    .expect(.appeared(.label("Payment Complete")))</code></pre>
  </section>

  <section class="outcomes" aria-label="What The Button Heist is for">
    <article>
      <span class="outcome-icon agent-icon" aria-hidden="true"></span>
      <h2>Agents steer from evidence.</h2>
      <p>Each action returns what changed, so the next step comes from the current contract.</p>
    </article>
    <article>
      <span class="outcome-icon test-icon" aria-hidden="true"></span>
      <h2>Tests assert the contract.</h2>
      <p>Durable black-box tests over product semantics, not view internals.</p>
    </article>
    <article>
      <span class="outcome-icon audit-icon" aria-hidden="true"></span>
      <h2>Every heist audits accessibility.</h2>
      <p>If a workflow cannot be reached or operated through the live tree, that failure matters.</p>
    </article>
  </section>

  <section class="process-note">
    <div class="target-mark" aria-hidden="true"></div>
    <div>
      <h2>In-process because that is where the real interface lives.</h2>
      <p>Outside the app you get proxies, snapshots, and tap coordinates. Inside the app you get the live accessibility hierarchy and interaction surface.</p>
    </div>
  </section>
</main>
