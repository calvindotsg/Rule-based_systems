# Rule-based systems
Rule-based decision making systems notes - IBM Operation decision manager rule engine and Object-oriented Java

## On job experience
Temporary Java software engineer in multi-national corporation developing next generation goverment project
- Paired with a senior colleague with tasks within development and testing phases of agile software development lifecycle, as an on-job learning experience
- Tasked with identifying and troubleshooting issues within backend rule engine and object-oriented Java component, with collaboration among hybrid team in resolving complex issues
- Utilised up to date information technology tools used to assist development within the context of a government contracted Information technology project. Namely: GitLab, mySQL, IBM Operational Decision Manager rule engine with Eclipse, Jira, MobaXterm

## Executive summary
Within the semester break of late May to early September 2021 after Year 2 of my undergraduate studies, I found temporary employment as Java Software engineer, with the scope of using IBM Operational Decision Manager for rule-based decision making for the company’s current project in developing next-generation government system. My job experience greatly provided much needed real world context within the ever evolving job industry as well as up to date information technology tools used to assist development. I seek to utilise this job experience gathered to value add to this project. 

## Notes
Rule project: stores business logic of application, allows dev to manage, build, and debug the items that comprise the business logic of your application

Contains: rule artifacts, business object model (BOM), vocabulary, and reference to the execution object model (XOM)

XOM - Execution Object Model: model used to execute the rules

BOM - Business Object Model: basis of the vocabulary that is used in business rules.

BAL - Business Action Language
- provides a simple if-then syntax that you use with a vocabulary to write business rules
- defines the syntax and provides constructs for expressing business rule conditions and actions, and the vocabulary defines the terms that you use in the business rules.

Action rules
- express a set of conditions followed by the actions to take if the conditions are true
- state business policies in a predefined business vocabulary that a computer can interpret, using BAL constructs and operators


Decision tables
- Presents logic as a table, where each row corresponds to an action rule
- useful for large sets of action rules with identical conditions


Operational Decision Manager combines decision making and change detection tools to provide a business rule management system that is easy to evolve, trace, audit, and test.

Why use decision management
- Business events and Business Rule Management Systems (BRMS) are used together to enable intelligent and responsive decision automation
- Detects and reacts to data patterns as they occur within a specified time period, thereafter provides appropriate automated decision response to transactional and process-oriented business systems
- Enables business users to manage decisions and make changes in a very short timeframe, increasing enterprise responsiveness to unforeseen events, as well as shortening response times as a result of higher levels of automation.

2 components

Decision server: 
- Rule design and event design within Eclipse with extension. 
- To automate response to highly variable decisions based on context of process, transaction or interaction.

Decision centre: 
- Rule management (decisions and events) based on organisational knowledge and best practices
- Suitable for less tech-savvy users, with control over rule specification, creation, testing and deployment of business logic

Business policy vs rules: if ... then ...

Policy: Typically found inside application code, in the form of if-then statements, although they may also be stored elsewhere for documentation purposes, such as in procedural manuals and other documents.

Rules: The business logic can be packaged and called from the application code as a business rule application. Therefore, changes to the business policy do not require changes to the application or process code.

Ruleflows: provides a way to set order which rule engine processes rules
- specifies how tasks are chained together: how, when, and under what conditions they are executed
- consists of the following elements: one start node, at least one end nodes, tasks, or transitions
- Fastpath mode: in order (sequential) with some optimization at compile time

Action task: contains rule action statements to be executed, using BAL but can only use action phrases associated with ruleset parameters

Subflow task: references another ruleflow or itself to be executed (avoid infinite loops)

Transitions: 
- connects task in rule flow and define sequence between tasks
- conditions determines if transition is part of execution flow, defined using BAL
- required when multiple transition origin from a task
- else condition applies only single among multiple transitions, specifies path when other conditions are not met

Branches
- a node that organizes conditional transitions

Ruleset - collection of one or more rules. Subset of RuleApp, containing collection of one or more rulesets

Parameters:
- transfer information between ruleflow tasks
- determine which path to follow through the transitions
- transfer information between the ruleflow and the application, where application obtains the results of ruleflow processing through ruleset parameter

Operation: 
app > (parses input parameters) > rule set > (parses output parameters) > app

3 directions between ruleset and application: 
- INPUT: Provided as input on execution
- OUTPUT: Parameter value set by execution of ruleset and provided as output from ruleset at execution completion
- INPUT_OUTPUT: Provided as input on execution, value modified by ruleset and provided as output at execution completion 

Ruleset variables: are internal to a ruleset and provide a way to exchange data between rules, functions, and tasks

Variables:
- defines a value of a specified type and verbalization
- used in business rules (need to verbalise), as input/output parameters in decision operations, pass data between tasks in rule flow
- Variable set: groups rule set variables


Events
- An event is an electronic signal indicating that a change in the state of the business has occurred.
- Event rules help detect, and respond to, event patterns among like or related events, missing events and aggregate events. Event rules also relate the pattern detection to a context and apply a dimension of time to the pattern. 
- By using predefined logic that describes how business systems are to interact, the event runtime can notify those systems in real time so that they take the appropriate action.
- Works with existing systems via Business event processing layer: Makes use of existing functions and communicates significant events to other system that require information to respond to critical events
- Able to discern pattern from seemingly unrelated events from multiple sources, then coordinate execution of responses

## References
- IBM OBM Tutorial - Getting started with business rules: https://www.ibm.com/docs/en/odm/8.10?topic=tutorials-getting-started-business-rules
- IBM OBM Documentation - What is Operational Decision Manager: https://www.ibm.com/docs/en/odm/8.0.1?topic=family-what-is-operational-decision-manager
- IBM OBM Documentation - Overview: BOM and execution object model (XOM): https://www.ibm.com/docs/en/odm/8.10?topic=models-overview-bom-execution-object-model-xom
