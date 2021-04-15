---
description: A política de metadados de foto para a propriedade System. Photo. Contrast.
ms.assetid: c5e2589d-507c-4b92-9ada-7d64e7c45dd8
title: Política de metadados de foto System. Photo. Contrast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d6ed34854b525e9eaac2ff5ac7339a75ad10e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506264"
---
# <a name="systemphotocontrast-photo-metadata-policy"></a><span data-ttu-id="a5ced-103">Política de metadados de foto System. Photo. Contrast</span><span class="sxs-lookup"><span data-stu-id="a5ced-103">System.Photo.Contrast Photo Metadata Policy</span></span>

<span data-ttu-id="a5ced-104">A política de metadados de foto para a propriedade [System. Photo. Contrast](../properties/props-system-photo-contrast.md) .</span><span class="sxs-lookup"><span data-stu-id="a5ced-104">The photo metadata policy for the [System.Photo.Contrast](../properties/props-system-photo-contrast.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a5ced-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a5ced-105">PKEY</span></span>

<span data-ttu-id="a5ced-106">\_Contraste de fotos PKEY \_</span><span class="sxs-lookup"><span data-stu-id="a5ced-106">PKEY\_Photo\_Contrast</span></span>

### <a name="containers"></a><span data-ttu-id="a5ced-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="a5ced-107">Containers</span></span>

<span data-ttu-id="a5ced-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a5ced-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a5ced-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a5ced-109">Read-Only</span></span>

<span data-ttu-id="a5ced-110">No</span><span class="sxs-lookup"><span data-stu-id="a5ced-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a5ced-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="a5ced-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a5ced-112">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="a5ced-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="a5ced-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="a5ced-113">Input Type</span></span>

<span data-ttu-id="a5ced-114">UShort</span><span class="sxs-lookup"><span data-stu-id="a5ced-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a5ced-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="a5ced-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a5ced-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="a5ced-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a5ced-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="a5ced-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a5ced-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="a5ced-118">Read Paths</span></span>



| <span data-ttu-id="a5ced-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="a5ced-119">Order</span></span> | <span data-ttu-id="a5ced-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="a5ced-120">Path</span></span>                          | <span data-ttu-id="a5ced-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a5ced-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a5ced-122">1</span><span class="sxs-lookup"><span data-stu-id="a5ced-122">1</span></span>     | <span data-ttu-id="a5ced-123">/App1/IFD/EXIF/{UShort = 41992}</span><span class="sxs-lookup"><span data-stu-id="a5ced-123">/app1/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="a5ced-124">ushort</span><span class="sxs-lookup"><span data-stu-id="a5ced-124">ushort</span></span>      |
| <span data-ttu-id="a5ced-125">2</span><span class="sxs-lookup"><span data-stu-id="a5ced-125">2</span></span>     | <span data-ttu-id="a5ced-126">/XMP/EXIF: contraste</span><span class="sxs-lookup"><span data-stu-id="a5ced-126">/xmp/exif:Contrast</span></span>            | <span data-ttu-id="a5ced-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="a5ced-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a5ced-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="a5ced-128">Write Paths</span></span>



| <span data-ttu-id="a5ced-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="a5ced-129">Order</span></span> | <span data-ttu-id="a5ced-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="a5ced-130">Path</span></span>                          | <span data-ttu-id="a5ced-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a5ced-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a5ced-132">1</span><span class="sxs-lookup"><span data-stu-id="a5ced-132">1</span></span>     | <span data-ttu-id="a5ced-133">/App1/IFD/EXIF/{UShort = 41992}</span><span class="sxs-lookup"><span data-stu-id="a5ced-133">/app1/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="a5ced-134">ushort</span><span class="sxs-lookup"><span data-stu-id="a5ced-134">ushort</span></span>      |
| <span data-ttu-id="a5ced-135">2</span><span class="sxs-lookup"><span data-stu-id="a5ced-135">2</span></span>     | <span data-ttu-id="a5ced-136">/XMP/EXIF: contraste</span><span class="sxs-lookup"><span data-stu-id="a5ced-136">/xmp/exif:Contrast</span></span>            | <span data-ttu-id="a5ced-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="a5ced-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a5ced-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="a5ced-138">Remove Paths</span></span>



| <span data-ttu-id="a5ced-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="a5ced-139">Order</span></span> | <span data-ttu-id="a5ced-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="a5ced-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="a5ced-141">1</span><span class="sxs-lookup"><span data-stu-id="a5ced-141">1</span></span>     | <span data-ttu-id="a5ced-142">/App1/IFD/EXIF/{UShort = 41992}</span><span class="sxs-lookup"><span data-stu-id="a5ced-142">/app1/ifd/exif/{ushort=41992}</span></span> |
| <span data-ttu-id="a5ced-143">2</span><span class="sxs-lookup"><span data-stu-id="a5ced-143">2</span></span>     | <span data-ttu-id="a5ced-144">/XMP/EXIF: contraste</span><span class="sxs-lookup"><span data-stu-id="a5ced-144">/xmp/exif:contrast</span></span>            |



 

### <a name="tiff-policies"></a><span data-ttu-id="a5ced-145">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="a5ced-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a5ced-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="a5ced-146">Read Paths</span></span>



| <span data-ttu-id="a5ced-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="a5ced-147">Order</span></span> | <span data-ttu-id="a5ced-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="a5ced-148">Path</span></span>                     | <span data-ttu-id="a5ced-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a5ced-149">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="a5ced-150">1</span><span class="sxs-lookup"><span data-stu-id="a5ced-150">1</span></span>     | <span data-ttu-id="a5ced-151">/IFD/EXIF/{UShort = 41992}</span><span class="sxs-lookup"><span data-stu-id="a5ced-151">/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="a5ced-152">ushort</span><span class="sxs-lookup"><span data-stu-id="a5ced-152">ushort</span></span>      |
| <span data-ttu-id="a5ced-153">2</span><span class="sxs-lookup"><span data-stu-id="a5ced-153">2</span></span>     | <span data-ttu-id="a5ced-154">/IFD/XMP/EXIF: contraste</span><span class="sxs-lookup"><span data-stu-id="a5ced-154">/ifd/xmp/exif:Contrast</span></span>   | <span data-ttu-id="a5ced-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="a5ced-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a5ced-156">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="a5ced-156">Write Paths</span></span>



| <span data-ttu-id="a5ced-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="a5ced-157">Order</span></span> | <span data-ttu-id="a5ced-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="a5ced-158">Path</span></span>                     | <span data-ttu-id="a5ced-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a5ced-159">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="a5ced-160">1</span><span class="sxs-lookup"><span data-stu-id="a5ced-160">1</span></span>     | <span data-ttu-id="a5ced-161">/IFD/EXIF/{UShort = 41992}</span><span class="sxs-lookup"><span data-stu-id="a5ced-161">/ifd/exif/{ushort=41992}</span></span> | <span data-ttu-id="a5ced-162">ushort</span><span class="sxs-lookup"><span data-stu-id="a5ced-162">ushort</span></span>      |
| <span data-ttu-id="a5ced-163">2</span><span class="sxs-lookup"><span data-stu-id="a5ced-163">2</span></span>     | <span data-ttu-id="a5ced-164">/IFD/XMP/EXIF: contraste</span><span class="sxs-lookup"><span data-stu-id="a5ced-164">/ifd/xmp/exif:Contrast</span></span>   | <span data-ttu-id="a5ced-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="a5ced-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a5ced-166">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="a5ced-166">Remove Paths</span></span>



| <span data-ttu-id="a5ced-167">Ordem</span><span class="sxs-lookup"><span data-stu-id="a5ced-167">Order</span></span> | <span data-ttu-id="a5ced-168">Caminho</span><span class="sxs-lookup"><span data-stu-id="a5ced-168">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="a5ced-169">1</span><span class="sxs-lookup"><span data-stu-id="a5ced-169">1</span></span>     | <span data-ttu-id="a5ced-170">/IFD/EXIF/{UShort = 41992}</span><span class="sxs-lookup"><span data-stu-id="a5ced-170">/ifd/exif/{ushort=41992}</span></span> |
| <span data-ttu-id="a5ced-171">2</span><span class="sxs-lookup"><span data-stu-id="a5ced-171">2</span></span>     | <span data-ttu-id="a5ced-172">/IFD/XMP/EXIF: contraste</span><span class="sxs-lookup"><span data-stu-id="a5ced-172">/ifd/xmp/exif:contrast</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="a5ced-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5ced-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5ced-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a5ced-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5ced-175">System. Photo. Contrast</span><span class="sxs-lookup"><span data-stu-id="a5ced-175">System.Photo.Contrast</span></span>](../properties/props-system-photo-contrast.md)
</dt> </dl>

 

 
