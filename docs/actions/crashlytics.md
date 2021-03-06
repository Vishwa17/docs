<!--
This file is auto-generated and will be re-generated every time the docs are updated.
To modify it, go to its source at https://github.com/fastlane/fastlane/blob/master/fastlane/lib/fastlane/actions/crashlytics.rb
-->

# crashlytics


Upload a new build to [Crashlytics Beta](http://try.crashlytics.com/beta/)




> Additionally, you can specify `notes`, `emails`, `groups` and `notifications`.<br>Distributing to Groups: When using the `groups` parameter, it's important to use the group **alias** names for each group you'd like to distribute to. A group's alias can be found in the web UI. If you're viewing the Beta page, you can open the groups dialog by clicking the 'Manage Groups' button.<br>This action uses the `submit` binary provided by the Crashlytics framework. If the binary is not found in its usual path, you'll need to specify the path manually by using the `crashlytics_path` option.


crashlytics ||
---|---
Supported platforms | ios, android, mac
Author | @KrauseFx, @pedrogimenez



## 3 Examples

```ruby
crashlytics
```

```ruby
# If you installed Crashlytics via CocoaPods
crashlytics(
  crashlytics_path: "./Pods/Crashlytics/submit", # path to your Crashlytics submit binary.
  api_token: "...",
  build_secret: "...",
  ipa_path: "./app.ipa"
)
```

```ruby
# If you installed Crashlytics via Carthage for iOS platform
crashlytics(
  crashlytics_path: "./Carthage/Build/iOS/Crashlytics.framework/submit", # path to your Crashlytics submit binary.
  api_token: "...",
  build_secret: "...",
  ipa_path: "./app.ipa"
)
```





## Parameters

Key | Description | Default
----|-------------|--------
  `ipa_path` | Path to your IPA file. Optional if you use the _gym_ or _xcodebuild_ action | [*](#parameters-legend-dynamic)
  `apk_path` | Path to your APK file | [*](#parameters-legend-dynamic)
  `crashlytics_path` | Path to the submit binary in the Crashlytics bundle (iOS) or `crashlytics-devtools.jar` file (Android) | 
  `api_token` | Crashlytics API Key | 
  `build_secret` | Crashlytics Build Secret | 
  `notes_path` | Path to the release notes | 
  `notes` | The release notes as string - uses :notes_path under the hood | 
  `groups` | The groups used for distribution, separated by commas | 
  `emails` | Pass email addresses of testers, separated by commas | 
  `notifications` | Crashlytics notification option (true/false) | `true`
  `debug` | Crashlytics debug option (true/false) | `false`

<em id="parameters-legend-dynamic">* = default value is dependent on the user's system</em>


<hr />
To show the documentation in your terminal, run
```no-highlight
fastlane action crashlytics
```

<a href="https://github.com/fastlane/fastlane/blob/master/fastlane/lib/fastlane/actions/crashlytics.rb" target="_blank">View source code</a>

<hr />

<a href="/actions/"><b>Back to actions</b></a>
