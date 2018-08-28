# emoji-cz-kr

```
> 🚧  작업중:   작업내용 임시 저장
  ✨  기능:    신규기능 추가
  🐛  수정:    버그 수정
  📚  문서:    문서 변경
  🎨  스타일:   코드에 영향을 미치지 않는 스타일 변경
  🔨  리팩터:   버그 수정이나 기능 추가가 아닌 코드 변경
  🔌  디펜던시:  디펜던시 변경
  🚀  성능:    성능 개선을 위한 코드 변경
  🚨  테스트:   테스트를 추가하거나 변경
  ⚙️  설정:    설정 변경
```

## Demo

위 쪽의 [커밋 히스토리](https://github.com/devjiro76/emoji-cz-kr/commits/master)를 보세요. :point_up:

## Depency

당연한 것이지만 commitizen 이 설치 되어 있어야 합니다.  
`npm install -g commitizen`

자세한 설치방법은 [commitizen 페이지](https://github.com/commitizen/cz-cli)를 참조.

## Installation

```
# 전역 설치
yarn global add https://github.com/devjiro76/emoji-cz-kr
# OR
# npm install --global https://github.com/devjiro76/emoji-cz-kr

# Local 설치
yarn add -D https://github.com/devjiro76/emoji-cz-kr
npm install --save-dev https://github.com/devjiro76/emoji-cz-kr
```

## Commitizen 에 Adopter 로 연결

```
# 전역설치 했을 경우
$ echo '{ "path": "emoji-cz-kr" }' > ~/.czrc

# Local 설치했을 경우 package.json 에 아래 항목 추가
"config": {
  "commitizen": {
    "path": "./node_modules/emoji-cz-kr"
  }
}
```

## Settings

3 가지 방법으로 디폴트 설정을 덮을 수 있습니다.

1. `package.json`
2. `.cz.json`
3. `.czrc`

```js
// in package.json
"config": {
  "commitizen": {
    // ...
    "emoji-cz-kr": {
      // Overwrite types prompted to the command line.
      "types": {
        "Fix": {
          "emoji": "🐝", // overwrite "Fix" emoji to a bee
          "name": "Bug", // overwrite "Fix" name to "Bug"
          "description": "Dirty bug" // overwrite description of "Fix"
        },
        // add a new type "Chore"
        "Chore": {
          "emoji": "❓",
          "description": "Other changes that don't modify src or test files"
        }
      },

      // Overwrite the output commit subject in the specified format.
      // Below is the default format,
      // [emoji] will be replace with the chose type's emoji,
      // [name] will be replace with the chose type's name,
      // [subject] will be replace with the subject you entered.
      // One example output of the format can be: `✨ Feat: initial commit`
      "format": "[emoji] [name]: [subject]"
    }
  }
}

// in .cz.json or .czrc
{
  "emoji-cz-kr": {
    //...
  }
}
```

## Author

Original: Kai Hao <kevin830726@gmail.com>  
Korean Version Translate: Devjiro76 <devjiro76@gmail.com>

## License

[MIT](LICENSE)
