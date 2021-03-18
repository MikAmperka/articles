# Как Сделать Олдскульную Неоновую Вывеску.

Как сделать не дорогую и эффектную неоновую вывеску с анимацией.

[![DIY Old-school Neon Street Sign](http://img.youtube.com/vi/zmeLh06xB2E/0.jpg)](https://youtu.be/zmeLh06xB2E)

[![DIY Neon Street Sign, Working Loop](http://img.youtube.com/vi/t6zGR22zTOM/0.jpg)](https://youtu.be/t6zGR22zTOM)

## Шаг 1. Вдохновитесь старыми неоновыми вывесками

Когда мы думаем о неоновых вывесках, первое что приходит на ум это ночные улицы Лас-Вегаса 30-х годов прошлого века с бесчисленным количеством красочных неоновых рекламных щитов. Тогда неон был всюду - на каждом рекламном рекламном щите и магазинной вывеске. И что только не изображали используя неоновые лампы: звезды, напитки, танцовщицы, ковбои, индейцы, цветы, музыкальные инструменты и так далее.

Мы в Амперке решили сделать свою неоновую вывеску в духе старых времен. Было решено что на вывеске будет неоновая ковбойша рекламирующая пивной паб. Так же мы решили добавить на вывеску какую-нибудь анимацию и управлять этой анимацией с помощью Arduino.

## Шаг 2. Выбор неона

В действительности настоящие неоновые лампы для вывесок это довольно дорогое удовольствие. Неоновая лампа - газоразрядная и состоит из фигурно изогнутой стеклянной трубки наполенной газом под небольшим давлением. Цвет свечения лампы зависит от того какой газ находится в трубке. Например, неон дает красно-оранжевый цвет, гелий дает бело-оранжевый цвет а аргон - сиреневый. Однако вне завимости от газа такие лампы все равно называют неоновыми. Для того чтобы зажечь такую лампу необходим специальный трансформатор низкого тока и большого напряжения в несколько киловольт способный "выбивать" электроны из молекул газа. Величина напряжения и тока так же влияет на оттенок свечения лампы. Неоновые трансформаторы дороги а для изготовления их своими руками потребуются серьездные расчеты и электронные компоненты. Ну а выдувание фигурных стеклянных трубкок это и вовсе настоящее ремесло требущее недюжинных знаний, подготовки и инструмента. Таким образом изготовление неоновых ламп в домашних условиях практически невозможно. 

Вместо настоящих неоновых ламп можно использовать светодиодный гибкий неон. Такой неон является превосходной заменой настоящему. По своей сути гибкий светодиодный неон это обычная или адресная светодиодная лента в прозрачной силиконовой оболочке. Светодиодный неон дешевый, его свечение так же эффектно и не уступает свечению настоящей неоновой лампы, а для работы со светодиодами не нужны особые навыки.

Для этого проекта мы использовали гибкий светодиодный неон [Arlight ARL](https://arlight.ru/catalog/gibkiy-neon-arl-581/) работающий от постоянного тока напряжением 12В, с сечением 8х16мм, и кратностю реза 10мм. Типоразмер гибкого неона 8х16мм является одним из самых распространенный и его не сложно найти.

Всего мы приобрели несколько катушек неона разных длин с свечением разных цветов:

* Желтый, 5 метров;
* Теплый белый 3000К, 10 метров;
* Синий, 5 метров;
* Холодный белый 5000К, 5 метров;
* Красный, 5 метров;
* Янтарный, 5 метров;
* Зеленый, 5 метров;

## Шаг 3. Придумайте дизайн вывески

Сперва нарисуйте эскиз вашей вывески на бумаге. Определитесь с размером вывески и тем что именно и где будет на ней нарисовано. Когда эскиз готов его нужно перенести в компьютер и задеталировать. Можно использовать любые графические редакторы но мы рекомендуем создать точный чертеж вывески используя 2D или 3D CAD системы.

У нашей ковбойши желтая шляпа и зеленый шейный платок. Мы добавили персонажу две простые анимации. Первая - ковбойша подмигиваем глазом. Вторая - ковбойша поднимает свою кружку с пивом и опускает ее слегка выплескивая пивную пену. Так же мы добавили слово "SALOON" в верхний правый угол вывески. Для слова салун мы решили так же добавить световые эффекты, например мигание, или "бегущий огонек".

Вот некоторые ключевые моменты при дизайне вывески:
* Чертеж вывески должен состоять из линий-конктуров. Линии контуры на чертеже соответствуют местам где будут впоследствии установлены отрезки гибкого светодиодного неона на реальной вывеске.
* Рисунок, персонажи, предметы на вывеске должены быть как можно проще. Но в то же время рисунок должен быть информативным.
* Для линий-контуров используйте плавные кривые линии и сплайны. Старайтесь избегать острых уголов и маленьких радиусов кривизны, ведь по ним потом не получится согнуть ленту. 
* Ширина каждой линии-контура на чертеже соответствует ширине того гибкого неона который вы испольуете. В нашем случае - 8мм.
* Длина каждой линии-контура должна быть кратна минимальной длине реза гибкого неона. В нашем случае кратность реза неоновой ленты - 10мм а длины всех контуров кратны 10мм. Используя CAD систему узнать длину сплайна или кривой не сложно.
* При использовани гибкого неона не допускайте перекрещивания. Если один отрезок ленты светодиодного неона наложится на другой то свечение будет видно только от верхнего отрезка. Если же вам все таки необходимо создать пересечение двух линий-контуров то попробуйте разрезать одну из линий в месте пересечения. Для примера взгляните на "подмигивающий" глаз нашей ковбойши. 
* Раскрасьте линии-контуры в те цвета которые соответствуют реальным цветам вашего гибкого неона.
* Помимо линий-контуров отрезков светодиодных лент не забудьте нарисовать и контур для основы всей вывески.


















[![CircleCI](https://circleci.com/gh/xodio/xod/tree/master.svg?style=shield)](https://circleci.com/gh/xodio/xod/tree/master) [![AppVeyor](https://ci.appveyor.com/api/projects/status/vk5ngjb4xw4m60ks?svg=true)](https://ci.appveyor.com/project/xod/xod)

XOD is a visual programming language for microcontrollers. This repository contains sources for XOD language core, XOD IDE and XOD standard library.

![Xoding demo](./.github/xoding.gif)

## Installation & Quick start

Download the latest IDE version for desktop or run the browser-based IDE at <https://xod.io>.

Documentation and tutorials are at <https://xod.io/docs/>.

## Building from source

XOD is written in JavaScript and ReasonML. You need Node.js and Yarn to build from source. Make sure they are available on your system.

Clone the repository and set working directory to its root. Then run:

```bash
# Install all JavaScript and ReasonML dependencies
yarn

# Build all packages of XOD
yarn build
```

To start the desktop IDE run:

```bash
yarn start:electron
```

Alternatively, run browser-based IDE:

```bash
yarn dev:browser
# IDE is available at <http://localhost:8080>
```

## Directory structure

The project is managed as a [Lerna](https://github.com/lerna/lerna) monorepo and split up in few directories:

* `packages/` — most of source code is here; navigate to a particular package to see it’s own `README` and get an idea what it is for
* `tools/` — utility scripts to assist build process and routine maintenance tasks
* `workspace/` — XOD standard library, default projects, and end-to-end fixtures

## Repository commands

You can run several commands on source files. They are available as yarn subcommands:

* `yarn build` — build, transpile, pack all
* `yarn build:electron` — build desktop IDE only
* `yarn build:cli` — build CLI tools only
* `yarn dev:browser` — run dev-version of browser IDE on localhost
* `yarn dist:electron` — build OS-specific distributive of desktop IDE
* `yarn test` — run unit tests
* `yarn test-cpp` — run C++ code tests
* `yarn test-func` — run functional tests
* `yarn tabtest` — run standard library tabular tests
* `yarn lint` — run the linter to check code style
* `yarn verify` — build, lint, test; run this prior to a pull request
* `yarn start:electron` — starts desktop IDE
* `yarn start:spectron-repl` — starts functional tests environment
* `yarn storybook` — starts React components viewer for visual inspection
* `yarn clean` — remove build artifacts and installed `node_modules`

Note that dependencies between tasks are not resolved. `test` and `start:*` expect that the project is already built.

### Scoping

Many commands (notably `build`, `dev`, `test`) support package scoping to save development time. To rebuild only `xod-project`:

```bash
yarn build --scope xod-project
```

To rebuild `xod-project` and its dependencies:

```bash
yarn build --scope xod-project --include-filtered-dependencies
```

Those are standard [Lerna flags](https://github.com/lerna/lerna#flags).

### Debugging functional tests

`yarn test-func` runs automated end-to-end functional tests.

You can set `XOD_DEBUG_TESTS` environment variable to keep IDE open on failure: `XOD_DEBUG_TESTS=1 yarn test-func`

Use `yarn start:spectron-repl` to run an interactive session and control the IDE window programmatically.

### Running C++ and tabular tests

You need `gcc` and `avr-gcc` to be installed system-wide to run C++ code tests. They are available as OS packages for most platforms.

## License

Copyright 2017-2019 XOD Inc.

This program is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License, version 3, as published by the Free Software Foundation.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License along with this program. If not, see <http://www.gnu.org/licenses/>.

As a special exception, the copyright holders give permission to link the code of portions of this program with the OpenSSL library under certain conditions as described in each individual source file and distribute linked combinations including the program with the OpenSSL library. You must comply with the GNU Affero General Public License in all respects for all of the code used other than as permitted herein. If you modify file(s) with this exception, you may extend this exception to your version of the file(s), but you are not obligated to do so. If you do not wish to do so, delete this exception statement from your version. If you delete this exception statement from all source files in the program, then also delete it in the license file.

## Contributing

Feel free to contribute to the project! See the general [Contibutor’s guide](https://xod.io/docs/contributing/) and [GitHub contribution guidelines](./CONTRIBUTING.md).
