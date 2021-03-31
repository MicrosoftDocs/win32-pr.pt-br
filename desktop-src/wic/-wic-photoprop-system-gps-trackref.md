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
# <a name="systemgpstrackref-photo-metadata-policy"></a><span data-ttu-id="295f8-103">Política de metadados de foto System. GPS. TrackRef</span><span class="sxs-lookup"><span data-stu-id="295f8-103">System.GPS.TrackRef Photo Metadata Policy</span></span>

<span data-ttu-id="295f8-104">A política de metadados de foto para a propriedade [System. GPS. TrackRef](../properties/props-system-gps-trackref.md) .</span><span class="sxs-lookup"><span data-stu-id="295f8-104">The photo metadata policy for the [System.GPS.TrackRef](../properties/props-system-gps-trackref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="295f8-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="295f8-105">PKEY</span></span>

<span data-ttu-id="295f8-106">PKEY \_ GPS \_ TrackRef</span><span class="sxs-lookup"><span data-stu-id="295f8-106">PKEY\_GPS\_TrackRef</span></span>

### <a name="containers"></a><span data-ttu-id="295f8-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="295f8-107">Containers</span></span>

<span data-ttu-id="295f8-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="295f8-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="295f8-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="295f8-109">Read-Only</span></span>

<span data-ttu-id="295f8-110">Não</span><span class="sxs-lookup"><span data-stu-id="295f8-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="295f8-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="295f8-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="295f8-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="295f8-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="295f8-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="295f8-113">Input Type</span></span>

<span data-ttu-id="295f8-114">String</span><span class="sxs-lookup"><span data-stu-id="295f8-114">String</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="295f8-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="295f8-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="295f8-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="295f8-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="295f8-117">Políticas JPEG</span><span class="sxs-lookup"><span data-stu-id="295f8-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="295f8-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="295f8-118">Read Paths</span></span>



| <span data-ttu-id="295f8-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="295f8-119">Order</span></span> | <span data-ttu-id="295f8-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="295f8-120">Path</span></span>                      | <span data-ttu-id="295f8-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="295f8-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="295f8-122">1</span><span class="sxs-lookup"><span data-stu-id="295f8-122">1</span></span>     | <span data-ttu-id="295f8-123">/App1/IFD/GPS/{UShort = 14}</span><span class="sxs-lookup"><span data-stu-id="295f8-123">/app1/ifd/gps/{ushort=14}</span></span> | <span data-ttu-id="295f8-124">ascii</span><span class="sxs-lookup"><span data-stu-id="295f8-124">ascii</span></span>       |
| <span data-ttu-id="295f8-125">2</span><span class="sxs-lookup"><span data-stu-id="295f8-125">2</span></span>     | <span data-ttu-id="295f8-126">/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="295f8-126">/xmp/exif:GPSTrackRef</span></span>     | <span data-ttu-id="295f8-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="295f8-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="295f8-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="295f8-128">Write Paths</span></span>



| <span data-ttu-id="295f8-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="295f8-129">Order</span></span> | <span data-ttu-id="295f8-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="295f8-130">Path</span></span>                      | <span data-ttu-id="295f8-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="295f8-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="295f8-132">1</span><span class="sxs-lookup"><span data-stu-id="295f8-132">1</span></span>     | <span data-ttu-id="295f8-133">/App1/IFD/GPS/{UShort = 14}</span><span class="sxs-lookup"><span data-stu-id="295f8-133">/app1/ifd/gps/{ushort=14}</span></span> | <span data-ttu-id="295f8-134">ascii</span><span class="sxs-lookup"><span data-stu-id="295f8-134">ascii</span></span>       |
| <span data-ttu-id="295f8-135">2</span><span class="sxs-lookup"><span data-stu-id="295f8-135">2</span></span>     | <span data-ttu-id="295f8-136">/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="295f8-136">/xmp/exif:GPSTrackRef</span></span>     | <span data-ttu-id="295f8-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="295f8-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="295f8-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="295f8-138">Remove Paths</span></span>



| <span data-ttu-id="295f8-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="295f8-139">Order</span></span> | <span data-ttu-id="295f8-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="295f8-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="295f8-141">1</span><span class="sxs-lookup"><span data-stu-id="295f8-141">1</span></span>     | <span data-ttu-id="295f8-142">/App1/IFD/GPS/{UShort = 14}</span><span class="sxs-lookup"><span data-stu-id="295f8-142">/app1/ifd/gps/{ushort=14}</span></span> |
| <span data-ttu-id="295f8-143">2</span><span class="sxs-lookup"><span data-stu-id="295f8-143">2</span></span>     | <span data-ttu-id="295f8-144">/xmp/exif:gpstrackref</span><span class="sxs-lookup"><span data-stu-id="295f8-144">/xmp/exif:gpstrackref</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="295f8-145">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="295f8-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="295f8-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="295f8-146">Read Paths</span></span>



| <span data-ttu-id="295f8-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="295f8-147">Order</span></span> | <span data-ttu-id="295f8-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="295f8-148">Path</span></span>                      | <span data-ttu-id="295f8-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="295f8-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="295f8-150">1</span><span class="sxs-lookup"><span data-stu-id="295f8-150">1</span></span>     | <span data-ttu-id="295f8-151">/IFD/GPS/{UShort = 14}</span><span class="sxs-lookup"><span data-stu-id="295f8-151">/ifd/gps/{ushort=14}</span></span>      | <span data-ttu-id="295f8-152">ascii</span><span class="sxs-lookup"><span data-stu-id="295f8-152">ascii</span></span>       |
| <span data-ttu-id="295f8-153">2</span><span class="sxs-lookup"><span data-stu-id="295f8-153">2</span></span>     | <span data-ttu-id="295f8-154">/ifd/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="295f8-154">/ifd/xmp/exif:GPSTrackRef</span></span> | <span data-ttu-id="295f8-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="295f8-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="295f8-156">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="295f8-156">Write Paths</span></span>



| <span data-ttu-id="295f8-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="295f8-157">Order</span></span> | <span data-ttu-id="295f8-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="295f8-158">Path</span></span>                      | <span data-ttu-id="295f8-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="295f8-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="295f8-160">1</span><span class="sxs-lookup"><span data-stu-id="295f8-160">1</span></span>     | <span data-ttu-id="295f8-161">/IFD/GPS/{UShort = 14}</span><span class="sxs-lookup"><span data-stu-id="295f8-161">/ifd/gps/{ushort=14}</span></span>      | <span data-ttu-id="295f8-162">ascii</span><span class="sxs-lookup"><span data-stu-id="295f8-162">ascii</span></span>       |
| <span data-ttu-id="295f8-163">2</span><span class="sxs-lookup"><span data-stu-id="295f8-163">2</span></span>     | <span data-ttu-id="295f8-164">/ifd/xmp/exif:GPSTrackRef</span><span class="sxs-lookup"><span data-stu-id="295f8-164">/ifd/xmp/exif:GPSTrackRef</span></span> | <span data-ttu-id="295f8-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="295f8-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="295f8-166">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="295f8-166">Remove Paths</span></span>



| <span data-ttu-id="295f8-167">Ordem</span><span class="sxs-lookup"><span data-stu-id="295f8-167">Order</span></span> | <span data-ttu-id="295f8-168">Caminho</span><span class="sxs-lookup"><span data-stu-id="295f8-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="295f8-169">1</span><span class="sxs-lookup"><span data-stu-id="295f8-169">1</span></span>     | <span data-ttu-id="295f8-170">/IFD/GPS/{UShort = 14}</span><span class="sxs-lookup"><span data-stu-id="295f8-170">/ifd/gps/{ushort=14}</span></span>      |
| <span data-ttu-id="295f8-171">2</span><span class="sxs-lookup"><span data-stu-id="295f8-171">2</span></span>     | <span data-ttu-id="295f8-172">/ifd/xmp/exif:gpstrackref</span><span class="sxs-lookup"><span data-stu-id="295f8-172">/ifd/xmp/exif:gpstrackref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="295f8-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="295f8-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="295f8-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="295f8-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="295f8-175">System. GPS. TrackRef</span><span class="sxs-lookup"><span data-stu-id="295f8-175">System.GPS.TrackRef</span></span>](../properties/props-system-gps-trackref.md)
</dt> </dl>

 

 
