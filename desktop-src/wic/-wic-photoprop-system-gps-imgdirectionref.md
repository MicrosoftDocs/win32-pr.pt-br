---
description: A política de metadados de foto para a propriedade System. GPS. ImgDirectionRef.
ms.assetid: 74ae0989-6d53-4d72-abe9-84f40c0c884a
title: Política de metadados de foto System. GPS. ImgDirectionRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80276ca8d1981935004dbec49fef588fcde330ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171519"
---
# <a name="systemgpsimgdirectionref-photo-metadata-policy"></a><span data-ttu-id="b0891-103">Política de metadados de foto System. GPS. ImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="b0891-103">System.GPS.ImgDirectionRef Photo Metadata Policy</span></span>

<span data-ttu-id="b0891-104">A política de metadados de foto para a propriedade [System. GPS. ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md) .</span><span class="sxs-lookup"><span data-stu-id="b0891-104">The photo metadata policy for the [System.GPS.ImgDirectionRef](../properties/props-system-gps-imgdirectionref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b0891-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="b0891-105">PKEY</span></span>

<span data-ttu-id="b0891-106">PKEY \_ GPS. ImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="b0891-106">PKEY\_GPS.ImgDirectionRef</span></span>

### <a name="containers"></a><span data-ttu-id="b0891-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="b0891-107">Containers</span></span>

<span data-ttu-id="b0891-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b0891-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b0891-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0891-109">Read-Only</span></span>

<span data-ttu-id="b0891-110">No</span><span class="sxs-lookup"><span data-stu-id="b0891-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b0891-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="b0891-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b0891-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="b0891-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="b0891-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="b0891-113">Input Type</span></span>

<span data-ttu-id="b0891-114">VT \_ LPWSTR é preferível, mas VT \_ LPSTR também é aceito.</span><span class="sxs-lookup"><span data-stu-id="b0891-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b0891-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="b0891-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="b0891-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="b0891-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="b0891-117">Políticas JPEG</span><span class="sxs-lookup"><span data-stu-id="b0891-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b0891-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="b0891-118">Read Paths</span></span>



| <span data-ttu-id="b0891-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="b0891-119">Order</span></span> | <span data-ttu-id="b0891-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="b0891-120">Path</span></span>                         | <span data-ttu-id="b0891-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b0891-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="b0891-122">1</span><span class="sxs-lookup"><span data-stu-id="b0891-122">1</span></span>     | <span data-ttu-id="b0891-123">/App1/IFD/GPS/{UShort = 16}</span><span class="sxs-lookup"><span data-stu-id="b0891-123">/app1/ifd/gps/{ushort=16}</span></span>    | <span data-ttu-id="b0891-124">ascii</span><span class="sxs-lookup"><span data-stu-id="b0891-124">ascii</span></span>       |
| <span data-ttu-id="b0891-125">2</span><span class="sxs-lookup"><span data-stu-id="b0891-125">2</span></span>     | <span data-ttu-id="b0891-126">/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="b0891-126">/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="b0891-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="b0891-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="b0891-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="b0891-128">Write Paths</span></span>



| <span data-ttu-id="b0891-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="b0891-129">Order</span></span> | <span data-ttu-id="b0891-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="b0891-130">Path</span></span>                         | <span data-ttu-id="b0891-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b0891-131">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="b0891-132">1</span><span class="sxs-lookup"><span data-stu-id="b0891-132">1</span></span>     | <span data-ttu-id="b0891-133">/App1/IFD/GPS/{UShort = 16}</span><span class="sxs-lookup"><span data-stu-id="b0891-133">/app1/ifd/gps/{ushort=16}</span></span>    | <span data-ttu-id="b0891-134">ascii</span><span class="sxs-lookup"><span data-stu-id="b0891-134">ascii</span></span>       |
| <span data-ttu-id="b0891-135">2</span><span class="sxs-lookup"><span data-stu-id="b0891-135">2</span></span>     | <span data-ttu-id="b0891-136">/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="b0891-136">/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="b0891-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="b0891-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="b0891-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="b0891-138">Remove Paths</span></span>



| <span data-ttu-id="b0891-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="b0891-139">Order</span></span> | <span data-ttu-id="b0891-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="b0891-140">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="b0891-141">1</span><span class="sxs-lookup"><span data-stu-id="b0891-141">1</span></span>     | <span data-ttu-id="b0891-142">/App1/IFD/GPS/{UShort = 16}</span><span class="sxs-lookup"><span data-stu-id="b0891-142">/app1/ifd/gps/{ushort=16}</span></span>    |
| <span data-ttu-id="b0891-143">2</span><span class="sxs-lookup"><span data-stu-id="b0891-143">2</span></span>     | <span data-ttu-id="b0891-144">/xmp/exif:gpsimgdirectionref</span><span class="sxs-lookup"><span data-stu-id="b0891-144">/xmp/exif:gpsimgdirectionref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="b0891-145">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="b0891-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b0891-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="b0891-146">Read Paths</span></span>



| <span data-ttu-id="b0891-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="b0891-147">Order</span></span> | <span data-ttu-id="b0891-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="b0891-148">Path</span></span>                             | <span data-ttu-id="b0891-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b0891-149">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="b0891-150">1</span><span class="sxs-lookup"><span data-stu-id="b0891-150">1</span></span>     | <span data-ttu-id="b0891-151">/IFD/GPS/{UShort = 16}</span><span class="sxs-lookup"><span data-stu-id="b0891-151">/ifd/gps/{ushort=16}</span></span>             | <span data-ttu-id="b0891-152">ascii</span><span class="sxs-lookup"><span data-stu-id="b0891-152">ascii</span></span>       |
| <span data-ttu-id="b0891-153">2</span><span class="sxs-lookup"><span data-stu-id="b0891-153">2</span></span>     | <span data-ttu-id="b0891-154">/ifd/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="b0891-154">/ifd/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="b0891-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="b0891-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="b0891-156">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="b0891-156">Write Paths</span></span>



| <span data-ttu-id="b0891-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="b0891-157">Order</span></span> | <span data-ttu-id="b0891-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="b0891-158">Path</span></span>                             | <span data-ttu-id="b0891-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b0891-159">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="b0891-160">1</span><span class="sxs-lookup"><span data-stu-id="b0891-160">1</span></span>     | <span data-ttu-id="b0891-161">/IFD/GPS/{UShort = 16}</span><span class="sxs-lookup"><span data-stu-id="b0891-161">/ifd/gps/{ushort=16}</span></span>             | <span data-ttu-id="b0891-162">ascii</span><span class="sxs-lookup"><span data-stu-id="b0891-162">ascii</span></span>       |
| <span data-ttu-id="b0891-163">2</span><span class="sxs-lookup"><span data-stu-id="b0891-163">2</span></span>     | <span data-ttu-id="b0891-164">/ifd/xmp/exif:GPSImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="b0891-164">/ifd/xmp/exif:GPSImgDirectionRef</span></span> | <span data-ttu-id="b0891-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="b0891-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="b0891-166">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="b0891-166">Remove Paths</span></span>



| <span data-ttu-id="b0891-167">Ordem</span><span class="sxs-lookup"><span data-stu-id="b0891-167">Order</span></span> | <span data-ttu-id="b0891-168">Caminho</span><span class="sxs-lookup"><span data-stu-id="b0891-168">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="b0891-169">1</span><span class="sxs-lookup"><span data-stu-id="b0891-169">1</span></span>     | <span data-ttu-id="b0891-170">/IFD/GPS/{UShort = 16}</span><span class="sxs-lookup"><span data-stu-id="b0891-170">/ifd/gps/{ushort=16}</span></span>             |
| <span data-ttu-id="b0891-171">2</span><span class="sxs-lookup"><span data-stu-id="b0891-171">2</span></span>     | <span data-ttu-id="b0891-172">/ifd/xmp/exif:gpsimgdirectionref</span><span class="sxs-lookup"><span data-stu-id="b0891-172">/ifd/xmp/exif:gpsimgdirectionref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b0891-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0891-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0891-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0891-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0891-175">System. GPS. ImgDirectionRef</span><span class="sxs-lookup"><span data-stu-id="b0891-175">System.GPS.ImgDirectionRef</span></span>](../properties/props-system-gps-imgdirectionref.md)
</dt> </dl>

 

 
