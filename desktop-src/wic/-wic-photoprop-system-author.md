---
description: A política de metadados de foto para a propriedade System. Author.
ms.assetid: 2de9c452-93be-40a4-a72b-5da590534dfd
title: Política de metadados de fotos do System. Author
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb90345257ef1623f7cda1ce4318af7a9f472df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105795467"
---
# <a name="systemauthor-photo-metadata-policy"></a><span data-ttu-id="23bd1-103">Política de metadados de fotos do System. Author</span><span class="sxs-lookup"><span data-stu-id="23bd1-103">System.Author Photo Metadata Policy</span></span>

<span data-ttu-id="23bd1-104">A política de metadados de foto para a propriedade [System. Author](../properties/props-system-author.md) .</span><span class="sxs-lookup"><span data-stu-id="23bd1-104">The photo metadata policy for the [System.Author](../properties/props-system-author.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="23bd1-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="23bd1-105">PKEY</span></span>

<span data-ttu-id="23bd1-106">Autor do PKEY \_</span><span class="sxs-lookup"><span data-stu-id="23bd1-106">PKEY\_Author</span></span>

### <a name="containers"></a><span data-ttu-id="23bd1-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="23bd1-107">Containers</span></span>

<span data-ttu-id="23bd1-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="23bd1-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="23bd1-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="23bd1-109">Read-Only</span></span>

<span data-ttu-id="23bd1-110">No</span><span class="sxs-lookup"><span data-stu-id="23bd1-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="23bd1-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="23bd1-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="23bd1-112">\_LPWStr do vetor VT VT \| \_</span><span class="sxs-lookup"><span data-stu-id="23bd1-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="23bd1-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="23bd1-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="23bd1-114">O \_ \| LPWSTR de vetor VT do VT \_ é preferencial, mas o o LPWStr do VT \_ também é aceito.</span><span class="sxs-lookup"><span data-stu-id="23bd1-114">VT\_VECTOR \| VT\_LPWSTR is preferred, but VT\_LPWSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="23bd1-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="23bd1-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="23bd1-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="23bd1-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="23bd1-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="23bd1-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="23bd1-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="23bd1-118">Read Paths</span></span>



| <span data-ttu-id="23bd1-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="23bd1-119">Order</span></span> | <span data-ttu-id="23bd1-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="23bd1-120">Path</span></span>                             | <span data-ttu-id="23bd1-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="23bd1-121">Disk Format</span></span>    |
|-------|----------------------------------|----------------|
| <span data-ttu-id="23bd1-122">1</span><span class="sxs-lookup"><span data-stu-id="23bd1-122">1</span></span>     | <span data-ttu-id="23bd1-123">/App1/IFD/{UShort = 315}</span><span class="sxs-lookup"><span data-stu-id="23bd1-123">/app1/ifd/{ushort=315}</span></span>           | <span data-ttu-id="23bd1-124">ascii</span><span class="sxs-lookup"><span data-stu-id="23bd1-124">ascii</span></span>          |
| <span data-ttu-id="23bd1-125">2</span><span class="sxs-lookup"><span data-stu-id="23bd1-125">2</span></span>     | <span data-ttu-id="23bd1-126">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="23bd1-126">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="23bd1-127">3</span><span class="sxs-lookup"><span data-stu-id="23bd1-127">3</span></span>     | <span data-ttu-id="23bd1-128">/XMP/ <xmpseq> DC: Creator</span><span class="sxs-lookup"><span data-stu-id="23bd1-128">/xmp/<xmpseq>dc:creator</span></span>    | <span data-ttu-id="23bd1-129">Unicode</span><span class="sxs-lookup"><span data-stu-id="23bd1-129">unicode</span></span>        |
| <span data-ttu-id="23bd1-130">4</span><span class="sxs-lookup"><span data-stu-id="23bd1-130">4</span></span>     | <span data-ttu-id="23bd1-131">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="23bd1-131">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="23bd1-132">5</span><span class="sxs-lookup"><span data-stu-id="23bd1-132">5</span></span>     | <span data-ttu-id="23bd1-133">/App1/IFD/{UShort = 40093}</span><span class="sxs-lookup"><span data-stu-id="23bd1-133">/app1/ifd/{ushort=40093}</span></span>         | <span data-ttu-id="23bd1-134">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="23bd1-134">unicode\_bytes</span></span> |
| <span data-ttu-id="23bd1-135">6</span><span class="sxs-lookup"><span data-stu-id="23bd1-135">6</span></span>     | <span data-ttu-id="23bd1-136">/XMP/TIFF: artista</span><span class="sxs-lookup"><span data-stu-id="23bd1-136">/xmp/tiff:artist</span></span>                 | <span data-ttu-id="23bd1-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="23bd1-137">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="23bd1-138">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="23bd1-138">Write Paths</span></span>



| <span data-ttu-id="23bd1-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="23bd1-139">Order</span></span> | <span data-ttu-id="23bd1-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="23bd1-140">Path</span></span>                             | <span data-ttu-id="23bd1-141">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="23bd1-141">Disk Format</span></span>    |
|-------|----------------------------------|----------------|
| <span data-ttu-id="23bd1-142">1</span><span class="sxs-lookup"><span data-stu-id="23bd1-142">1</span></span>     | <span data-ttu-id="23bd1-143">/XMP/ <xmpseq> DC: Creator</span><span class="sxs-lookup"><span data-stu-id="23bd1-143">/xmp/<xmpseq>dc:creator</span></span>    | <span data-ttu-id="23bd1-144">Unicode</span><span class="sxs-lookup"><span data-stu-id="23bd1-144">unicode</span></span>        |
| <span data-ttu-id="23bd1-145">2</span><span class="sxs-lookup"><span data-stu-id="23bd1-145">2</span></span>     | <span data-ttu-id="23bd1-146">/XMP/TIFF: artista</span><span class="sxs-lookup"><span data-stu-id="23bd1-146">/xmp/tiff:artist</span></span>                 | <span data-ttu-id="23bd1-147">Unicode</span><span class="sxs-lookup"><span data-stu-id="23bd1-147">unicode</span></span>        |
| <span data-ttu-id="23bd1-148">3</span><span class="sxs-lookup"><span data-stu-id="23bd1-148">3</span></span>     | <span data-ttu-id="23bd1-149">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="23bd1-149">/app13/irb/8bimiptc/iptc/by-line</span></span> |                |
| <span data-ttu-id="23bd1-150">4</span><span class="sxs-lookup"><span data-stu-id="23bd1-150">4</span></span>     | <span data-ttu-id="23bd1-151">/App1/IFD/{UShort = 315}</span><span class="sxs-lookup"><span data-stu-id="23bd1-151">/app1/ifd/{ushort=315}</span></span>           | <span data-ttu-id="23bd1-152">ascii</span><span class="sxs-lookup"><span data-stu-id="23bd1-152">ascii</span></span>          |
| <span data-ttu-id="23bd1-153">5</span><span class="sxs-lookup"><span data-stu-id="23bd1-153">5</span></span>     | <span data-ttu-id="23bd1-154">/App1/IFD/{UShort = 40093}</span><span class="sxs-lookup"><span data-stu-id="23bd1-154">/app1/ifd/{ushort=40093}</span></span>         | <span data-ttu-id="23bd1-155">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="23bd1-155">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="23bd1-156">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="23bd1-156">Remove Paths</span></span>



| <span data-ttu-id="23bd1-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="23bd1-157">Order</span></span> | <span data-ttu-id="23bd1-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="23bd1-158">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="23bd1-159">1</span><span class="sxs-lookup"><span data-stu-id="23bd1-159">1</span></span>     | <span data-ttu-id="23bd1-160">/XMP/DC: criador</span><span class="sxs-lookup"><span data-stu-id="23bd1-160">/xmp/dc:creator</span></span>                  |
| <span data-ttu-id="23bd1-161">2</span><span class="sxs-lookup"><span data-stu-id="23bd1-161">2</span></span>     | <span data-ttu-id="23bd1-162">/XMP/TIFF: artista</span><span class="sxs-lookup"><span data-stu-id="23bd1-162">/xmp/tiff:artist</span></span>                 |
| <span data-ttu-id="23bd1-163">3</span><span class="sxs-lookup"><span data-stu-id="23bd1-163">3</span></span>     | <span data-ttu-id="23bd1-164">/app13/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="23bd1-164">/app13/irb/8bimiptc/iptc/by-line</span></span> |
| <span data-ttu-id="23bd1-165">4</span><span class="sxs-lookup"><span data-stu-id="23bd1-165">4</span></span>     | <span data-ttu-id="23bd1-166">/App1/IFD/{UShort = 315}</span><span class="sxs-lookup"><span data-stu-id="23bd1-166">/app1/ifd/{ushort=315}</span></span>           |
| <span data-ttu-id="23bd1-167">5</span><span class="sxs-lookup"><span data-stu-id="23bd1-167">5</span></span>     | <span data-ttu-id="23bd1-168">/App1/IFD/{UShort = 40093}</span><span class="sxs-lookup"><span data-stu-id="23bd1-168">/app1/ifd/{ushort=40093}</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="23bd1-169">Política TIFF</span><span class="sxs-lookup"><span data-stu-id="23bd1-169">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="23bd1-170">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="23bd1-170">Read Paths</span></span>



| <span data-ttu-id="23bd1-171">Ordem</span><span class="sxs-lookup"><span data-stu-id="23bd1-171">Order</span></span> | <span data-ttu-id="23bd1-172">Caminho</span><span class="sxs-lookup"><span data-stu-id="23bd1-172">Path</span></span>                              | <span data-ttu-id="23bd1-173">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="23bd1-173">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="23bd1-174">1</span><span class="sxs-lookup"><span data-stu-id="23bd1-174">1</span></span>     | <span data-ttu-id="23bd1-175">/IFD/{UShort = 315}</span><span class="sxs-lookup"><span data-stu-id="23bd1-175">/ifd/{ushort=315}</span></span>                 | <span data-ttu-id="23bd1-176">ascii</span><span class="sxs-lookup"><span data-stu-id="23bd1-176">ascii</span></span>          |
| <span data-ttu-id="23bd1-177">2</span><span class="sxs-lookup"><span data-stu-id="23bd1-177">2</span></span>     | <span data-ttu-id="23bd1-178">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="23bd1-178">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="23bd1-179">3</span><span class="sxs-lookup"><span data-stu-id="23bd1-179">3</span></span>     | <span data-ttu-id="23bd1-180">/IFD/XMP/ <xmpseq> DC: Creator</span><span class="sxs-lookup"><span data-stu-id="23bd1-180">/ifd/xmp/<xmpseq>dc:creator</span></span> | <span data-ttu-id="23bd1-181">Unicode</span><span class="sxs-lookup"><span data-stu-id="23bd1-181">unicode</span></span>        |
| <span data-ttu-id="23bd1-182">4</span><span class="sxs-lookup"><span data-stu-id="23bd1-182">4</span></span>     | <span data-ttu-id="23bd1-183">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="23bd1-183">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="23bd1-184">5</span><span class="sxs-lookup"><span data-stu-id="23bd1-184">5</span></span>     | <span data-ttu-id="23bd1-185">/IFD/{UShort = 40093}</span><span class="sxs-lookup"><span data-stu-id="23bd1-185">/ifd/{ushort=40093}</span></span>               | <span data-ttu-id="23bd1-186">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="23bd1-186">unicode\_bytes</span></span> |
| <span data-ttu-id="23bd1-187">6</span><span class="sxs-lookup"><span data-stu-id="23bd1-187">6</span></span>     | <span data-ttu-id="23bd1-188">/ifd/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="23bd1-188">/ifd/irb/8bimiptc/iptc/by-line</span></span>    |                |
| <span data-ttu-id="23bd1-189">7</span><span class="sxs-lookup"><span data-stu-id="23bd1-189">7</span></span>     | <span data-ttu-id="23bd1-190">/IFD/XMP/TIFF: artista</span><span class="sxs-lookup"><span data-stu-id="23bd1-190">/ifd/xmp/tiff:artist</span></span>              | <span data-ttu-id="23bd1-191">Unicode</span><span class="sxs-lookup"><span data-stu-id="23bd1-191">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="23bd1-192">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="23bd1-192">Write Paths</span></span>



| <span data-ttu-id="23bd1-193">Ordem</span><span class="sxs-lookup"><span data-stu-id="23bd1-193">Order</span></span> | <span data-ttu-id="23bd1-194">Caminho</span><span class="sxs-lookup"><span data-stu-id="23bd1-194">Path</span></span>                              | <span data-ttu-id="23bd1-195">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="23bd1-195">Disk Format</span></span>    |
|-------|-----------------------------------|----------------|
| <span data-ttu-id="23bd1-196">1</span><span class="sxs-lookup"><span data-stu-id="23bd1-196">1</span></span>     | <span data-ttu-id="23bd1-197">/IFD/XMP/ <xmpseq> DC: Creator</span><span class="sxs-lookup"><span data-stu-id="23bd1-197">/ifd/xmp/<xmpseq>dc:creator</span></span> | <span data-ttu-id="23bd1-198">Unicode</span><span class="sxs-lookup"><span data-stu-id="23bd1-198">unicode</span></span>        |
| <span data-ttu-id="23bd1-199">2</span><span class="sxs-lookup"><span data-stu-id="23bd1-199">2</span></span>     | <span data-ttu-id="23bd1-200">/IFD/XMP/TIFF: artista</span><span class="sxs-lookup"><span data-stu-id="23bd1-200">/ifd/xmp/tiff:artist</span></span>              | <span data-ttu-id="23bd1-201">Unicode</span><span class="sxs-lookup"><span data-stu-id="23bd1-201">unicode</span></span>        |
| <span data-ttu-id="23bd1-202">3</span><span class="sxs-lookup"><span data-stu-id="23bd1-202">3</span></span>     | <span data-ttu-id="23bd1-203">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="23bd1-203">/ifd/iptc/by-line</span></span>                 |                |
| <span data-ttu-id="23bd1-204">4</span><span class="sxs-lookup"><span data-stu-id="23bd1-204">4</span></span>     | <span data-ttu-id="23bd1-205">/IFD/{UShort = 315}</span><span class="sxs-lookup"><span data-stu-id="23bd1-205">/ifd/{ushort=315}</span></span>                 | <span data-ttu-id="23bd1-206">\_vetor ASCII</span><span class="sxs-lookup"><span data-stu-id="23bd1-206">ascii\_vector</span></span>  |
| <span data-ttu-id="23bd1-207">5</span><span class="sxs-lookup"><span data-stu-id="23bd1-207">5</span></span>     | <span data-ttu-id="23bd1-208">/IFD/{UShort = 40093}</span><span class="sxs-lookup"><span data-stu-id="23bd1-208">/ifd/{ushort=40093}</span></span>               | <span data-ttu-id="23bd1-209">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="23bd1-209">unicode\_bytes</span></span> |
| <span data-ttu-id="23bd1-210">6</span><span class="sxs-lookup"><span data-stu-id="23bd1-210">6</span></span>     | <span data-ttu-id="23bd1-211">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="23bd1-211">/ifd/iptc/by-line</span></span>                 |                |



 

### <a name="remove-paths"></a><span data-ttu-id="23bd1-212">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="23bd1-212">Remove Paths</span></span>



| <span data-ttu-id="23bd1-213">Ordem</span><span class="sxs-lookup"><span data-stu-id="23bd1-213">Order</span></span> | <span data-ttu-id="23bd1-214">Caminho</span><span class="sxs-lookup"><span data-stu-id="23bd1-214">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="23bd1-215">1</span><span class="sxs-lookup"><span data-stu-id="23bd1-215">1</span></span>     | <span data-ttu-id="23bd1-216">/IFD/XMP/DC: criador</span><span class="sxs-lookup"><span data-stu-id="23bd1-216">/ifd/xmp/dc:creator</span></span>            |
| <span data-ttu-id="23bd1-217">2</span><span class="sxs-lookup"><span data-stu-id="23bd1-217">2</span></span>     | <span data-ttu-id="23bd1-218">/IFD/XMP/TIFF: artista</span><span class="sxs-lookup"><span data-stu-id="23bd1-218">/ifd/xmp/tiff:artist</span></span>           |
| <span data-ttu-id="23bd1-219">3</span><span class="sxs-lookup"><span data-stu-id="23bd1-219">3</span></span>     | <span data-ttu-id="23bd1-220">/ifd/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="23bd1-220">/ifd/iptc/by-line</span></span>              |
| <span data-ttu-id="23bd1-221">4</span><span class="sxs-lookup"><span data-stu-id="23bd1-221">4</span></span>     | <span data-ttu-id="23bd1-222">/ifd/irb/8bimiptc/iptc/by-line</span><span class="sxs-lookup"><span data-stu-id="23bd1-222">/ifd/irb/8bimiptc/iptc/by-line</span></span> |
| <span data-ttu-id="23bd1-223">5</span><span class="sxs-lookup"><span data-stu-id="23bd1-223">5</span></span>     | <span data-ttu-id="23bd1-224">/IFD/{UShort = 315}</span><span class="sxs-lookup"><span data-stu-id="23bd1-224">/ifd/{ushort=315}</span></span>              |
| <span data-ttu-id="23bd1-225">6</span><span class="sxs-lookup"><span data-stu-id="23bd1-225">6</span></span>     | <span data-ttu-id="23bd1-226">/IFD/{UShort = 40093}</span><span class="sxs-lookup"><span data-stu-id="23bd1-226">/ifd/{ushort=40093}</span></span>            |



 

### <a name="remarks"></a><span data-ttu-id="23bd1-227">Comentários</span><span class="sxs-lookup"><span data-stu-id="23bd1-227">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="23bd1-228">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="23bd1-228">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23bd1-229">System.Author</span><span class="sxs-lookup"><span data-stu-id="23bd1-229">System.Author</span></span>](../properties/props-system-author.md)
</dt> </dl>

 

 
