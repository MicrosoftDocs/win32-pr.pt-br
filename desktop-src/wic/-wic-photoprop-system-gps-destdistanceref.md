---
description: A política de metadados de foto para a propriedade System. GPS. DestDistanceRef.
ms.assetid: eb671f34-7366-4182-b72e-0dd7830751e0
title: Política de metadados de foto System. GPS. DestDistanceRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bba6e04bee00aaed868fcc02059403fe479f8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105794448"
---
# <a name="systemgpsdestdistanceref-photo-metadata-policy"></a><span data-ttu-id="43d25-103">Política de metadados de foto System. GPS. DestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="43d25-103">System.GPS.DestDistanceRef Photo Metadata Policy</span></span>

<span data-ttu-id="43d25-104">A política de metadados de foto para a propriedade [System. GPS. DestDistanceRef](../properties/props-system-gps-destdistanceref.md) .</span><span class="sxs-lookup"><span data-stu-id="43d25-104">The photo metadata policy for the [System.GPS.DestDistanceRef](../properties/props-system-gps-destdistanceref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="43d25-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="43d25-105">PKEY</span></span>

<span data-ttu-id="43d25-106">PKEY \_ DestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="43d25-106">PKEY\_DestDistanceRef</span></span>

### <a name="containers"></a><span data-ttu-id="43d25-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="43d25-107">Containers</span></span>

<span data-ttu-id="43d25-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="43d25-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="43d25-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43d25-109">Read-Only</span></span>

<span data-ttu-id="43d25-110">No</span><span class="sxs-lookup"><span data-stu-id="43d25-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="43d25-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="43d25-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="43d25-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="43d25-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="43d25-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="43d25-113">Input Type</span></span>

<span data-ttu-id="43d25-114">VT \_ LPWSTR ou VT \_ LPSTR são aceitos.</span><span class="sxs-lookup"><span data-stu-id="43d25-114">VT\_LPWSTR or VT\_LPSTR are accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="43d25-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="43d25-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="43d25-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="43d25-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="43d25-117">Políticas JPEG</span><span class="sxs-lookup"><span data-stu-id="43d25-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="43d25-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="43d25-118">Read Paths</span></span>



| <span data-ttu-id="43d25-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="43d25-119">Order</span></span> | <span data-ttu-id="43d25-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="43d25-120">Path</span></span>                         | <span data-ttu-id="43d25-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="43d25-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="43d25-122">1</span><span class="sxs-lookup"><span data-stu-id="43d25-122">1</span></span>     | <span data-ttu-id="43d25-123">/App1/IFD/GPS/{UShort = 25}</span><span class="sxs-lookup"><span data-stu-id="43d25-123">/app1/ifd/gps/{ushort=25}</span></span>    | <span data-ttu-id="43d25-124">ascii</span><span class="sxs-lookup"><span data-stu-id="43d25-124">ascii</span></span>       |
| <span data-ttu-id="43d25-125">2</span><span class="sxs-lookup"><span data-stu-id="43d25-125">2</span></span>     | <span data-ttu-id="43d25-126">/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="43d25-126">/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="43d25-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="43d25-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="43d25-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="43d25-128">Write Paths</span></span>



| <span data-ttu-id="43d25-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="43d25-129">Order</span></span> | <span data-ttu-id="43d25-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="43d25-130">Path</span></span>                         | <span data-ttu-id="43d25-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="43d25-131">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="43d25-132">1</span><span class="sxs-lookup"><span data-stu-id="43d25-132">1</span></span>     | <span data-ttu-id="43d25-133">/App1/IFD/GPS/{UShort = 25}</span><span class="sxs-lookup"><span data-stu-id="43d25-133">/app1/ifd/gps/{ushort=25}</span></span>    | <span data-ttu-id="43d25-134">ascii</span><span class="sxs-lookup"><span data-stu-id="43d25-134">ascii</span></span>       |
| <span data-ttu-id="43d25-135">2</span><span class="sxs-lookup"><span data-stu-id="43d25-135">2</span></span>     | <span data-ttu-id="43d25-136">/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="43d25-136">/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="43d25-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="43d25-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="43d25-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="43d25-138">Remove Paths</span></span>



| <span data-ttu-id="43d25-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="43d25-139">Order</span></span> | <span data-ttu-id="43d25-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="43d25-140">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="43d25-141">1</span><span class="sxs-lookup"><span data-stu-id="43d25-141">1</span></span>     | <span data-ttu-id="43d25-142">/App1/IFD/GPS/{UShort = 25}</span><span class="sxs-lookup"><span data-stu-id="43d25-142">/app1/ifd/gps/{ushort=25}</span></span>    |
| <span data-ttu-id="43d25-143">2</span><span class="sxs-lookup"><span data-stu-id="43d25-143">2</span></span>     | <span data-ttu-id="43d25-144">/xmp/exif:gpsdestdistanceref</span><span class="sxs-lookup"><span data-stu-id="43d25-144">/xmp/exif:gpsdestdistanceref</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="43d25-145">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="43d25-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="43d25-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="43d25-146">Read Paths</span></span>



| <span data-ttu-id="43d25-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="43d25-147">Order</span></span> | <span data-ttu-id="43d25-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="43d25-148">Path</span></span>                             | <span data-ttu-id="43d25-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="43d25-149">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="43d25-150">1</span><span class="sxs-lookup"><span data-stu-id="43d25-150">1</span></span>     | <span data-ttu-id="43d25-151">/IFD/GPS/{UShort = 25}</span><span class="sxs-lookup"><span data-stu-id="43d25-151">/ifd/gps/{ushort=25}</span></span>             | <span data-ttu-id="43d25-152">ascii</span><span class="sxs-lookup"><span data-stu-id="43d25-152">ascii</span></span>       |
| <span data-ttu-id="43d25-153">2</span><span class="sxs-lookup"><span data-stu-id="43d25-153">2</span></span>     | <span data-ttu-id="43d25-154">/ifd/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="43d25-154">/ifd/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="43d25-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="43d25-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="43d25-156">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="43d25-156">Write Paths</span></span>



| <span data-ttu-id="43d25-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="43d25-157">Order</span></span> | <span data-ttu-id="43d25-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="43d25-158">Path</span></span>                             | <span data-ttu-id="43d25-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="43d25-159">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="43d25-160">1</span><span class="sxs-lookup"><span data-stu-id="43d25-160">1</span></span>     | <span data-ttu-id="43d25-161">/IFD/GPS/{UShort = 25}</span><span class="sxs-lookup"><span data-stu-id="43d25-161">/ifd/gps/{ushort=25}</span></span>             | <span data-ttu-id="43d25-162">ascii</span><span class="sxs-lookup"><span data-stu-id="43d25-162">ascii</span></span>       |
| <span data-ttu-id="43d25-163">2</span><span class="sxs-lookup"><span data-stu-id="43d25-163">2</span></span>     | <span data-ttu-id="43d25-164">/ifd/xmp/exif:GPSDestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="43d25-164">/ifd/xmp/exif:GPSDestDistanceRef</span></span> | <span data-ttu-id="43d25-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="43d25-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="43d25-166">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="43d25-166">Remove Paths</span></span>



| <span data-ttu-id="43d25-167">Ordem</span><span class="sxs-lookup"><span data-stu-id="43d25-167">Order</span></span> | <span data-ttu-id="43d25-168">Caminho</span><span class="sxs-lookup"><span data-stu-id="43d25-168">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="43d25-169">1</span><span class="sxs-lookup"><span data-stu-id="43d25-169">1</span></span>     | <span data-ttu-id="43d25-170">/IFD/GPS/{UShort = 25}</span><span class="sxs-lookup"><span data-stu-id="43d25-170">/ifd/gps/{ushort=25}</span></span>             |
| <span data-ttu-id="43d25-171">2</span><span class="sxs-lookup"><span data-stu-id="43d25-171">2</span></span>     | <span data-ttu-id="43d25-172">/ifd/xmp/exif:gpsdestdistanceref</span><span class="sxs-lookup"><span data-stu-id="43d25-172">/ifd/xmp/exif:gpsdestdistanceref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="43d25-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="43d25-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="43d25-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="43d25-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43d25-175">System. GPS. DestDistanceRef</span><span class="sxs-lookup"><span data-stu-id="43d25-175">System.GPS.DestDistanceRef</span></span>](../properties/props-system-gps-destdistanceref.md)
</dt> </dl>

 

 
