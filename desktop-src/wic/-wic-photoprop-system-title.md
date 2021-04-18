---
description: A política de metadados de foto para a propriedade System. Title.
ms.assetid: 84da345e-ec03-48fe-8fda-043b706e4e1c
title: Política de metadados de foto System. title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b02513f3f566576999e83b09c156d36ac480c17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786154"
---
# <a name="systemtitle-photo-metadata-policy"></a><span data-ttu-id="d2320-103">Política de metadados de foto System. title</span><span class="sxs-lookup"><span data-stu-id="d2320-103">System.Title Photo Metadata Policy</span></span>

<span data-ttu-id="d2320-104">A política de metadados de foto para a propriedade [System. title](../properties/props-system-title.md) .</span><span class="sxs-lookup"><span data-stu-id="d2320-104">The photo metadata policy for the [System.Title](../properties/props-system-title.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d2320-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="d2320-105">PKEY</span></span>

<span data-ttu-id="d2320-106">Título do PKEY \_</span><span class="sxs-lookup"><span data-stu-id="d2320-106">PKEY\_Title</span></span>

### <a name="containers"></a><span data-ttu-id="d2320-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="d2320-107">Containers</span></span>

<span data-ttu-id="d2320-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d2320-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d2320-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d2320-109">Read-Only</span></span>

<span data-ttu-id="d2320-110">No</span><span class="sxs-lookup"><span data-stu-id="d2320-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d2320-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="d2320-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d2320-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="d2320-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="d2320-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="d2320-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="d2320-114">Um VT \_ LPWSTR ou VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="d2320-114">Either VT\_LPWSTR or VT\_LPSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d2320-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="d2320-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="d2320-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="d2320-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="d2320-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="d2320-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d2320-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="d2320-118">Read Paths</span></span>



| <span data-ttu-id="d2320-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="d2320-119">Order</span></span> | <span data-ttu-id="d2320-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="d2320-120">Path</span></span>                                | <span data-ttu-id="d2320-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d2320-121">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="d2320-122">1</span><span class="sxs-lookup"><span data-stu-id="d2320-122">1</span></span>     | <span data-ttu-id="d2320-123">/App1/IFD/{UShort = 40091}</span><span class="sxs-lookup"><span data-stu-id="d2320-123">/app1/ifd/{ushort=40091}</span></span>            | <span data-ttu-id="d2320-124">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-124">unicode\_bytes</span></span> |
| <span data-ttu-id="d2320-125">2</span><span class="sxs-lookup"><span data-stu-id="d2320-125">2</span></span>     | <span data-ttu-id="d2320-126">/XMP/ <xmpalt> DC: title</span><span class="sxs-lookup"><span data-stu-id="d2320-126">/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="d2320-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-127">unicode</span></span>        |
| <span data-ttu-id="d2320-128">3</span><span class="sxs-lookup"><span data-stu-id="d2320-128">3</span></span>     | <span data-ttu-id="d2320-129">/XMP/DC: título</span><span class="sxs-lookup"><span data-stu-id="d2320-129">/xmp/dc:title</span></span>                       | <span data-ttu-id="d2320-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-130">unicode</span></span>        |
| <span data-ttu-id="d2320-131">4</span><span class="sxs-lookup"><span data-stu-id="d2320-131">4</span></span>     | <span data-ttu-id="d2320-132">/App1/IFD/EXIF/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="d2320-132">/app1/ifd/exif/{ushort=37510}</span></span>       | <span data-ttu-id="d2320-133">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-133">unicode</span></span>        |
| <span data-ttu-id="d2320-134">5</span><span class="sxs-lookup"><span data-stu-id="d2320-134">5</span></span>     | <span data-ttu-id="d2320-135">/App1/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="d2320-135">/app1/ifd/{ushort=270}</span></span>              | <span data-ttu-id="d2320-136">ascii</span><span class="sxs-lookup"><span data-stu-id="d2320-136">ascii</span></span>          |
| <span data-ttu-id="d2320-137">6</span><span class="sxs-lookup"><span data-stu-id="d2320-137">6</span></span>     | <span data-ttu-id="d2320-138">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="d2320-138">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="d2320-139">7</span><span class="sxs-lookup"><span data-stu-id="d2320-139">7</span></span>     | <span data-ttu-id="d2320-140">/XMP/ <xmpalt> DC: Descrição</span><span class="sxs-lookup"><span data-stu-id="d2320-140">/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="d2320-141">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-141">unicode</span></span>        |
| <span data-ttu-id="d2320-142">8</span><span class="sxs-lookup"><span data-stu-id="d2320-142">8</span></span>     | <span data-ttu-id="d2320-143">/XMP/DC: Descrição</span><span class="sxs-lookup"><span data-stu-id="d2320-143">/xmp/dc:description</span></span>                 | <span data-ttu-id="d2320-144">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-144">unicode</span></span>        |
| <span data-ttu-id="d2320-145">9</span><span class="sxs-lookup"><span data-stu-id="d2320-145">9</span></span>     | <span data-ttu-id="d2320-146">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="d2320-146">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="d2320-147">10</span><span class="sxs-lookup"><span data-stu-id="d2320-147">10</span></span>    | <span data-ttu-id="d2320-148">/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="d2320-148">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="d2320-149">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-149">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="d2320-150">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="d2320-150">Write Paths</span></span>



| <span data-ttu-id="d2320-151">Ordem</span><span class="sxs-lookup"><span data-stu-id="d2320-151">Order</span></span> | <span data-ttu-id="d2320-152">Caminho</span><span class="sxs-lookup"><span data-stu-id="d2320-152">Path</span></span>                                | <span data-ttu-id="d2320-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d2320-153">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="d2320-154">1</span><span class="sxs-lookup"><span data-stu-id="d2320-154">1</span></span>     | <span data-ttu-id="d2320-155">/App1/IFD/{UShort = 40091}</span><span class="sxs-lookup"><span data-stu-id="d2320-155">/app1/ifd/{ushort=40091}</span></span>            | <span data-ttu-id="d2320-156">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-156">unicode\_bytes</span></span> |
| <span data-ttu-id="d2320-157">2</span><span class="sxs-lookup"><span data-stu-id="d2320-157">2</span></span>     | <span data-ttu-id="d2320-158">/XMP/DC: título</span><span class="sxs-lookup"><span data-stu-id="d2320-158">/xmp/dc:title</span></span>                       | <span data-ttu-id="d2320-159">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-159">unicode</span></span>        |
| <span data-ttu-id="d2320-160">3</span><span class="sxs-lookup"><span data-stu-id="d2320-160">3</span></span>     | <span data-ttu-id="d2320-161">/XMP/ <xmpalt> DC: title</span><span class="sxs-lookup"><span data-stu-id="d2320-161">/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="d2320-162">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-162">unicode</span></span>        |
| <span data-ttu-id="d2320-163">4</span><span class="sxs-lookup"><span data-stu-id="d2320-163">4</span></span>     | <span data-ttu-id="d2320-164">/App1/IFD/EXIF/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="d2320-164">/app1/ifd/exif/{ushort=37510}</span></span>       | <span data-ttu-id="d2320-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-165">unicode</span></span>        |
| <span data-ttu-id="d2320-166">5</span><span class="sxs-lookup"><span data-stu-id="d2320-166">5</span></span>     | <span data-ttu-id="d2320-167">/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="d2320-167">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="d2320-168">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-168">unicode</span></span>        |
| <span data-ttu-id="d2320-169">6</span><span class="sxs-lookup"><span data-stu-id="d2320-169">6</span></span>     | <span data-ttu-id="d2320-170">/App1/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="d2320-170">/app1/ifd/{ushort=270}</span></span>              | <span data-ttu-id="d2320-171">ascii</span><span class="sxs-lookup"><span data-stu-id="d2320-171">ascii</span></span>          |
| <span data-ttu-id="d2320-172">7</span><span class="sxs-lookup"><span data-stu-id="d2320-172">7</span></span>     | <span data-ttu-id="d2320-173">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="d2320-173">/app13/irb/8bimiptc/iptc/caption</span></span>    |                |
| <span data-ttu-id="d2320-174">8</span><span class="sxs-lookup"><span data-stu-id="d2320-174">8</span></span>     | <span data-ttu-id="d2320-175">/XMP/DC: Descrição</span><span class="sxs-lookup"><span data-stu-id="d2320-175">/xmp/dc:description</span></span>                 | <span data-ttu-id="d2320-176">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-176">unicode</span></span>        |
| <span data-ttu-id="d2320-177">9</span><span class="sxs-lookup"><span data-stu-id="d2320-177">9</span></span>     | <span data-ttu-id="d2320-178">/XMP/ <xmpalt> DC: Descrição</span><span class="sxs-lookup"><span data-stu-id="d2320-178">/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="d2320-179">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-179">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="d2320-180">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="d2320-180">Remove Paths</span></span>



| <span data-ttu-id="d2320-181">Ordem</span><span class="sxs-lookup"><span data-stu-id="d2320-181">Order</span></span> | <span data-ttu-id="d2320-182">Caminho</span><span class="sxs-lookup"><span data-stu-id="d2320-182">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="d2320-183">1</span><span class="sxs-lookup"><span data-stu-id="d2320-183">1</span></span>     | <span data-ttu-id="d2320-184">/App1/IFD/{UShort = 40091}</span><span class="sxs-lookup"><span data-stu-id="d2320-184">/app1/ifd/{ushort=40091}</span></span>            |
| <span data-ttu-id="d2320-185">2</span><span class="sxs-lookup"><span data-stu-id="d2320-185">2</span></span>     | <span data-ttu-id="d2320-186">/XMP/DC: título</span><span class="sxs-lookup"><span data-stu-id="d2320-186">/xmp/dc:title</span></span>                       |
| <span data-ttu-id="d2320-187">3</span><span class="sxs-lookup"><span data-stu-id="d2320-187">3</span></span>     | <span data-ttu-id="d2320-188">/App1/IFD/EXIF/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="d2320-188">/app1/ifd/exif/{ushort=37510}</span></span>       |
| <span data-ttu-id="d2320-189">4</span><span class="sxs-lookup"><span data-stu-id="d2320-189">4</span></span>     | <span data-ttu-id="d2320-190">/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="d2320-190">/xmp/<xmpalt>exif:UserComment</span></span> |
| <span data-ttu-id="d2320-191">5</span><span class="sxs-lookup"><span data-stu-id="d2320-191">5</span></span>     | <span data-ttu-id="d2320-192">/App1/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="d2320-192">/app1/ifd/{ushort=270}</span></span>              |
| <span data-ttu-id="d2320-193">6</span><span class="sxs-lookup"><span data-stu-id="d2320-193">6</span></span>     | <span data-ttu-id="d2320-194">/app13/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="d2320-194">/app13/irb/8bimiptc/iptc/caption</span></span>    |
| <span data-ttu-id="d2320-195">7</span><span class="sxs-lookup"><span data-stu-id="d2320-195">7</span></span>     | <span data-ttu-id="d2320-196">/XMP/DC: Descrição</span><span class="sxs-lookup"><span data-stu-id="d2320-196">/xmp/dc:description</span></span>                 |



 

### <a name="tiff-policy"></a><span data-ttu-id="d2320-197">Política TIFF</span><span class="sxs-lookup"><span data-stu-id="d2320-197">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d2320-198">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="d2320-198">Read Paths</span></span>



| <span data-ttu-id="d2320-199">Ordem</span><span class="sxs-lookup"><span data-stu-id="d2320-199">Order</span></span> | <span data-ttu-id="d2320-200">Caminho</span><span class="sxs-lookup"><span data-stu-id="d2320-200">Path</span></span>                                    | <span data-ttu-id="d2320-201">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d2320-201">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="d2320-202">1</span><span class="sxs-lookup"><span data-stu-id="d2320-202">1</span></span>     | <span data-ttu-id="d2320-203">/IFD/{UShort = 40091}</span><span class="sxs-lookup"><span data-stu-id="d2320-203">/ifd/{ushort=40091}</span></span>                     | <span data-ttu-id="d2320-204">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-204">unicode\_bytes</span></span> |
| <span data-ttu-id="d2320-205">2</span><span class="sxs-lookup"><span data-stu-id="d2320-205">2</span></span>     | <span data-ttu-id="d2320-206">/IFD/XMP/ <xmpalt> DC: title</span><span class="sxs-lookup"><span data-stu-id="d2320-206">/ifd/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="d2320-207">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-207">unicode</span></span>        |
| <span data-ttu-id="d2320-208">3</span><span class="sxs-lookup"><span data-stu-id="d2320-208">3</span></span>     | <span data-ttu-id="d2320-209">/IFD/XMP/DC: título</span><span class="sxs-lookup"><span data-stu-id="d2320-209">/ifd/xmp/dc:title</span></span>                       | <span data-ttu-id="d2320-210">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-210">unicode</span></span>        |
| <span data-ttu-id="d2320-211">4</span><span class="sxs-lookup"><span data-stu-id="d2320-211">4</span></span>     | <span data-ttu-id="d2320-212">/IFD/EXIF/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="d2320-212">/ifd/exif/{ushort=37510}</span></span>                | <span data-ttu-id="d2320-213">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-213">unicode</span></span>        |
| <span data-ttu-id="d2320-214">5</span><span class="sxs-lookup"><span data-stu-id="d2320-214">5</span></span>     | <span data-ttu-id="d2320-215">/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="d2320-215">/ifd/{ushort=270}</span></span>                       | <span data-ttu-id="d2320-216">ascii</span><span class="sxs-lookup"><span data-stu-id="d2320-216">ascii</span></span>          |
| <span data-ttu-id="d2320-217">6</span><span class="sxs-lookup"><span data-stu-id="d2320-217">6</span></span>     | <span data-ttu-id="d2320-218">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="d2320-218">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="d2320-219">7</span><span class="sxs-lookup"><span data-stu-id="d2320-219">7</span></span>     | <span data-ttu-id="d2320-220">/IFD/XMP/ <xmpalt> DC: Descrição</span><span class="sxs-lookup"><span data-stu-id="d2320-220">/ifd/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="d2320-221">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-221">unicode</span></span>        |
| <span data-ttu-id="d2320-222">8</span><span class="sxs-lookup"><span data-stu-id="d2320-222">8</span></span>     | <span data-ttu-id="d2320-223">/IFD/XMP/DC: Descrição</span><span class="sxs-lookup"><span data-stu-id="d2320-223">/ifd/xmp/dc:description</span></span>                 | <span data-ttu-id="d2320-224">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-224">unicode</span></span>        |
| <span data-ttu-id="d2320-225">9</span><span class="sxs-lookup"><span data-stu-id="d2320-225">9</span></span>     | <span data-ttu-id="d2320-226">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="d2320-226">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="d2320-227">10</span><span class="sxs-lookup"><span data-stu-id="d2320-227">10</span></span>    | <span data-ttu-id="d2320-228">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="d2320-228">/ifd/irb/8bimiptc/iptc/caption</span></span>          |                |
| <span data-ttu-id="d2320-229">11</span><span class="sxs-lookup"><span data-stu-id="d2320-229">11</span></span>    | <span data-ttu-id="d2320-230">/IFD/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="d2320-230">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="d2320-231">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-231">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="d2320-232">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="d2320-232">Write Paths</span></span>



| <span data-ttu-id="d2320-233">Ordem</span><span class="sxs-lookup"><span data-stu-id="d2320-233">Order</span></span> | <span data-ttu-id="d2320-234">Caminho</span><span class="sxs-lookup"><span data-stu-id="d2320-234">Path</span></span>                                    | <span data-ttu-id="d2320-235">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d2320-235">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="d2320-236">1</span><span class="sxs-lookup"><span data-stu-id="d2320-236">1</span></span>     | <span data-ttu-id="d2320-237">/IFD/{UShort = 40091}</span><span class="sxs-lookup"><span data-stu-id="d2320-237">/ifd/{ushort=40091}</span></span>                     | <span data-ttu-id="d2320-238">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-238">unicode\_bytes</span></span> |
| <span data-ttu-id="d2320-239">2</span><span class="sxs-lookup"><span data-stu-id="d2320-239">2</span></span>     | <span data-ttu-id="d2320-240">/IFD/XMP/DC: título</span><span class="sxs-lookup"><span data-stu-id="d2320-240">/ifd/xmp/dc:title</span></span>                       | <span data-ttu-id="d2320-241">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-241">unicode</span></span>        |
| <span data-ttu-id="d2320-242">3</span><span class="sxs-lookup"><span data-stu-id="d2320-242">3</span></span>     | <span data-ttu-id="d2320-243">/IFD/XMP/ <xmpalt> DC: title</span><span class="sxs-lookup"><span data-stu-id="d2320-243">/ifd/xmp/<xmpalt>dc:title</span></span>         | <span data-ttu-id="d2320-244">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-244">unicode</span></span>        |
| <span data-ttu-id="d2320-245">4</span><span class="sxs-lookup"><span data-stu-id="d2320-245">4</span></span>     | <span data-ttu-id="d2320-246">/IFD/EXIF/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="d2320-246">/ifd/exif/{ushort=37510}</span></span>                | <span data-ttu-id="d2320-247">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-247">unicode</span></span>        |
| <span data-ttu-id="d2320-248">5</span><span class="sxs-lookup"><span data-stu-id="d2320-248">5</span></span>     | <span data-ttu-id="d2320-249">/IFD/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="d2320-249">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="d2320-250">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-250">unicode</span></span>        |
| <span data-ttu-id="d2320-251">6</span><span class="sxs-lookup"><span data-stu-id="d2320-251">6</span></span>     | <span data-ttu-id="d2320-252">/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="d2320-252">/ifd/{ushort=270}</span></span>                       | <span data-ttu-id="d2320-253">ascii</span><span class="sxs-lookup"><span data-stu-id="d2320-253">ascii</span></span>          |
| <span data-ttu-id="d2320-254">7</span><span class="sxs-lookup"><span data-stu-id="d2320-254">7</span></span>     | <span data-ttu-id="d2320-255">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="d2320-255">/ifd/iptc/caption</span></span>                       |                |
| <span data-ttu-id="d2320-256">8</span><span class="sxs-lookup"><span data-stu-id="d2320-256">8</span></span>     | <span data-ttu-id="d2320-257">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="d2320-257">/ifd/irb/8bimiptc/iptc/caption</span></span>          |                |
| <span data-ttu-id="d2320-258">9</span><span class="sxs-lookup"><span data-stu-id="d2320-258">9</span></span>     | <span data-ttu-id="d2320-259">/IFD/XMP/DC: Descrição</span><span class="sxs-lookup"><span data-stu-id="d2320-259">/ifd/xmp/dc:description</span></span>                 | <span data-ttu-id="d2320-260">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-260">unicode</span></span>        |
| <span data-ttu-id="d2320-261">10</span><span class="sxs-lookup"><span data-stu-id="d2320-261">10</span></span>    | <span data-ttu-id="d2320-262">/IFD/XMP/ <xmpalt> DC: Descrição</span><span class="sxs-lookup"><span data-stu-id="d2320-262">/ifd/xmp/<xmpalt>dc:description</span></span>   | <span data-ttu-id="d2320-263">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2320-263">unicode</span></span>        |



 

### <a name="remove-paths"></a><span data-ttu-id="d2320-264">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="d2320-264">Remove Paths</span></span>



| <span data-ttu-id="d2320-265">Ordem</span><span class="sxs-lookup"><span data-stu-id="d2320-265">Order</span></span> | <span data-ttu-id="d2320-266">Caminho</span><span class="sxs-lookup"><span data-stu-id="d2320-266">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="d2320-267">1</span><span class="sxs-lookup"><span data-stu-id="d2320-267">1</span></span>     | <span data-ttu-id="d2320-268">/IFD/{UShort = 40091}</span><span class="sxs-lookup"><span data-stu-id="d2320-268">/ifd/{ushort=40091}</span></span>                     |
| <span data-ttu-id="d2320-269">2</span><span class="sxs-lookup"><span data-stu-id="d2320-269">2</span></span>     | <span data-ttu-id="d2320-270">/IFD/XMP/DC: título</span><span class="sxs-lookup"><span data-stu-id="d2320-270">/ifd/xmp/dc:title</span></span>                       |
| <span data-ttu-id="d2320-271">3</span><span class="sxs-lookup"><span data-stu-id="d2320-271">3</span></span>     | <span data-ttu-id="d2320-272">/IFD/EXIF/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="d2320-272">/ifd/exif/{ushort=37510}</span></span>                |
| <span data-ttu-id="d2320-273">4</span><span class="sxs-lookup"><span data-stu-id="d2320-273">4</span></span>     | <span data-ttu-id="d2320-274">/IFD/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="d2320-274">/ifd/xmp/<xmpalt>exif:UserComment</span></span> |
| <span data-ttu-id="d2320-275">5</span><span class="sxs-lookup"><span data-stu-id="d2320-275">5</span></span>     | <span data-ttu-id="d2320-276">/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="d2320-276">/ifd/{ushort=270}</span></span>                       |
| <span data-ttu-id="d2320-277">6</span><span class="sxs-lookup"><span data-stu-id="d2320-277">6</span></span>     | <span data-ttu-id="d2320-278">/ifd/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="d2320-278">/ifd/iptc/caption</span></span>                       |
| <span data-ttu-id="d2320-279">7</span><span class="sxs-lookup"><span data-stu-id="d2320-279">7</span></span>     | <span data-ttu-id="d2320-280">/ifd/irb/8bimiptc/iptc/caption</span><span class="sxs-lookup"><span data-stu-id="d2320-280">/ifd/irb/8bimiptc/iptc/caption</span></span>          |
| <span data-ttu-id="d2320-281">8</span><span class="sxs-lookup"><span data-stu-id="d2320-281">8</span></span>     | <span data-ttu-id="d2320-282">/IFD/XMP/DC: Descrição</span><span class="sxs-lookup"><span data-stu-id="d2320-282">/ifd/xmp/dc:description</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="d2320-283">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2320-283">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2320-284">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d2320-284">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2320-285">System.Title</span><span class="sxs-lookup"><span data-stu-id="d2320-285">System.Title</span></span>](../properties/props-system-title.md)
</dt> </dl>

 

 
