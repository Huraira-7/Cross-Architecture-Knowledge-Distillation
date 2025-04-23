# Cross-Architecture-Knowledge-Distillation

## Project Overview
Here is a brief project overview:

This project encounters errors when attempting to read a PDF file named "final_report.pdf" in the "final_project" directory, likely due to issues with the file's format or reading process. Additionally, the project exceeds token limits for the `llama3-70b-8192` model in the `on_demand` service tier, resulting in rate limit exceeded errors. The project requires optimization to reduce message size and avoid these errors, or consideration of upgrading to a higher service tier for increased token limits.

# Cross-Architecture-Knowledge-Distillation

## Overview
This repository, Cross-Architecture-Knowledge-Distillation, contains the following summarized content based on the files analyzed:

### final_project/cifar_noisy_scrambled_dataset.ipynb
Error creating final summary: Error code: 413 - {'error': {'message': 'Request too large for model `llama3-70b-8192` in organization `org_01jrs9kgpnfv698wasqg7gxpkp` service tier `on_demand` on tokens per minute (TPM): Limit 6000, Requested 188642, please reduce your message size and try again. Need more tokens? Upgrade to Dev Tier today at https://console.groq.com/settings/billing', 'type': 'tokens', 'code': 'rate_limit_exceeded'}}

### final_project/cifar_texture_bias_dataset.ipynb
Error creating final summary: Error code: 413 - {'error': {'message': 'Request too large for model `llama3-70b-8192` in organization `org_01jrs9kgpnfv698wasqg7gxpkp` service tier `on_demand` on tokens per day (TPD): Limit 500000, Requested 794007, please reduce your message size and try again. Need more tokens? Upgrade to Dev Tier today at https://console.groq.com/settings/billing', 'type': 'tokens', 'code': 'rate_limit_exceeded'}}

### final_project/final_report.pdf
Here is a concise summary:

An error occurred while attempting to read a PDF file named "final_report.pdf" located in the "final_project" directory. The error message indicates that a 'bytes' object, which is used to represent the file's content, does not have a 'seek' attribute. This suggests that the file is not being read correctly, possibly due to an issue with the file's format or the reading process.

### final_project/resnet-to-vit.ipynb
Error creating final summary: Error code: 413 - {'error': {'message': 'Request too large for model `llama3-70b-8192` in organization `org_01jrs9kgpnfv698wasqg7gxpkp` service tier `on_demand` on tokens per minute (TPM): Limit 6000, Requested 54371, please reduce your message size and try again. Need more tokens? Upgrade to Dev Tier today at https://console.groq.com/settings/billing', 'type': 'tokens', 'code': 'rate_limit_exceeded'}}

### final_project/shape_bias_slic_cifar_dataset.ipynb
Error creating final summary: Error code: 413 - {'error': {'message': 'Request too large for model `llama3-70b-8192` in organization `org_01jrs9kgpnfv698wasqg7gxpkp` service tier `on_demand` on tokens per day (TPD): Limit 500000, Requested 804897, please reduce your message size and try again. Need more tokens? Upgrade to Dev Tier today at https://console.groq.com/settings/billing', 'type': 'tokens', 'code': 'rate_limit_exceeded'}}

### final_project/vit-to-resnet.ipynb
Error creating final summary: Error code: 413 - {'error': {'message': 'Request too large for model `llama3-70b-8192` in organization `org_01jrs9kgpnfv698wasqg7gxpkp` service tier `on_demand` on tokens per minute (TPM): Limit 6000, Requested 298309, please reduce your message size and try again. Need more tokens? Upgrade to Dev Tier today at https://console.groq.com/settings/billing', 'type': 'tokens', 'code': 'rate_limit_exceeded'}}

