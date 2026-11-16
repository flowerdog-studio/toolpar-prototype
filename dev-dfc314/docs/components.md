# Компоненты

Имена компонентов совпадают с Figma «Toolpar DS». Колонка «В прототипе» показывает, где компонент собран в `index.html`: функция-рендер или CSS-класс. Поведение и размеры берите оттуда, внешний вид и варианты — из Figma.

## Действия (Components / Actions)

| Figma | В прототипе | Варианты и поведение |
|---|---|---|
| Button | `.btn` + `.btn-primary` / `.btn-secondary` / `.btn-sm` | Type: Primary (жёлтая), Secondary (серая), Dark (чёрная, на жёлтом баннере). Size: XL/L 56, M 48. State: Default, Hover, Pressed, Disabled (30%). Опционально иконка слева, 20 px. |
| InstallmentButton | `.btn-installment` | Красная кнопка рассрочки с иконкой банка. В товаре квадратная 56, в мобильной липкой панели 48. |
| IconButton | `.iconbtn` | 48 × 48, иконка 24. Ghost — стрелки каруселей (hover `--icon-hover`, край ленты — disabled). |
| Link | `.link` | Подчёркнутая ссылка («Заказать звонок»). |

## Поля и фильтры (Components / Inputs)

| Figma | В прототипе | Поведение |
|---|---|---|
| SearchField | `.search` в `Header()` | Серое поле 48, кнопка-стрелка справа. На мобилке поле раскрывается из иконки поиска в хедере. |
| Checkbox | `Check()`, `.check` | Квадрат без скругления; отмеченный — жёлтый с галочкой. |
| FilterHeader, FilterOption | `FGroup()` | Группа фильтра в сайдбаре категории: заголовок, чекбоксы с количеством, «Ещё / Свернуть» (Disclosure). |
| Disclosure | `More()` | Раскрытие длинного списка. |
| PriceRange, RangeSlider, Slider/Rail, Slider/Thumb | `PriceRange()`, `rangeSet()` | Два поля «от / до» и двойной ползунок, синхронизированы. |
| SortOption, SortMenu | `.sortmenu` | Выпадающее меню сортировки «по популярности ⌄». |
| QuantityStepper | `Stepper()`, `.stepper` | − количество +. В карточке появляется вместо кнопки корзины после добавления (фон `--control-on-photo`). |
| CategoryLink | `.subcat` | Ссылка-подкатегория (подчёркивается при наведении). |
| Tab | вкладки «Акций» (`data-ptab`), `.ck-tabs` (корзина) | Активная вкладка — чёрный текст с подчёркиванием 2 px, неактивные — серые. |
| RadioOption, OptionCard, TextField | `.ck-opt`, `.ck-pick`, поля оформления | Выбор доставки и оплаты, данные получателя. |

## Коммерция (Components / Commerce)

| Figma | В прототипе | Поведение |
|---|---|---|
| ProductCard | `ProductCard()`, `.pcard` | Фото 1:1 на сером, при наведении — листание фото по зонам (точки внизу), кнопка корзины в углу фото. Название — ровно 3 строки с троеточием, бренд жирнее. Бонус (+1%), доставка («сегодня» / дата). Состояния: Default, Hover (текст оливковый), In cart (счётчик), Out of stock (в конце списка). |
| Badge | `.badge` | «−15%», «ХИТ» — жёлтые; «Новинка» — синяя. Левый верхний угол фото. |
| Price | `.t-price-l`, `.t-price-xl`, `.t-price-old*` | Цена + зачёркнутая старая. |
| Bonus | `.bonus` | «+N бонусов» с жёлтой точкой; виден только при режиме пользователя (в Figma — переменная `user/show-bonus`). |
| DeliveryInfo | `Delivery()` | Иконка + «Доставка / сегодня». |
| CartItem | `Line()`, `.ck-line` | Строка корзины: чекбокс, фото, название, цена, количество, избранное, удалить. |
| ShipmentThumb | `.ck-grp .tb` | Миниатюры товаров в отправлении. |
| SummaryRow | `Summary()`, `.ck-sum` | Итог: товары, скидка, доставка, бонусы, «Оформить заказ». Липкий справа. |
| OrderItem, OrderStep | `Order()`, `.lk-*` | Заказ в личном кабинете: статус-пульс, состав, информация. |

## Навигация (Components / Navigation)

| Figma | В прототипе | Поведение |
|---|---|---|
| UtilityNav | `Header()` → `.utility` | Город, телефон, «Заказать звонок»; справа: Контакты, Адреса магазинов, О компании, Покупателям, **Система привилегий**, Сотрудничество. Текущий раздел — жирнее. |
| ShoppingNav | `Header()` → `.shopping` | Логотип, «Каталог», поиск, Войти / Заказы / Корзина. Липкий (sticky) при прокрутке, высота 92. |
| CatalogMenuItem | `CatalogMenu()`, `.mitem` | Открытый каталог: три колонки, при наведении на пункт — подменю; невыбранные колонки серые (`--text-menu-inactive`). |
| HeaderAction | `.haction` | Иконка + подпись; у корзины — счётчик (Micro Bold). |
| AccountMenuItem | `.bp-nav`, меню ЛК | Пункт бокового меню с количеством (бренды по направлениям). |
| Footer | `Footer()` | 4 колонки (контакты 510 + 3 × 240), логотип, копирайт, Visa/Mastercard серым. На мобилке — аккордеоны. |

## Товар (Components / Product)

ProductGallery и GalleryThumb (`.gallery`: главное фото, миниатюры, зум, стрелки), VariantChip и VariantGroup (модификации), DeliveryOption, SpecRow (характеристики), BulletItem, BenefitStat, DocumentRow, Tag, SectionHeader, Stars, ReviewItem, RatingSummary, ReelCard, IconAction — всё в функции `Product()` и мобильной `MProduct()`.

**SectionHeader** — заголовок секции H1 с вариантами: Default, With arrows (стрелки каруселей справа), With link («Все предложения» рядом с заголовком), With arrows and link. Отступ до контента 32.

## Маркетинг (Components / Marketing)

| Figma | В прототипе | Поведение |
|---|---|---|
| HeroBanner | `setupHero()`, `.hero` | 3 слайда, автопрокрутка каждые 6 с (пауза, если вкладка скрыта), свайп и перетаскивание, точки-индикаторы. Текстовый блок в левом нижнем углу, кнопка фиксирована, текст растёт вверх. |
| PromoCard | `.promo` | Карточка акции: фото, срок, заголовок H3, описание. Hover — фото ×1,03. |
| BrandTile | `.brand-tile` | Логотип бренда в рамке; hover — логотип ×1,08. |
| InstagramCTA | блок в ленте рилсов | Жёлтая плитка «Мы в Instagram». |
| ReelCard, ReelViewer | `Reel()`, `Viewer()` | Карточка 9:16, ↗ в Instagram. Просмотр — полноэкранный, фон `--overlay-scrim`, прогресс, звук, листание. |
| Pagination | `.pagination` | Точки слайдов баннера. |
| AlphabetLetter, BrandLink | `.bp-abc`, `.bp-g .names` | Алфавит со ссылками-якорями; группы брендов в две колонки по 240. |

Исходники баннеров и фото с нужным кропом лежат на этой же странице Figma, в секции «Исходники изображений».

## Покупателям (Components / Help)

HelpSearch (`HSearch()` — поиск по всем статьям с подсветкой абзаца), SearchResultItem (`.hs-item`), TopicCard (`.h-topic` — кликабельна целиком), TopicLink (`.h-tl`), FaqItem (`.h-fq` — аккордеон: вопрос H4, ответ Body/Text, ссылка «Подробнее»; свойство Show more), HelpContactCard (`HContact()`, `.h-contact`), TocLink (`.h-toc` — оглавление статьи, липкое, подсвечивает текущий раздел), StepItem (`.h-steps`), Callout (`.h-note`), PagerLink (`.h-pager`).

## Мобильные (Components / Mobile)

M/Header (липкая строка 56: логотип, город, поиск), M/TabBar и M/TabItem (нижняя панель: Главная, Каталог, Корзина, Заказы, Войти), M/ProductCard, M/FilterBar, M/FilterChip, M/BottomSheet (шторки фильтров, сортировки, рассрочки), M/StickyBuyBar (липкая покупка в товаре), M/Accordion, M/CatalogRow, M/CatalogHeader, M/SectionHeader, M/HeroBanner, M/PromoCard, M/ReelCard, M/CartItem, M/CheckoutBar, M/BrandTile, M/Footer, M/InstagramCTA, M/ProductGallery, M/BackLink, M/StatusBar (только для макетов).

В прототипе это функции `MHeader()`, `MTab()`, `MHome()`, `MCatalog()`, `MCategory()`, `MFilters()`, `MSheet()`, `MProduct()`, `MBuyBar()`, `MFooter()`, `MViewer()` и классы `.m-*`. Страницы «Покупателям», «Акции», «Бренды», «О компании», «Система привилегий», «Спасибо», корзина и ЛК на мобилке используют веб-разметку с мобильными стилями (`.m .…`).
