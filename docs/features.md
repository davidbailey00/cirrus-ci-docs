---
hide:
  - navigation
  - toc
---
## Free for Open Source 

To support Open Source community Cirrus CI provides [Linux](guide/linux.md), [Windows](guide/windows.md), [macOS](guide/macOS.md) and [FreeBSD](guide/FreeBSD.md)
services free of charge with [some limits](faq.md#are-there-any-limits) but *without* a cap on how many minutes a month OSS projects can consume.

## Per-second billing

Use [compute credits](pricing.md#compute-credits) to run as many parallel tasks as you want and pay only for CPU time
used by these tasks. Or [bring your own infrastructure](#bring-you-own-infrastructure) and pay directly to your cloud provider
within your current billing.

## No concurrency limit. No queues

Cirrus CI leverages elasticity of the modern clouds to always have available resources to process your builds.
**Engineers should never wait for builds to start**.

## Bring Your Own Infrastructure 

Cirrus CI supports [bringing your own infrastructure](guide/supported-computing-services.md) (BYO) for full control over security and for easy integration with
your current workflow.

<p align="center">
  <a href="/guide/supported-computing-services#google-cloud">
    <img style="width:128px;height:128px;" src="/assets/images/gcp/Google Cloud Platform.svg"/>
  </a>
  <a href="/guide/supported-computing-services#aws">
    <img style="width:128px;height:128px;" src="/assets/images/aws/AWS.svg"/>
  </a>
  <a href="/guide/supported-computing-services#azure">
    <img style="width:128px;height:128px;" src="/assets/images/azure/Microsoft Azure.svg"/>
  </a>
</p>

## Flexible execution environment
 
Cirrus CI allows to use any Unix or Windows VMs, any Docker containers, any amount of CPUs, optional SSDs and GPUs.

## Simple but very powerful configuration format 

Learn more about how to configure tasks [here](guide/writing-tasks.md). Configure things like:

* [Matrix Builds](guide/writing-tasks.md#matrix-modification)
* [Dependencies between tasks](guide/writing-tasks.md#dependencies)
* [Conditional Task Execution](guide/writing-tasks.md#conditional-task-execution)
* [Local HTTP Cache](guide/writing-tasks.md#http-cache)
* [Dockerfile as a CI environment](guide/docker-builder-vm.md#dockerfile-as-a-ci-environment)
* [Monorepo Support](guide/writing-tasks.md#supported-functions)

Check [Quick Start](guide/quick-start.md) guide for more features.

## Comparison with popular CIaaS

Here is a high level comparison with popular continuous-integration-as-a-service solutions:

**Name**        | **[Linux][1] [Windows][2] [macOS][3]** | **[FreeBSD][4]**   | **Customizable CPU/Memory**    | **For Open Source**                                           | **For Personal Private Repositories**                          | **For Organizational Private Repositories**
--------------- | -------------------------------------- | -------------------| ------------------------------ | ------------------------------------------------------------- | -------------------------------------------------------------- | --------------------------------
Cirrus CI       | :white_check_mark:                     | :white_check_mark: | :white_check_mark: (any value) | [34 concurrent CPUs with **no monthly limit** on minutes][6]  | $10/month with the same OSS limits 👈                          | [Per-second usage with no parallel limit](#per-second-billing)<br>[Connect your cloud](#bring-your-own-infrastructure) for $10/month/seat
GitHub Actions  | :white_check_mark:                     | :x:                | :x:                            | 20 concurrent jobs with no monthly limit on minutes           | 2,000 minutes/month for free                                   | Per-minute usage with no parallel limit<br>Host and manage additional runners at no additional cost
Travis CI       | :white_check_mark:                     | :x:                | :x:                            | 1000 minutes per account per month                            | $69/month for 1 concurrent job                                 | $49/month per additional concurrency job
CircleCI        | :white_check_mark:                     | :x:                | :white_check_mark: (4 types)   | 40,000 minutes per organization per month                     | 1,000 minutes/month for free<br>$69/month for 2 concurrent job | $15/month/user + per-minute usage with up to 80 parallel jobs
AppVeyor        | :white_check_mark:                     | :x:                | :x:                            | 1 concurrent job with no monthly limit on minutes             | $59/month for 1 concurrent job                                 | $50/month per additional concurrency job

[1]: guide/linux.md
[2]: guide/windows.md
[3]: guide/macOS.md
[4]: guide/FreeBSD.md
[5]: faq.md#any-discounts
[6]: faq.md#are-there-any-limits

Feel free to [contact support](mailto:support@cirruslabs.org) if you have questions for your particular case.
