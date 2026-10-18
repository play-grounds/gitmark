# gitmark console

Marks, as they land. A read-only page that listens on a few Nostr relays for NIP-34 repository
announcements (kind 30617) carrying `chain`, `txo` and `commit` tags, the event `git mark announce`
publishes, checks each event's id and signature in the browser, and shows them newest first:
when, repo, commit, chain, coin, agent.

Live: https://play-grounds.github.io/gitmark/

- Click a row for the agent (did:nostr, npub), its base taproot address, the coin's amount and
  state from the chain's explorer, and the whole trail read from the repo's `blocktrails.json`.
- `?chain=txbt4` and `?q=<repo, pubkey, npub or did>` make any view a link.
- Relays: nostr.oxtr.dev, relay.primal.net, relay.snort.social, relay.damus.io. The strip at the
  bottom shows which answered and how many events each sent.

One file, no build. Nothing is sent from this page. Signatures are verified with
[@noble/curves](https://github.com/paulmillr/noble-curves) loaded from jsDelivr.

Related: [gitmark](https://git-mark.com) (the CLI), [ngit](https://play-grounds.github.io/ngit/)
(all repository announcements), [utxo](https://bitcoin-kernel.com/utxo/) (one coin, shown).
