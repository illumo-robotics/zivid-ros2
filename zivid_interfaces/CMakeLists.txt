cmake_minimum_required(VERSION 3.5)

project(zivid_interfaces)

find_package(ament_cmake REQUIRED)
find_package(builtin_interfaces REQUIRED)
find_package(rosidl_default_generators REQUIRED)

rosidl_generate_interfaces(zivid_interfaces
                           "srv/CaptureAssistantSuggestSettings.srv"
                           "srv/CameraInfoModelName.srv"
                           "srv/CameraInfoSerialNumber.srv"
                           "srv/IsConnected.srv"
                           "srv/LoadSettingsFromFile.srv"
                           "srv/LoadSettings2DFromFile.srv"
                           DEPENDENCIES
                           builtin_interfaces)

ament_export_dependencies(rosidl_default_runtime)
ament_package()
