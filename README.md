# Study SysML2 Using Epsilon

This repo studies SysML2 using the Eclipse Epsilon. Since SysML contributors published ECORE model of SysML2, this allows the applications of Model-Driven Enigneering more easily. We look at the usage of Epsilon for creating and querying SysML models using Epsilon languages and supporting tools within Eclispe workbence. 

Please note that SysML2 introduced a textual language and we are subject to look at the language in the next step. However, this study start with SysML2 metamodel and SysML models created with Flexmi files.  


# Important SysML textual language design notes

The design of SysML textual language uses the following strategy.

```
High-level SysML2 Element defined by XTEXT
```
DefinitionElement returns SysML::Element :
	  Package
	| Comment
	| TextualRepresentation
	| AnnotatingFeature
	| Dependency	  
	| AttributeDefinition
	| EnumerationDefinition
	| OccurrenceDefinition
	| IndividualDefinition
	| ItemDefinition
	| PartDefinition
	| ConnectionDefinition
	| InterfaceDefinition
	| AllocationDefinition
	| PortDefinition
	| ActionDefinition
	| CalculationDefinition
	| StateDefinition
	| ConstraintDefinition
	| RequirementDefinition
	| ConcernDefinition
	| CaseDefinition
	| AnalysisCaseDefinition
	| VerificationCaseDefinition
	| UseCaseDefinition
	| ViewDefinition
	| ViewpointDefinition
	| RenderingDefinition
;
```

High-level SysML2 Usage defined by XTEXT
```
Parameter returns SysML::Usage :
      {SysML::ReferenceUsage} ( direction = FeatureDirection )? ( ParameterDeclaration | ReferenceUsageKeyword ParameterDeclaration?)
    | {SysML::AttributeUsage} ( direction = FeatureDirection )? AttributeUsageKeyword ParameterDeclaration?
    | {SysML::OccurrenceUsage} ( direction = FeatureDirection )? OccurrenceUsageKeyword ParameterDeclaration?
    | {SysML::ItemUsage} ( direction = FeatureDirection )? ItemUsageKeyword ParameterDeclaration?
    | {SysML::PartUsage} ( direction = FeatureDirection )? PartUsageKeyword ParameterDeclaration?
    | {SysML::ViewUsage} ( direction = FeatureDirection )? ViewUsageKeyword ParameterDeclaration?
    | {SysML::RenderingUsage} ( direction = FeatureDirection )? RenderingUsageKeyword ParameterDeclaration?
    | {SysML::ActionUsage} ( direction = FeatureDirection )? ActionUsageKeyword ParameterDeclaration?
    | {SysML::CalculationUsage} ( direction = FeatureDirection )? CalculationUsageKeyword ParameterDeclaration?
    | {SysML::StateUsage} ( direction = FeatureDirection )? StateUsageKeyword ParameterDeclaration?
    | {SysML::ConstraintUsage} ( direction = FeatureDirection )? ConstraintUsageKeyword ParameterDeclaration?
    | {SysML::RequirementUsage} ( direction = FeatureDirection )? RequirementUsageKeyword ParameterDeclaration?
    | {SysML::ConcernUsage} ( direction = FeatureDirection )? ConcernUsageKeyword ParameterDeclaration?
    | {SysML::AnalysisCaseUsage} ( direction = FeatureDirection )? AnalysisCaseUsageKeyword ParameterDeclaration?
    | {SysML::VerificationCaseUsage} ( direction = FeatureDirection )? VerificationCaseUsageKeyword ParameterDeclaration?
    | {SysML::UseCaseUsage} ( direction = FeatureDirection )? UseCaseUsageKeyword ParameterDeclaration?
    | {SysML::ViewpointUsage} ( direction = FeatureDirection )? ViewpointUsageKeyword ParameterDeclaration?
;
```
```
