---
description: A política de metadados de foto para a propriedade System. GPS. TrackRef.
ms.assetid: e6912177-8add-4520-b396-c28060b359c7
title: Política de metadados de foto System. GPS. TrackRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95fc63de6eaffd697798c08ff74a46c3d15c7818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172057"
---
# <a name="systemgpstrackref-photo-metadata-policy"></a><span data-ttu-id="f94a3-103">Política de metadados de foto System. GPS. TrackRef</span><span class="sxs-lookup"><span data-stu-id="f94a3-103">System.GPS.TrackRef Photo Metadata Policy</span></span>

<span data-ttu-id="f94a3-104">A política de metadados de foto para a propriedade [System. GPS. TrackRef](../properties/props-system-gps-trackref.md) .</span><span class="sxs-lookup"><span data-stu-id="f94a3-104">The photo metadata policy for the [System.GPS.TrackRef](../properties/props-system-gps-trackref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f94a3-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="f94a3-105">PKEY</span></span>

<span data-ttu-id="f94a3-106">PKEY \_ GPS \_ TrackRef</span><span class="sxs-lookup"><span data-stu-id="f94a3-106">PKEY\_GPS\_TrackRef</span></span>

### <a name="containers"></a><span data-ttu-id="f94a3-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="f94a3-107">Containers</span></span>

<span data-ttu-id="f94a3-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f94a3-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f94a3-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f94a3-109">Read-Only</span></span>

<span data-ttu-id="f94a3-110">No</span><span class="sxs-lookup"><span data-stu-id="f94a3-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f94a3-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="f94a3-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f94a3-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="f94a3-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="f94a3-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="f94a3-113">Input Type</span></span>

<span data-ttu-id="f94a3-114">String</span><span class="sxs-lookup"><span data-stu-id="f94a3-114">String</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f94a3-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="f94a3-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="f94a3-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="f94a3-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="f94a3-117">Políticas JPEG</span><span class="sxs-lookup"><span data-stu-id="f94a3-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="f94a3-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="f94a3-118">Read Paths</span></span>



| <span data-ttu-id="f94a3-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="f94a3-119">Order</span></span> | <span data-ttu-id="f94a3-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="f94a3-120">Path</span></span>                      | <span data-ttu-id="f94a3-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="f94a3-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="f94a3-122">1</span><span class="sxs-lookup"><span data-stu-id="f94a3-122">1</span></span>     | <span data-ttu-id="f94a3-123">/App1/IFD/GPS/{UShort = 14}</span><span class="sxs-lookup"><span data-stu-id="f94a3-123">/app1/ifd/gps/{ushort=14}</span></span> | <span data-ttu-id="f94a3-124">ascii</span><span class="sxs-lookup"><span data-stu-id="f94a3-124">ascii</span></span>       |
| <span data-ttu-id="f94a3-125">2</span><span class="sxs-lookup"><span data-stu-id="f94a3-125">2</span></span>     | <span data-ttu-id="f94a3-126">/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="f94a3-126">/xmp/exif:GPSTrackRef</span></span>     | <span data-ttu-id="f94a3-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="f94a3-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="f94a3-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="f94a3-128">Write Paths</span></span>



| <span data-ttu-id="f94a3-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="f94a3-129">Order</span></span> | <span data-ttu-id="f94a3-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="f94a3-130">Path</span></span>                      | <span data-ttu-id="f94a3-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="f94a3-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="f94a3-132">1</span><span class="sxs-lookup"><span data-stu-id="f94a3-132">1</span></span>     | <span data-ttu-id="f94a3-133">/App1/IFD/GPS/{UShort = 14}</span><span class="sxs-lookup"><span data-stu-id="f94a3-133">/app1/ifd/gps/{ushort=14}</span></span> | <span data-ttu-id="f94a3-134">ascii</span><span class="sxs-lookup"><span data-stu-id="f94a3-134">ascii</span></span>       |
| <span data-ttu-id="f94a3-135">2</span><span class="sxs-lookup"><span data-stu-id="f94a3-135">2</span></span>     | <span data-ttu-id="f94a3-136">/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="f94a3-136">/xmp/exif:GPSTrackRef</span></span>     | <span data-ttu-id="f94a3-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="f94a3-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="f94a3-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="f94a3-138">Remove Paths</span></span>



| <span data-ttu-id="f94a3-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="f94a3-139">Order</span></span> | <span data-ttu-id="f94a3-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="f94a3-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="f94a3-141">1</span><span class="sxs-lookup"><span data-stu-id="f94a3-141">1</span></span>     | <span data-ttu-id="f94a3-142">/App1/IFD/GPS/{UShort = 14}</span><span class="sxs-lookup"><span data-stu-id="f94a3-142">/app1/ifd/gps/{ushort=14}</span></span> |
| <span data-ttu-id="f94a3-143">2</span><span class="sxs-lookup"><span data-stu-id="f94a3-143">2</span></span>     | <span data-ttu-id="f94a3-144">/xmp/exif:gpstrackref</span><span class="sxs-lookup"><span data-stu-id="f94a3-144">/xmp/exif:gpstrackref</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="f94a3-145">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="f94a3-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="f94a3-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="f94a3-146">Read Paths</span></span>



| <span data-ttu-id="f94a3-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="f94a3-147">Order</span></span> | <span data-ttu-id="f94a3-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="f94a3-148">Path</span></span>                      | <span data-ttu-id="f94a3-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="f94a3-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="f94a3-150">1</span><span class="sxs-lookup"><span data-stu-id="f94a3-150">1</span></span>     | <span data-ttu-id="f94a3-151">/IFD/GPS/{UShort = 14}</span><span class="sxs-lookup"><span data-stu-id="f94a3-151">/ifd/gps/{ushort=14}</span></span>      | <span data-ttu-id="f94a3-152">ascii</span><span class="sxs-lookup"><span data-stu-id="f94a3-152">ascii</span></span>       |
| <span data-ttu-id="f94a3-153">2</span><span class="sxs-lookup"><span data-stu-id="f94a3-153">2</span></span>     | <span data-ttu-id="f94a3-154">/ifd/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="f94a3-154">/ifd/xmp/exif:GPSTrackRef</span></span> | <span data-ttu-id="f94a3-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="f94a3-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="f94a3-156">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="f94a3-156">Write Paths</span></span>



| <span data-ttu-id="f94a3-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="f94a3-157">Order</span></span> | <span data-ttu-id="f94a3-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="f94a3-158">Path</span></span>                      | <span data-ttu-id="f94a3-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="f94a3-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="f94a3-160">1</span><span class="sxs-lookup"><span data-stu-id="f94a3-160">1</span></span>     | <span data-ttu-id="f94a3-161">/IFD/GPS/{UShort = 14}</span><span class="sxs-lookup"><span data-stu-id="f94a3-161">/ifd/gps/{ushort=14}</span></span>      | <span data-ttu-id="f94a3-162">ascii</span><span class="sxs-lookup"><span data-stu-id="f94a3-162">ascii</span></span>       |
| <span data-ttu-id="f94a3-163">2</span><span class="sxs-lookup"><span data-stu-id="f94a3-163">2</span></span>     | <span data-ttu-id="f94a3-164">/ifd/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="f94a3-164">/ifd/xmp/exif:GPSTrackRef</span></span> | <span data-ttu-id="f94a3-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="f94a3-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="f94a3-166">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="f94a3-166">Remove Paths</span></span>



| <span data-ttu-id="f94a3-167">Ordem</span><span class="sxs-lookup"><span data-stu-id="f94a3-167">Order</span></span> | <span data-ttu-id="f94a3-168">Caminho</span><span class="sxs-lookup"><span data-stu-id="f94a3-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="f94a3-169">1</span><span class="sxs-lookup"><span data-stu-id="f94a3-169">1</span></span>     | <span data-ttu-id="f94a3-170">/IFD/GPS/{UShort = 14}</span><span class="sxs-lookup"><span data-stu-id="f94a3-170">/ifd/gps/{ushort=14}</span></span>      |
| <span data-ttu-id="f94a3-171">2</span><span class="sxs-lookup"><span data-stu-id="f94a3-171">2</span></span>     | <span data-ttu-id="f94a3-172">/ifd/xmp/exif:gpstrackref</span><span class="sxs-lookup"><span data-stu-id="f94a3-172">/ifd/xmp/exif:gpstrackref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f94a3-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="f94a3-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f94a3-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f94a3-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f94a3-175">System. GPS. TrackRef</span><span class="sxs-lookup"><span data-stu-id="f94a3-175">System.GPS.TrackRef</span></span>](../properties/props-system-gps-trackref.md)
</dt> </dl>

 

 
