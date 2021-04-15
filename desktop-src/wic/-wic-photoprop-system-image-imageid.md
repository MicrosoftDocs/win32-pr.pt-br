---
description: A política de metadados de foto para a propriedade System. Image. Imageid.
ms.assetid: 2a092d16-e7b9-4ffe-9bdb-01ed328ca26f
title: Política de metadados de foto System. Image. Imageid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab812a8719c905002c91d33a65cc2b570d37cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505933"
---
# <a name="systemimageimageid-photo-metadata-policy"></a><span data-ttu-id="beccc-103">Política de metadados de foto System. Image. Imageid</span><span class="sxs-lookup"><span data-stu-id="beccc-103">System.Image.ImageID Photo Metadata Policy</span></span>

<span data-ttu-id="beccc-104">A política de metadados de foto para a propriedade [System. Image. imageid](../properties/props-system-image-imageid.md) .</span><span class="sxs-lookup"><span data-stu-id="beccc-104">The photo metadata policy for the [System.Image.ImageID](../properties/props-system-image-imageid.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="beccc-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="beccc-105">PKEY</span></span>

<span data-ttu-id="beccc-106">\_Imageid de imagem PKEY \_</span><span class="sxs-lookup"><span data-stu-id="beccc-106">PKEY\_Image\_ImageID</span></span>

### <a name="containers"></a><span data-ttu-id="beccc-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="beccc-107">Containers</span></span>

<span data-ttu-id="beccc-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="beccc-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="beccc-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="beccc-109">Read-Only</span></span>

<span data-ttu-id="beccc-110">No</span><span class="sxs-lookup"><span data-stu-id="beccc-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="beccc-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="beccc-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="beccc-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="beccc-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="beccc-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="beccc-113">Input Type</span></span>

<span data-ttu-id="beccc-114">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="beccc-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="beccc-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="beccc-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="beccc-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="beccc-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="beccc-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="beccc-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="beccc-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="beccc-118">Read Paths</span></span>



| <span data-ttu-id="beccc-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="beccc-119">Order</span></span> | <span data-ttu-id="beccc-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="beccc-120">Path</span></span>                          | <span data-ttu-id="beccc-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="beccc-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="beccc-122">1</span><span class="sxs-lookup"><span data-stu-id="beccc-122">1</span></span>     | <span data-ttu-id="beccc-123">/App1/IFD/EXIF/{UShort = 42016}</span><span class="sxs-lookup"><span data-stu-id="beccc-123">/app1/ifd/exif/{ushort=42016}</span></span> | <span data-ttu-id="beccc-124">ascii</span><span class="sxs-lookup"><span data-stu-id="beccc-124">ascii</span></span>       |
| <span data-ttu-id="beccc-125">2</span><span class="sxs-lookup"><span data-stu-id="beccc-125">2</span></span>     | <span data-ttu-id="beccc-126">/XMP/EXIF: ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="beccc-126">/xmp/exif:ImageUniqueID</span></span>       | <span data-ttu-id="beccc-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="beccc-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="beccc-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="beccc-128">Write Paths</span></span>



| <span data-ttu-id="beccc-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="beccc-129">Order</span></span> | <span data-ttu-id="beccc-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="beccc-130">Path</span></span>                          | <span data-ttu-id="beccc-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="beccc-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="beccc-132">1</span><span class="sxs-lookup"><span data-stu-id="beccc-132">1</span></span>     | <span data-ttu-id="beccc-133">/App1/IFD/EXIF/{UShort = 42016}</span><span class="sxs-lookup"><span data-stu-id="beccc-133">/app1/ifd/exif/{ushort=42016}</span></span> | <span data-ttu-id="beccc-134">ascii</span><span class="sxs-lookup"><span data-stu-id="beccc-134">ascii</span></span>       |
| <span data-ttu-id="beccc-135">2</span><span class="sxs-lookup"><span data-stu-id="beccc-135">2</span></span>     | <span data-ttu-id="beccc-136">/XMP/EXIF: ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="beccc-136">/xmp/exif:ImageUniqueID</span></span>       | <span data-ttu-id="beccc-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="beccc-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="beccc-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="beccc-138">Remove Paths</span></span>



| <span data-ttu-id="beccc-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="beccc-139">Order</span></span> | <span data-ttu-id="beccc-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="beccc-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="beccc-141">1</span><span class="sxs-lookup"><span data-stu-id="beccc-141">1</span></span>     | <span data-ttu-id="beccc-142">/App1/IFD/EXIF/{UShort = 42016}</span><span class="sxs-lookup"><span data-stu-id="beccc-142">/app1/ifd/exif/{ushort=42016}</span></span> |
| <span data-ttu-id="beccc-143">2</span><span class="sxs-lookup"><span data-stu-id="beccc-143">2</span></span>     | <span data-ttu-id="beccc-144">/XMP/EXIF: ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="beccc-144">/xmp/exif:ImageUniqueID</span></span>       |



 

### <a name="tiff-policy"></a><span data-ttu-id="beccc-145">Política TIFF</span><span class="sxs-lookup"><span data-stu-id="beccc-145">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="beccc-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="beccc-146">Read Paths</span></span>



| <span data-ttu-id="beccc-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="beccc-147">Order</span></span> | <span data-ttu-id="beccc-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="beccc-148">Path</span></span>                        | <span data-ttu-id="beccc-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="beccc-149">Disk Format</span></span> |
|-------|-----------------------------|-------------|
|       | <span data-ttu-id="beccc-150">/IFD/EXIF/{UShort = 42016}</span><span class="sxs-lookup"><span data-stu-id="beccc-150">/ifd/exif/{ushort=42016}</span></span>    | <span data-ttu-id="beccc-151">ascii</span><span class="sxs-lookup"><span data-stu-id="beccc-151">ascii</span></span>       |
|       | <span data-ttu-id="beccc-152">/IFD/XMP/EXIF: ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="beccc-152">/ifd/xmp/exif:ImageUniqueID</span></span> | <span data-ttu-id="beccc-153">Unicode</span><span class="sxs-lookup"><span data-stu-id="beccc-153">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="beccc-154">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="beccc-154">Write Paths</span></span>



| <span data-ttu-id="beccc-155">Ordem</span><span class="sxs-lookup"><span data-stu-id="beccc-155">Order</span></span> | <span data-ttu-id="beccc-156">Caminho</span><span class="sxs-lookup"><span data-stu-id="beccc-156">Path</span></span>                        | <span data-ttu-id="beccc-157">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="beccc-157">Disk Format</span></span> |
|-------|-----------------------------|-------------|
|       | <span data-ttu-id="beccc-158">/IFD/EXIF/{UShort = 42016}</span><span class="sxs-lookup"><span data-stu-id="beccc-158">/ifd/exif/{ushort=42016}</span></span>    | <span data-ttu-id="beccc-159">ascii</span><span class="sxs-lookup"><span data-stu-id="beccc-159">ascii</span></span>       |
|       | <span data-ttu-id="beccc-160">/IFD/XMP/EXIF: ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="beccc-160">/ifd/xmp/exif:ImageUniqueID</span></span> | <span data-ttu-id="beccc-161">Unicode</span><span class="sxs-lookup"><span data-stu-id="beccc-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="beccc-162">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="beccc-162">Remove Paths</span></span>



| <span data-ttu-id="beccc-163">Ordem</span><span class="sxs-lookup"><span data-stu-id="beccc-163">Order</span></span> | <span data-ttu-id="beccc-164">Caminho</span><span class="sxs-lookup"><span data-stu-id="beccc-164">Path</span></span>                        |
|-------|-----------------------------|
|       | <span data-ttu-id="beccc-165">/IFD/EXIF/{UShort = 42016}</span><span class="sxs-lookup"><span data-stu-id="beccc-165">/ifd/exif/{ushort=42016}</span></span>    |
|       | <span data-ttu-id="beccc-166">/IFD/XMP/EXIF: ImageUniqueID</span><span class="sxs-lookup"><span data-stu-id="beccc-166">/ifd/xmp/exif:ImageUniqueID</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="beccc-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="beccc-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="beccc-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="beccc-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="beccc-169">System. Image. Imageid</span><span class="sxs-lookup"><span data-stu-id="beccc-169">System.Image.ImageID</span></span>](../properties/props-system-image-imageid.md)
</dt> </dl>

 

 
