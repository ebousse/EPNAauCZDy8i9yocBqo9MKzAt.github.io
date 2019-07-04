# Abstract

> Runtime monitoring is a fundamental technique used throughout the lifecycle of a system for many purposes, such as debugging, testing, or live analytics. While runtime monitoring for general purpose programming languages has seen a great amount of research, developing such complex facilities for any executable Domain Specific Language (DSL) remains a challenging, reoccurring and error prone task. A generic solution must both support a wide range of executable DSLs and induce as little execution time overhead as possible. Our contribution is a fully generic approach based on a temporal property language with a semantics tailored for runtime verification. Properties can be compiled to efficient runtime monitors that can be attached to any kind of executable model. Efficiency is bolstered using a novel combination of structural model queries and complex event processing. Our evaluation shows that the approach is applicable with an average execution time overhead ranging from 53% (with around 3 model changes per execution state) to 87.5% (with between 100 to 400 model changes per execution state), with no noticeable overhead induced by increased execution length.

# Resources

 - [Complete translational semantics for temporal patterns (25 rules)](https://raw.githubusercontent.com/EPNAauCZDy8i9yocBqo9MKzAt/EPNAauCZDy8i9yocBqo9MKzAt.github.io/master/Runtime_Monitoring_for_Executable_DSLs__Full_Semantics.pdf)
 - [Code & Evaluation materials](https://github.com/EPNAauCZDy8i9yocBqo9MKzAt/EPNAauCZDy8i9yocBqo9MKzAt.github.io/raw/master/evaluation_materials.zip)

# Running the evaluation

Preparing the GEMOC Studio

 - Download the latest version of the GEMOC Studio: (http://gemoc.org/download.html)
 - Install VIATRA on top of the GEMOC Studio: (https://www.eclipse.org/viatra/downloads.html)
 - Start the GEMOC Studio in a new workspace

Getting the benchmark code

 - Download and extract the zip containing the code and evaluation materials
 - Import the projects contained in the "plugins" and "eval/plugins" folders into the current workspace of the GEMOC Studio

Configuring the Activity Diagram language

 - Start a new Eclipse application inside the opened GEMOC Studio using the "Eclipse Application" launch configuration type
 - In this new workspace, import the 8 projects contained in the "eval/language" folder

Configuring the benchmark code

 - Still in the nested Eclipse application, import the "org.eclipse.gemoc.benchmark.property.monitor" project from the "eval/plugins" folder
 - Open the "BenchmarkSingleJVMTestSuite" class  from the "org.eclipse.gemoc.benchmark.property.monitor" project and complete the missing static fields with: your java home, the path to your gemoc launcher (e.g. "/home/\<username\>/Downloads/gemoc-studio/plugins/org.eclipse.equinox.launcher_1.5.0.v20180512-1130.jar"), the path to the current workspace, and the path where you want to write the output of the evaluation
 - Run the "BenchmarkSingleJVMTestSuite" as a JUnit Plug-in Test (this step is necessary to automatically launch tests)
 - Close the nested Eclipse application

Running the benchmark

 - Run the "BenchmarkTimeTestSuite" from the "org.eclipse.gemoc.benchmark.property.monitor" project as a JUnit Test
