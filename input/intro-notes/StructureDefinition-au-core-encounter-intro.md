### Usage scenarios

The following are supported usage scenarios for this profile:

- Query for a specific patient encounter
- Query for all patient encounters
- Record or update a patient encounter


### Comparison with other national and international IGs

A resource conforming to this profile:
- **MAY** be conformant to [US Core Encounter](http://hl7.org/fhir/us/core/StructureDefinition/us-core-encounter) if Encounter.type is supplied

No equivalent International Patient Access or International Patient Summary profile.

Conformance in reverse is not guaranteed, i.e. a resource conforming to [US Core](http://hl7.org/fhir/us/core) **MAY NOT** conform to AU Core.


### Profile specific implementation guidance
- The Encounter resource can represent a reason as a code with `Encounter.reasonCode`, or a reference with `Encounter.reasonReference` to a Condition or other resource.
  - Although both are marked as *Must Support*, responders are not required to support both a code and a reference, but they **SHALL** support *at least one* of these elements
  - A requester **SHALL** support both elements