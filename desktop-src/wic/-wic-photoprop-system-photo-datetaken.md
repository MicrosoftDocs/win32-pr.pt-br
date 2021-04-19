---
description: A política de metadados de foto para a propriedade System. Photo. DateTaken.
ms.assetid: 800aa01b-6064-45df-a40e-6537819df4d7
title: Política de metadados de foto System. Photo. DateTaken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc1d3fb50a9a94e4bb13b35a0a5726572d78429f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798007"
---
# <a name="systemphotodatetaken-photo-metadata-policy"></a><span data-ttu-id="a4e00-103">Política de metadados de foto System. Photo. DateTaken</span><span class="sxs-lookup"><span data-stu-id="a4e00-103">System.Photo.DateTaken Photo Metadata Policy</span></span>

<span data-ttu-id="a4e00-104">A política de metadados de foto para a propriedade [System. Photo. DateTaken](../properties/props-system-photo-datetaken.md) .</span><span class="sxs-lookup"><span data-stu-id="a4e00-104">The photo metadata policy for the [System.Photo.DateTaken](../properties/props-system-photo-datetaken.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a4e00-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a4e00-105">PKEY</span></span>

<span data-ttu-id="a4e00-106">PKEY \_ Photo \_ DateTaken</span><span class="sxs-lookup"><span data-stu-id="a4e00-106">PKEY\_Photo\_DateTaken</span></span>

### <a name="containers"></a><span data-ttu-id="a4e00-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="a4e00-107">Containers</span></span>

<span data-ttu-id="a4e00-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a4e00-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a4e00-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4e00-109">Read-Only</span></span>

<span data-ttu-id="a4e00-110">No</span><span class="sxs-lookup"><span data-stu-id="a4e00-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a4e00-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="a4e00-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a4e00-112">FILETIME do VT \_</span><span class="sxs-lookup"><span data-stu-id="a4e00-112">VT\_FILETIME</span></span>

### <a name="input-type"></a><span data-ttu-id="a4e00-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="a4e00-113">Input Type</span></span>

<span data-ttu-id="a4e00-114">Datetime</span><span class="sxs-lookup"><span data-stu-id="a4e00-114">DateTime</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a4e00-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="a4e00-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a4e00-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="a4e00-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a4e00-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="a4e00-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a4e00-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="a4e00-118">Read Paths</span></span>



| <span data-ttu-id="a4e00-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4e00-119">Order</span></span> | <span data-ttu-id="a4e00-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4e00-120">Path</span></span>                                  | <span data-ttu-id="a4e00-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a4e00-121">Disk Format</span></span> |
|-------|---------------------------------------|-------------|
| <span data-ttu-id="a4e00-122">1</span><span class="sxs-lookup"><span data-stu-id="a4e00-122">1</span></span>     | <span data-ttu-id="a4e00-123">/App1/IFD/EXIF/{UShort = 36867}</span><span class="sxs-lookup"><span data-stu-id="a4e00-123">/app1/ifd/exif/{ushort=36867}</span></span>         | <span data-ttu-id="a4e00-124">ascii</span><span class="sxs-lookup"><span data-stu-id="a4e00-124">ascii</span></span>       |
| <span data-ttu-id="a4e00-125">2</span><span class="sxs-lookup"><span data-stu-id="a4e00-125">2</span></span>     | <span data-ttu-id="a4e00-126">/app13/IRB/8bimiptc/IPTC/Date criado</span><span class="sxs-lookup"><span data-stu-id="a4e00-126">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="a4e00-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4e00-127">unicode</span></span>     |
| <span data-ttu-id="a4e00-128">3</span><span class="sxs-lookup"><span data-stu-id="a4e00-128">3</span></span>     | <span data-ttu-id="a4e00-129">/XMP/XMP: CreateDate</span><span class="sxs-lookup"><span data-stu-id="a4e00-129">/xmp/xmp:CreateDate</span></span>                   | <span data-ttu-id="a4e00-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4e00-130">unicode</span></span>     |
| <span data-ttu-id="a4e00-131">4</span><span class="sxs-lookup"><span data-stu-id="a4e00-131">4</span></span>     | <span data-ttu-id="a4e00-132">/App1/IFD/EXIF/{UShort = 36868}</span><span class="sxs-lookup"><span data-stu-id="a4e00-132">/app1/ifd/exif/{ushort=36868}</span></span>         | <span data-ttu-id="a4e00-133">ascii</span><span class="sxs-lookup"><span data-stu-id="a4e00-133">ascii</span></span>       |
| <span data-ttu-id="a4e00-134">5</span><span class="sxs-lookup"><span data-stu-id="a4e00-134">5</span></span>     | <span data-ttu-id="a4e00-135">/app13/IRB/8bimiptc/IPTC/Date criado</span><span class="sxs-lookup"><span data-stu-id="a4e00-135">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="a4e00-136">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4e00-136">unicode</span></span>     |
| <span data-ttu-id="a4e00-137">6</span><span class="sxs-lookup"><span data-stu-id="a4e00-137">6</span></span>     | <span data-ttu-id="a4e00-138">/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="a4e00-138">/xmp/exif:DateTimeOriginal</span></span>            | <span data-ttu-id="a4e00-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4e00-139">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a4e00-140">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="a4e00-140">Write Paths</span></span>



| <span data-ttu-id="a4e00-141">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4e00-141">Order</span></span> | <span data-ttu-id="a4e00-142">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4e00-142">Path</span></span>                                  | <span data-ttu-id="a4e00-143">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a4e00-143">Disk Format</span></span> |
|-------|---------------------------------------|-------------|
| <span data-ttu-id="a4e00-144">1</span><span class="sxs-lookup"><span data-stu-id="a4e00-144">1</span></span>     | <span data-ttu-id="a4e00-145">/App1/IFD/EXIF/{UShort = 36867}</span><span class="sxs-lookup"><span data-stu-id="a4e00-145">/app1/ifd/exif/{ushort=36867}</span></span>         | <span data-ttu-id="a4e00-146">ascii</span><span class="sxs-lookup"><span data-stu-id="a4e00-146">ascii</span></span>       |
| <span data-ttu-id="a4e00-147">2</span><span class="sxs-lookup"><span data-stu-id="a4e00-147">2</span></span>     | <span data-ttu-id="a4e00-148">/app13/IRB/8bimiptc/IPTC/Date criado</span><span class="sxs-lookup"><span data-stu-id="a4e00-148">/app13/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="a4e00-149">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4e00-149">unicode</span></span>     |
| <span data-ttu-id="a4e00-150">3</span><span class="sxs-lookup"><span data-stu-id="a4e00-150">3</span></span>     | <span data-ttu-id="a4e00-151">/XMP/XMP: CreateDate</span><span class="sxs-lookup"><span data-stu-id="a4e00-151">/xmp/xmp:CreateDate</span></span>                   | <span data-ttu-id="a4e00-152">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4e00-152">unicode</span></span>     |
| <span data-ttu-id="a4e00-153">4</span><span class="sxs-lookup"><span data-stu-id="a4e00-153">4</span></span>     | <span data-ttu-id="a4e00-154">/App1/IFD/EXIF/{UShort = 36868}</span><span class="sxs-lookup"><span data-stu-id="a4e00-154">/app1/ifd/exif/{ushort=36868}</span></span>         | <span data-ttu-id="a4e00-155">ascii</span><span class="sxs-lookup"><span data-stu-id="a4e00-155">ascii</span></span>       |
| <span data-ttu-id="a4e00-156">5</span><span class="sxs-lookup"><span data-stu-id="a4e00-156">5</span></span>     | <span data-ttu-id="a4e00-157">/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="a4e00-157">/xmp/exif:DateTimeOriginal</span></span>            | <span data-ttu-id="a4e00-158">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4e00-158">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a4e00-159">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="a4e00-159">Remove Paths</span></span>



| <span data-ttu-id="a4e00-160">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4e00-160">Order</span></span> | <span data-ttu-id="a4e00-161">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4e00-161">Path</span></span>                                  |
|-------|---------------------------------------|
| <span data-ttu-id="a4e00-162">1</span><span class="sxs-lookup"><span data-stu-id="a4e00-162">1</span></span>     | <span data-ttu-id="a4e00-163">/App1/IFD/EXIF/{UShort = 36867}</span><span class="sxs-lookup"><span data-stu-id="a4e00-163">/app1/ifd/exif/{ushort=36867}</span></span>         |
| <span data-ttu-id="a4e00-164">2</span><span class="sxs-lookup"><span data-stu-id="a4e00-164">2</span></span>     | <span data-ttu-id="a4e00-165">/App1/IFD/EXIF/{UShort = 37521}</span><span class="sxs-lookup"><span data-stu-id="a4e00-165">/app1/ifd/exif/{ushort=37521}</span></span>         |
| <span data-ttu-id="a4e00-166">3</span><span class="sxs-lookup"><span data-stu-id="a4e00-166">3</span></span>     | <span data-ttu-id="a4e00-167">/App1/IFD/EXIF/{UShort = 36868}</span><span class="sxs-lookup"><span data-stu-id="a4e00-167">/app1/ifd/exif/{ushort=36868}</span></span>         |
| <span data-ttu-id="a4e00-168">4</span><span class="sxs-lookup"><span data-stu-id="a4e00-168">4</span></span>     | <span data-ttu-id="a4e00-169">/App1/IFD/EXIF/{UShort = 37522}</span><span class="sxs-lookup"><span data-stu-id="a4e00-169">/app1/ifd/exif/{ushort=37522}</span></span>         |
| <span data-ttu-id="a4e00-170">5</span><span class="sxs-lookup"><span data-stu-id="a4e00-170">5</span></span>     | <span data-ttu-id="a4e00-171">/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="a4e00-171">/xmp/exif:DateTimeOriginal</span></span>            |
| <span data-ttu-id="a4e00-172">6</span><span class="sxs-lookup"><span data-stu-id="a4e00-172">6</span></span>     | <span data-ttu-id="a4e00-173">/XMP/XMP: CreateDate</span><span class="sxs-lookup"><span data-stu-id="a4e00-173">/xmp/xmp:CreateDate</span></span>                   |
| <span data-ttu-id="a4e00-174">7</span><span class="sxs-lookup"><span data-stu-id="a4e00-174">7</span></span>     | <span data-ttu-id="a4e00-175">/app13/IRB/8bimiptc/IPTC/Date criado</span><span class="sxs-lookup"><span data-stu-id="a4e00-175">/app13/irb/8bimiptc/iptc/date created</span></span> |
| <span data-ttu-id="a4e00-176">8</span><span class="sxs-lookup"><span data-stu-id="a4e00-176">8</span></span>     | <span data-ttu-id="a4e00-177">/app13/IRB/8bimiptc/IPTC/time criado</span><span class="sxs-lookup"><span data-stu-id="a4e00-177">/app13/irb/8bimiptc/iptc/time created</span></span> |



 

### <a name="tiff-policy"></a><span data-ttu-id="a4e00-178">Política TIFF</span><span class="sxs-lookup"><span data-stu-id="a4e00-178">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a4e00-179">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="a4e00-179">Read Paths</span></span>



| <span data-ttu-id="a4e00-180">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4e00-180">Order</span></span> | <span data-ttu-id="a4e00-181">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4e00-181">Path</span></span>                                | <span data-ttu-id="a4e00-182">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a4e00-182">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="a4e00-183">1</span><span class="sxs-lookup"><span data-stu-id="a4e00-183">1</span></span>     | <span data-ttu-id="a4e00-184">/IFD/EXIF/{UShort = 36867}</span><span class="sxs-lookup"><span data-stu-id="a4e00-184">/ifd/exif/{ushort=36867}</span></span>            | <span data-ttu-id="a4e00-185">ascii</span><span class="sxs-lookup"><span data-stu-id="a4e00-185">ascii</span></span>       |
| <span data-ttu-id="a4e00-186">2</span><span class="sxs-lookup"><span data-stu-id="a4e00-186">2</span></span>     | <span data-ttu-id="a4e00-187">/IFD/IPTC/Date criado</span><span class="sxs-lookup"><span data-stu-id="a4e00-187">/ifd/iptc/date created</span></span>              | <span data-ttu-id="a4e00-188">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4e00-188">unicode</span></span>     |
| <span data-ttu-id="a4e00-189">3</span><span class="sxs-lookup"><span data-stu-id="a4e00-189">3</span></span>     | <span data-ttu-id="a4e00-190">/IFD/XMP/XMP: CreateDate</span><span class="sxs-lookup"><span data-stu-id="a4e00-190">/ifd/xmp/xmp:CreateDate</span></span>             | <span data-ttu-id="a4e00-191">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4e00-191">unicode</span></span>     |
| <span data-ttu-id="a4e00-192">4</span><span class="sxs-lookup"><span data-stu-id="a4e00-192">4</span></span>     | <span data-ttu-id="a4e00-193">/IFD/EXIF/{UShort = 36868}</span><span class="sxs-lookup"><span data-stu-id="a4e00-193">/ifd/exif/{ushort=36868}</span></span>            | <span data-ttu-id="a4e00-194">ascii</span><span class="sxs-lookup"><span data-stu-id="a4e00-194">ascii</span></span>       |
| <span data-ttu-id="a4e00-195">5</span><span class="sxs-lookup"><span data-stu-id="a4e00-195">5</span></span>     | <span data-ttu-id="a4e00-196">/IFD/IPTC/Date criado</span><span class="sxs-lookup"><span data-stu-id="a4e00-196">/ifd/iptc/date created</span></span>              | <span data-ttu-id="a4e00-197">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4e00-197">unicode</span></span>     |
| <span data-ttu-id="a4e00-198">6</span><span class="sxs-lookup"><span data-stu-id="a4e00-198">6</span></span>     | <span data-ttu-id="a4e00-199">/IFD/IRB/8bimiptc/IPTC/Date criado</span><span class="sxs-lookup"><span data-stu-id="a4e00-199">/ifd/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="a4e00-200">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4e00-200">unicode</span></span>     |
| <span data-ttu-id="a4e00-201">7</span><span class="sxs-lookup"><span data-stu-id="a4e00-201">7</span></span>     | <span data-ttu-id="a4e00-202">/ifd/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="a4e00-202">/ifd/xmp/exif:DateTimeOriginal</span></span>      | <span data-ttu-id="a4e00-203">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4e00-203">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a4e00-204">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="a4e00-204">Write Paths</span></span>



| <span data-ttu-id="a4e00-205">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4e00-205">Order</span></span> | <span data-ttu-id="a4e00-206">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4e00-206">Path</span></span>                                | <span data-ttu-id="a4e00-207">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a4e00-207">Disk Format</span></span> |
|-------|-------------------------------------|-------------|
| <span data-ttu-id="a4e00-208">1</span><span class="sxs-lookup"><span data-stu-id="a4e00-208">1</span></span>     | <span data-ttu-id="a4e00-209">/IFD/EXIF/{UShort = 36867}</span><span class="sxs-lookup"><span data-stu-id="a4e00-209">/ifd/exif/{ushort=36867}</span></span>            | <span data-ttu-id="a4e00-210">ascii</span><span class="sxs-lookup"><span data-stu-id="a4e00-210">ascii</span></span>       |
| <span data-ttu-id="a4e00-211">2</span><span class="sxs-lookup"><span data-stu-id="a4e00-211">2</span></span>     | <span data-ttu-id="a4e00-212">/IFD/IPTC/Date criado</span><span class="sxs-lookup"><span data-stu-id="a4e00-212">/ifd/iptc/date created</span></span>              | <span data-ttu-id="a4e00-213">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4e00-213">unicode</span></span>     |
| <span data-ttu-id="a4e00-214">3</span><span class="sxs-lookup"><span data-stu-id="a4e00-214">3</span></span>     | <span data-ttu-id="a4e00-215">/IFD/XMP/XMP: CreateDate</span><span class="sxs-lookup"><span data-stu-id="a4e00-215">/ifd/xmp/xmp:CreateDate</span></span>             | <span data-ttu-id="a4e00-216">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4e00-216">unicode</span></span>     |
| <span data-ttu-id="a4e00-217">4</span><span class="sxs-lookup"><span data-stu-id="a4e00-217">4</span></span>     | <span data-ttu-id="a4e00-218">/IFD/EXIF/{UShort = 36868}</span><span class="sxs-lookup"><span data-stu-id="a4e00-218">/ifd/exif/{ushort=36868}</span></span>            | <span data-ttu-id="a4e00-219">ascii</span><span class="sxs-lookup"><span data-stu-id="a4e00-219">ascii</span></span>       |
| <span data-ttu-id="a4e00-220">5</span><span class="sxs-lookup"><span data-stu-id="a4e00-220">5</span></span>     | <span data-ttu-id="a4e00-221">/IFD/IRB/8bimiptc/IPTC/Date criado</span><span class="sxs-lookup"><span data-stu-id="a4e00-221">/ifd/irb/8bimiptc/iptc/date created</span></span> | <span data-ttu-id="a4e00-222">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4e00-222">unicode</span></span>     |
| <span data-ttu-id="a4e00-223">6</span><span class="sxs-lookup"><span data-stu-id="a4e00-223">6</span></span>     | <span data-ttu-id="a4e00-224">/ifd/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="a4e00-224">/ifd/xmp/exif:DateTimeOriginal</span></span>      | <span data-ttu-id="a4e00-225">Unicode</span><span class="sxs-lookup"><span data-stu-id="a4e00-225">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a4e00-226">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="a4e00-226">Remove Paths</span></span>



| <span data-ttu-id="a4e00-227">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4e00-227">Order</span></span> | <span data-ttu-id="a4e00-228">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4e00-228">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="a4e00-229">1</span><span class="sxs-lookup"><span data-stu-id="a4e00-229">1</span></span>     | <span data-ttu-id="a4e00-230">/IFD/EXIF/{UShort = 36867}</span><span class="sxs-lookup"><span data-stu-id="a4e00-230">/ifd/exif/{ushort=36867}</span></span>            |
| <span data-ttu-id="a4e00-231">2</span><span class="sxs-lookup"><span data-stu-id="a4e00-231">2</span></span>     | <span data-ttu-id="a4e00-232">/IFD/EXIF/{UShort = 37521}</span><span class="sxs-lookup"><span data-stu-id="a4e00-232">/ifd/exif/{ushort=37521}</span></span>            |
| <span data-ttu-id="a4e00-233">3</span><span class="sxs-lookup"><span data-stu-id="a4e00-233">3</span></span>     | <span data-ttu-id="a4e00-234">/IFD/EXIF/{UShort = 36868}</span><span class="sxs-lookup"><span data-stu-id="a4e00-234">/ifd/exif/{ushort=36868}</span></span>            |
| <span data-ttu-id="a4e00-235">4</span><span class="sxs-lookup"><span data-stu-id="a4e00-235">4</span></span>     | <span data-ttu-id="a4e00-236">/IFD/EXIF/{UShort = 37522}</span><span class="sxs-lookup"><span data-stu-id="a4e00-236">/ifd/exif/{ushort=37522}</span></span>            |
| <span data-ttu-id="a4e00-237">5</span><span class="sxs-lookup"><span data-stu-id="a4e00-237">5</span></span>     | <span data-ttu-id="a4e00-238">/ifd/xmp/exif:DateTimeOriginal</span><span class="sxs-lookup"><span data-stu-id="a4e00-238">/ifd/xmp/exif:DateTimeOriginal</span></span>      |
| <span data-ttu-id="a4e00-239">6</span><span class="sxs-lookup"><span data-stu-id="a4e00-239">6</span></span>     | <span data-ttu-id="a4e00-240">/IFD/XMP/XMP: CreateDate</span><span class="sxs-lookup"><span data-stu-id="a4e00-240">/ifd/xmp/xmp:CreateDate</span></span>             |
| <span data-ttu-id="a4e00-241">7</span><span class="sxs-lookup"><span data-stu-id="a4e00-241">7</span></span>     | <span data-ttu-id="a4e00-242">/IFD/IPTC/Date criado</span><span class="sxs-lookup"><span data-stu-id="a4e00-242">/ifd/iptc/date created</span></span>              |
| <span data-ttu-id="a4e00-243">8</span><span class="sxs-lookup"><span data-stu-id="a4e00-243">8</span></span>     | <span data-ttu-id="a4e00-244">/IFD/IPTC/time criado</span><span class="sxs-lookup"><span data-stu-id="a4e00-244">/ifd/iptc/time created</span></span>              |
| <span data-ttu-id="a4e00-245">9</span><span class="sxs-lookup"><span data-stu-id="a4e00-245">9</span></span>     | <span data-ttu-id="a4e00-246">/IFD/IRB/8bimiptc/IPTC/Date criado</span><span class="sxs-lookup"><span data-stu-id="a4e00-246">/ifd/irb/8bimiptc/iptc/date created</span></span> |
| <span data-ttu-id="a4e00-247">10</span><span class="sxs-lookup"><span data-stu-id="a4e00-247">10</span></span>    | <span data-ttu-id="a4e00-248">/IFD/IRB/8bimiptc/IPTC/time criado</span><span class="sxs-lookup"><span data-stu-id="a4e00-248">/ifd/irb/8bimiptc/iptc/time created</span></span> |



 

### <a name="png-policy"></a><span data-ttu-id="a4e00-249">Política de PNG</span><span class="sxs-lookup"><span data-stu-id="a4e00-249">PNG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a4e00-250">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="a4e00-250">Read Paths</span></span>



| <span data-ttu-id="a4e00-251">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4e00-251">Order</span></span> | <span data-ttu-id="a4e00-252">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4e00-252">Path</span></span>                      | <span data-ttu-id="a4e00-253">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a4e00-253">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="a4e00-254">1</span><span class="sxs-lookup"><span data-stu-id="a4e00-254">1</span></span>     | <span data-ttu-id="a4e00-255">/\[\*\]Texto/hora de criação</span><span class="sxs-lookup"><span data-stu-id="a4e00-255">/\[\*\]tEXt/Creation Time</span></span> | <span data-ttu-id="a4e00-256">ascii</span><span class="sxs-lookup"><span data-stu-id="a4e00-256">ascii</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="a4e00-257">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="a4e00-257">Write Paths</span></span>



| <span data-ttu-id="a4e00-258">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4e00-258">Order</span></span> | <span data-ttu-id="a4e00-259">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4e00-259">Path</span></span>                      | <span data-ttu-id="a4e00-260">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a4e00-260">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="a4e00-261">2</span><span class="sxs-lookup"><span data-stu-id="a4e00-261">2</span></span>     | <span data-ttu-id="a4e00-262">/\[\*\]Texto/hora de criação</span><span class="sxs-lookup"><span data-stu-id="a4e00-262">/\[\*\]tEXt/Creation Time</span></span> | <span data-ttu-id="a4e00-263">ascii</span><span class="sxs-lookup"><span data-stu-id="a4e00-263">ascii</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="a4e00-264">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="a4e00-264">Remove Paths</span></span>



| <span data-ttu-id="a4e00-265">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4e00-265">Order</span></span> | <span data-ttu-id="a4e00-266">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4e00-266">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="a4e00-267">3</span><span class="sxs-lookup"><span data-stu-id="a4e00-267">3</span></span>     | <span data-ttu-id="a4e00-268">/\[\*\]Texto/hora de criação</span><span class="sxs-lookup"><span data-stu-id="a4e00-268">/\[\*\]tEXt/Creation Time</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a4e00-269">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4e00-269">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4e00-270">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4e00-270">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4e00-271">System. Photo. DateTaken</span><span class="sxs-lookup"><span data-stu-id="a4e00-271">System.Photo.DateTaken</span></span>](../properties/props-system-photo-datetaken.md)
</dt> </dl>

 

 
