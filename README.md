![TALQ Consortium](https://www.talq-consortium.org/data/images/1/2/8/logo.png)

# TALQ - The Smart City Protocol

The [TALQ Consortium](https://www.talq-consortium.org/) has developed the Smart City Protocol, a globally accepted interface standard for smart city device networks. This software protocol is a specification for information exchange, suitable for implementation in various products and systems. In this way interoperability between Central Management Software (CMS) and Outdoor Device Networks (ODN) from different vendors is enabled, such that a single CMS can control different ODNs in different parts of a city or region.

TALQ provides answers to the main challenges of building really smart cities including increasing safety and comfort for inhabitants, reducing energy consumption and CO<sub>2</sub> emissions worldwide, raising cost efficiency for operators managing a smart city.

Driven originally by smart street lighting vendors, TALQ is now an open industry consortium addressing the entire smart city environment allowing manufacturers of smart city applications to join as members and certify their products as TALQ-compliant. Other stakeholders such as cities, municipalities, utilities, consultants, universities and many others can join the consortium as Partners Let’s TALQ !


# TALQ 2: A RESTful API


The TALQ protocol has been defined with the [OpenAPI Specification (OAS), formerly Swagger](https://github.com/OAI/OpenAPI-Specification), the standard de facto for defining RESTful APIs. An OpenAPI definition can then be used by documentation generation tools to display the API, code generation tools to generate servers and clients in various programming languages, testing tools, and many other use cases. Thanks to this specification manufacturers can dramatically shorten the development times and increase code quality when aiming to become interoperable.

The TALQ Specification is splitted in three files, named with the [Semantic versioning](#semantic-versioning):

- [Data model OAS file](oas/talq-data-model-2-3-0.json): The data model defines all TALQ objects used in the protocol such as Devices, Calendars, Control Programs, etc.
- [API for Outdoor Device Network (Gateway) OAS file](oas/talq-api-gateway-2-3-0.json): It defines the Gateway RESTful API with each resource, methods, parameters, etc.
- [API for Central Management Software (CMS) OAS file](oas/talq-api-cms-2-3-0.json): It defines the CMS RESTful API with each resource, methods, parameters, etc.

## Versions

All the released versions of the TALQ Specification are in the table below: 

| Name                                                                | Version         | Date        | 
| ------------------------------------------------------------------- | --------------- | ----------- |
| [oas/talq-data-model-2-3-0.json](oas/talq-data-model-2-3-0.json)    | [2.3.0](#230) | 2021/03/01  |
| [oas/talq-api-gateway-2-3-0.json](oas/talq-api-gateway-2-3-0.json)  | [2.3.0](#230) | 2021/03/01  |
| [oas/talq-api-cms-2-3-0.json](oas/talq-api-cms-2-3-0.json)          | [2.3.0](#230) | 2021/03/01  |
|                                                                     |               |             |
| [oas/talq-data-model-2-2-0.json](oas/talq-data-model-2-2-0.json)    | [2.2.0](#220) | 2020/04/01  |
| [oas/talq-api-gateway-2-2-0.json](oas/talq-api-gateway-2-2-0.json)  | [2.2.0](#220) | 2020/04/01  |
| [oas/talq-api-cms-2-2-0.json](oas/talq-api-cms-2-2-0.json)          | [2.2.0](#220) | 2020/04/01  |
|                                                                     |               |             |
| [oas/talq-data-model-2-1-1.json](old-version.md)                    | 2.1.1         | 2019/10/01  |
| [oas/talq-api-gateway-2-1-1.json](old-version.md)                   | 2.1.1         | 2019/10/01  |
| [oas/talq-api-cms-2-1-1.json](old-version.md)                       | 2.1.1         | 2019/10/01  |

# How to get in touch with TALQ

Feel free to contact TALQ via the website [contact form](https://www.talq-consortium.org/4-contact/).

To stay up-to-date you can sign up for the TALQ Newsletter which is published approx. three times a year.

# Release notes

## 2.3.0

### Data model

- `LampType.lumenDepreciationCurve` description improved: missing decriptions for the components of the set have been added and the set is stated as ordered.
- `Group.purpose` unusable enum values are deprecated: `attributes` and `lampType`.
- `controlGearComFailure` deprecated at `fLampActuatorEvents`. A new `controlGearCommFailure` event has been added.
- Added `notInProperPosition` event type to `FMovementSensorEvents`
- Added `newCmsAttached` event attribute to `GatewayFunction`
- Deprecated `LampMonitorFunction.absolutLampPowerTooLow` event attribute
- Deprecated `LampMonitorFunction.absolutLampPowerTooLow` event attribute
- Added `absoluteLampPowerTooLow` event attribute `LampMonitorFunction`
- Added `absoluteLampPowerTooLow` event attribute `LampMonitorFunction`
- `LampType` has low/highLampVoltage attributes. The specs clearly mention that these **are NOT** `low/highSupplyVoltage`. But `low/highSupplyVoltage` events (and associated threshold) were missing in the Lamp Monitor function. The risk was that some members used the Lamp Type’s `low/highLampVoltage` as a `low/highSupplyVoltage` which should be in the `LampMonitorFunction`, together with the `supplyVoltage` attribute. Thus, in order to fix this issue the changes below have been introduced:
    + New configuration attribute `highSupplyVoltageThreshold` added to `LampMonitorFunction`
    + New configuration attribute `lowSupplyVoltageThreshold` added to `LampMonitorFunction`
    + New event attribute `supplyVoltageTooHigh` added to `LampMonitorFunction`
    + New event attribute `supplyVoltageTooLow` added to `LampMonitorFunction`
    + A warning added at the `LampType.lowLampVoltageThreshold` description: a new `LampMonitor.lowSupplyVoltageThreshold` attribute has been added.
    + A warning added at the `LampType.highLampVoltageThreshold` description: a new `LampMonitor.highSupplyVoltageThreshold` attribute has been added.
- New `PeriodicRecordingMode.content.attributeScope` attribute added to filter the attributes to be logged by scope.
- New `VendorRecordingMode.content.attributeScope` attribute added to filter the attributes to be logged by scope.
- New `DataCollectionService.attributeScopeSupported` attribute added to announce whether attributeScope is supported.
- New waste management profile for existing functions and attributes.
- New attributes `contentsType` and `contentsOtherType` added at `FillingLevelSensorFunction`
- New function `WasteContainerFunction` added.
- New function `pHSensorFunction` added.
- New function `WeightSensorFunction` added.
- New function `GasSensorFunction` added.
- New `ControlService.maxNumberOfPowerFactorThresholdDimmingCurveItems` attribute added.
- New `ControlService.maxNumberOfLumenDepreciationCurveItems` attribute added.
- New `LampType.powerFactorThresholdDimmingCurve` attribute added.
- `powerFactor` attributes' description improved by adding that it must be a positive number "The power factor can get values in the range from 0 to 1."
- Clarification added at the `BasicFunction` description: As stated at the Sepc, this function is mandatory for both Gateway and CMS sides for all physical devices, although the x-talq-profiles definition for Lighting will continue stating that it is optional for Gateway until the release 3.0.0 to keep backwards compatibility. This will be modified at 3.0.0.
- `ControlProgramOne.activePeriods` attribute clarified adding "_If no active period is defined within a control program, the program is active during the whole day._"
- `readOnly` description clarified.
- `gatewayAddress` and `cmsAddress` description defined. 
- Clarification added at the `CalendarRule` description: _A rule is composed of a day-based or a date-based condition and an action. The start of startDate and the end of endDate are assumed to be offset in the way that dayOffset is configured. Thus, given startDate=Day1 and endDate=Day2, when dayOffset=12 (noon-to-noon) the calendar rule becomes active at at 12:00 (noon) of Day1 and ends at noon of Day2+1._ Clarification added at the `CalendarRule.endDate` description: _Last date on which the rule is active. If not specified, the rule shall apply always after the startDate._
- Clarification added to the `OverrideCommand` description related to how to use it when an `ExternalControlEffect` is set inside a `DynamicControl`
- Example added to `AstroClockActivePeriod` related to offsets. 

### API for CMS:

None


### API for Gateway

- Description of the getLogReport extended and improved.

# 2.2.0

## Data model

- Added missing DynamicControl option to ControlService.
- Added missing AstroClockTimeControl option to ControlService.
- Add support for DC supply type to Lamp Monitor Function, new attribute supplyType and descriptions modification.
- New function SolarBatteryChargerFunction.
- New function BatteryManagementSystemFunction.
- New function TrafficCounterFunction.
- New function LocationSensorFunction.
- New function AccelerometerFunction.
- New function OrientationFunction.
- Fixed ResourceReference description, it not only refers to device or groups, but to other entities such as calendars.
- New function FluidLevelSensorFunction.
- Fixed required attributes for entity `Orientation`.
- Changes at TALQErrorMessage entity: list of recommended error keys and schema modification in order to refer sources of the error.
- Added ramp rates to manual and automatic control: CommandBase and ControlEffect entities affected.
- Clarification added when several override commands are received at the same actuator.
- Add new x-talq-profiles extension to all the attributes & functions at the DM file.
- Added supportedProfiles array inside configuration service announcement.
- Added states property array of State in the CommandDesc entity.
- Added devicesPaginationSupported attribute to Configuration Service
- Clarify Attribute.timestamp at the DM.
- Fix AstroAndSensorActivePeriod definition: onLevel and offLevel are missing
- Add programSecondsSupported attribute to ControlService
- BasicFunction.hardwareUpdating renamed to BasicFunction.hardwareUpdated
- Add invalidLampType event type. Also event attribute added to LampActuator and LampMonitor.
- Add mandatoriness tags for all entities at DM OAS file.


## API for CMS:

- Added pagination to getDevices
- Add mandatoriness tags for all paths.

## API for Gateway

- The getLoggerConfig operation was incorrectly located under /logger-configs/ instead of /logger-configs/{loggerConfig} path.
- Added pagination to getDevices
- Add mandatoriness tags for all paths.
- Added asynchronous behaviour to assignCommand by adding the 202-Accepted response
- Added getGroup and getLoggerConfig operations to the Gateway API
 

# Semantic versioning

TCT uses the [Semantic versioning](https://semver.org/spec/v2.0.0.html) guide:

Given a version number MAJOR.MINOR.PATCH, increment the:

- MAJOR version when you make incompatible API changes,
- MINOR version when you add functionality in a backwards-compatible manner, and
- PATCH version when you make backwards-compatible bug fixes.

Additional labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format.

The TCT software and the OAS files use the same version number. To avoid confusion the PATCH version only will be incremented when the change is in the OAS files. If the change is only because of software bug fixes, an update number label will be added to the release number. 


