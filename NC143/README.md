# Nine Crowns 1.4.3 — Minecraft Java 26.1 / Fabric

Questa versione integra i visual corretti forniti nel pack `NineCrowns_VISUALS_FIXED_MC26.1` e rende obbligatorie le proprietà degli oggetti speciali.

## Oggetti

- **Spada OP**: Sharpness V, veramente indistruttibile (`minecraft:unbreakable`), 20% Veleno I e 10% Slowness I per 3 secondi sui colpi validi.
- **Lancia OP di Netherite**: Lunge V + Sharpness V, veramente indistruttibile, Jab configurato a 5 cuori base e abilità fulmine con cooldown 60 s.
- **Corona dell'Imperatore**: Protection X, veramente indistruttibile; Speed II, Strength II e Fire Resistance I solo mentre è indossata.
- **Corona Vuota**: veramente indistruttibile, senza enchant obbligatori.

Gli enchant sopra i limiti survival normali (Protection X e Lunge V) vengono scritti direttamente nei componenti dell'ItemStack. Sharpness V viene forzato anche sulla Lancia OP. Le proprietà vengono riapplicate anche agli oggetti ottenuti con Creative o `/give`, quindi non dipendono soltanto dalla ricetta.

## Visual

I quattro oggetti usano gli ID reali della mod:

- `ninecrowns:op_sword`
- `ninecrowns:op_spear`
- `ninecrowns:empty_crown`
- `ninecrowns:emperor_crown`

Il pack visual originale usava i nomi `spada_op` e `lancia_op`: in questa versione sono stati rinominati e collegati agli ID veri della mod.

La Lancia OP ha due modelli distinti:

- GUI/hotbar/ground: `op_spear`
- prima/terza persona: `op_spear_in_hand`, con parent vanilla `minecraft:item/spear_in_hand`

Le corone includono i file equipment per humanoid e humanoid_baby, quindi la Corona dell'Imperatore resta indossabile nello slot testa.

## Build GitHub

Il workflow è già incluso in `.github/workflows/main.yml`.

1. Carica nella **root del repository**: `.github`, `src`, `build.gradle`, `settings.gradle`, `gradle.properties`, ecc.
2. Vai su **Actions → Build NineCrowns → Run workflow**.
3. Un tick verde significa che il workflow ha compilato e controllato il JAR.
4. Scarica l'artifact `NineCrowns-26.1-v1.4.3-VERIFIED`.
5. Dentro trovi `ninecrowns-26.1-1.4.3.jar`.

Il workflow controlla anche che nel JAR esistano classi, texture principali, modello spear in-hand e i file Fabric.
