---
description: A política de metadados de foto para a propriedade System. Photo. saturação.
ms.assetid: 1dbb7515-7022-404c-928a-9eb09e43e7a7
title: Política de metadados de foto System. Photo. saturação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcb2b199458f063f2c28d7f6780a6ea907f76f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011536"
---
# <a name="systemphotosaturation-photo-metadata-policy"></a><span data-ttu-id="5dfe6-103">Política de metadados de foto System. Photo. saturação</span><span class="sxs-lookup"><span data-stu-id="5dfe6-103">System.Photo.Saturation Photo Metadata Policy</span></span>

<span data-ttu-id="5dfe6-104">A política de metadados de foto para a propriedade [System. Photo. saturação](../properties/props-system-photo-saturation.md) .</span><span class="sxs-lookup"><span data-stu-id="5dfe6-104">The photo metadata policy for the [System.Photo.Saturation](../properties/props-system-photo-saturation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="5dfe6-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="5dfe6-105">PKEY</span></span>

<span data-ttu-id="5dfe6-106">\_Saturação de fotos PKEY \_</span><span class="sxs-lookup"><span data-stu-id="5dfe6-106">PKEY\_Photo\_Saturation</span></span>

### <a name="containers"></a><span data-ttu-id="5dfe6-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="5dfe6-107">Containers</span></span>

<span data-ttu-id="5dfe6-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="5dfe6-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="5dfe6-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5dfe6-109">Read-Only</span></span>

<span data-ttu-id="5dfe6-110">No</span><span class="sxs-lookup"><span data-stu-id="5dfe6-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="5dfe6-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="5dfe6-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="5dfe6-112">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="5dfe6-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="5dfe6-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="5dfe6-113">Input Type</span></span>

<span data-ttu-id="5dfe6-114">UShort</span><span class="sxs-lookup"><span data-stu-id="5dfe6-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="5dfe6-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="5dfe6-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="5dfe6-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="5dfe6-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="5dfe6-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="5dfe6-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="5dfe6-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="5dfe6-118">Read Paths</span></span>



| <span data-ttu-id="5dfe6-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="5dfe6-119">Order</span></span> | <span data-ttu-id="5dfe6-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="5dfe6-120">Path</span></span>                          | <span data-ttu-id="5dfe6-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5dfe6-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="5dfe6-122">1</span><span class="sxs-lookup"><span data-stu-id="5dfe6-122">1</span></span>     | <span data-ttu-id="5dfe6-123">/App1/IFD/EXIF/{UShort = 41993}</span><span class="sxs-lookup"><span data-stu-id="5dfe6-123">/app1/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="5dfe6-124">ushort</span><span class="sxs-lookup"><span data-stu-id="5dfe6-124">ushort</span></span>      |
| <span data-ttu-id="5dfe6-125">2</span><span class="sxs-lookup"><span data-stu-id="5dfe6-125">2</span></span>     | <span data-ttu-id="5dfe6-126">/XMP/EXIF: saturação</span><span class="sxs-lookup"><span data-stu-id="5dfe6-126">/xmp/exif:Saturation</span></span>          | <span data-ttu-id="5dfe6-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="5dfe6-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="5dfe6-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="5dfe6-128">Write Paths</span></span>



| <span data-ttu-id="5dfe6-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="5dfe6-129">Order</span></span> | <span data-ttu-id="5dfe6-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="5dfe6-130">Path</span></span>                          | <span data-ttu-id="5dfe6-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5dfe6-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="5dfe6-132">1</span><span class="sxs-lookup"><span data-stu-id="5dfe6-132">1</span></span>     | <span data-ttu-id="5dfe6-133">/App1/IFD/EXIF/{UShort = 41993}</span><span class="sxs-lookup"><span data-stu-id="5dfe6-133">/app1/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="5dfe6-134">ushort</span><span class="sxs-lookup"><span data-stu-id="5dfe6-134">ushort</span></span>      |
| <span data-ttu-id="5dfe6-135">2</span><span class="sxs-lookup"><span data-stu-id="5dfe6-135">2</span></span>     | <span data-ttu-id="5dfe6-136">/XMP/EXIF: saturação</span><span class="sxs-lookup"><span data-stu-id="5dfe6-136">/xmp/exif:Saturation</span></span>          | <span data-ttu-id="5dfe6-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="5dfe6-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="5dfe6-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="5dfe6-138">Remove Paths</span></span>



| <span data-ttu-id="5dfe6-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="5dfe6-139">Order</span></span> | <span data-ttu-id="5dfe6-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="5dfe6-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="5dfe6-141">1</span><span class="sxs-lookup"><span data-stu-id="5dfe6-141">1</span></span>     | <span data-ttu-id="5dfe6-142">/App1/IFD/EXIF/{UShort = 41993}</span><span class="sxs-lookup"><span data-stu-id="5dfe6-142">/app1/ifd/exif/{ushort=41993}</span></span> |
| <span data-ttu-id="5dfe6-143">2</span><span class="sxs-lookup"><span data-stu-id="5dfe6-143">2</span></span>     | <span data-ttu-id="5dfe6-144">/XMP/EXIF: saturação</span><span class="sxs-lookup"><span data-stu-id="5dfe6-144">/xmp/exif:saturation</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="5dfe6-145">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="5dfe6-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="5dfe6-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="5dfe6-146">Read Paths</span></span>



| <span data-ttu-id="5dfe6-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="5dfe6-147">Order</span></span> | <span data-ttu-id="5dfe6-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="5dfe6-148">Path</span></span>                     | <span data-ttu-id="5dfe6-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5dfe6-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="5dfe6-150">1</span><span class="sxs-lookup"><span data-stu-id="5dfe6-150">1</span></span>     | <span data-ttu-id="5dfe6-151">/IFD/EXIF/{UShort = 41993}</span><span class="sxs-lookup"><span data-stu-id="5dfe6-151">/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="5dfe6-152">ushort</span><span class="sxs-lookup"><span data-stu-id="5dfe6-152">ushort</span></span>      |
| <span data-ttu-id="5dfe6-153">2</span><span class="sxs-lookup"><span data-stu-id="5dfe6-153">2</span></span>     | <span data-ttu-id="5dfe6-154">/IFD/XMP/EXIF: saturação</span><span class="sxs-lookup"><span data-stu-id="5dfe6-154">/ifd/xmp/exif:Saturation</span></span> | <span data-ttu-id="5dfe6-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="5dfe6-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="5dfe6-156">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="5dfe6-156">Write Paths</span></span>



| <span data-ttu-id="5dfe6-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="5dfe6-157">Order</span></span> | <span data-ttu-id="5dfe6-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="5dfe6-158">Path</span></span>                     | <span data-ttu-id="5dfe6-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5dfe6-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="5dfe6-160">1</span><span class="sxs-lookup"><span data-stu-id="5dfe6-160">1</span></span>     | <span data-ttu-id="5dfe6-161">/IFD/EXIF/{UShort = 41993}</span><span class="sxs-lookup"><span data-stu-id="5dfe6-161">/ifd/exif/{ushort=41993}</span></span> | <span data-ttu-id="5dfe6-162">ushort</span><span class="sxs-lookup"><span data-stu-id="5dfe6-162">ushort</span></span>      |
| <span data-ttu-id="5dfe6-163">2</span><span class="sxs-lookup"><span data-stu-id="5dfe6-163">2</span></span>     | <span data-ttu-id="5dfe6-164">/IFD/XMP/EXIF: saturação</span><span class="sxs-lookup"><span data-stu-id="5dfe6-164">/ifd/xmp/exif:Saturation</span></span> | <span data-ttu-id="5dfe6-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="5dfe6-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="5dfe6-166">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="5dfe6-166">Remove Paths</span></span>



| <span data-ttu-id="5dfe6-167">Ordem</span><span class="sxs-lookup"><span data-stu-id="5dfe6-167">Order</span></span> | <span data-ttu-id="5dfe6-168">Caminho</span><span class="sxs-lookup"><span data-stu-id="5dfe6-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="5dfe6-169">1</span><span class="sxs-lookup"><span data-stu-id="5dfe6-169">1</span></span>     | <span data-ttu-id="5dfe6-170">/IFD/EXIF/{UShort = 41993}</span><span class="sxs-lookup"><span data-stu-id="5dfe6-170">/ifd/exif/{ushort=41993}</span></span> |
| <span data-ttu-id="5dfe6-171">2</span><span class="sxs-lookup"><span data-stu-id="5dfe6-171">2</span></span>     | <span data-ttu-id="5dfe6-172">/IFD/XMP/EXIF: saturação</span><span class="sxs-lookup"><span data-stu-id="5dfe6-172">/ifd/xmp/exif:saturation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5dfe6-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="5dfe6-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="5dfe6-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5dfe6-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dfe6-175">System. Photo. saturação</span><span class="sxs-lookup"><span data-stu-id="5dfe6-175">System.Photo.Saturation</span></span>](../properties/props-system-photo-saturation.md)
</dt> </dl>

 

 
