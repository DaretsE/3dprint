# 🖨️ Калькулятор 3D-печати

## 🚀 Развёртывание

1. Создайте репозиторий на GitHub
2. Загрузите `index.html` и `config/pricing.json`
3. Settings → Pages → Deploy from branch (main / root)
4. Готово!

## ⚙️ Настройка цен

Редактируйте `config/pricing.json`:
- `pricePerKg` — цена пластика (₽/кг)
- `pricePerLiter` — цена смолы (₽/л)
- `operatorMarkupPercent.fdm` — наценка FDM (%)
- `operatorMarkupPercent.resin` — наценка фотополимер (%)

## 📦 Надбавка к расходу материала

В разделе `materialOverhead` файла `config/pricing.json`:

| Параметр | Значение | Описание |
|---|---|---|
| `fdmPercent` | `0` | Надбавка к расходу FDM (0 = отключена) |
| `resinPercent` | `0` | Надбавка к расходу смолы (0 = отключена) |
| `showInInterface` | `0` | Показывать надбавку в интерфейсе (`0` = нет, `1` = да) |

**Пример:** если клиент вводит 100г, а `fdmPercent` = `15`, то цена считается как за 115г.  
При `showInInterface: 1` поле «Расход материала» будет отображаться как «📦 Расход материала (+15%)».
