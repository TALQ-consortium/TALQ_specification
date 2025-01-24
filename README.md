![TALQ Consortium](img/talq_logo.png)


# TALQ - The Smart City Protocol

The [TALQ Consortium](https://www.talq-consortium.org/) has developed the Smart City Protocol, a globally accepted interface standard for smart city device networks. This software protocol is a specification for information exchange, suitable for implementation in various products and systems. In this way interoperability between Central Management Software (CMS) and Outdoor Device Networks (ODN) from different vendors is enabled, such that a single CMS can control different ODNs in different parts of a city or region.

TALQ provides answers to the main challenges of building really smart cities including increasing safety and comfort for inhabitants, reducing energy consumption and CO<sub>2</sub> emissions worldwide, raising cost efficiency for operators managing a smart city.

Driven originally by smart street lighting vendors, TALQ is now an open industry consortium addressing the entire smart city environment allowing manufacturers of smart city applications to join as members and certify their products as TALQ-compliant. Other stakeholders such as cities, municipalities, utilities, consultants, universities and many others can join the consortium as Partners Let’s TALQ !

# Why to certify your product
TALQ Certification verifies that a product has implemented the TALQ protocol according to the TALQ specification. Read the [CERTIFICATION.md file](CERTIFICATION.md).

> **Important Notice**: TALQ Trademark Usage
>
> Please note that according to our [LICENSE](LICENSE), only TALQ members are authorized to use the TALQ trademarks (logo and name). 

# TALQ 2: A RESTful API


The TALQ protocol has been defined with the [OpenAPI Specification (OAS), formerly Swagger](https://github.com/OAI/OpenAPI-Specification), the standard de facto for defining RESTful APIs. An OpenAPI definition can then be used by documentation generation tools to display the API, code generation tools to generate servers and clients in various programming languages, testing tools, and many other use cases. Thanks to this specification manufacturers can dramatically shorten the development times and increase code quality when aiming to become interoperable.

The TALQ Specification is splitted in four files, named with the [Semantic versioning](#semantic-versioning):

- [Approved TALQ Specification](20250124-TALQ-Specification-Approved-Version-2.6.2.pdf): This document helps to understand the technical specifications of the TALQ Smart City Protocol.
- [Data model OAS file](oas/talq-data-model-2-6-2-online.json): The data model defines all TALQ objects used in the protocol such as Devices, Calendars, Control Programs, etc.
- [API for Outdoor Device Network (Gateway) OAS file](oas/talq-api-gateway-2-6-2-online.json): It defines the Gateway RESTful API with each resource, methods, parameters, etc.
- [API for Central Management Software (CMS) OAS file](oas/talq-api-cms-2-6-2-online.json): It defines the CMS RESTful API with each resource, methods, parameters, etc.

## Versions

All the released versions of the TALQ Specification are in the table below: 

| Name                                                                | Version       | Date        | 
| ------------------------------------------------------------------- | --------------| ----------- |
| [oas/talq-data-model-2-6-2.json](oas/talq-data-model-2-6-2-online.json)    | [2.6.2](#262) | 2025/01/24  |
| [oas/talq-api-gateway-2-6-2.json](oas/talq-api-gateway-2-6-2-online.json)  | [2.6.2](#262) | 2025/01/24  |
| [oas/talq-api-cms-2-6-2.json](oas/talq-api-cms-2-6-2.json-online)          | [2.6.2](#262) | 2025/01/24  |
|                                                                     |               |             |
| [oas/talq-data-model-2-6-1.json](oas/talq-data-model-2-6-1-online.json)    | [2.6.1](#261) | 2024/06/27  |
| [oas/talq-api-gateway-2-6-1.json](oas/talq-api-gateway-2-6-1-online.json)  | [2.6.1](#261) | 2024/06/27  |
| [oas/talq-api-cms-2-6-1.json](oas/talq-api-cms-2-6-1.json-online)          | [2.6.1](#261) | 2024/06/27  |
|                                                                     |               |             |
| [oas/talq-data-model-2-6-0.json](old-version.md)                    | [2.6.0](#260) | 2024/01/17  |
| [oas/talq-api-gateway-2-6-0.json](old-version.md)                   | [2.6.0](#260) | 2024/01/17  |
| [oas/talq-api-cms-2-6-0.json](old-version.md)                       | [2.6.0](#260) | 2024/01/17  |
|                                                                     |               |             |
| [oas/talq-data-model-2-5-1.json](old-version.md)                    | [2.5.1](#251) | 2023/06/02  |
| [oas/talq-api-gateway-2-5-1.json](old-version.md)                   | [2.5.1](#251) | 2023/06/02  |
| [oas/talq-api-cms-2-5-1.json](old-version.md)                       | [2.5.1](#251) | 2023/06/02  |
|                                                                     |               |             |
| [oas/talq-data-model-2-5-0.json](old-version.md)                    | [2.5.0](#250) | 2023/01/05  |
| [oas/talq-api-gateway-2-5-0.json](old-version.md)                   | [2.5.0](#250) | 2023/01/05  |
| [oas/talq-api-cms-2-5-0.json](old-version.md)                       | [2.5.0](#250) | 2023/01/05  |
|                                                                     |               |             |
| [oas/talq-data-model-2-4-1.json](old-version.md)                    | [2.4.1](#241) | 2022/04/08  |
| [oas/talq-api-gateway-2-4-1.json](old-version.md)                   | [2.4.1](#241) | 2022/04/08  |
| [oas/talq-api-cms-2-4-1.json](old-version.md)                       | [2.4.1](#241) | 2022/04/08  |
|                                                                     |               |             |
| [oas/talq-data-model-2-4-0.json](old-version.md)                    | [2.4.0](#240) | 2021/12/15  |
| [oas/talq-api-gateway-2-4-0.json](old-version.md)                   | [2.4.0](#240) | 2021/12/15  |
| [oas/talq-api-cms-2-4-0.json](old-version.md)                       | [2.4.0](#240) | 2021/12/15  |
|                                                                     |               |             |
| [oas/talq-data-model-2-3-0.json](old-version.md)                    | [2.3.0](#230) | 2021/03/01  |
| [oas/talq-api-gateway-2-3-0.json](old-version.md)                   | [2.3.0](#230) | 2021/03/01  |
| [oas/talq-api-cms-2-3-0.json](old-version.md)                       | [2.3.0](#230) | 2021/03/01  |
|                                                                     |               |             |
| [oas/talq-data-model-2-2-0.json](old-version.md)                    | [2.2.0](#220) | 2020/04/01  |
| [oas/talq-api-gateway-2-2-0.json](old-version.md)                   | [2.2.0](#220) | 2020/04/01  |
| [oas/talq-api-cms-2-2-0.json](old-version.md)                       | [2.2.0](#220) | 2020/04/01  |
|                                                                     |               |             |
| [oas/talq-data-model-2-1-1.json](old-version.md)                    | 2.1.1         | 2019/10/01  |
| [oas/talq-api-gateway-2-1-1.json](old-version.md)                   | 2.1.1         | 2019/10/01  |
| [oas/talq-api-cms-2-1-1.json](old-version.md)                       | 2.1.1         | 2019/10/01  |

# How to get in touch with TALQ

Feel free to contact TALQ via the website [contact form](https://www.talq-consortium.org/4-contact/).

To stay up-to-date you can sign up for the TALQ Newsletter which is published approx. three times a year.

# Release notes

# Release notes

## 2.6.2
### At Data model

- Add `genericError` key in `TALQErrorMessage`.
- Clarify the use of `entity` in an `AssignCommand`.

### At API for CMS:

- Add `application/json` to all count methods.


### At API for Gateway

- Add `application/json` to all count methods.
- Clarify the `getLogReport` description.


## 2.6.1

### At Data model

The OAS data model is updated to clarify some usages:

- Adding in the `DynamicControl` description: _If no period is defined, the dynamic control is applied for the full day._
- Adding in the `DynamicControl.period` description: _If startTime is equal to endTime, it means the full day period is active. This full-day period can be from noon to noon, or midnight to midnight, based on the dayOffset._
- Adding in the `AbsoluteActivePeriod` description: _If startTime is equal to endTime, it means the full day period is active. This full-day period can be from noon to noon, or midnight to midnight, based on the dayOffset._
- Adding in the `ResourceReference.address`  description: _Both, Gateway and CMS, must support all address modalities._
- Adding in the `ccDate` description: _The end day must be higher than the start day._
- Adding in the `ccDay` description: _The end weekday must be higher than the start weekday._


### At API for CMS:

- The parameters `functionId` and `attributeName` definitions were missing in GET `/devices/{deviceAddress}/{functionId}/{attributeName}`


### At API for Gateway


## 2.6.0

### At Data model

- Added `CabinetConfigurationFunction`.
- Added `CabinetMonitorFunction`.
- The `SegmentMonitor.cabinetDoorOpen` and `SegmentMonitor.leakageDetected` event properties deprecated.
- Add `SegmentMonitor.actualState`.
- Clarify the `AssignCommand` description for de-associate.
- Add `ValueActivePeriod`, used by `ControlProgram` and `RecordingMode`.
- Add `activePeriods` to `RecordingMode`.
- Add `recordingActivePeriodsSupported` and `supportedTypes` to `DataCollectService`.
- Add `cmsRefId` in `AssignCommand`.
- Add `CCTColorState`.
- Add `LevelAndCCTColorState`.
- Add `LevelAndRGBWAFColorState`.
- Add `LevelAndXYColorState`.
- Add `RGBWAFColorState`.
- Add `XYColorState`.
- Add `AttributeCCTColorState`.
- Add `AttributeLevelAndCCTColorState`.
- Add `AttributeLevelAndRGBWAFColorState`.
- Add `AttributeLevelAndXYColorState`.
- Add `AttributeRGBWAFColorState`.
- Add `AttributeXYColorState`.
- Fixed: "kg" unit replaced by "Kilograms".
- Added "Watts" unit to AtributeDesc to be aligned.
- Added "SquareMeters" unit to AtributeDesc to be aligned.
- Fixed: "m2" unit replaced by "SquareMeters".
- Add `LampMonitorFunction.actuatorReference` attribute.
- Add `SegmentMonitorFunction.actuatorReference` attribute.
- Add `ElectricalMeterFunction.actuatorReference` attribute.

### At API for CMS:

- Added getLampTypes method to CMS API.
- Addded new error response for semantic errors: 422-Unprocessable Entity
- Addded new request parameters: `talqRequestId` and `talqOriginRequestId`.

### At API for Gateway

- Added getLampTypes method to Gateway API.
- Added getAssignCommands method to Gateway API.
- Added new error response for semantic errors: 422-Unprocessable Entity.
- Added new asynchronous response for POST override-commands: 202-Accepted.
- The asynchronous 202-Accepted response was added for POST, PATCH, PUT and DELETE requests on /devices, /devices/{deviceAddress}, /devices/{deviceAddress}/{functionId} and /devices/{deviceAddress}/{functionId}/{attributeName}.
- Addded new request parameters: `talqRequestId` and `talqOriginRequestId`. 

## 2.5.1

### At Data model

- `BasicFunction.cabinetDoorOpen` was deprecated by `SegmentMonitorFunction.cabinetDoorOpen` with version 2.4.0, but it was described the opposite in the Specs. 
- The `whiteList` and `blackList` fields of the `EventRecordingMode.sourceEvents` field must be handled the same as`LoggerConfig` `sourceAddressses` field.
- The `DriverType.address` must be mandatory for all profiles.
- `TrafficCounter` function was mandatory for lighting asset management profile for CMS & GW when it should be optional.
- `Control Service` should not be mandatory for `Asset Management Profile`
- `LuminaireType.corrosionClass`: Fix the enum list `C1` instead of `"Enum:C1"`
- `LuminaireType.aerodinamicResistance` deprecated because of a typo in the name, `LuminaireType.aerodynamicResistance` must be used instead
- `DriverType.aerodinamicResistance` deprecated because of a typo in the name, `LuminaireType.aerodynamicResistance` must be used instead
- `LuminaireType.materialLlightCover` deprecated because of a typo in the name, `materialLightCover` must be used instead
- Added "x-talq-unit" to the `LuminaireType`'s properties: `lowCurrentThreshold`, `highCurrentThreshold`, `address`, `name`, `gtin`, `manufacturerName`, `productFamily`, `model`, `hardwareVersion`, `lightSourceType`, `lightDistributionType`, `lcsRating`, `lightPhotometry`, `driverReplaceable`, `lightSourceReplaceable`, `materialEnclosure`, `materialLlightCover`, `materialLightCover`, `lightCoverShape`, `socketTypes`, `controlVoltMax`, `controlVoltMin`, `minLightOutput`, `virtualLightOutput`, `daliLedLinear`, `warmUpTime`, `maxOperatingHours`, `powerLightGradient`, `lampPowerTolerance`, `lampPowerHighThreshold`, `lampPowerLowThreshold`, `powerFactorThreshold`, `lumenDepreciationCurve`, `cloType`, `powerFactorThresholdDimmingCurve`, `lightSourceLedNumber`, `lightSourceGtin`, `lightSourceManufacturerName`, `lightSourceProductFamily`, `lightSourceModel`, `electricalIsolationClass`.
- Added "x-talq-unit" to the `BracketType`'s properties: `address`, `name`, `gtin`, `manufacturerName`, `productFamily`, `model`, `mountingOptions`. 
- Added "x-talq-unit" to the `DriverType`'s properties: `address`, `name`, `controlElectricalInterfaceTypes`, `controlInterfaceProtocolTypes`, `programInterfaceType`, `gtin`, `manufacturerName`, `productFamily`, `model`, `hardwareVersion`, `controlOutputType`, `dimmingOutputType`, `dimmingOutputs`.
- Added "x-talq-unit" to the `ControllerType`'s propertoes: `address`, `name`, `gtin`, `manufacturerName`, `productFamily`, `model`, `mechanicalInterfaces`, `electricalInterfaces`, `protocols`.
- Fixing some descriptions of clientAddress, where it is the address of the Gateway.
- Added `powerConsumption` to `LuminaireType`. 
- Clarify `DynamicControl.period` definition.
- Clarify `AbsoluteActivePeriod` definition regarding where to split a period that covers two days.
- Clarify `SensorActivePeriod` and `AstroAndSensorActivePeriod` with `onLevel` and `offLevel` definitions when using a Photocell as sensor.


### At API for CMS

None

### At API for Gateway

None

## 2.5.0

### Data model

- Added **LuminaireType**
- Added **BracketType**
- Added **DriverType**
- Added **ControllerType**
- Added **LuminaireAssetFunction**
- Added **DriverAssetFunction**
- Added **ControllerAssetFunction**
- Added `LampMonitor.dimmingFailure` status attribute; Added `dimmingFailure` event type.
- Fixed `totalReactiveEnergy` and `totalApparentEnergy` attributes descriptions (units were wrong). 
- Added `x-talq-unit` extension to all attributes with the TALQ Units.
- `LampType` description improved. 
- `EventLogData` description added.
- Added `gatewayRetryPeriod` (deprecating `retryPeriod`), `cmsRetryPeriod`, `gatewayNumberOfRetries` and `cmsNumberOfRetries` attributes in `GatewayFunction`.
- Fixed descriptions at `ElectricalMeterFunction`'s attributes: `phase1VoltageTooHigh`, `phase1VoltageTooLow`, `phase2VoltageTooHigh`, `phase2VoltageTooLow`, `phase3VoltageTooHigh` and `phase3VoltageTooLow`.
- Clarified `cmsRefId` description.

### At API for CMS:

- Added resource luminaire-types with methods:
    + **getLuminaireTypes**: Get the list of all luminaire types
    + **addLuminaireTypes**: Add a list of new luminaire types
    + **updateLuminaireTypes**: Update a list of existing luminaire types
    + **getLuminaireTypesCount**: Get the count of luminaire types
    + **getLuminaireType**: Get a single luminaireType by address
    + **updateLuminaireType**: Update a single luminaire type by id
    + **deleteLuminaireType**: Delete a single luminaire type
- Added resource bracket-types with methods:
    + **getLuminaireTypes**: Get the list of all bracket types
    + **addLuminaireTypes**: Add a list of new bracket types
    + **updateLuminaireTypes**: Update a list of existing bracket types
    + **getLuminaireTypesCount**: Get the count of bracket types
    + **getLuminaireType**: Get a single bracketType by address
    + **updateLuminaireType**: Update a single bracket type by id
    + **deleteLuminaireType**: Delete a single bracket type
- Added resource driver-types with methods:
    + **getLuminaireTypes**: Get the list of all driver types
    + **addLuminaireTypes**: Add a list of new driver types
    + **updateLuminaireTypes**: Update a list of existing driver types
    + **getLuminaireTypesCount**: Get the count of driver types
    + **getLuminaireType**: Get a single driverType by address
    + **updateLuminaireType**: Update a single driver type by id
    + **deleteLuminaireType**: Delete a single driver type
- Added resource controller-types with methods:
    + **getLuminaireTypes**: Get the list of all controller types
    + **addLuminaireTypes**: Add a list of new controller types
    + **updateLuminaireTypes**: Update a list of existing controller types
    + **getLuminaireTypesCount**: Get the count of controller types
    + **getLuminaireType**: Get a single controllerType by address
    + **updateLuminaireType**: Update a single controller type by id
    + **deleteLuminaireType**: Delete a single controller type
- Clarification added a the `addDeviceClasses` method: device class announcement.

### At API for Gateway

- Added resource luminaire-types with methods:
    + **getLuminaireTypes**: Get the list of all luminaire types
    + **addLuminaireTypes**: Add a list of new luminaire types
    + **updateLuminaireTypes**: Update a list of existing luminaire types
    + **getLuminaireTypesCount**: Get the count of luminaire types
    + **getLuminaireType**: Get a single luminaireType by address
    + **updateLuminaireType**: Update a single luminaire type by id
    + **deleteLuminaireType**: Delete a single luminaire type
- Added resource bracket-types with methods:
    + **getLuminaireTypes**: Get the list of all bracket types
    + **addLuminaireTypes**: Add a list of new bracket types
    + **updateLuminaireTypes**: Update a list of existing bracket types
    + **getLuminaireTypesCount**: Get the count of bracket types
    + **getLuminaireType**: Get a single bracketType by address
    + **updateLuminaireType**: Update a single bracket type by id
    + **deleteLuminaireType**: Delete a single bracket type
- Added resource driver-types with methods:
    + **getLuminaireTypes**: Get the list of all driver types
    + **addLuminaireTypes**: Add a list of new driver types
    + **updateLuminaireTypes**: Update a list of existing driver types
    + **getLuminaireTypesCount**: Get the count of driver types
    + **getLuminaireType**: Get a single driverType by address
    + **updateLuminaireType**: Update a single driver type by id
    + **deleteLuminaireType**: Delete a single driver type
- Added resource controller-types with methods:
    + **getLuminaireTypes**: Get the list of all controller types
    + **addLuminaireTypes**: Add a list of new controller types
    + **updateLuminaireTypes**: Update a list of existing controller types
    + **getLuminaireTypesCount**: Get the count of controller types
    + **getLuminaireType**: Get a single controllerType by address
    + **updateLuminaireType**: Update a single controller type by id
    + **deleteLuminaireType**: Delete a single controller type

## 2.4.1

### Data model

- Clarification added to VendorRecordingMode.content property; difference in content between no value or empty array as value.
- Clarification for read-only attributes when sent by the CMS. 
- All `startTime` and `endTime` properties related to entities in a control program must follow the hh:mm:ss format.
- Clarification added to LoggerConfig.sourceAddresses for different combinations of white and black lists. 
- VendorAttributeDesc.type enum list completed with new types introduced in 2.4.0
- The `VendorAttributeDesc` `type` and `scope` properties are made required since the CMS is not able to dynamically create the appropriate UI without this information.

### At API for CMS:

- Added a 409-Conflict status response to the `post` request in `services`, `device-classes`, `devices` and `lamp-types` resources.


### At API for Gateway

- Added a 409-Conflict status response to the `post` request in `devices`, `control-programs`, `calendars`, `lamp-types`, `logger-configs`  and `groups` resources.

## 2.4.0

### Data model

- `GenericActuator.feedbackCommand` and `LampActuatorActuator.feedbackLightCommand` descriptions improved.
- New `SimpleActuatorFunction` added: A function that allows the new profiles to use actuators without the complexity of calendars.
- New `TimeFunction` added, deprecating the related attributes at `BasicFunction`
- New attributes added to `BasicFunction`: `commandConfirmation`, `reboot`, `factoryReset`, `configurationReset` and `operatingHours`. 
- Deprecated temperature related attributes from functions `LampMonitor`, `SolarBatterySensor` and `BatteryManagementSystem`. The attributes shall be replaced by the `TemperatureSensorFunction`.
- New attributes added to `TemperatureSensorFunction`: `applicationType`, `minMeasuredTemperature`, `maxMeasuredTemperature` and `measuredTemperatureSince`.
- New attributes added to `LocationSensorFunction`: `uncertainty`, `compassDirection`, `velocity`, `speed` and `applicationType`. The `velocity` attribute's type is AttributeVelocity which contains several velocity componentes such as horizontal speed, bearing, vertical speed, direction and velocity uncertainty.
- New `applicationType` attribute added to all functions except those that can only be instantiated once in a device: `Basic`, `Gateway` and `Time`.
- All `xxxSince` attributes' descriptions have been clarified.
- Added `smartParking` and `smartTraffic` profiles to all functions, attributes and services. 
- Added `supplyLoss` to `ElectricalMeter` function.
- New `SegmentMonitorFunction` added, deprecating `BasicFunction.cabinetDoorOpen` attribute.
- New `NoiseMonitoringSensorFunction` added.
- New `AtmosphericSensorFunction` added.
- New `WindSensorFunction` added.
- New `PrecipitationSensorFunction` added.
- New `SkySensorFunction` added.
- New `GullySensorFunction` added.
- New `WaterFlowSensorFunction` added.
- New `WaterQualitySensorFunction` added.
- `ParticulateMatterSensorFunction` extended with 24 h averages.
- `GasSensorFunction` extended with 1h and 8h averages.
- `TrafficCounterFunction` extended with averages, min, max and traffic direction.
- New `TextDisplayActuatorFunction` added.
- New `ParkingSensorFunction` added.
- New `ParkingCameraSensorFunction` added.
- Clarification added to `Attribute.timestamp`: the attribute timestamp is a key protocol data and so a mandatory requirement to certify a product (mainly a GW).

### API for CMS:

None

### API for Gateway

None

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


