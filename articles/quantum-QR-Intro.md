---
# Mandatory fields. See more on aka.ms/skyeye/meta.
title: The Q# Programming Language | Microsoft Docs 
description: The Q# Programming Language
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com 
ms.date: 12/11/2017
ms.topic: article
# Use only one of the following. Use ms.service for services, ms.prod for on-prem. Remove the # before the relevant field.
# For Quantum products none of these categories have been defined  yet.
# ms.service: service-name-from-white-list
# ms.prod: product-name-from-white-list
# ms.technology: tech-name-from-white-list
---

# The Q# Programming Language

# Introduction

A natural model for quantum computation is to treat the quantum computer 
as a coprocessor, similar to that used for GPUs, FPGAs, and other adjunct 
processors.
The primary control logic runs classical code on a classical "host" computer.
When appropriate and necessary, the host program can invoke a sub-program 
that runs on the adjunct processor.
When the sub-program completes, the host program gets access to the 
sub-program's results.

In this model, there are three levels of computation:

 - Classical computation that reads input data, sets up the quantum 
    computation, triggers the quantum computation, processes the results 
    of the computation, and presents the results to the user.
 - Quantum computation that happens directly in the quantum device and 
    implements a quantum algorithm.
 - Classical computation that is required by the quantum algorithm during 
    its execution.

There is no intrinsic requirement that these three levels all be written 
in the same language.
Indeed, quantum computation has somewhat different control structures and 
resource management needs than classical computation, so using a custom 
programming language allows common patterns in quantum algorithms to be 
expressed more naturally.

Keeping classical computations separate means that the quantum programming 
language may be very constrained.
These constraints may allow better optimization or faster execution 
of the quantum algorithm.

Q# (Q-sharp) is a domain-specific programming language used for 
expressing quantum algorithms.
It is to be used for writing sub-programs that execute on an adjunct 
quantum processor, under the control of a classical host program and computer.

Q# provides a small set of primitive types, along with two ways 
(arrays and tuples) for creating new, structured types. 
It supports a basic procedural model for writing programs, 
with loops and if/then statements. 
The top-level constructs in Q# are user defined types, operations, 
and functions.

The following sections detail:
- [The Type Model](quantum-QR-TypeModel.md)
- [Expressions](quantum-QR-Expressions.md)
- [Statements](quantum-QR-Statements.md)
- [File Structure](quantum-QR-FileStructure.md)



