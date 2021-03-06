This profile defines a representation of a Personal Health Notes document for a patient in an Australian healthcare context. 

##### **Usage Scenarios**
The following are the usage scenarios expected:
* An individual or their authorised representative authors a personal health notes document to be exchanged with the My Health Record system

##### **Each Composition SHALL have**
* a profile assertion to this profile
* a single section
* a section title
* a section code
* a section text
* zero emptyReason

#####  **Must Support**
In the context of this profile [Must Support](http://hl7.org/fhir/STU3/conformance-rules.html#mustSupport) SHALL be interpreted as follows.
* The system SHALL be able to store and retrieve the following elements:
    * type
    * title
    * section
    * section.title
    * section.code
    * section.text

* The system SHALL be able to [PLACEHOLDER-TEXT](https://jira.digitalhealth.gov.au/browse/CIFMM-2217):
    * section.emptyReason

##### **Profile-specific implementation guidance**
* For the usage scenarios for this profile it is required that the composition include only the specified top-level section; additional sections to handle local content not covered by the primary design can be included as a child section if necessary.
* Where additional content beyond that flagged with must support is provided it:
    * shall not qualify or negate content described by this profile as must support
    * shall be clinically safe for receivers of the document to ignore the non-narrative additions when interpreting the existing content

##### **Examples**

[Personal Health Notes - diabetes note](Composition-composition-phn-example1.html)

[Personal Health Notes - exercise note](Composition-composition-phn-example2.html)