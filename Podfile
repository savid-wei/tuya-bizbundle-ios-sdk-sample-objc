source 'https://github.com/tuya/tuya-pod-specs.git'
source "https://github.com/TuyaInc/TuyaPublicSpecs.git"
source 'https://github.com/CocoaPods/Specs.git'

use_frameworks!

platform :ios, '11.0'
inhibit_all_warnings!

target 'tuya-bizbundle-ios-sample-objc_Example' do
  pod 'SVProgressHUD'
  pod 'ThingSmartHomeKit', '~> 5.0.0'
  #pod 'ThingSmartActivatorBizBundle'
  #pod 'ThingSmartCameraPanelBizBundle'
  #pod 'ThingSmartCameraRNPanelBizBundle'
  #pod 'ThingSmartCameraSettingBizBundle'
  #pod 'ThingSmartCloudServiceBizBundle'
  #pod 'ThingSmartDeviceDetailBizBundle'

  # 家庭
  pod 'ThingSmartFamilyBizBundle', '~> 5.0.0'
  
  # 帮助
  pod 'ThingSmartHelpCenterBizBundle', '~> 5.0.0'

  # 消息中心
  pod 'ThingSmartMessageBizBundle', '~> 5.0.0'

  # 微信分享需引入（可选）
  # pod 'ThingSocialWeChat', '~> 5.0.0'
  # QQ 分享需引入（可选）
  # pod 'ThingSocialQQ', '~> 5.0.0'
  # 社交分享业务包
  pod 'ThingSmartShareBizBundle', '~> 5.0.0'

  #pod 'ThingSmartOTABizBundle'
  #pod 'ThingSmartPanelBizBundle'
  #pod 'ThingSmartSceneBizBundle'
  #pod 'ThingSmartSkillQuickBindBizBundle'
  #pod 'ThingSmartLightSceneBizBundle', '5.0.0-rc.3.10'
end
post_install do |installer|
  installer.pods_project.targets.each do |target|
    target.build_configurations.each do |config|
      # 消除文档警告
      config.build_settings['CLANG_WARN_DOCUMENTATION_COMMENTS'] = 'NO'
      # iOS 模拟器去除 arm64
      config.build_settings["EXCLUDED_ARCHS[sdk=iphonesimulator*]"] = "arm64"
    end
  end
end
