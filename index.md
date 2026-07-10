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
    <article class="panel hierarchy-panel">
      <h2>Settled contract</h2>
      <ol class="tree">
        <li>
          <span class="node-icon app-icon" aria-hidden="true"></span>
          <span>App</span>
          <ol>
            <li>
              <span class="node-icon window-icon" aria-hidden="true"></span>
              <span>Window</span>
              <ol>
                <li>
                  <span class="node-icon button-icon" aria-hidden="true"></span>
                  <span>Pay</span>
                </li>
                <li>
                  <span class="node-icon value-icon" aria-hidden="true"></span>
                  <span>Total</span>
                </li>
                <li>
                  <span class="node-icon receipt-icon" aria-hidden="true"></span>
                  <span>Receipt</span>
                </li>
              </ol>
            </li>
          </ol>
        </li>
      </ol>
    </article>

    <div class="action-step" aria-label="Declared accessibility action">
      <span>declared action</span>
      <code>accessibilityActivate()</code>
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

    <article class="panel receipt-panel">
      <h2>Receipt</h2>
      <dl class="receipt-list">
        <div>
          <dt>before</dt>
          <dd>settled contract</dd>
        </div>
        <div>
          <dt>action</dt>
          <dd>declared activation</dd>
        </div>
        <div>
          <dt>after</dt>
          <dd>settled contract</dd>
        </div>
        <div>
          <dt>result</dt>
          <dd>contract held</dd>
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
