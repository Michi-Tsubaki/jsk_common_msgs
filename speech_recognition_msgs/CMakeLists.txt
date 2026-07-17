cmake_minimum_required(VERSION 3.8)
project(speech_recognition_msgs)

find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/Grammar.msg"
  "msg/PhraseRule.msg"
  "msg/SpeechRecognitionCandidates.msg"
  "msg/Vocabulary.msg"
  "srv/SpeechRecognition.srv"
)

ament_export_dependencies(rosidl_default_runtime)

ament_package()
