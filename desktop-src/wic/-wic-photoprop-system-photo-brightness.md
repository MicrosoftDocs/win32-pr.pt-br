---
description: A política de metadados de foto para a propriedade System. Photo. pobrilho.
ms.assetid: 3fd73845-f1d9-468c-abf8-081109880974
title: Política de metadados de foto System. Photo. Brightness
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7328b4d40b8d1582dcc17b317b706b2695c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922561"
---
# <a name="systemphotobrightness-photo-metadata-policy"></a><span data-ttu-id="bb9e9-103">Política de metadados de foto System. Photo. Brightness</span><span class="sxs-lookup"><span data-stu-id="bb9e9-103">System.Photo.Brightness Photo Metadata Policy</span></span>

<span data-ttu-id="bb9e9-104">A política de metadados de foto para a propriedade [System. Photo. pobrilho](../properties/props-system-photo-aperture.md) .</span><span class="sxs-lookup"><span data-stu-id="bb9e9-104">The photo metadata policy for the [System.Photo.Brightness](../properties/props-system-photo-aperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="bb9e9-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="bb9e9-105">PKEY</span></span>

<span data-ttu-id="bb9e9-106">PKEY \_ brilho da foto \_</span><span class="sxs-lookup"><span data-stu-id="bb9e9-106">PKEY\_Photo\_Brightness</span></span>

### <a name="containers"></a><span data-ttu-id="bb9e9-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="bb9e9-107">Containers</span></span>

<span data-ttu-id="bb9e9-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="bb9e9-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="bb9e9-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bb9e9-109">Read-Only</span></span>

<span data-ttu-id="bb9e9-110">Yes</span><span class="sxs-lookup"><span data-stu-id="bb9e9-110">Yes</span></span>

### <a name="input-type"></a><span data-ttu-id="bb9e9-111">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="bb9e9-111">Input Type</span></span>

<span data-ttu-id="bb9e9-112">Double</span><span class="sxs-lookup"><span data-stu-id="bb9e9-112">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="bb9e9-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="bb9e9-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="bb9e9-114">Esse valor é gerado em System. Photo. ApertureNumerator e System. Photo. ApertureDenominator.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-114">This value is generated from System.Photo.ApertureNumerator and System.Photo.ApertureDenominator.</span></span> <span data-ttu-id="bb9e9-115">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-115">It cannot be written directly.</span></span> <span data-ttu-id="bb9e9-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="bb9e9-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="bb9e9-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="bb9e9-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="bb9e9-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="bb9e9-118">Read Paths</span></span>



| <span data-ttu-id="bb9e9-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="bb9e9-119">Order</span></span> | <span data-ttu-id="bb9e9-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="bb9e9-120">Path</span></span>                          | <span data-ttu-id="bb9e9-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="bb9e9-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="bb9e9-122">1</span><span class="sxs-lookup"><span data-stu-id="bb9e9-122">1</span></span>     | <span data-ttu-id="bb9e9-123">/App1/IFD/EXIF/{UShort = 37379}</span><span class="sxs-lookup"><span data-stu-id="bb9e9-123">/app1/ifd/exif/{ushort=37379}</span></span> |             |
| <span data-ttu-id="bb9e9-124">2</span><span class="sxs-lookup"><span data-stu-id="bb9e9-124">2</span></span>     | <span data-ttu-id="bb9e9-125">/XMP/EXIF: Brightness</span><span class="sxs-lookup"><span data-stu-id="bb9e9-125">/xmp/exif:BrightnessValue</span></span>     |             |



 

### <a name="write-paths"></a><span data-ttu-id="bb9e9-126">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="bb9e9-126">Write Paths</span></span>



| <span data-ttu-id="bb9e9-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="bb9e9-127">Order</span></span> | <span data-ttu-id="bb9e9-128">Caminho</span><span class="sxs-lookup"><span data-stu-id="bb9e9-128">Path</span></span>                          | <span data-ttu-id="bb9e9-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="bb9e9-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="bb9e9-130">1</span><span class="sxs-lookup"><span data-stu-id="bb9e9-130">1</span></span>     | <span data-ttu-id="bb9e9-131">/App1/IFD/EXIF/{UShort = 37379}</span><span class="sxs-lookup"><span data-stu-id="bb9e9-131">/app1/ifd/exif/{ushort=37379}</span></span> |             |
| <span data-ttu-id="bb9e9-132">2</span><span class="sxs-lookup"><span data-stu-id="bb9e9-132">2</span></span>     | <span data-ttu-id="bb9e9-133">/XMP/EXIF: Brightness</span><span class="sxs-lookup"><span data-stu-id="bb9e9-133">/xmp/exif:BrightnessValue</span></span>     |             |



 

### <a name="remove-paths"></a><span data-ttu-id="bb9e9-134">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="bb9e9-134">Remove Paths</span></span>



| <span data-ttu-id="bb9e9-135">Ordem</span><span class="sxs-lookup"><span data-stu-id="bb9e9-135">Order</span></span> | <span data-ttu-id="bb9e9-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="bb9e9-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="bb9e9-137">1</span><span class="sxs-lookup"><span data-stu-id="bb9e9-137">1</span></span>     | <span data-ttu-id="bb9e9-138">/App1/IFD/EXIF/{UShort = 37379}</span><span class="sxs-lookup"><span data-stu-id="bb9e9-138">/app1/ifd/exif/{ushort=37379}</span></span> |
| <span data-ttu-id="bb9e9-139">2</span><span class="sxs-lookup"><span data-stu-id="bb9e9-139">2</span></span>     | <span data-ttu-id="bb9e9-140">/XMP/EXIF: Brightness</span><span class="sxs-lookup"><span data-stu-id="bb9e9-140">/xmp/exif:brightnessvalue</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="bb9e9-141">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="bb9e9-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="bb9e9-142">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="bb9e9-142">Read Paths</span></span>



| <span data-ttu-id="bb9e9-143">Ordem</span><span class="sxs-lookup"><span data-stu-id="bb9e9-143">Order</span></span> | <span data-ttu-id="bb9e9-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="bb9e9-144">Path</span></span>                          | <span data-ttu-id="bb9e9-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="bb9e9-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="bb9e9-146">1</span><span class="sxs-lookup"><span data-stu-id="bb9e9-146">1</span></span>     | <span data-ttu-id="bb9e9-147">/IFD/EXIF/{UShort = 37379}</span><span class="sxs-lookup"><span data-stu-id="bb9e9-147">/ifd/exif/{ushort=37379}</span></span>      |             |
| <span data-ttu-id="bb9e9-148">2</span><span class="sxs-lookup"><span data-stu-id="bb9e9-148">2</span></span>     | <span data-ttu-id="bb9e9-149">/IFD/XMP/EXIF: Brightness</span><span class="sxs-lookup"><span data-stu-id="bb9e9-149">/ifd/xmp/exif:BrightnessValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="bb9e9-150">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="bb9e9-150">Write Paths</span></span>



| <span data-ttu-id="bb9e9-151">Ordem</span><span class="sxs-lookup"><span data-stu-id="bb9e9-151">Order</span></span> | <span data-ttu-id="bb9e9-152">Caminho</span><span class="sxs-lookup"><span data-stu-id="bb9e9-152">Path</span></span>                          | <span data-ttu-id="bb9e9-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="bb9e9-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="bb9e9-154">1</span><span class="sxs-lookup"><span data-stu-id="bb9e9-154">1</span></span>     | <span data-ttu-id="bb9e9-155">/IFD/EXIF/{UShort = 37379}</span><span class="sxs-lookup"><span data-stu-id="bb9e9-155">/ifd/exif/{ushort=37379}</span></span>      |             |
| <span data-ttu-id="bb9e9-156">2</span><span class="sxs-lookup"><span data-stu-id="bb9e9-156">2</span></span>     | <span data-ttu-id="bb9e9-157">/IFD/XMP/EXIF: Brightness</span><span class="sxs-lookup"><span data-stu-id="bb9e9-157">/ifd/xmp/exif:BrightnessValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="bb9e9-158">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="bb9e9-158">Remove Paths</span></span>



| <span data-ttu-id="bb9e9-159">Ordem</span><span class="sxs-lookup"><span data-stu-id="bb9e9-159">Order</span></span> | <span data-ttu-id="bb9e9-160">Caminho</span><span class="sxs-lookup"><span data-stu-id="bb9e9-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="bb9e9-161">1</span><span class="sxs-lookup"><span data-stu-id="bb9e9-161">1</span></span>     | <span data-ttu-id="bb9e9-162">/IFD/EXIF/{UShort = 37379}</span><span class="sxs-lookup"><span data-stu-id="bb9e9-162">/ifd/exif/{ushort=37379}</span></span>      |
| <span data-ttu-id="bb9e9-163">2</span><span class="sxs-lookup"><span data-stu-id="bb9e9-163">2</span></span>     | <span data-ttu-id="bb9e9-164">/IFD/XMP/EXIF: Brightness</span><span class="sxs-lookup"><span data-stu-id="bb9e9-164">/ifd/xmp/exif:brightnessvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bb9e9-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb9e9-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb9e9-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb9e9-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb9e9-167">System. Photo. Brightness</span><span class="sxs-lookup"><span data-stu-id="bb9e9-167">System.Photo.Brightness</span></span>](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
