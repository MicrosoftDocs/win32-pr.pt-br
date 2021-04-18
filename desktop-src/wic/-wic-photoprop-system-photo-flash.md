---
description: A política de metadados de foto para a propriedade System. Photo. flash.
ms.assetid: 24b400a4-f4c7-4b59-a9e3-8a20144cd52e
title: Política de metadados de foto System. Photo. flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0302e0f310d2f9a6a4390b0d4856578cc2f43e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787011"
---
# <a name="systemphotoflash-photo-metadata-policy"></a><span data-ttu-id="b153d-103">Política de metadados de foto System. Photo. flash</span><span class="sxs-lookup"><span data-stu-id="b153d-103">System.Photo.Flash Photo Metadata Policy</span></span>

<span data-ttu-id="b153d-104">A política de metadados de foto para a propriedade [System. Photo. flash](../properties/props-system-photo-exposuretime.md) .</span><span class="sxs-lookup"><span data-stu-id="b153d-104">The photo metadata policy for the [System.Photo.Flash](../properties/props-system-photo-exposuretime.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b153d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="b153d-105">PKEY</span></span>

<span data-ttu-id="b153d-106">PKEY \_ Photo \_ flash</span><span class="sxs-lookup"><span data-stu-id="b153d-106">PKEY\_Photo\_Flash</span></span>

### <a name="containers"></a><span data-ttu-id="b153d-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="b153d-107">Containers</span></span>

<span data-ttu-id="b153d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b153d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b153d-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b153d-109">Read-Only</span></span>

<span data-ttu-id="b153d-110">No</span><span class="sxs-lookup"><span data-stu-id="b153d-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b153d-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="b153d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b153d-112">VT \_ UI1 (se o esquema de origem era XMP) ou VT \_ UI2 (se o esquema de origem era EXIF)</span><span class="sxs-lookup"><span data-stu-id="b153d-112">VT\_UI1 (if the source schema was XMP), or VT\_UI2 (if the source schema was EXIF)</span></span>

<span data-ttu-id="b153d-113">\\lang1036</span><span class="sxs-lookup"><span data-stu-id="b153d-113">\\lang1036</span></span>

### <a name="input-type"></a><span data-ttu-id="b153d-114">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="b153d-114">Input Type</span></span>

<span data-ttu-id="b153d-115">VT \_ UI1, VTUI2, VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="b153d-115">VT\_UI1, VTUI2, VT\_UI4</span></span>

<span data-ttu-id="b153d-116">\\lang1033</span><span class="sxs-lookup"><span data-stu-id="b153d-116">\\lang1033</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b153d-117">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="b153d-117">Conflict Resolution Policy</span></span>

<span data-ttu-id="b153d-118">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="b153d-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b153d-119">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="b153d-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b153d-120">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="b153d-120">Read Paths</span></span>



| <span data-ttu-id="b153d-121">Ordem</span><span class="sxs-lookup"><span data-stu-id="b153d-121">Order</span></span> | <span data-ttu-id="b153d-122">Caminho</span><span class="sxs-lookup"><span data-stu-id="b153d-122">Path</span></span>                             | <span data-ttu-id="b153d-123">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b153d-123">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="b153d-124">1</span><span class="sxs-lookup"><span data-stu-id="b153d-124">1</span></span>     | <span data-ttu-id="b153d-125">/App1/IFD/EXIF/{UShort = 37385}</span><span class="sxs-lookup"><span data-stu-id="b153d-125">/app1/ifd/exif/{ushort=37385}</span></span>    | <span data-ttu-id="b153d-126">ushort</span><span class="sxs-lookup"><span data-stu-id="b153d-126">ushort</span></span>      |
| <span data-ttu-id="b153d-127">2</span><span class="sxs-lookup"><span data-stu-id="b153d-127">2</span></span>     | <span data-ttu-id="b153d-128">/XMP/ <xmpstruct> EXIF: flash</span><span class="sxs-lookup"><span data-stu-id="b153d-128">/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="b153d-129">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="b153d-129">Write Paths</span></span>



| <span data-ttu-id="b153d-130">Ordem</span><span class="sxs-lookup"><span data-stu-id="b153d-130">Order</span></span> | <span data-ttu-id="b153d-131">Caminho</span><span class="sxs-lookup"><span data-stu-id="b153d-131">Path</span></span>                             | <span data-ttu-id="b153d-132">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b153d-132">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="b153d-133">1</span><span class="sxs-lookup"><span data-stu-id="b153d-133">1</span></span>     | <span data-ttu-id="b153d-134">/App1/IFD/EXIF/{UShort = 37385}</span><span class="sxs-lookup"><span data-stu-id="b153d-134">/app1/ifd/exif/{ushort=37385}</span></span>    | <span data-ttu-id="b153d-135">ushort</span><span class="sxs-lookup"><span data-stu-id="b153d-135">ushort</span></span>      |
| <span data-ttu-id="b153d-136">2</span><span class="sxs-lookup"><span data-stu-id="b153d-136">2</span></span>     | <span data-ttu-id="b153d-137">/XMP/ <xmpstruct> EXIF: flash</span><span class="sxs-lookup"><span data-stu-id="b153d-137">/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b153d-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="b153d-138">Remove Paths</span></span>



| <span data-ttu-id="b153d-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="b153d-139">Order</span></span> | <span data-ttu-id="b153d-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="b153d-140">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="b153d-141">1</span><span class="sxs-lookup"><span data-stu-id="b153d-141">1</span></span>     | <span data-ttu-id="b153d-142">/App1/IFD/EXIF/{UShort = 37385}</span><span class="sxs-lookup"><span data-stu-id="b153d-142">/app1/ifd/exif/{ushort=37385}</span></span>    |
| <span data-ttu-id="b153d-143">2</span><span class="sxs-lookup"><span data-stu-id="b153d-143">2</span></span>     | <span data-ttu-id="b153d-144">/XMP/ <xmpstruct> EXIF: flash</span><span class="sxs-lookup"><span data-stu-id="b153d-144">/xmp/<xmpstruct>exif:flash</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="b153d-145">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="b153d-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b153d-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="b153d-146">Read Paths</span></span>



| <span data-ttu-id="b153d-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="b153d-147">Order</span></span> | <span data-ttu-id="b153d-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="b153d-148">Path</span></span>                                 | <span data-ttu-id="b153d-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b153d-149">Disk Format</span></span> |
|-------|--------------------------------------|-------------|
| <span data-ttu-id="b153d-150">1</span><span class="sxs-lookup"><span data-stu-id="b153d-150">1</span></span>     | <span data-ttu-id="b153d-151">/IFD/EXIF/{UShort = 37385}</span><span class="sxs-lookup"><span data-stu-id="b153d-151">/ifd/exif/{ushort=37385}</span></span>             | <span data-ttu-id="b153d-152">ushort</span><span class="sxs-lookup"><span data-stu-id="b153d-152">ushort</span></span>      |
| <span data-ttu-id="b153d-153">2</span><span class="sxs-lookup"><span data-stu-id="b153d-153">2</span></span>     | <span data-ttu-id="b153d-154">/IFD/XMP/ <xmpstruct> EXIF: flash</span><span class="sxs-lookup"><span data-stu-id="b153d-154">/ifd/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="b153d-155">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="b153d-155">Write Paths</span></span>



| <span data-ttu-id="b153d-156">Ordem</span><span class="sxs-lookup"><span data-stu-id="b153d-156">Order</span></span> | <span data-ttu-id="b153d-157">Caminho</span><span class="sxs-lookup"><span data-stu-id="b153d-157">Path</span></span>                                 | <span data-ttu-id="b153d-158">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b153d-158">Disk Format</span></span> |
|-------|--------------------------------------|-------------|
| <span data-ttu-id="b153d-159">1</span><span class="sxs-lookup"><span data-stu-id="b153d-159">1</span></span>     | <span data-ttu-id="b153d-160">/IFD/EXIF/{UShort = 37385}</span><span class="sxs-lookup"><span data-stu-id="b153d-160">/ifd/exif/{ushort=37385}</span></span>             | <span data-ttu-id="b153d-161">ushort</span><span class="sxs-lookup"><span data-stu-id="b153d-161">ushort</span></span>      |
| <span data-ttu-id="b153d-162">2</span><span class="sxs-lookup"><span data-stu-id="b153d-162">2</span></span>     | <span data-ttu-id="b153d-163">/IFD/XMP/ <xmpstruct> EXIF: flash</span><span class="sxs-lookup"><span data-stu-id="b153d-163">/ifd/xmp/<xmpstruct>exif:Flash</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b153d-164">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="b153d-164">Remove Paths</span></span>



| <span data-ttu-id="b153d-165">Ordem</span><span class="sxs-lookup"><span data-stu-id="b153d-165">Order</span></span> | <span data-ttu-id="b153d-166">Caminho</span><span class="sxs-lookup"><span data-stu-id="b153d-166">Path</span></span>                                 |
|-------|--------------------------------------|
| <span data-ttu-id="b153d-167">1</span><span class="sxs-lookup"><span data-stu-id="b153d-167">1</span></span>     | <span data-ttu-id="b153d-168">/IFD/EXIF/{UShort = 37385}</span><span class="sxs-lookup"><span data-stu-id="b153d-168">/ifd/exif/{ushort=37385}</span></span>             |
| <span data-ttu-id="b153d-169">2</span><span class="sxs-lookup"><span data-stu-id="b153d-169">2</span></span>     | <span data-ttu-id="b153d-170">/IFD/XMP/ <xmpstruct> EXIF: flash</span><span class="sxs-lookup"><span data-stu-id="b153d-170">/ifd/xmp/<xmpstruct>exif:flash</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b153d-171">Comentários</span><span class="sxs-lookup"><span data-stu-id="b153d-171">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b153d-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b153d-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b153d-173">System. Photo. flash</span><span class="sxs-lookup"><span data-stu-id="b153d-173">System.Photo.Flash</span></span>](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
