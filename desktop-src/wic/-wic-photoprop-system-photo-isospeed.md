---
description: A política de metadados de foto para a propriedade System. Photo. ISOSpeed.
ms.assetid: 22b5552c-41b1-4090-a827-b920dcbba5e9
title: Política de metadados de foto System. Photo. ISOSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2988f774f70721ab1817ffaf605098ab1164316a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296969"
---
# <a name="systemphotoisospeed-photo-metadata-policy"></a><span data-ttu-id="b3bf5-103">Política de metadados de foto System. Photo. ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="b3bf5-103">System.Photo.ISOSpeed Photo Metadata Policy</span></span>

<span data-ttu-id="b3bf5-104">A política de metadados de foto para a propriedade [System. Photo. ISOSpeed](../properties/props-system-photo-focallengthinfilm.md) .</span><span class="sxs-lookup"><span data-stu-id="b3bf5-104">The photo metadata policy for the [System.Photo.ISOSpeed](../properties/props-system-photo-focallengthinfilm.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b3bf5-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="b3bf5-105">PKEY</span></span>

<span data-ttu-id="b3bf5-106">PKEY \_ Photo \_ ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="b3bf5-106">PKEY\_Photo\_ISOSpeed</span></span>

### <a name="containers"></a><span data-ttu-id="b3bf5-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="b3bf5-107">Containers</span></span>

<span data-ttu-id="b3bf5-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b3bf5-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b3bf5-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3bf5-109">Read-Only</span></span>

<span data-ttu-id="b3bf5-110">No</span><span class="sxs-lookup"><span data-stu-id="b3bf5-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b3bf5-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="b3bf5-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b3bf5-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="b3bf5-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="b3bf5-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="b3bf5-113">Input Type</span></span>

<span data-ttu-id="b3bf5-114">UShort</span><span class="sxs-lookup"><span data-stu-id="b3bf5-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b3bf5-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="b3bf5-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="b3bf5-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="b3bf5-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b3bf5-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="b3bf5-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b3bf5-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="b3bf5-118">Read Paths</span></span>



| <span data-ttu-id="b3bf5-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="b3bf5-119">Order</span></span> | <span data-ttu-id="b3bf5-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="b3bf5-120">Path</span></span>                                    | <span data-ttu-id="b3bf5-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b3bf5-121">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="b3bf5-122">1</span><span class="sxs-lookup"><span data-stu-id="b3bf5-122">1</span></span>     | <span data-ttu-id="b3bf5-123">/App1/IFD/EXIF/{UShort = 34855}</span><span class="sxs-lookup"><span data-stu-id="b3bf5-123">/app1/ifd/exif/{ushort=34855}</span></span>           | <span data-ttu-id="b3bf5-124">ushort</span><span class="sxs-lookup"><span data-stu-id="b3bf5-124">ushort</span></span>      |
| <span data-ttu-id="b3bf5-125">2</span><span class="sxs-lookup"><span data-stu-id="b3bf5-125">2</span></span>     | <span data-ttu-id="b3bf5-126">/XMP/ <xmpseq> EXIF: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="b3bf5-126">/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="b3bf5-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="b3bf5-127">unicode</span></span>     |
| <span data-ttu-id="b3bf5-128">3</span><span class="sxs-lookup"><span data-stu-id="b3bf5-128">3</span></span>     | <span data-ttu-id="b3bf5-129">/xmp/exif:ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="b3bf5-129">/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="b3bf5-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="b3bf5-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="b3bf5-131">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="b3bf5-131">Write Paths</span></span>



| <span data-ttu-id="b3bf5-132">Ordem</span><span class="sxs-lookup"><span data-stu-id="b3bf5-132">Order</span></span> | <span data-ttu-id="b3bf5-133">Caminho</span><span class="sxs-lookup"><span data-stu-id="b3bf5-133">Path</span></span>                                    | <span data-ttu-id="b3bf5-134">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b3bf5-134">Disk Format</span></span> |
|-------|-----------------------------------------|-------------|
| <span data-ttu-id="b3bf5-135">1</span><span class="sxs-lookup"><span data-stu-id="b3bf5-135">1</span></span>     | <span data-ttu-id="b3bf5-136">/App1/IFD/EXIF/{UShort = 34855}</span><span class="sxs-lookup"><span data-stu-id="b3bf5-136">/app1/ifd/exif/{ushort=34855}</span></span>           | <span data-ttu-id="b3bf5-137">ushort</span><span class="sxs-lookup"><span data-stu-id="b3bf5-137">ushort</span></span>      |
| <span data-ttu-id="b3bf5-138">2</span><span class="sxs-lookup"><span data-stu-id="b3bf5-138">2</span></span>     | <span data-ttu-id="b3bf5-139">/XMP/ <xmpseq> EXIF: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="b3bf5-139">/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="b3bf5-140">Unicode</span><span class="sxs-lookup"><span data-stu-id="b3bf5-140">unicode</span></span>     |
| <span data-ttu-id="b3bf5-141">3</span><span class="sxs-lookup"><span data-stu-id="b3bf5-141">3</span></span>     | <span data-ttu-id="b3bf5-142">/xmp/exif:ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="b3bf5-142">/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="b3bf5-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="b3bf5-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="b3bf5-144">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="b3bf5-144">Remove Paths</span></span>



| <span data-ttu-id="b3bf5-145">Ordem</span><span class="sxs-lookup"><span data-stu-id="b3bf5-145">Order</span></span> | <span data-ttu-id="b3bf5-146">Caminho</span><span class="sxs-lookup"><span data-stu-id="b3bf5-146">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="b3bf5-147">1</span><span class="sxs-lookup"><span data-stu-id="b3bf5-147">1</span></span>     | <span data-ttu-id="b3bf5-148">/App1/IFD/EXIF/{UShort = 34855}</span><span class="sxs-lookup"><span data-stu-id="b3bf5-148">/app1/ifd/exif/{ushort=34855}</span></span>           |
| <span data-ttu-id="b3bf5-149">2</span><span class="sxs-lookup"><span data-stu-id="b3bf5-149">2</span></span>     | <span data-ttu-id="b3bf5-150">/XMP/ <xmpseq> EXIF: isospeedratings</span><span class="sxs-lookup"><span data-stu-id="b3bf5-150">/xmp/<xmpseq>exif:isospeedratings</span></span> |
| <span data-ttu-id="b3bf5-151">3</span><span class="sxs-lookup"><span data-stu-id="b3bf5-151">3</span></span>     | <span data-ttu-id="b3bf5-152">/xmp/exif:isospeed</span><span class="sxs-lookup"><span data-stu-id="b3bf5-152">/xmp/exif:isospeed</span></span>                      |



 

### <a name="tiff-policies"></a><span data-ttu-id="b3bf5-153">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="b3bf5-153">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b3bf5-154">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="b3bf5-154">Read Paths</span></span>



| <span data-ttu-id="b3bf5-155">Ordem</span><span class="sxs-lookup"><span data-stu-id="b3bf5-155">Order</span></span> | <span data-ttu-id="b3bf5-156">Caminho</span><span class="sxs-lookup"><span data-stu-id="b3bf5-156">Path</span></span>                                        | <span data-ttu-id="b3bf5-157">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b3bf5-157">Disk Format</span></span> |
|-------|---------------------------------------------|-------------|
| <span data-ttu-id="b3bf5-158">1</span><span class="sxs-lookup"><span data-stu-id="b3bf5-158">1</span></span>     | <span data-ttu-id="b3bf5-159">/IFD/EXIF/{UShort = 34855}</span><span class="sxs-lookup"><span data-stu-id="b3bf5-159">/ifd/exif/{ushort=34855}</span></span>                    | <span data-ttu-id="b3bf5-160">ushort</span><span class="sxs-lookup"><span data-stu-id="b3bf5-160">ushort</span></span>      |
| <span data-ttu-id="b3bf5-161">2</span><span class="sxs-lookup"><span data-stu-id="b3bf5-161">2</span></span>     | <span data-ttu-id="b3bf5-162">/IFD/XMP/ <xmpseq> EXIF: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="b3bf5-162">/ifd/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="b3bf5-163">Unicode</span><span class="sxs-lookup"><span data-stu-id="b3bf5-163">unicode</span></span>     |
| <span data-ttu-id="b3bf5-164">3</span><span class="sxs-lookup"><span data-stu-id="b3bf5-164">3</span></span>     | <span data-ttu-id="b3bf5-165">/ifd/xmp/exif:ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="b3bf5-165">/ifd/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="b3bf5-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="b3bf5-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="b3bf5-167">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="b3bf5-167">Write Paths</span></span>



| <span data-ttu-id="b3bf5-168">Ordem</span><span class="sxs-lookup"><span data-stu-id="b3bf5-168">Order</span></span> | <span data-ttu-id="b3bf5-169">Caminho</span><span class="sxs-lookup"><span data-stu-id="b3bf5-169">Path</span></span>                                        | <span data-ttu-id="b3bf5-170">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b3bf5-170">Disk Format</span></span> |
|-------|---------------------------------------------|-------------|
| <span data-ttu-id="b3bf5-171">1</span><span class="sxs-lookup"><span data-stu-id="b3bf5-171">1</span></span>     | <span data-ttu-id="b3bf5-172">/IFD/EXIF/{UShort = 34855}</span><span class="sxs-lookup"><span data-stu-id="b3bf5-172">/ifd/exif/{ushort=34855}</span></span>                    | <span data-ttu-id="b3bf5-173">ushort</span><span class="sxs-lookup"><span data-stu-id="b3bf5-173">ushort</span></span>      |
| <span data-ttu-id="b3bf5-174">2</span><span class="sxs-lookup"><span data-stu-id="b3bf5-174">2</span></span>     | <span data-ttu-id="b3bf5-175">/IFD/XMP/ <xmpseq> EXIF: ISOSpeedRatings</span><span class="sxs-lookup"><span data-stu-id="b3bf5-175">/ifd/xmp/<xmpseq>exif:ISOSpeedRatings</span></span> | <span data-ttu-id="b3bf5-176">Unicode</span><span class="sxs-lookup"><span data-stu-id="b3bf5-176">unicode</span></span>     |
| <span data-ttu-id="b3bf5-177">3</span><span class="sxs-lookup"><span data-stu-id="b3bf5-177">3</span></span>     | <span data-ttu-id="b3bf5-178">/ifd/xmp/exif:ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="b3bf5-178">/ifd/xmp/exif:ISOSpeed</span></span>                      | <span data-ttu-id="b3bf5-179">Unicode</span><span class="sxs-lookup"><span data-stu-id="b3bf5-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="b3bf5-180">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="b3bf5-180">Remove Paths</span></span>



| <span data-ttu-id="b3bf5-181">Ordem</span><span class="sxs-lookup"><span data-stu-id="b3bf5-181">Order</span></span> | <span data-ttu-id="b3bf5-182">Caminho</span><span class="sxs-lookup"><span data-stu-id="b3bf5-182">Path</span></span>                                        |
|-------|---------------------------------------------|
| <span data-ttu-id="b3bf5-183">1</span><span class="sxs-lookup"><span data-stu-id="b3bf5-183">1</span></span>     | <span data-ttu-id="b3bf5-184">/IFD/EXIF/{UShort = 34855}</span><span class="sxs-lookup"><span data-stu-id="b3bf5-184">/ifd/exif/{ushort=34855}</span></span>                    |
| <span data-ttu-id="b3bf5-185">2</span><span class="sxs-lookup"><span data-stu-id="b3bf5-185">2</span></span>     | <span data-ttu-id="b3bf5-186">/IFD/XMP/ <xmpseq> EXIF: isospeedratings</span><span class="sxs-lookup"><span data-stu-id="b3bf5-186">/ifd/xmp/<xmpseq>exif:isospeedratings</span></span> |
| <span data-ttu-id="b3bf5-187">3</span><span class="sxs-lookup"><span data-stu-id="b3bf5-187">3</span></span>     | <span data-ttu-id="b3bf5-188">/ifd/xmp/exif:isospeed</span><span class="sxs-lookup"><span data-stu-id="b3bf5-188">/ifd/xmp/exif:isospeed</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="b3bf5-189">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3bf5-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3bf5-190">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3bf5-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3bf5-191">System. Photo. ISOSpeed</span><span class="sxs-lookup"><span data-stu-id="b3bf5-191">System.Photo.ISOSpeed</span></span>](../properties/props-system-photo-focallengthinfilm.md)
</dt> </dl>

 

 
