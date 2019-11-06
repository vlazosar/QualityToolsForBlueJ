

# Quality Tools for BlueJ (QT4BJ) - Development Conventions

This document describes intended and preferred conventions for development and maintenance of the  _Quality Tools for BlueJ_  software product.

-   [Project File Hierarchy](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#Project-File-Hierarchy)
-   [Agile Principles](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#Agile-Principles)
-   [Coding Convention Guide](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#Coding-Convention-Guide)
-   [Build Environment](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#Build-Environment)

----------

## [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#gradle-file-hierarchy)Project File Hierarchy

```
.
├── .github/ISSUE_TEMPLATE  	# Templates for user stories and bug reports
├── docs                    	# Documentation files
├── gradle/wrapper		# Gradle wrapper script
├── src                     	# Source files
├── .gitignore
├── AntGradleComparison.md	# Comparison report of Ant vs Gradle build tools
├── DevelopmentConventions.md	# Development and maintenance conventions document
├── IvyAntGradleMavenComparisonReport.md
				# Comparison report of Ant vs Gradle vs Ivy build tools
├── RequirementsSourceInfo.md	# Guide for creating similar project development goals
├── Vision.md			# States the project goal and stakeholder types
├── build.gradle		# Gradle files
├── gradlew
├── gradlew.bat
├── settings.gradle
├── toolsForIntegration.md	# List of code analysis tools to be implemented and descriptions
├── LICENSE
└── README.md
```
**Github Issue Templates**
```
.
├── ...
├── .github
│   ├──ISSUE_TEMPLATE  		# Templates for user stories and bug reports
│      ├── bug_report.md     	 # Bug report template
│      ├── user-story.md      	  # User story template
│   └── ...                 	# etc.
└── ...
```
**Documentation**
```
.
├── ...
├── docs                    	# Documentation files
│   ├── README.md            	 # Read me explaining project objective
│   ├── _config.yml           	  # Sets theme jekyll-theme-tactile
│   └── ...                 	# etc.
└── ...
```
**Gradle Wrapper**
```
├── ...
├── gradle 			# Gradle wrapper script
│   ├── wrapper
│      ├── gradle-wrapper.jar        # Gradle wrapper script jar
│      ├── gradle-wrapper.properties  # Gradle wrapper script properties
│   └── ...                 	# etc.
└── ...
```
**Source**
```
├── ...
├── src 			# Source files
│   ├── main    		 # Java main class files
│	   ├── java 
│	      ├── HelloWorld.java		
│   ├── test 			 # Java test class files
│	   ├── java
│	      ├── HelloWorldTest.java
│   └── ...                 	# etc.
└── ...
```
Credit to [https://github.com/kriasoft] for
Folder Structure Convention Outline

----------

## [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#agile-principles)Agile Principles

### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#working-software)Working Software

#### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#the-project-code-base-is-always-buildable-and-runnable)The project code base is always buildable and runnable.

For example, no merge results in a non-buildable state or a buildable product that does not execute.

### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#incremental-development)Incremental Development

#### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#the-project-code-base-is-relevant-to-the-current-iteration)The project code base is relevant to the current iteration.

Architectural elements, tests, and implementation code match requirements associated with the current and previous versions of the product.

For example, tests and code for features identified for future versions are excluded from the project code base.

### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#behavior-driven-development)Behavior-Driven Development

#### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#all-code-is-associated-with-an-explicit-requirement-specification-user-story)All code is associated with an explicit requirement specification (User Story).

_Tracing backward_  from tests reveals the requirement(s) that such tests verify in the product.

_Tracing backward_  from code likewise reveals the requirement(s) that such code implements in the product.

### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#test-driven-development)Test-Driven Development

#### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#all-code-is-associated-with-an-explicit-means-for-verification)All code is associated with an explicit means for verification.

For example, new code is not merged into the project code base prior to the existence of automated test code for that new code.

_Tracing backward_  from the code reveals the tests used to verify the behavior of the code.

The intent is for code to be developed using a  _test-first_  methodology, in which automated tests are written prior to writing the implementation.

Tests associated with successful implementation remains in the code base as  _regression tests._

(Note: Test coverage tools may facilitate  _tracing forward_  from a test to code that the test is intended to verify.)

----------

## [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#coding-convention-guide)Coding Convention Guide

### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#style-convention-precedence-and-references)Style Convention Precedence and References

#### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#project-specific-conventions-take-precedence)[Project-specific conventions](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/ConventionGuide.md#Project-Specific-Conventions)  take precedence.

If no project-specific convention is applicable, use the  [Sun Convention](https://www.oracle.com/technetwork/java/codeconvtoc-136057.html)  guide.

If something is not covered in the project-specific or the Sun Convention guide, use the  [Google Convention](https://google.github.io/styleguide/javaguide.html)  guide.

If a topic is not covered by any guides, use best judgement and consider opening a project issue to formalize the decision.

-   Sun Convention guide:  [https://www.oracle.com/technetwork/java/codeconvtoc-136057.html](https://www.oracle.com/technetwork/java/codeconvtoc-136057.html)
-   Google Convention guide:  [https://google.github.io/styleguide/javaguide.html](https://google.github.io/styleguide/javaguide.html)

### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#project-specific-conventions)Project-Specific Conventions

-   Multiple authors are indicated using multiple @author tags, one tag per line, one author per tag.
-   Where practicable, style conventions are embodied in configuration files for the  [Checkstyle](https://checkstyle.sourceforge.io/)  tool.

----------

## [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#build-environment)Build Environment

The following tools are established as comprising and contributing to the build environment for the QT4BJ project.

### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#build-automation)Build Automation

#### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#gradle)Gradle

TODO: add overview and external links

### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#unit-testing-framework)Unit Testing Framework

#### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#junit-5)Junit 5

TODO: add overview and external links

### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#test-coverage-assessment)Test Coverage Assessment

#### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#jacoco)JaCoCo

TODO: add overview and external links

### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#design-complexity-assessment)Design Complexity Assessment

#### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#jacoco-1)JaCoCo

TODO: add overview and external links

### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#source-code-shortcoming-identification)Source Code Shortcoming Identification

#### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#checkstyle)Checkstyle

TODO: add overview and external links

#### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#pmd)PMD

TODO: add overview and external links

#### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#spotbugs)SpotBugs

TODO: add overview and external links

----------

_The following tools are under consideration for inclusion in the QT4BJ build environment._

#### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#travis-ci)Travis CI

TODO: add overview and external links

#### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#openclover)OpenClover

TODO: add overview and external links

#### [](https://github.com/MetroCS/QualityToolsForBlueJ/blob/master/DevelopmentConventions.md#accesslint)AccessLint

TODO: add overview and external links

