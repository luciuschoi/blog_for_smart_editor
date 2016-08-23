# Smart Editor for Rails projects

기존의 [smart editor](https://github.com/YelloMobile/smart_editor_rails)는 레일스 버전 4.0.0.rc1 까지만 지원합니다.
그래서 원저 저장소를 포크하여 gemspec에서 레일스 의존성 버전을 4.2.6으로 업그레이드하였습니다.

```ruby
gem 'smart_editor', github: "luciuschoi/smart_editor_rails", branch: "rails4"
```

번들 인스톨 후 사용법은 원저 저장소의 문서를 참고하시고, 레일스 4버전에서 도입된 Turbolinks 문제는 아래와 같이 `data: { turbolinks: false }` 옵션을 `link_to` 헬퍼에 추가해 주어 해당 링크에 대해서 Turbolinks 기능이 작동하지 못하도록 처리합니다.


```erb
<%= link_to "링크", resource_path, data: { turbolinks: false } %>
```
