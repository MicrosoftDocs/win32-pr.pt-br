---
description: A política de metadados de foto para a propriedade System. Photo. nitidez.
ms.assetid: 0fda4832-940b-4b5a-bd20-7e48c7800925
title: Política de metadados de foto System. Photo. nitidez
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d635691f0b0e0801c1e37a006faa686aff0a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766288"
---
# <a name="systemphotosharpness-photo-metadata-policy"></a><span data-ttu-id="439fe-103">Política de metadados de foto System. Photo. nitidez</span><span class="sxs-lookup"><span data-stu-id="439fe-103">System.Photo.Sharpness Photo Metadata Policy</span></span>

<span data-ttu-id="439fe-104">A política de metadados de foto para a propriedade [System. Photo. nitidez](../properties/props-system-photo-sharpness.md) .</span><span class="sxs-lookup"><span data-stu-id="439fe-104">The photo metadata policy for the [System.Photo.Sharpness](../properties/props-system-photo-sharpness.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="439fe-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="439fe-105">PKEY</span></span>

<span data-ttu-id="439fe-106">\_Nitidez da foto PKEY \_</span><span class="sxs-lookup"><span data-stu-id="439fe-106">PKEY\_Photo\_Sharpness</span></span>

### <a name="containers"></a><span data-ttu-id="439fe-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="439fe-107">Containers</span></span>

<span data-ttu-id="439fe-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="439fe-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="439fe-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="439fe-109">Read-Only</span></span>

<span data-ttu-id="439fe-110">No</span><span class="sxs-lookup"><span data-stu-id="439fe-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="439fe-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="439fe-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="439fe-112">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="439fe-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="439fe-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="439fe-113">Input Type</span></span>

<span data-ttu-id="439fe-114">UShort</span><span class="sxs-lookup"><span data-stu-id="439fe-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="439fe-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="439fe-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="439fe-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="439fe-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="439fe-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="439fe-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="439fe-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="439fe-118">Read Paths</span></span>



| <span data-ttu-id="439fe-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="439fe-119">Order</span></span> | <span data-ttu-id="439fe-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="439fe-120">Path</span></span>                          | <span data-ttu-id="439fe-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="439fe-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="439fe-122">1</span><span class="sxs-lookup"><span data-stu-id="439fe-122">1</span></span>     | <span data-ttu-id="439fe-123">/App1/IFD/EXIF/{UShort = 41994}</span><span class="sxs-lookup"><span data-stu-id="439fe-123">/app1/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="439fe-124">ushort</span><span class="sxs-lookup"><span data-stu-id="439fe-124">ushort</span></span>      |
| <span data-ttu-id="439fe-125">2</span><span class="sxs-lookup"><span data-stu-id="439fe-125">2</span></span>     | <span data-ttu-id="439fe-126">/XMP/EXIF: nitidez</span><span class="sxs-lookup"><span data-stu-id="439fe-126">/xmp/exif:Sharpness</span></span>           | <span data-ttu-id="439fe-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="439fe-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="439fe-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="439fe-128">Write Paths</span></span>



| <span data-ttu-id="439fe-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="439fe-129">Order</span></span> | <span data-ttu-id="439fe-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="439fe-130">Path</span></span>                          | <span data-ttu-id="439fe-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="439fe-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="439fe-132">1</span><span class="sxs-lookup"><span data-stu-id="439fe-132">1</span></span>     | <span data-ttu-id="439fe-133">/App1/IFD/EXIF/{UShort = 41994}</span><span class="sxs-lookup"><span data-stu-id="439fe-133">/app1/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="439fe-134">ushort</span><span class="sxs-lookup"><span data-stu-id="439fe-134">ushort</span></span>      |
| <span data-ttu-id="439fe-135">2</span><span class="sxs-lookup"><span data-stu-id="439fe-135">2</span></span>     | <span data-ttu-id="439fe-136">/XMP/EXIF: nitidez</span><span class="sxs-lookup"><span data-stu-id="439fe-136">/xmp/exif:Sharpness</span></span>           | <span data-ttu-id="439fe-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="439fe-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="439fe-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="439fe-138">Remove Paths</span></span>



| <span data-ttu-id="439fe-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="439fe-139">Order</span></span> | <span data-ttu-id="439fe-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="439fe-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="439fe-141">1</span><span class="sxs-lookup"><span data-stu-id="439fe-141">1</span></span>     | <span data-ttu-id="439fe-142">/App1/IFD/EXIF/{UShort = 41994}</span><span class="sxs-lookup"><span data-stu-id="439fe-142">/app1/ifd/exif/{ushort=41994}</span></span> |
| <span data-ttu-id="439fe-143">2</span><span class="sxs-lookup"><span data-stu-id="439fe-143">2</span></span>     | <span data-ttu-id="439fe-144">/XMP/EXIF: nitidez</span><span class="sxs-lookup"><span data-stu-id="439fe-144">/xmp/exif:sharpness</span></span>           |



 

### <a name="tiff-policies"></a><span data-ttu-id="439fe-145">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="439fe-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="439fe-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="439fe-146">Read Paths</span></span>



| <span data-ttu-id="439fe-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="439fe-147">Order</span></span> | <span data-ttu-id="439fe-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="439fe-148">Path</span></span>                     | <span data-ttu-id="439fe-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="439fe-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="439fe-150">1</span><span class="sxs-lookup"><span data-stu-id="439fe-150">1</span></span>     | <span data-ttu-id="439fe-151">/IFD/EXIF/{UShort = 41994}</span><span class="sxs-lookup"><span data-stu-id="439fe-151">/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="439fe-152">ushort</span><span class="sxs-lookup"><span data-stu-id="439fe-152">ushort</span></span>      |
| <span data-ttu-id="439fe-153">2</span><span class="sxs-lookup"><span data-stu-id="439fe-153">2</span></span>     | <span data-ttu-id="439fe-154">/IFD/XMP/EXIF: nitidez</span><span class="sxs-lookup"><span data-stu-id="439fe-154">/ifd/xmp/exif:Sharpness</span></span>  | <span data-ttu-id="439fe-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="439fe-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="439fe-156">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="439fe-156">Write Paths</span></span>



| <span data-ttu-id="439fe-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="439fe-157">Order</span></span> | <span data-ttu-id="439fe-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="439fe-158">Path</span></span>                     | <span data-ttu-id="439fe-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="439fe-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="439fe-160">1</span><span class="sxs-lookup"><span data-stu-id="439fe-160">1</span></span>     | <span data-ttu-id="439fe-161">/IFD/EXIF/{UShort = 41994}</span><span class="sxs-lookup"><span data-stu-id="439fe-161">/ifd/exif/{ushort=41994}</span></span> | <span data-ttu-id="439fe-162">ushort</span><span class="sxs-lookup"><span data-stu-id="439fe-162">ushort</span></span>      |
| <span data-ttu-id="439fe-163">2</span><span class="sxs-lookup"><span data-stu-id="439fe-163">2</span></span>     | <span data-ttu-id="439fe-164">/IFD/XMP/EXIF: nitidez</span><span class="sxs-lookup"><span data-stu-id="439fe-164">/ifd/xmp/exif:Sharpness</span></span>  | <span data-ttu-id="439fe-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="439fe-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="439fe-166">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="439fe-166">Remove Paths</span></span>



| <span data-ttu-id="439fe-167">Ordem</span><span class="sxs-lookup"><span data-stu-id="439fe-167">Order</span></span> | <span data-ttu-id="439fe-168">Caminho</span><span class="sxs-lookup"><span data-stu-id="439fe-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="439fe-169">1</span><span class="sxs-lookup"><span data-stu-id="439fe-169">1</span></span>     | <span data-ttu-id="439fe-170">/IFD/EXIF/{UShort = 41994}</span><span class="sxs-lookup"><span data-stu-id="439fe-170">/ifd/exif/{ushort=41994}</span></span> |
| <span data-ttu-id="439fe-171">2</span><span class="sxs-lookup"><span data-stu-id="439fe-171">2</span></span>     | <span data-ttu-id="439fe-172">/IFD/XMP/EXIF: nitidez</span><span class="sxs-lookup"><span data-stu-id="439fe-172">/ifd/xmp/exif:sharpness</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="439fe-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="439fe-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="439fe-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="439fe-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="439fe-175">System. Photo. nitidez</span><span class="sxs-lookup"><span data-stu-id="439fe-175">System.Photo.Sharpness</span></span>](../properties/props-system-photo-sharpness.md)
</dt> </dl>

 

 
