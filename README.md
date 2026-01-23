# EFI Hackintosh — MACHINIST X99 PR9

Repositório com a EFI que utilizo no meu Hackintosh baseado na placa-mãe **MACHINIST X99 PR9** (X99 mod chinesa), ajustada para funcionar com macOS moderno.

> ⚠️ **Aviso**: Use por sua conta e risco. Cada hardware pode exigir pequenos ajustes. Sempre faça backup da sua EFI atual antes de testar.

---

## 🖥️ Configuração de Hardware

| Componente        | Modelo / Detalhes                   | Status                               |            |
| ----------------- | ----------------------------------- | ------------------------------------ | ---------- |
| Placa-mãe         | MACHINIST X99 PR9 (X99 mod chinesa) | ✅                                    |            |
| CPU               | Xeon E5-2680 v4 (Broadwell-EP)      | ✅ Compatível                         |            |
| GPU               | AMD Radeon RX 5500 XT (Navi)        | ✅ Excelente     |            |
| Memória RAM       | 32 GB                               | ✅                                    |            |
| Armazenamento     | SSD                                 | ✅                                    |            |
| Wi‑Fi / Bluetooth | Intel AX210                         | ⚠️ Wi‑Fi não funciona / Bluetooth OK | ⚠️ Parcial |

---

## 💿 Versão do macOS

* **macOS Tahoe 26.2**

> 🔒 **Compatibilidade travada**: Esta EFI foi **testada e validada** com **macOS Tahoe 26.2 + OpenCore 1.0.7**.
> Atualizações de macOS ou OpenCore podem exigir ajustes na EFI.

---

## ⚙️ O que está funcionando

* Boot estável
* Aceleração gráfica (RX 5500 XT)
* Áudio
* USB
* Ethernet
* Sleep / Wake (básico)

---

## ❌ Não funcionando ainda

* **Wi‑Fi (Intel AX210)**

  * Wi‑Fi: sem suporte nativo no macOS

---

## 📁 Estrutura do Repositório

```
EFI/
├── BOOT/
│   └── BOOTx64.efi
└── OC/
    ├── ACPI/
    ├── Drivers/
    ├── Kexts/
    ├── Tools/
    ├── config.plist
    └── OpenCore.efi
```

---

## 🛠️ Bootloader

* **OpenCore 1.0.7**

---

## 📌 Observações Importantes

* SMBIOS configurado para modelo compatível com Broadwell-EP
* Mapeamento de USB personalizado para a X99 PR9
* SSDT específicos para X99 (CPU, USB, EC, etc.)
* GPU sem necessidade de WhateverGreen (Navi nativo)

---

## 🚀 Como usar

1. Clone este repositório:

   ```bash
   git clone git@github.com:gabrielcayres1/Hackintosh-Machinist-PR9.git
   ```
2. Monte a partição EFI do seu disco.
3. Substitua a pasta `EFI` existente pela deste repositório.
4. Ajuste o `config.plist`:

   * Serial, MLB e ROM
   * SMBIOS, se necessário
5. Reinicie e teste.

---

## 📚 Referências úteis

* BASE EFI Intel HEDT X99 Broadwell-E (Luchina Gabriel):

  * [git@github.com](mailto:git@github.com):luchina-gabriel/BASE-EFI-INTEL-HEDT-5THGEN-X99-BROADWELL-E-PUBLIC.git

* IntelBluetoothFirmware (AX210 / Bluetooth):

  * [https://github.com/lshbluesky/IntelBluetoothFirmware/tree/master/IntelBluetoothFirmware](https://github.com/lshbluesky/IntelBluetoothFirmware/tree/master/IntelBluetoothFirmware)

---

## 🧩 TODO

* [ ] Ativar Wi‑Fi (AX210 ou alternativa)
* [ ] Validar Bluetooth
* [ ] Refinar power management
* [ ] Testar upgrades de macOS

---

## 📝 Licença

Uso livre para fins educacionais. Não há garantia de funcionamento em outros hardwares.

---

**Autor:** Gabriel Cayres

