---
description: A política de metadados de foto para a propriedade System. Image. ColorSpace.
ms.assetid: 10770f16-8db2-4719-bce3-452f578002ec
title: Política de metadados de foto System. Image. ColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6ef2003d05fa19b958b28950f71ec2d5f73027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760580"
---
# <a name="systemimagecolorspace-photo-metadata-policy"></a><span data-ttu-id="0b52b-103">Política de metadados de foto System. Image. ColorSpace</span><span class="sxs-lookup"><span data-stu-id="0b52b-103">System.Image.ColorSpace Photo Metadata Policy</span></span>

<span data-ttu-id="0b52b-104">A política de metadados de foto para a propriedade [System. Image. colorspace](../properties/props-system-image-colorspace.md) .</span><span class="sxs-lookup"><span data-stu-id="0b52b-104">The photo metadata policy for the [System.Image.ColorSpace](../properties/props-system-image-colorspace.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="0b52b-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="0b52b-105">PKEY</span></span>

<span data-ttu-id="0b52b-106">PKEY \_ Image \_ colorspace</span><span class="sxs-lookup"><span data-stu-id="0b52b-106">PKEY\_Image\_ColorSpace</span></span>

### <a name="containers"></a><span data-ttu-id="0b52b-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="0b52b-107">Containers</span></span>

<span data-ttu-id="0b52b-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="0b52b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="0b52b-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b52b-109">Read-Only</span></span>

<span data-ttu-id="0b52b-110">Yes</span><span class="sxs-lookup"><span data-stu-id="0b52b-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="0b52b-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="0b52b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="0b52b-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="0b52b-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="0b52b-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="0b52b-113">Input Type</span></span>

<span data-ttu-id="0b52b-114">UShort</span><span class="sxs-lookup"><span data-stu-id="0b52b-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="0b52b-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="0b52b-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="0b52b-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="0b52b-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="0b52b-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="0b52b-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="0b52b-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="0b52b-118">Read Paths</span></span>



| <span data-ttu-id="0b52b-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="0b52b-119">Order</span></span> | <span data-ttu-id="0b52b-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="0b52b-120">Path</span></span>                          | <span data-ttu-id="0b52b-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="0b52b-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="0b52b-122">1</span><span class="sxs-lookup"><span data-stu-id="0b52b-122">1</span></span>     | <span data-ttu-id="0b52b-123">/App1/IFD/EXIF/{UShort = 40961}</span><span class="sxs-lookup"><span data-stu-id="0b52b-123">/app1/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="0b52b-124">ushort</span><span class="sxs-lookup"><span data-stu-id="0b52b-124">ushort</span></span>      |
| <span data-ttu-id="0b52b-125">2</span><span class="sxs-lookup"><span data-stu-id="0b52b-125">2</span></span>     | <span data-ttu-id="0b52b-126">/xmp/exif:ColorSpace</span><span class="sxs-lookup"><span data-stu-id="0b52b-126">/xmp/exif:ColorSpace</span></span>          | <span data-ttu-id="0b52b-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="0b52b-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0b52b-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="0b52b-128">Write Paths</span></span>



| <span data-ttu-id="0b52b-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="0b52b-129">Order</span></span> | <span data-ttu-id="0b52b-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="0b52b-130">Path</span></span>                          | <span data-ttu-id="0b52b-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="0b52b-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="0b52b-132">1</span><span class="sxs-lookup"><span data-stu-id="0b52b-132">1</span></span>     | <span data-ttu-id="0b52b-133">/App1/IFD/EXIF/{UShort = 40961}</span><span class="sxs-lookup"><span data-stu-id="0b52b-133">/app1/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="0b52b-134">ushort</span><span class="sxs-lookup"><span data-stu-id="0b52b-134">ushort</span></span>      |
| <span data-ttu-id="0b52b-135">2</span><span class="sxs-lookup"><span data-stu-id="0b52b-135">2</span></span>     | <span data-ttu-id="0b52b-136">/xmp/exif:ColorSpace</span><span class="sxs-lookup"><span data-stu-id="0b52b-136">/xmp/exif:ColorSpace</span></span>          | <span data-ttu-id="0b52b-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="0b52b-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0b52b-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="0b52b-138">Remove Paths</span></span>



| <span data-ttu-id="0b52b-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="0b52b-139">Order</span></span> | <span data-ttu-id="0b52b-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="0b52b-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="0b52b-141">1</span><span class="sxs-lookup"><span data-stu-id="0b52b-141">1</span></span>     | <span data-ttu-id="0b52b-142">/App1/IFD/EXIF/{UShort = 40961}</span><span class="sxs-lookup"><span data-stu-id="0b52b-142">/app1/ifd/exif/{ushort=40961}</span></span> |
| <span data-ttu-id="0b52b-143">2</span><span class="sxs-lookup"><span data-stu-id="0b52b-143">2</span></span>     | <span data-ttu-id="0b52b-144">/xmp/exif:colorspace</span><span class="sxs-lookup"><span data-stu-id="0b52b-144">/xmp/exif:colorspace</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="0b52b-145">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="0b52b-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0b52b-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="0b52b-146">Read Paths</span></span>



| <span data-ttu-id="0b52b-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="0b52b-147">Order</span></span> | <span data-ttu-id="0b52b-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="0b52b-148">Path</span></span>                     | <span data-ttu-id="0b52b-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="0b52b-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="0b52b-150">1</span><span class="sxs-lookup"><span data-stu-id="0b52b-150">1</span></span>     | <span data-ttu-id="0b52b-151">/IFD/EXIF/{UShort = 40961}</span><span class="sxs-lookup"><span data-stu-id="0b52b-151">/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="0b52b-152">ushort</span><span class="sxs-lookup"><span data-stu-id="0b52b-152">ushort</span></span>      |
| <span data-ttu-id="0b52b-153">2</span><span class="sxs-lookup"><span data-stu-id="0b52b-153">2</span></span>     | <span data-ttu-id="0b52b-154">/ifd/xmp/exif:ColorSpace</span><span class="sxs-lookup"><span data-stu-id="0b52b-154">/ifd/xmp/exif:ColorSpace</span></span> | <span data-ttu-id="0b52b-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="0b52b-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0b52b-156">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="0b52b-156">Write Paths</span></span>



| <span data-ttu-id="0b52b-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="0b52b-157">Order</span></span> | <span data-ttu-id="0b52b-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="0b52b-158">Path</span></span>                     | <span data-ttu-id="0b52b-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="0b52b-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="0b52b-160">1</span><span class="sxs-lookup"><span data-stu-id="0b52b-160">1</span></span>     | <span data-ttu-id="0b52b-161">/IFD/EXIF/{UShort = 40961}</span><span class="sxs-lookup"><span data-stu-id="0b52b-161">/ifd/exif/{ushort=40961}</span></span> | <span data-ttu-id="0b52b-162">ushort</span><span class="sxs-lookup"><span data-stu-id="0b52b-162">ushort</span></span>      |
| <span data-ttu-id="0b52b-163">2</span><span class="sxs-lookup"><span data-stu-id="0b52b-163">2</span></span>     | <span data-ttu-id="0b52b-164">/ifd/xmp/exif:ColorSpace</span><span class="sxs-lookup"><span data-stu-id="0b52b-164">/ifd/xmp/exif:ColorSpace</span></span> | <span data-ttu-id="0b52b-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="0b52b-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0b52b-166">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="0b52b-166">Remove Paths</span></span>



| <span data-ttu-id="0b52b-167">Ordem</span><span class="sxs-lookup"><span data-stu-id="0b52b-167">Order</span></span> | <span data-ttu-id="0b52b-168">Caminho</span><span class="sxs-lookup"><span data-stu-id="0b52b-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="0b52b-169">1</span><span class="sxs-lookup"><span data-stu-id="0b52b-169">1</span></span>     | <span data-ttu-id="0b52b-170">/IFD/EXIF/{UShort = 40961}</span><span class="sxs-lookup"><span data-stu-id="0b52b-170">/ifd/exif/{ushort=40961}</span></span> |
| <span data-ttu-id="0b52b-171">2</span><span class="sxs-lookup"><span data-stu-id="0b52b-171">2</span></span>     | <span data-ttu-id="0b52b-172">/ifd/xmp/exif:colorspace</span><span class="sxs-lookup"><span data-stu-id="0b52b-172">/ifd/xmp/exif:colorspace</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0b52b-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b52b-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b52b-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0b52b-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b52b-175">System. Image. ColorSpace</span><span class="sxs-lookup"><span data-stu-id="0b52b-175">System.Image.ColorSpace</span></span>](../properties/props-system-image-colorspace.md)
</dt> </dl>

 

 
