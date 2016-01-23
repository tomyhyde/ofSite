# 오픈프레임웍스 사이트

이 저장소는 [openFrameworks](http://openFrameworks.cc/)웹사이트를 생성하기 위한 콘텐츠와 코드를 담고 있습니다.

## 참여하기

웹페이지나 도큐먼트를 수정하는데 참여하기 위해, 이 저장소를 fork하여 작어하시고, github을 통해 pull request를 보내주시면 됩니다.

Most of the content is in the `content` folder in markdown folder.
대부분의 콘텐츠는 `content`내에 마크다운으로 담겨 있습니다.

`tutorials` 폴더는 카테고리를 의미하는 폴더들로 되어있고, 각 폴더안에 `.markdown` 확장자를 가진 텍스트파일이 담겨 있습니다. 포함되는 이미지/다른 자료들은 텍스트 파일명과 같은 이름의 폴더에 담겨있습니다. 각 튜토리얼은 최종적으로 같은 폴더 구조에 html로 생성되기 떄문에 이미지/자료들의 링크를 작성할때에는 상대적인 경로로 작성해야 하며, 폴더를 포함해서는 안됩니다. 이와 같이요:

```md
![img](image.png)
```

`documentation` 폴더는 OF API 레퍼런스들을 담고 있으며, 역시 마크다운포맷입니다. 이 문서들은 코드에 의해 생성되나, 모든 클래스, 함수 및 변수들의 `description`필드는 마크다운으로 직접 편집할 수 있습니다.

## 로컬 사이트 구축을 위한 세팅

이 사이트는 [nikola](https://getnikola.com)를 기반으로 합니다. 쉽게 구축, 설치, 사용을 위해 최상위 폴더에 스크립트가 준비되어 있습니다.

- ./install.sh는 nikola및 필요한 의존성을 설치합니다. 현재는 리눅스에서만 테스트 되었지만, python3, pip, asciidoc이 설치된 맥킨토시라면 동작할 것입니다.

- ./auto_build.sh는 수정된 파일이 있을때마다 nikola를 구동하고 수정된 파일이 있을때마다 웹을 빌드합니다.

- ./serve.sh는 로컬 웹서버를 시작하여 브라우저에서 확인할 수 있도록 웹사이트를 제공합니다. 

번역에 참여하는것과 같이 큰 수정을 할 계획이 있으시다면, 가장 쉬운 방법은 위에서 언급한 마지막 2개의 스크립트를 실행시켜둔 상태에서 콘텐츠 파일을 수정하면 되며, 사이트는 자동으로 업데이트 됩니다.

## 도큐먼트-스타일 마크다운

사이트의 일부분 도큐먼트들은 마크다운으로 작성되어 있습니다. 마크다운은 위키-스타일 문법입니다. 자세한 사항은 [Daringfireball](http://daringfireball.net/projects/markdown/)를 살펴보시기 바랍니다.

문법을 체크하는 가장 쉬운 방법은 사이트의 많은 페이지들을 살펴보는 것이지만, 아래에 몇가지 유용한 팁을 알려드립니다:

코드를 삽입하려면, 아래와 같이 작성하시면 됩니다. 시작과 끝을 주의하시고, 시작의 끝은 ".cpp"로 마치시면 됩니다.

	```cpp
	for(int i = 0; i < 16; i++) {
		ofLog() << i;
	}
	```


이미지는 일반적인 마크다운 포맷을 사용하여 추가합니다:

    ![Image Title](filename.png "alt text")

도큐먼트 공헌에 관한 최종 설명은, [문서 공헌하기](http://www.openframeworks.kr/tutorials/developers/003_contributing_to_the_documentation.html) 튜토리얼을 참고해주시기 바랍니다.
