# KoreanSchool

> Fetch Korean Schools Data from NEIS and School Info

[![npm](https://img.shields.io/npm/v/korean-school.svg?style=flat-square)](https://www.npmjs.com/package/korean-school) [![npm](https://img.shields.io/npm/dt/korean-school.svg?style=flat-square)](https://www.npmjs.com/package/korean-school)

## ChangeLog

See [CHANGELOG](./CHANGELOG.md)

## Features

- Find the school data by its location and name
- Fetch the school meal from NEIS
- Fetch the school information from School Info

## Installation

- Install with npm:

```bash
npm install korean-school --save
```

- Clone the repo:

```bash
git clone https://github.com/Astro36/KoreanSchool.git
```

## Usage

### API Documentation

See [API](./API.md)

### Example

Fetch the daily school meal:

```javascript
const school = require('korean-school');
school.neis.getMeal(school.find('경기도', '백석고'), new Date(), (meal) => {
  if (meal !== null) {
    console.log(meal.breakfast);
    console.log(meal.lunch);
    console.log(meal.dinner);
  }
});
```

You can see more examples on [API](./API.md) documentation.

## License

```text
KoreanSchool
Copyright (C) 2017  Astro

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
```

KoreanSchool is licensed under the [GPL 3.0](./LICENSE).
