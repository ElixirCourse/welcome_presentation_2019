#HSLIDE
## Функционално програмиране с Elixir

#HSLIDE
![Image-Absolute](assets/elixir-logo.png)

#HSLIDE
### Кои сме ние?

* Ние ползваме Elixir в свободното си време. <!-- .element: class="fragment" -->
* Ние ползваме професионално Elixir. <!-- .element: class="fragment" -->
* Това е втората година на курса. <!-- .element: class="fragment" -->
* Създаваме материали и код свързани с курса.   <!-- .element: class="fragment" -->

#HSLIDE
![Image-Absolute](assets/sofia_elixir.png)

#HSLIDE
### Кои сте вие?

* Искате да разберете защо напоследък се говори за Erlang/Elixir?             <!-- .element: class="fragment" -->
* Фенове сте на Elixir/Erlang и искате да учите Elixir?                       <!-- .element: class="fragment" -->
* Искате да изкарате курс от типа 'Програмиране с |език|', за да си обогатите познанията? <!-- .element: class="fragment" -->
* Искате да запишете курс от типа 'Програмиране с |език|' за лесни кредити? <!-- .element: class="fragment" -->

#HSLIDE
### Защо да учим нов език?!

* Нали си знам PHP | JAVA | C# | Ruby | Python | Това-с-което-(ще-)си-вадя-хляба? <!-- .element: class="fragment" -->
* Тези хипстъри, дето всяка година учат нов език, за нищо не стават!  <!-- .element: class="fragment" -->
* Всяка година, не, всяка седмица нова 'технология', то не може всичко я! <!-- .element: class="fragment" -->

#HSLIDE
![Image-Absolute](assets/Haters_gonna_hate.jpg)

#HSLIDE
### Защо да учим Elixir?

* Всички твърдения от предния слайд са вярни. Не всичко работи за всички. <!-- .element: class="fragment" -->
* Няма сребърен куршум, но за всичко си има набор от добри инструменти. <!-- .element: class="fragment" -->
* Дайте шанс на този набор от инструменти? <!-- .element: class="fragment" -->

#HSLIDE
### Какво е Elixir?

* Elixir е език, който върви на BEAM. <!-- .element: class="fragment" -->
* BEAM e виртуалната машина на Erlang.  <!-- .element: class="fragment" -->
* Ахаа! Значи нещо като Scala, както се отнася към Java?  <!-- .element: class="fragment" -->
* И да, и не.  <!-- .element: class="fragment" -->
* Elixir е Erlang. Но и нещо повече. <!-- .element: class="fragment" -->

#HSLIDE
### Какво е Erlang?

![Image-Absolute](assets/what_is_erlang.png)

#HSLIDE
Erlang е създаден с цел: писане на телеком програми

* Конкурентни (едно устройство трябва да може да поддържа хиляди едновременни транзакции). <!-- .element: class="fragment" -->
* Толерантни към грешки и проблеми - както софтуерни, така и хардуерни.  <!-- .element: class="fragment" -->
* Практически нулев downtime.  <!-- .element: class="fragment" -->
* Кодът им трябва да може да се заменя с по-нови версии, докато те работят.  <!-- .element: class="fragment" -->

#HSLIDE
#### А какви проблеми имаме днес?
![Image-Absolute](assets/internet.jpeg) <!-- .element: class="fragment" -->

#HSLIDE
![Image-Absolute](assets/fun1.jpg)

#HSLIDE
![Image-Absolute](assets/fridge.jpg)

#HSLIDE
![Image-Absolute](assets/social_media.gif)

#HSLIDE
Joe Armstrong (създател на Erlang) нарича Erlang език за конкурентно-ориентирано програмиране, като се базира на няколко правила:

#HSLIDE
### Erlang!
1. Кодът върви в процеси, които са на ниво език.
2. Тези процеси не споделят памет - имат собствен стек и собствен heap. <!-- .element: class="fragment" -->
3. Много са евтини за създаване и си комуникират чрез размяна на съобщения.  <!-- .element: class="fragment" -->
4. Лесно могат да си комуникират помежду си, дори да са на различни машини. <!-- .element: class="fragment" -->
5. Ако един процес 'умре', другите продължават да живеят. Може нов да го замести, зависи от стратегията. <!-- .element: class="fragment" -->

#HSLIDE
### Erlang върви на BEAM

* BEAM е способна да използва всички ядра на процесора без проблем. <!-- .element: class="fragment" -->
* BEAM-level процесите са много малки 1KB-2KB при създаването си. <!-- .element: class="fragment" -->
* Можем да създаваме огромен брой процеси без да се притесняваме. Говорим за милиони.  <!-- .element: class="fragment" -->
* Scheduler-ите на BEAM използват стратегия, различна от стратегиите в други езици - превантивна стратегия.  <!-- .element: class="fragment" -->

#HSLIDE
### Let it CRASH!!!
![Image-Absolute](assets/let_it_crash.jpg)

#HSLIDE
### Кой ползва Erlang?

#HSLIDE
* Amazon - за базата данни SimpleDB
* Yahoo! - за URL bookmarking  <!-- .element: class="fragment" -->
* WhatsApp - написана на Erlang, real-time съобщения, купена от Facebook  <!-- .element: class="fragment" -->

#HSLIDE
* T-Mobile, Motorola, Ericsson - за SMS услуги и 3G/4G мрежи. Ericsson са създатели на Erlang.
* RabbitMQ - AMQP имплементация  <!-- .element: class="fragment" -->
* CouchDB - популярна база данни  <!-- .element: class="fragment" -->
* Riak - data store  <!-- .element: class="fragment" -->

#HSLIDE
### Та какво е Elixir??

* Elixir наследява всички специфики и идеологии на Erlang. Все пак върви на BEAM. <!-- .element: class="fragment" -->
* Elixir може да използва всичко писано на Erlang. <!-- .element: class="fragment" -->
* Elixir идва с много добър инструментариум. <!-- .element: class="fragment" -->
* Elixir има много добро и бързо-растящо общество. <!-- .element: class="fragment" -->
* Elixir е модерен език, добър за web и IoT. <!-- .element: class="fragment" -->
* Споменахме ли, че е функционален език? <!-- .element: class="fragment" -->

#HSLIDE
![Image-Absolute](assets/functional.jpeg)

#HSLIDE
### Началото

* Езикът се ползва някъде от 2013 (2011 първи копки) година, което го прави доста млад. <!-- .element: class="fragment" -->
* Създателят на Elixir, Жозе Валим (José Valim), идва от ruby/rails света. <!-- .element: class="fragment" -->
* Бързо набира популярност сред рубистите и ерлангаджиите. <!-- .element: class="fragment" -->

#HSLIDE
![Image-Absolute](assets/jose.jpg)

#HSLIDE
### Защо да учим Elixir?
* Защото можем да си напишем сървис, който ще поддържа хиляди потребителя online и ще живее в един OS процес.
* Защото имаме качествен инструментариум! <!-- .element: class="fragment" -->

#HSLIDE
### Инструментариум

* Elixir идва с mix. <!-- .element: class="fragment" -->
* Mix изпънява различни задачи - да речем прави нов Elixir проект. <!-- .element: class="fragment" -->
* Много лесно е да си напишем и своя задачка. <!-- .element: class="fragment" -->

#HSLIDE
### MIX
![Image-Absolute](assets/mix.jpg)

#HSLIDE
### Инструментариум

* Всъщност с mix можем да си направим собствена библиотека. <!-- .element: class="fragment" -->
* И да я качим в hex, откъдето можем да сваляме библиотеки на други хора. <!-- .element: class="fragment" -->
* Също така mix се справя страхотно с dependencies. <!-- .element: class="fragment" -->
* Има вградена добра библиотека за тестване. <!-- .element: class="fragment" -->
* Има лесен начин за генериране на HTML документация с връзки към кода. <!-- .element: class="fragment" -->

#HSLIDE
### NOT MIX
![Image-Absolute](assets/npm.jpeg)

#HSLIDE
### Защо да учим Elixir?
* Защото можем да си напишем сървис, който ще поддържа хиляди потребителя online и ще живее в един OS процес.
* Защото имаме качествен инструментариум!
* Защото езикът е доста приятен и лесен за продуктивна работа!! <!-- .element: class="fragment" -->

#HSLIDE
### Продуктивност

![Image-Absolute](assets/productivity.jpg)

#HSLIDE
### Езикът Elixir в няколко изречения:

* Модули, които са колекции от функции.
* Всичко е immutable.
* Кодът е изграден от композирани функции.
* Всичко върви в BEAM-процес.
* Кодът в тези BEAM-процеси е последователен, процесите вървят конкурентно един на друг.


#HSLIDE
#### Модули, колекции от функции:

```elixir
defmodule MyModule do
  import OtherModule

  def public_function(x) do
    x * private_function(x)
  end

  defp private_function(x) do
    x + other_module_public_function(x)
  end
end
```

#HSLIDE
#### Кодът е изграден от композирани функции:

```elixir
[1, 2, 3, 4, 5]
|> Enum.map(fn n -> n * n end)
|> Enum.filter(fn n -> n > 10 end)
|> Enum.reduce(1, &(&1 + &2))

# -> 42
```

#HSLIDE
#### Кодът е изграден от композирани функции:

```elixir
File.stream!("path/to/some/file")
|> Stream.flat_map(&String.split(&1, " "))
|> Enum.reduce(%{}, fn word, acc ->
  Map.update(acc, word, 1, & &1 + 1)
end)
|> Enum.to_list()
```

#HSLIDE
#### Pipes

![Image-Absolute](assets/pipes.jpg)

#HSLIDE
#### Функционален език:
```elixir
4 = 4                 # Интерпретира се без грешка
5 = 4                 # Грешка - MatchError
a = 4                 # Няма грешка, 'a' има стойност 4
4 = a                 # Също няма грешка
{d, e, 5} = {7, 6, 5} # d става 7, e става 6

f = fn (x) -> x * x end
f.(3)
# -> 9
```

#HSLIDE
#### Функционален език:
```elixir
f = fn
  (5) -> {:ok, 5}
  (x) -> {:error, x}
end
{:ok, x} = f.(5)     # Успех, x получава стойност 5
{:ok, x} = f.(6)     # Грешка, резултатът е {:error, 6}

Map.put(%{a: 3}, :b, 4)
# %{a: 3, b: 4} -> Нов map
```

#HSLIDE
#### Процеси:
Процесите в Elixir/Erlang се създават със `spawn`.

```elixir
# Тази функция ще се изпълни в нов процес:
pid = spawn fn -> 2 * 21 end

Process.alive?(pid)
# false, тъй като функцията се изпълнява бързо.

# Можем да ползваме pid-а на текущия процес с:
self()
Process.alive?(self()) # true
```

#HSLIDE
#### Процеси:

```elixir
pid = spawn(fn ->
  receive do
    {:howdy, message} -> IO.puts(message)
    {_, message} -> IO.puts("Няма значение")
  end
end)

send pid, {:howdy, "Как си?"}
```

#HSLIDE
Parallel map(collection):

```elixir
defmodule PEnum do
  def pmap(collection, mapper) do
    collection
    |> Enum.map(&(Task.async(fn -> mapper.(&1) end)))
    |> Enum.map(&Task.await/1)
  end
end
```

#HSLIDE
No shared state, threads and locks.

![Image-Absolute](assets/suffer.jpg)

#HSLIDE
### Защо Elixir?
* Защото можем да си напишем сървис, който ще поддържа хиляди потребителя online и ще живее в един OS процес.
* Защото имаме качествен инструментариум!
* Защото езикът е доста приятен и лесен за продуктивна работа!!
* Защото с Elixir сме МЕТА! <!-- .element: class="fragment" -->

#HSLIDE
### Metaprogramming

![Image-Absolute](assets/metaprogramming.jpg)

#HSLIDE
### Metaprogramming

* Всъщност defmodule е макро.
* Както и def за функция.
* Както и почти всичко, което ще ползвате.

#HSLIDE
### Metaprogramming

##### Elixir е написан на Elixir

![Image-Absolute](assets/elixir_is_elixir.png)

#HSLIDE
### Metaprogramming

##### Позволява ни да правим такива неща
```elixir
from Post,
  where: [category: "fresh and new"],
  order_by: [desc: :published_at],
  select: [:id, :title, :body]
```

#HSLIDE
### Metaprogramming

##### Това пък е резултат от неуспешен тест

![Image-Absolute](assets/failed_test.png)

#HSLIDE
### Защо Elixir?
* Защото можем да си напишем сървис, който ще поддържа хиляди потребителя online и ще живее в един OS процес.
* Защото имаме качествен инструментариум!
* Защото езикът е доста приятен и лесен за продуктивна работа!!
* Защото с Elixir сме МЕТА!
* Защото обществото около Elixir ще ви приветства! <!-- .element: class="fragment" -->

#HSLIDE
#### Обществото
* Elixir обществото раздвижи Erlang обществото.
* Erlang се развива, Elixir програмисти правят PR-и, помагат.
* Имаме и ще имаме множество чудесни библиотеки.


#HSLIDE
### В Elixir/Erlang има бъдеще

![Image-Absolute](assets/ouroboros-by-zarathus.jpg)

#HSLIDE
### Защо да учим Elixir?
* Защото можем да си напишем сървис, който ще поддържа хиляди потребителя online и ще живее в един OS процес.
* Защото имаме качествен инструментариум!
* Защото езикът е доста приятен и лесен за продуктивна работа!!
* Защото с Elixir сме МЕТА!
* Защото обществото около Elixir ще ви приветства!
* И всички тези mixture-и! <!-- .element: class="fragment" -->

#HSLIDE
#### Plug & Phoenix

![Image-Absolute](assets/phoenix_and_plug.jpg)

#HSLIDE
#### Ecto

![Image-Absolute](assets/ecto.png)

#HSLIDE
#### И още и още

![Image-Absolute](assets/explore.png)

#HSLIDE
#### Ще си говорим и за доста advanced неща!

![Image-Absolute](assets/distribution.jpg)

#HSLIDE
### Кой ползва Elixir?

#HSLIDE
* Adobe - За колаборативна работа над фотографски материали.
* Discord - За voice/text чат за геймъри.
* Pinterest - Социална мрежа, написана на Elixir. За споделяне и тагване на хоби идеи по снимки.

#HSLIDE
* Pivotal - RabbitMQ CLI е написан на Elixir.
* Slack - Сървърите, поддържащи видео разговорите, са на Elixir.
* http://elixir-companies.com - Списък с компании, ползващи Elixir.

#HSLIDE
### Защо да научим Elixir?
* Защото е модерен, конкурентен език.
* Защото хората зад и около него са опитни.
* Защото основата му, Erlang, е стабилна и доказана.
* Защото е функционален език.
* Защото е подходящ за писане и поддръжка на много типове приложения.
* Защото ще разшири кръгозора ви.
* Защо не?

#HSLIDE
## Малко информация за курса
![Image-Absolute](assets/Craft-Beer.jpeg)

#HSLIDE
## Добре дошли!
* Ако сте записали курса за да вземете някоя изборна, ОТПИШЕТЕ ГО, няма да ви е лесно. <!-- .element: class="fragment" -->
* Ако смятате, че Обектно-ориентираното програмиране е единственият начин, този курс не е за вас. <!-- .element: class="fragment" -->
* Ако нямате достатъчно време което да отделяте също ще ви е трудно. <!-- .element: class="fragment" -->

#HSLIDE
## Философия на курс

There will be no foolish wand waving or silly incantations in this class. As such, I don't expect many of you to enjoy the subtle science and exact art that is potion making. However, for those select few, who possess the predisposition, I can teach you how to bewitch the mind and ensnare the senses. I can tell you how to bottle fame, brew glory and even put a stopper in death.

#HSLIDE
## Какво ще трябва да научите в курса
* Elixir <!-- .element: class="fragment" -->
* да мислите и моделирате чрез функции, а не обекти <!-- .element: class="fragment" -->
* да съпоставяте образци <!-- .element: class="fragment" -->
* да изпозвате git <!-- .element: class="fragment" -->
* да сте истински шамани и алхимици способни да миксират всякакви отвари  <!-- .element: class="fragment" -->

#HSLIDE
## Организация на курса
* Курсът ще се провежда всеки Вторник и Четвъртък от 19&#58;15 до 21:00.  <!-- .element: class="fragment" -->
* Ще се стараем за всяка тема да имаме подробна публикация в блога ни. <!-- .element: class="fragment" -->
* обикновено на лекция ще имаме презентация, но винаги сме готови да обсъдим нещо, което не е включено в нея. <!-- .element: class="fragment" -->

#HSLIDE
## Организация на курса
* Лекциите ще бъдат разделени в 3 основни блока <!-- .element: class="fragment" -->
  * Първият блок ще бъде информация за самия език и неговите идиоми <!-- .element: class="fragment" -->
  * Във втория ще говорим за паралелизъм и кокурентност <!-- .element: class="fragment" -->
  * В края на семестъра ще говорим за различни библиотеки и за неща котио смятаме за интересни <!-- .element: class="fragment" -->
  * Доста често ще говорим за Erlang <!-- .element: class="fragment" -->

#HSLIDE
## Оценяване
* Максимум 135 точки  <!-- .element: class="fragment" -->
  * 3 домашни за общо 45 точки
  * Семестриален проект за 30 точки (Ние ще ви дадем задание за проекта)
  * Kурсов проект от 40 до 80 точки (Определени от нас спрямо сложносттан. Най-често 60 точки)
* Допълнителни точки <!-- .element: class="fragment" -->
  * Бонус точки, ако добавите нещо, към някой проект с отворен код свързан с Elixir.
  * Бонус точки за неща, които ние преценим.

#HSLIDE
## Скала за оценяване
Оценнка|2|3|4|5|6|
-|-|-|-|-|-
Точки|0-64|65-74|75-94|95-114|115-135

#HSLIDE
## Ресурси
* Имаме сайт http://blog.elixir-lang.bg
* Имаме Facebook група https://www.facebook.com/groups/636900123169076/
* Имаме mail [course@elixir-lang.bg](mailto:course@elixir-lang.bg)
* Github https://github.com/ElixirCourse


#HSLIDE
## Край
![Image-Absolute](assets/gimpy.jpg)
