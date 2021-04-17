---
description: A política de metadados de foto para a propriedade System. Photo. MaxAperture.
ms.assetid: 9d12d265-0b0a-44d9-bbf6-ca7d748382ee
title: Política de metadados de foto System. Photo. MaxAperture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f3dab4d5ebf89033de03dfce887a7cea10fa11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812862"
---
# <a name="systemphotomaxaperture-photo-metadata-policy"></a><span data-ttu-id="e04ac-103">Política de metadados de foto System. Photo. MaxAperture</span><span class="sxs-lookup"><span data-stu-id="e04ac-103">System.Photo.MaxAperture Photo Metadata Policy</span></span>

<span data-ttu-id="e04ac-104">A política de metadados de foto para a propriedade [System. Photo. MaxAperture](../properties/props-system-photo-maxaperture.md) .</span><span class="sxs-lookup"><span data-stu-id="e04ac-104">The photo metadata policy for the [System.Photo.MaxAperture](../properties/props-system-photo-maxaperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="e04ac-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="e04ac-105">PKEY</span></span>

<span data-ttu-id="e04ac-106">PKEY \_ Photo \_ MaxAperture</span><span class="sxs-lookup"><span data-stu-id="e04ac-106">PKEY\_Photo\_MaxAperture</span></span>

### <a name="containers"></a><span data-ttu-id="e04ac-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="e04ac-107">Containers</span></span>

<span data-ttu-id="e04ac-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="e04ac-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="e04ac-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e04ac-109">Read-Only</span></span>

<span data-ttu-id="e04ac-110">Yes</span><span class="sxs-lookup"><span data-stu-id="e04ac-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="e04ac-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="e04ac-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="e04ac-112">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="e04ac-112">VT\_R8</span></span>

### <a name="input-type"></a><span data-ttu-id="e04ac-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="e04ac-113">Input Type</span></span>

<span data-ttu-id="e04ac-114">Double</span><span class="sxs-lookup"><span data-stu-id="e04ac-114">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="e04ac-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="e04ac-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="e04ac-116">Esse valor é gerado em System. Photo. MaxApertureNumerator e System. Photo. MaxApertureDenominator.</span><span class="sxs-lookup"><span data-stu-id="e04ac-116">This value is generated from System.Photo.MaxApertureNumerator and System.Photo.MaxApertureDenominator.</span></span> <span data-ttu-id="e04ac-117">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="e04ac-117">It cannot be written directly.</span></span> <span data-ttu-id="e04ac-118">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="e04ac-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="e04ac-119">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="e04ac-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="e04ac-120">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="e04ac-120">Read Paths</span></span>



| <span data-ttu-id="e04ac-121">Ordem</span><span class="sxs-lookup"><span data-stu-id="e04ac-121">Order</span></span> | <span data-ttu-id="e04ac-122">Caminho</span><span class="sxs-lookup"><span data-stu-id="e04ac-122">Path</span></span>                          | <span data-ttu-id="e04ac-123">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e04ac-123">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="e04ac-124">1</span><span class="sxs-lookup"><span data-stu-id="e04ac-124">1</span></span>     | <span data-ttu-id="e04ac-125">/App1/IFD/EXIF/{UShort = 37381}</span><span class="sxs-lookup"><span data-stu-id="e04ac-125">/app1/ifd/exif/{ushort=37381}</span></span> |             |
| <span data-ttu-id="e04ac-126">2</span><span class="sxs-lookup"><span data-stu-id="e04ac-126">2</span></span>     | <span data-ttu-id="e04ac-127">/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="e04ac-127">/xmp/exif:MaxApertureValue</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="e04ac-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="e04ac-128">Write Paths</span></span>



| <span data-ttu-id="e04ac-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="e04ac-129">Order</span></span> | <span data-ttu-id="e04ac-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="e04ac-130">Path</span></span>                          | <span data-ttu-id="e04ac-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e04ac-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="e04ac-132">1</span><span class="sxs-lookup"><span data-stu-id="e04ac-132">1</span></span>     | <span data-ttu-id="e04ac-133">/App1/IFD/EXIF/{UShort = 37381}</span><span class="sxs-lookup"><span data-stu-id="e04ac-133">/app1/ifd/exif/{ushort=37381}</span></span> |             |
| <span data-ttu-id="e04ac-134">2</span><span class="sxs-lookup"><span data-stu-id="e04ac-134">2</span></span>     | <span data-ttu-id="e04ac-135">/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="e04ac-135">/xmp/exif:MaxApertureValue</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="e04ac-136">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="e04ac-136">Remove Paths</span></span>



| <span data-ttu-id="e04ac-137">Ordem</span><span class="sxs-lookup"><span data-stu-id="e04ac-137">Order</span></span> | <span data-ttu-id="e04ac-138">Caminho</span><span class="sxs-lookup"><span data-stu-id="e04ac-138">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="e04ac-139">1</span><span class="sxs-lookup"><span data-stu-id="e04ac-139">1</span></span>     | <span data-ttu-id="e04ac-140">/App1/IFD/EXIF/{UShort = 37381}</span><span class="sxs-lookup"><span data-stu-id="e04ac-140">/app1/ifd/exif/{ushort=37381}</span></span> |
| <span data-ttu-id="e04ac-141">2</span><span class="sxs-lookup"><span data-stu-id="e04ac-141">2</span></span>     | <span data-ttu-id="e04ac-142">/xmp/exif:maxaperturevalue</span><span class="sxs-lookup"><span data-stu-id="e04ac-142">/xmp/exif:maxaperturevalue</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="e04ac-143">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="e04ac-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="e04ac-144">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="e04ac-144">Read Paths</span></span>



| <span data-ttu-id="e04ac-145">Ordem</span><span class="sxs-lookup"><span data-stu-id="e04ac-145">Order</span></span> | <span data-ttu-id="e04ac-146">Caminho</span><span class="sxs-lookup"><span data-stu-id="e04ac-146">Path</span></span>                           | <span data-ttu-id="e04ac-147">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e04ac-147">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="e04ac-148">1</span><span class="sxs-lookup"><span data-stu-id="e04ac-148">1</span></span>     | <span data-ttu-id="e04ac-149">/IFD/EXIF/{UShort = 37381}</span><span class="sxs-lookup"><span data-stu-id="e04ac-149">/ifd/exif/{ushort=37381}</span></span>       |             |
| <span data-ttu-id="e04ac-150">2</span><span class="sxs-lookup"><span data-stu-id="e04ac-150">2</span></span>     | <span data-ttu-id="e04ac-151">/ifd/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="e04ac-151">/ifd/xmp/exif:MaxApertureValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="e04ac-152">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="e04ac-152">Write Paths</span></span>



| <span data-ttu-id="e04ac-153">Ordem</span><span class="sxs-lookup"><span data-stu-id="e04ac-153">Order</span></span> | <span data-ttu-id="e04ac-154">Caminho</span><span class="sxs-lookup"><span data-stu-id="e04ac-154">Path</span></span>                           | <span data-ttu-id="e04ac-155">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="e04ac-155">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="e04ac-156">1</span><span class="sxs-lookup"><span data-stu-id="e04ac-156">1</span></span>     | <span data-ttu-id="e04ac-157">/IFD/EXIF/{UShort = 37381}</span><span class="sxs-lookup"><span data-stu-id="e04ac-157">/ifd/exif/{ushort=37381}</span></span>       |             |
| <span data-ttu-id="e04ac-158">2</span><span class="sxs-lookup"><span data-stu-id="e04ac-158">2</span></span>     | <span data-ttu-id="e04ac-159">/ifd/xmp/exif:MaxApertureValue</span><span class="sxs-lookup"><span data-stu-id="e04ac-159">/ifd/xmp/exif:MaxApertureValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="e04ac-160">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="e04ac-160">Remove Paths</span></span>



| <span data-ttu-id="e04ac-161">Ordem</span><span class="sxs-lookup"><span data-stu-id="e04ac-161">Order</span></span> | <span data-ttu-id="e04ac-162">Caminho</span><span class="sxs-lookup"><span data-stu-id="e04ac-162">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="e04ac-163">1</span><span class="sxs-lookup"><span data-stu-id="e04ac-163">1</span></span>     | <span data-ttu-id="e04ac-164">/IFD/EXIF/{UShort = 37381}</span><span class="sxs-lookup"><span data-stu-id="e04ac-164">/ifd/exif/{ushort=37381}</span></span>       |
| <span data-ttu-id="e04ac-165">2</span><span class="sxs-lookup"><span data-stu-id="e04ac-165">2</span></span>     | <span data-ttu-id="e04ac-166">/ifd/xmp/exif:maxaperturevalue</span><span class="sxs-lookup"><span data-stu-id="e04ac-166">/ifd/xmp/exif:maxaperturevalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e04ac-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="e04ac-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="e04ac-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e04ac-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e04ac-169">System. Photo. MaxAperture</span><span class="sxs-lookup"><span data-stu-id="e04ac-169">System.Photo.MaxAperture</span></span>](../properties/props-system-photo-maxaperture.md)
</dt> </dl>

 

 
