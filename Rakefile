def run_tests(deviceName, platformName, platformVersion, app, junit)
  system("deviceName=\"#{deviceName}\" platformName=\"#{platformName}\" platformVersion=\"#{platformVersion}\" app=\"#{app}\" JUNIT_DIR=\"#{junit}\" parallel_cucumber features -n 20")
end

task :Galaxy_S5_Device do
  run_tests('Samsung Galaxy S5 Device', 'Android', '4.4', 'http://saucelabs.com/example_files/ContactManager.apk', 'junit_reports/test_Samsung_Galaxy_S5_4.4_real_device')
end

task :Galaxy_S4_Device do
  run_tests('Samsung Galaxy S4 Device', 'Android', '4.4', 'http://saucelabs.com/example_files/ContactManager.apk', 'junit_reports/test_Samsung_Galaxy_S4_4.4_real_device')
end

multitask :test_sauce => [
    :Galaxy_S5_Device,
    :Galaxy_S4_Device

  ] do
    puts 'Running automation'
end
