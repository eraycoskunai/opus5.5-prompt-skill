# Opus 5.5 Prompt Skill

Claude Opus 5.5 için prompt yazan, mevcut promptları denetleyip yeniden yazan bir Claude skill'i. Kurallar, Anthropic'in resmi rehberine dayanıyor: [Prompting Claude Opus 5.5](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-claude-opus-5-5).

## Ne yapar?

Ona bir hedef ya da hazır bir prompt verirsin, o da şunları yapar:

- Eskimiş alışkanlıkları temizler. "Adım adım düşün", "dikkatli ol" gibi artık işe yaramayan ifadeleri ve reddedilebilen "önce akıl yürütmeni yaz" kalıbını çıkarır.
- Promptu Opus 5.5'e göre yeniden kurar. "Bitti"nin tanımını yazar, modelin yarıda durmaması için checklist ve durma kuralı ekler, gerekirse süre bütçesi koyar.
- Tasarım isteklerinde "jenerik olmasın" yerine somut bir yasak listesi yazar.
- Uygun effort seviyesini önerir.
- CLAUDE.md ya da sistem promptuna eklenecek satırları ayrıca verir.

Çıktı her seferinde aynı düzende gelir: kopyalanmaya hazır prompt, nelerin neden değiştiği, önerilen ayarlar.

## Kurulum

**Claude Code**

```bash
git clone https://github.com/eraycoskunai/opus5.5-prompt-skill
cp -r opus5.5-prompt-skill/opus-5-5-prompt ~/.claude/skills/
```

Sadece bir projede kullanmak istersen klasörü projenin içindeki `.claude/skills/` altına kopyala.

**Claude uygulaması (claude.ai)**

`opus-5-5-prompt` klasörünü zip'le ve Claude uygulamasının ayarlarındaki skill yükleme bölümünden yükle.

## Kullanım

Skill, prompt yazma ya da iyileştirme isteklerinde kendiliğinden devreye girer. İstersen adıyla da çağırabilirsin:

```
/opus-5-5-prompt Bu promptu Opus 5.5 için düzelt: "Adım adım düşün ve bana bir landing page yap, jenerik olmasın."
```

```
Claude Code'a vereceğim bir görev var: ödeme sistemimizi yeni API istemcisine taşımak. Opus 5.5 için prompt hazırla.
```

```
CLAUDE.md'me modelin yarıda durmamasını sağlayan kurallar ekle.
```

## Dosyalar

```
opus-5-5-prompt/
└── SKILL.md   # skill'in kendisi
```

## Not

Bu skill yalnızca Anthropic'in resmi rehberindeki kuralları kullanır. Rehber güncellenirse skill de güncellenmeli.
