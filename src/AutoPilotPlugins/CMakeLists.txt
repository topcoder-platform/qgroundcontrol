
add_library(AutoPilotPlugins
	APM/APMAirframeComponent.cc
	APM/APMAirframeComponentAirframes.cc
	APM/APMAirframeComponentController.cc
	APM/APMAirframeLoader.cc
	APM/APMAutoPilotPlugin.cc
	APM/APMCameraComponent.cc
	APM/APMCompassCal.cc
	APM/APMFlightModesComponent.cc
	APM/APMFlightModesComponentController.cc
	APM/APMLightsComponent.cc
	APM/APMPowerComponent.cc
	APM/APMRadioComponent.cc
	APM/APMSafetyComponent.cc
	APM/APMSensorsComponent.cc
	APM/APMSensorsComponentController.cc
	APM/APMSubFrameComponent.cc
	APM/APMTuningComponent.cc
	APM/APMHeliComponent.cc

	Common/ESP8266Component.cc
	Common/ESP8266ComponentController.cc
	Common/MotorComponent.cc
	Common/RadioComponentController.cc
	Common/SyslinkComponent.cc
	Common/SyslinkComponentController.cc

	PX4/AirframeComponent.cc
	PX4/AirframeComponentAirframes.cc
	PX4/AirframeComponentController.cc
	PX4/CameraComponent.cc
	PX4/FlightModesComponent.cc
	PX4/PowerComponent.cc
	PX4/PowerComponentController.cc
	PX4/PX4AdvancedFlightModesController.cc
	PX4/PX4AirframeLoader.cc
	PX4/PX4AutoPilotPlugin.cc
	PX4/PX4RadioComponent.cc
	PX4/PX4SimpleFlightModesController.cc
	PX4/PX4TuningComponent.cc
	PX4/SafetyComponent.cc
	PX4/SensorsComponent.cc
	PX4/SensorsComponentController.cc

	AutoPilotPlugin.cc
	Generic/GenericAutoPilotPlugin.cc
)

target_link_libraries(AutoPilotPlugins
	PUBLIC
		qgc
)

target_include_directories(AutoPilotPlugins
	PUBLIC
		${CMAKE_CURRENT_SOURCE_DIR}
		APM
		Common
		PX4
	)
