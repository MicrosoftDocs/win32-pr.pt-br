---
description: A política de metadados de foto para a propriedade System. Photo. EXIFVersion.
ms.assetid: 0f9c5ea8-918f-4101-8492-3f408145a73e
title: Política de metadados de foto System. Photo. EXIFVersion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb823db41cb54a06fba235df5be4bb4acd55ea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171316"
---
# <a name="systemphotoexifversion-photo-metadata-policy"></a><span data-ttu-id="d81b7-103">Política de metadados de foto System. Photo. EXIFVersion</span><span class="sxs-lookup"><span data-stu-id="d81b7-103">System.Photo.EXIFVersion Photo Metadata Policy</span></span>

<span data-ttu-id="d81b7-104">A política de metadados de foto para a propriedade [System. Photo. EXIFVersion](../properties/props-system-photo-exifversion.md) .</span><span class="sxs-lookup"><span data-stu-id="d81b7-104">The photo metadata policy for the [System.Photo.EXIFVersion](../properties/props-system-photo-exifversion.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d81b7-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="d81b7-105">PKEY</span></span>

<span data-ttu-id="d81b7-106">PKEY \_ Photo \_ EXIFVersion</span><span class="sxs-lookup"><span data-stu-id="d81b7-106">PKEY\_Photo\_EXIFVersion</span></span>

### <a name="containers"></a><span data-ttu-id="d81b7-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="d81b7-107">Containers</span></span>

<span data-ttu-id="d81b7-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d81b7-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d81b7-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d81b7-109">Read-Only</span></span>

<span data-ttu-id="d81b7-110">No</span><span class="sxs-lookup"><span data-stu-id="d81b7-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d81b7-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="d81b7-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d81b7-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="d81b7-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="d81b7-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="d81b7-113">Input Type</span></span>

<span data-ttu-id="d81b7-114">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d81b7-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d81b7-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="d81b7-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="d81b7-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="d81b7-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="d81b7-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="d81b7-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d81b7-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="d81b7-118">Read Paths</span></span>



| <span data-ttu-id="d81b7-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="d81b7-119">Order</span></span> | <span data-ttu-id="d81b7-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="d81b7-120">Path</span></span>                          | <span data-ttu-id="d81b7-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d81b7-121">Disk Format</span></span>   |
|-------|-------------------------------|---------------|
| <span data-ttu-id="d81b7-122">1</span><span class="sxs-lookup"><span data-stu-id="d81b7-122">1</span></span>     | <span data-ttu-id="d81b7-123">/App1/IFD/EXIF/{UShort = 36864}</span><span class="sxs-lookup"><span data-stu-id="d81b7-123">/app1/ifd/exif/{ushort=36864}</span></span> | <span data-ttu-id="d81b7-124">versão do EXIF \_</span><span class="sxs-lookup"><span data-stu-id="d81b7-124">exif\_version</span></span> |
| <span data-ttu-id="d81b7-125">2</span><span class="sxs-lookup"><span data-stu-id="d81b7-125">2</span></span>     | <span data-ttu-id="d81b7-126">/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="d81b7-126">/xmp/exif:ExifVersion</span></span>         | <span data-ttu-id="d81b7-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="d81b7-127">unicode</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="d81b7-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="d81b7-128">Write Paths</span></span>



| <span data-ttu-id="d81b7-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="d81b7-129">Order</span></span> | <span data-ttu-id="d81b7-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="d81b7-130">Path</span></span>                          | <span data-ttu-id="d81b7-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d81b7-131">Disk Format</span></span>   |
|-------|-------------------------------|---------------|
| <span data-ttu-id="d81b7-132">1</span><span class="sxs-lookup"><span data-stu-id="d81b7-132">1</span></span>     | <span data-ttu-id="d81b7-133">/App1/IFD/EXIF/{UShort = 36864}</span><span class="sxs-lookup"><span data-stu-id="d81b7-133">/app1/ifd/exif/{ushort=36864}</span></span> | <span data-ttu-id="d81b7-134">versão do EXIF \_</span><span class="sxs-lookup"><span data-stu-id="d81b7-134">exif\_version</span></span> |
| <span data-ttu-id="d81b7-135">2</span><span class="sxs-lookup"><span data-stu-id="d81b7-135">2</span></span>     | <span data-ttu-id="d81b7-136">/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="d81b7-136">/xmp/exif:ExifVersion</span></span>         | <span data-ttu-id="d81b7-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="d81b7-137">unicode</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="d81b7-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="d81b7-138">Remove Paths</span></span>



| <span data-ttu-id="d81b7-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="d81b7-139">Order</span></span> | <span data-ttu-id="d81b7-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="d81b7-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="d81b7-141">1</span><span class="sxs-lookup"><span data-stu-id="d81b7-141">1</span></span>     | <span data-ttu-id="d81b7-142">/App1/IFD/EXIF/{UShort = 36864}</span><span class="sxs-lookup"><span data-stu-id="d81b7-142">/app1/ifd/exif/{ushort=36864}</span></span> |
| <span data-ttu-id="d81b7-143">2</span><span class="sxs-lookup"><span data-stu-id="d81b7-143">2</span></span>     | <span data-ttu-id="d81b7-144">/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="d81b7-144">/xmp/exif:ExifVersion</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="d81b7-145">Política TIFF</span><span class="sxs-lookup"><span data-stu-id="d81b7-145">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d81b7-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="d81b7-146">Read Paths</span></span>



| <span data-ttu-id="d81b7-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="d81b7-147">Order</span></span> | <span data-ttu-id="d81b7-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="d81b7-148">Path</span></span>                      | <span data-ttu-id="d81b7-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d81b7-149">Disk Format</span></span>   |
|-------|---------------------------|---------------|
| <span data-ttu-id="d81b7-150">1</span><span class="sxs-lookup"><span data-stu-id="d81b7-150">1</span></span>     | <span data-ttu-id="d81b7-151">/IFD/EXIF/{UShort = 36864}</span><span class="sxs-lookup"><span data-stu-id="d81b7-151">/ifd/exif/{ushort=36864}</span></span>  | <span data-ttu-id="d81b7-152">versão do EXIF \_</span><span class="sxs-lookup"><span data-stu-id="d81b7-152">exif\_version</span></span> |
| <span data-ttu-id="d81b7-153">2</span><span class="sxs-lookup"><span data-stu-id="d81b7-153">2</span></span>     | <span data-ttu-id="d81b7-154">/ifd/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="d81b7-154">/ifd/xmp/exif:ExifVersion</span></span> | <span data-ttu-id="d81b7-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="d81b7-155">unicode</span></span>       |



 

### <a name="write-paths"></a><span data-ttu-id="d81b7-156">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="d81b7-156">Write Paths</span></span>



| <span data-ttu-id="d81b7-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="d81b7-157">Order</span></span> | <span data-ttu-id="d81b7-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="d81b7-158">Path</span></span>                      | <span data-ttu-id="d81b7-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d81b7-159">Disk Format</span></span>   |
|-------|---------------------------|---------------|
| <span data-ttu-id="d81b7-160">1</span><span class="sxs-lookup"><span data-stu-id="d81b7-160">1</span></span>     | <span data-ttu-id="d81b7-161">/IFD/EXIF/{UShort = 36864}</span><span class="sxs-lookup"><span data-stu-id="d81b7-161">/ifd/exif/{ushort=36864}</span></span>  | <span data-ttu-id="d81b7-162">versão do EXIF \_</span><span class="sxs-lookup"><span data-stu-id="d81b7-162">exif\_version</span></span> |
| <span data-ttu-id="d81b7-163">2</span><span class="sxs-lookup"><span data-stu-id="d81b7-163">2</span></span>     | <span data-ttu-id="d81b7-164">/ifd/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="d81b7-164">/ifd/xmp/exif:ExifVersion</span></span> | <span data-ttu-id="d81b7-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="d81b7-165">unicode</span></span>       |



 

### <a name="remove-paths"></a><span data-ttu-id="d81b7-166">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="d81b7-166">Remove Paths</span></span>



| <span data-ttu-id="d81b7-167">Ordem</span><span class="sxs-lookup"><span data-stu-id="d81b7-167">Order</span></span> | <span data-ttu-id="d81b7-168">Caminho</span><span class="sxs-lookup"><span data-stu-id="d81b7-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="d81b7-169">1</span><span class="sxs-lookup"><span data-stu-id="d81b7-169">1</span></span>     | <span data-ttu-id="d81b7-170">/IFD/EXIF/{UShort = 36864}</span><span class="sxs-lookup"><span data-stu-id="d81b7-170">/ifd/exif/{ushort=36864}</span></span>  |
| <span data-ttu-id="d81b7-171">2</span><span class="sxs-lookup"><span data-stu-id="d81b7-171">2</span></span>     | <span data-ttu-id="d81b7-172">/ifd/xmp/exif:ExifVersion</span><span class="sxs-lookup"><span data-stu-id="d81b7-172">/ifd/xmp/exif:ExifVersion</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d81b7-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="d81b7-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d81b7-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d81b7-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d81b7-175">System. Photo. EXIFVersion</span><span class="sxs-lookup"><span data-stu-id="d81b7-175">System.Photo.EXIFVersion</span></span>](../properties/props-system-photo-exifversion.md)
</dt> </dl>

 

 
