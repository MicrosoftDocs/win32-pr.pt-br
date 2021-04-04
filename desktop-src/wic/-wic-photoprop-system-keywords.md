---
description: A política de metadados de foto para a propriedade System. Keywords.
ms.assetid: bc9de56f-444c-45a2-9822-fba2fe618d38
title: Política de metadados de foto System. Keywords
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5d25e7f1919527d474395397d6df62863f7b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171318"
---
# <a name="systemkeywords-photo-metadata-policy"></a><span data-ttu-id="eb056-103">Política de metadados de foto System. Keywords</span><span class="sxs-lookup"><span data-stu-id="eb056-103">System.Keywords Photo Metadata Policy</span></span>

<span data-ttu-id="eb056-104">A política de metadados de foto para a propriedade [System. Keywords](../properties/props-system-keywords.md) .</span><span class="sxs-lookup"><span data-stu-id="eb056-104">The photo metadata policy for the [System.Keywords](../properties/props-system-keywords.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="eb056-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="eb056-105">PKEY</span></span>

<span data-ttu-id="eb056-106">\_Palavras-chave PKEY</span><span class="sxs-lookup"><span data-stu-id="eb056-106">PKEY\_Keywords</span></span>

### <a name="containers"></a><span data-ttu-id="eb056-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="eb056-107">Containers</span></span>

<span data-ttu-id="eb056-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="eb056-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="eb056-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eb056-109">Read-Only</span></span>

<span data-ttu-id="eb056-110">No</span><span class="sxs-lookup"><span data-stu-id="eb056-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="eb056-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="eb056-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="eb056-112">\_LPWStr do vetor VT VT \| \_</span><span class="sxs-lookup"><span data-stu-id="eb056-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="eb056-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="eb056-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="eb056-114">O \_ LPWSTR de vetor \| VT VT \_ é preferencial.</span><span class="sxs-lookup"><span data-stu-id="eb056-114">VT\_VECTOR \| VT\_LPWSTR is preferred.</span></span> <span data-ttu-id="eb056-115">Um \_ LPWSTR VT contendo uma cadeia de caracteres delimitada por ponto e vírgula também é aceito.</span><span class="sxs-lookup"><span data-stu-id="eb056-115">A VT\_LPWSTR containing a semicolon-delimited string is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="eb056-116">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="eb056-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="eb056-117">Valores de esquemas diferentes são mesclados.</span><span class="sxs-lookup"><span data-stu-id="eb056-117">Values from different schemas are merged.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="eb056-118">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="eb056-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="eb056-119">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="eb056-119">Read Paths</span></span>



| <span data-ttu-id="eb056-120">Ordem</span><span class="sxs-lookup"><span data-stu-id="eb056-120">Order</span></span> | <span data-ttu-id="eb056-121">Caminho</span><span class="sxs-lookup"><span data-stu-id="eb056-121">Path</span></span>                              | <span data-ttu-id="eb056-122">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="eb056-122">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="eb056-123">1</span><span class="sxs-lookup"><span data-stu-id="eb056-123">1</span></span>     | <span data-ttu-id="eb056-124">/XMP/ <xmpbag> DC: subject</span><span class="sxs-lookup"><span data-stu-id="eb056-124">/xmp/<xmpbag>dc:subject</span></span>     | <span data-ttu-id="eb056-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="eb056-125">unicode</span></span>        |
| <span data-ttu-id="eb056-126">2</span><span class="sxs-lookup"><span data-stu-id="eb056-126">2</span></span>     | <span data-ttu-id="eb056-127">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="eb056-127">/app13/irb/8bimiptc/iptc/keywords</span></span> |                |
| <span data-ttu-id="eb056-128">3</span><span class="sxs-lookup"><span data-stu-id="eb056-128">3</span></span>     | <span data-ttu-id="eb056-129">/App1/IFD/{UShort = 18247}</span><span class="sxs-lookup"><span data-stu-id="eb056-129">/app1/ifd/{ushort=18247}</span></span>          | <span data-ttu-id="eb056-130">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="eb056-130">unicode\_bytes</span></span> |
| <span data-ttu-id="eb056-131">4</span><span class="sxs-lookup"><span data-stu-id="eb056-131">4</span></span>     | <span data-ttu-id="eb056-132">/App1/IFD/{UShort = 40094}</span><span class="sxs-lookup"><span data-stu-id="eb056-132">/app1/ifd/{ushort=40094}</span></span>          | <span data-ttu-id="eb056-133">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="eb056-133">unicode\_bytes</span></span> |



 

### <a name="write-paths"></a><span data-ttu-id="eb056-134">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="eb056-134">Write Paths</span></span>



| <span data-ttu-id="eb056-135">Ordem</span><span class="sxs-lookup"><span data-stu-id="eb056-135">Order</span></span> | <span data-ttu-id="eb056-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="eb056-136">Path</span></span>                                              | <span data-ttu-id="eb056-137">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="eb056-137">Disk Format</span></span>    |
|-------|---------------------------------------------------|----------------|
| <span data-ttu-id="eb056-138">1</span><span class="sxs-lookup"><span data-stu-id="eb056-138">1</span></span>     | <span data-ttu-id="eb056-139">/XMP/ <xmpbag> DC: subject</span><span class="sxs-lookup"><span data-stu-id="eb056-139">/xmp/<xmpbag>dc:subject</span></span>                     | <span data-ttu-id="eb056-140">Unicode</span><span class="sxs-lookup"><span data-stu-id="eb056-140">unicode</span></span>        |
| <span data-ttu-id="eb056-141">2</span><span class="sxs-lookup"><span data-stu-id="eb056-141">2</span></span>     | <span data-ttu-id="eb056-142">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="eb056-142">/app13/irb/8bimiptc/iptc/keywords</span></span>                 |                |
| <span data-ttu-id="eb056-143">3</span><span class="sxs-lookup"><span data-stu-id="eb056-143">3</span></span>     | <span data-ttu-id="eb056-144">/App1/IFD/{UShort = 18247}</span><span class="sxs-lookup"><span data-stu-id="eb056-144">/app1/ifd/{ushort=18247}</span></span>                          | <span data-ttu-id="eb056-145">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="eb056-145">unicode\_bytes</span></span> |
| <span data-ttu-id="eb056-146">4</span><span class="sxs-lookup"><span data-stu-id="eb056-146">4</span></span>     | <span data-ttu-id="eb056-147">/App1/IFD/{UShort = 40094}</span><span class="sxs-lookup"><span data-stu-id="eb056-147">/app1/ifd/{ushort=40094}</span></span>                          | <span data-ttu-id="eb056-148">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="eb056-148">unicode\_bytes</span></span> |
| <span data-ttu-id="eb056-149">5</span><span class="sxs-lookup"><span data-stu-id="eb056-149">5</span></span>     | <span data-ttu-id="eb056-150">/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="eb056-150">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>  | <span data-ttu-id="eb056-151">Unicode</span><span class="sxs-lookup"><span data-stu-id="eb056-151">unicode</span></span>        |
| <span data-ttu-id="eb056-152">6</span><span class="sxs-lookup"><span data-stu-id="eb056-152">6</span></span>     | <span data-ttu-id="eb056-153">/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="eb056-153">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span> | <span data-ttu-id="eb056-154">Unicode</span><span class="sxs-lookup"><span data-stu-id="eb056-154">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="eb056-155">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="eb056-155">Remove Paths</span></span>



| <span data-ttu-id="eb056-156">Ordem</span><span class="sxs-lookup"><span data-stu-id="eb056-156">Order</span></span> | <span data-ttu-id="eb056-157">Caminho</span><span class="sxs-lookup"><span data-stu-id="eb056-157">Path</span></span>                                              |
|-------|---------------------------------------------------|
| <span data-ttu-id="eb056-158">1</span><span class="sxs-lookup"><span data-stu-id="eb056-158">1</span></span>     | <span data-ttu-id="eb056-159">/XMP/DC: assunto</span><span class="sxs-lookup"><span data-stu-id="eb056-159">/xmp/dc:subject</span></span>                                   |
| <span data-ttu-id="eb056-160">2</span><span class="sxs-lookup"><span data-stu-id="eb056-160">2</span></span>     | <span data-ttu-id="eb056-161">/app13/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="eb056-161">/app13/irb/8bimiptc/iptc/keywords</span></span>                 |
| <span data-ttu-id="eb056-162">3</span><span class="sxs-lookup"><span data-stu-id="eb056-162">3</span></span>     | <span data-ttu-id="eb056-163">/App1/IFD/{UShort = 18247}</span><span class="sxs-lookup"><span data-stu-id="eb056-163">/app1/ifd/{ushort=18247}</span></span>                          |
| <span data-ttu-id="eb056-164">4</span><span class="sxs-lookup"><span data-stu-id="eb056-164">4</span></span>     | <span data-ttu-id="eb056-165">/App1/IFD/{UShort = 40094}</span><span class="sxs-lookup"><span data-stu-id="eb056-165">/app1/ifd/{ushort=40094}</span></span>                          |
| <span data-ttu-id="eb056-166">5</span><span class="sxs-lookup"><span data-stu-id="eb056-166">5</span></span>     | <span data-ttu-id="eb056-167">/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="eb056-167">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>  |
| <span data-ttu-id="eb056-168">6</span><span class="sxs-lookup"><span data-stu-id="eb056-168">6</span></span>     | <span data-ttu-id="eb056-169">/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="eb056-169">/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span> |



 

### <a name="tiff-policy"></a><span data-ttu-id="eb056-170">Política TIFF</span><span class="sxs-lookup"><span data-stu-id="eb056-170">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="eb056-171">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="eb056-171">Read Paths</span></span>



| <span data-ttu-id="eb056-172">Ordem</span><span class="sxs-lookup"><span data-stu-id="eb056-172">Order</span></span> | <span data-ttu-id="eb056-173">Caminho</span><span class="sxs-lookup"><span data-stu-id="eb056-173">Path</span></span>                              | <span data-ttu-id="eb056-174">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="eb056-174">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="eb056-175">1</span><span class="sxs-lookup"><span data-stu-id="eb056-175">1</span></span>     | <span data-ttu-id="eb056-176">/IFD/XMP/ <xmpbag> DC: subject</span><span class="sxs-lookup"><span data-stu-id="eb056-176">/ifd/xmp/<xmpbag>dc:subject</span></span> | <span data-ttu-id="eb056-177">Unicode</span><span class="sxs-lookup"><span data-stu-id="eb056-177">unicode</span></span>        |
| <span data-ttu-id="eb056-178">2</span><span class="sxs-lookup"><span data-stu-id="eb056-178">2</span></span>     | <span data-ttu-id="eb056-179">/ifd/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="eb056-179">/ifd/iptc/keywords</span></span>                |                |
| <span data-ttu-id="eb056-180">3</span><span class="sxs-lookup"><span data-stu-id="eb056-180">3</span></span>     | <span data-ttu-id="eb056-181">/IFD/{UShort = 18247}</span><span class="sxs-lookup"><span data-stu-id="eb056-181">/ifd/{ushort=18247}</span></span>               | <span data-ttu-id="eb056-182">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="eb056-182">unicode\_bytes</span></span> |
| <span data-ttu-id="eb056-183">4</span><span class="sxs-lookup"><span data-stu-id="eb056-183">4</span></span>     | <span data-ttu-id="eb056-184">/IFD/{UShort = 40094}</span><span class="sxs-lookup"><span data-stu-id="eb056-184">/ifd/{ushort=40094}</span></span>               | <span data-ttu-id="eb056-185">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="eb056-185">unicode\_bytes</span></span> |
| <span data-ttu-id="eb056-186">5</span><span class="sxs-lookup"><span data-stu-id="eb056-186">5</span></span>     | <span data-ttu-id="eb056-187">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="eb056-187">/ifd/irb/8bimiptc/iptc/keywords</span></span>   |                |



 

### <a name="write-paths"></a><span data-ttu-id="eb056-188">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="eb056-188">Write Paths</span></span>



| <span data-ttu-id="eb056-189">Ordem</span><span class="sxs-lookup"><span data-stu-id="eb056-189">Order</span></span> | <span data-ttu-id="eb056-190">Caminho</span><span class="sxs-lookup"><span data-stu-id="eb056-190">Path</span></span>                                                             | <span data-ttu-id="eb056-191">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="eb056-191">Disk Format</span></span>    |
|-------|------------------------------------------------------------------|----------------|
| <span data-ttu-id="eb056-192">1</span><span class="sxs-lookup"><span data-stu-id="eb056-192">1</span></span>     | <span data-ttu-id="eb056-193">/IFD/XMP/ <xmpbag> DC: subject</span><span class="sxs-lookup"><span data-stu-id="eb056-193">/ifd/xmp/<xmpbag>dc:subject</span></span>                                | <span data-ttu-id="eb056-194">Unicode</span><span class="sxs-lookup"><span data-stu-id="eb056-194">unicode</span></span>        |
| <span data-ttu-id="eb056-195">2</span><span class="sxs-lookup"><span data-stu-id="eb056-195">2</span></span>     | <span data-ttu-id="eb056-196">/ifd/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="eb056-196">/ifd/iptc/keywords</span></span>                                               |                |
| <span data-ttu-id="eb056-197">3</span><span class="sxs-lookup"><span data-stu-id="eb056-197">3</span></span>     | <span data-ttu-id="eb056-198">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="eb056-198">/ifd/irb/8bimiptc/iptc/keywords</span></span>                                  |                |
| <span data-ttu-id="eb056-199">4</span><span class="sxs-lookup"><span data-stu-id="eb056-199">4</span></span>     | <span data-ttu-id="eb056-200">/IFD/{UShort = 18247}</span><span class="sxs-lookup"><span data-stu-id="eb056-200">/ifd/{ushort=18247}</span></span>                                              | <span data-ttu-id="eb056-201">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="eb056-201">unicode\_bytes</span></span> |
| <span data-ttu-id="eb056-202">5</span><span class="sxs-lookup"><span data-stu-id="eb056-202">5</span></span>     | <span data-ttu-id="eb056-203">/IFD/{UShort = 40094}</span><span class="sxs-lookup"><span data-stu-id="eb056-203">/ifd/{ushort=40094}</span></span>                                              | <span data-ttu-id="eb056-204">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="eb056-204">unicode\_bytes</span></span> |
| <span data-ttu-id="eb056-205">6</span><span class="sxs-lookup"><span data-stu-id="eb056-205">6</span></span>     | <span data-ttu-id="eb056-206">/IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="eb056-206">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>             | <span data-ttu-id="eb056-207">Unicode</span><span class="sxs-lookup"><span data-stu-id="eb056-207">unicode</span></span>        |
| <span data-ttu-id="eb056-208">7</span><span class="sxs-lookup"><span data-stu-id="eb056-208">7</span></span>     | <span data-ttu-id="eb056-209">/IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="eb056-209">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span>            | <span data-ttu-id="eb056-210">Unicode</span><span class="sxs-lookup"><span data-stu-id="eb056-210">unicode</span></span>        |
| <span data-ttu-id="eb056-211">8</span><span class="sxs-lookup"><span data-stu-id="eb056-211">8</span></span>     | <span data-ttu-id="eb056-212">/IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC \_ TIFF \_ IRB</span><span class="sxs-lookup"><span data-stu-id="eb056-212">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC\_TIFF\_IRB</span></span> | <span data-ttu-id="eb056-213">Unicode</span><span class="sxs-lookup"><span data-stu-id="eb056-213">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="eb056-214">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="eb056-214">Remove Paths</span></span>



| <span data-ttu-id="eb056-215">Ordem</span><span class="sxs-lookup"><span data-stu-id="eb056-215">Order</span></span> | <span data-ttu-id="eb056-216">Caminho</span><span class="sxs-lookup"><span data-stu-id="eb056-216">Path</span></span>                                                             |
|-------|------------------------------------------------------------------|
| <span data-ttu-id="eb056-217">1</span><span class="sxs-lookup"><span data-stu-id="eb056-217">1</span></span>     | <span data-ttu-id="eb056-218">/IFD/XMP/DC: assunto</span><span class="sxs-lookup"><span data-stu-id="eb056-218">/ifd/xmp/dc:subject</span></span>                                              |
| <span data-ttu-id="eb056-219">2</span><span class="sxs-lookup"><span data-stu-id="eb056-219">2</span></span>     | <span data-ttu-id="eb056-220">/ifd/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="eb056-220">/ifd/iptc/keywords</span></span>                                               |
| <span data-ttu-id="eb056-221">3</span><span class="sxs-lookup"><span data-stu-id="eb056-221">3</span></span>     | <span data-ttu-id="eb056-222">/ifd/irb/8bimiptc/iptc/keywords</span><span class="sxs-lookup"><span data-stu-id="eb056-222">/ifd/irb/8bimiptc/iptc/keywords</span></span>                                  |
| <span data-ttu-id="eb056-223">4</span><span class="sxs-lookup"><span data-stu-id="eb056-223">4</span></span>     | <span data-ttu-id="eb056-224">/IFD/{UShort = 18247}</span><span class="sxs-lookup"><span data-stu-id="eb056-224">/ifd/{ushort=18247}</span></span>                                              |
| <span data-ttu-id="eb056-225">5</span><span class="sxs-lookup"><span data-stu-id="eb056-225">5</span></span>     | <span data-ttu-id="eb056-226">/IFD/{UShort = 40094}</span><span class="sxs-lookup"><span data-stu-id="eb056-226">/ifd/{ushort=40094}</span></span>                                              |
| <span data-ttu-id="eb056-227">6</span><span class="sxs-lookup"><span data-stu-id="eb056-227">6</span></span>     | <span data-ttu-id="eb056-228">/IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordXMP</span><span class="sxs-lookup"><span data-stu-id="eb056-228">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordXMP</span></span>             |
| <span data-ttu-id="eb056-229">7</span><span class="sxs-lookup"><span data-stu-id="eb056-229">7</span></span>     | <span data-ttu-id="eb056-230">/IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC</span><span class="sxs-lookup"><span data-stu-id="eb056-230">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC</span></span>            |
| <span data-ttu-id="eb056-231">8</span><span class="sxs-lookup"><span data-stu-id="eb056-231">8</span></span>     | <span data-ttu-id="eb056-232">/IFD/XMP/ <xmpbag> MicrosoftPhoto: LastKeywordIPTC \_ TIFF \_ IRB</span><span class="sxs-lookup"><span data-stu-id="eb056-232">/ifd/xmp/<xmpbag>MicrosoftPhoto:LastKeywordIPTC\_TIFF\_IRB</span></span> |



 

### <a name="remarks"></a><span data-ttu-id="eb056-233">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb056-233">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb056-234">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="eb056-234">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb056-235">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="eb056-235">System.Keywords</span></span>](../properties/props-system-keywords.md)
</dt> </dl>

 

 
