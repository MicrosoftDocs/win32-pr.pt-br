---
description: A política de metadados de foto para a propriedade System. GPS. satélites.
ms.assetid: 5dbbbeaf-e67d-45f6-95b2-de3287202d41
title: Política de metadados de foto System. GPS. satélites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980393accdb1bee3d2a44dd539f3c9fb169c648b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759516"
---
# <a name="systemgpssatellites-photo-metadata-policy"></a><span data-ttu-id="4a323-103">Política de metadados de foto System. GPS. satélites</span><span class="sxs-lookup"><span data-stu-id="4a323-103">System.GPS.Satellites Photo Metadata Policy</span></span>

<span data-ttu-id="4a323-104">A política de metadados de foto para a propriedade [System. GPS. satélites](../properties/props-system-gps-satellites.md) .</span><span class="sxs-lookup"><span data-stu-id="4a323-104">The photo metadata policy for the [System.GPS.Satellites](../properties/props-system-gps-satellites.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4a323-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="4a323-105">PKEY</span></span>

<span data-ttu-id="4a323-106">\_Satélites de GPS PKEY \_</span><span class="sxs-lookup"><span data-stu-id="4a323-106">PKEY\_GPS\_Satellites</span></span>

### <a name="containers"></a><span data-ttu-id="4a323-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="4a323-107">Containers</span></span>

<span data-ttu-id="4a323-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="4a323-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4a323-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4a323-109">Read-Only</span></span>

<span data-ttu-id="4a323-110">No</span><span class="sxs-lookup"><span data-stu-id="4a323-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4a323-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="4a323-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4a323-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="4a323-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="4a323-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="4a323-113">Input Type</span></span>

<span data-ttu-id="4a323-114">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4a323-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4a323-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="4a323-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="4a323-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="4a323-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="4a323-117">Políticas JPEG</span><span class="sxs-lookup"><span data-stu-id="4a323-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="4a323-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="4a323-118">Read Paths</span></span>



| <span data-ttu-id="4a323-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="4a323-119">Order</span></span> | <span data-ttu-id="4a323-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="4a323-120">Path</span></span>                     | <span data-ttu-id="4a323-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4a323-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="4a323-122">1</span><span class="sxs-lookup"><span data-stu-id="4a323-122">1</span></span>     | <span data-ttu-id="4a323-123">/App1/IFD/GPS/{UShort = 8}</span><span class="sxs-lookup"><span data-stu-id="4a323-123">/app1/ifd/gps/{ushort=8}</span></span> | <span data-ttu-id="4a323-124">ascii</span><span class="sxs-lookup"><span data-stu-id="4a323-124">ascii</span></span>       |
| <span data-ttu-id="4a323-125">2</span><span class="sxs-lookup"><span data-stu-id="4a323-125">2</span></span>     | <span data-ttu-id="4a323-126">/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="4a323-126">/xmp/exif:GPSSatellites</span></span>  | <span data-ttu-id="4a323-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="4a323-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="4a323-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="4a323-128">Write Paths</span></span>



| <span data-ttu-id="4a323-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="4a323-129">Order</span></span> | <span data-ttu-id="4a323-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="4a323-130">Path</span></span>                     | <span data-ttu-id="4a323-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4a323-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="4a323-132">1</span><span class="sxs-lookup"><span data-stu-id="4a323-132">1</span></span>     | <span data-ttu-id="4a323-133">/App1/IFD/GPS/{UShort = 8}</span><span class="sxs-lookup"><span data-stu-id="4a323-133">/app1/ifd/gps/{ushort=8}</span></span> | <span data-ttu-id="4a323-134">ascii</span><span class="sxs-lookup"><span data-stu-id="4a323-134">ascii</span></span>       |
| <span data-ttu-id="4a323-135">2</span><span class="sxs-lookup"><span data-stu-id="4a323-135">2</span></span>     | <span data-ttu-id="4a323-136">/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="4a323-136">/xmp/exif:GPSSatellites</span></span>  | <span data-ttu-id="4a323-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="4a323-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="4a323-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="4a323-138">Remove Paths</span></span>



| <span data-ttu-id="4a323-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="4a323-139">Order</span></span> | <span data-ttu-id="4a323-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="4a323-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="4a323-141">1</span><span class="sxs-lookup"><span data-stu-id="4a323-141">1</span></span>     | <span data-ttu-id="4a323-142">/App1/IFD/GPS/{UShort = 8}</span><span class="sxs-lookup"><span data-stu-id="4a323-142">/app1/ifd/gps/{ushort=8}</span></span> |
| <span data-ttu-id="4a323-143">2</span><span class="sxs-lookup"><span data-stu-id="4a323-143">2</span></span>     | <span data-ttu-id="4a323-144">/xmp/exif:gpssatellites</span><span class="sxs-lookup"><span data-stu-id="4a323-144">/xmp/exif:gpssatellites</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="4a323-145">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="4a323-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="4a323-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="4a323-146">Read Paths</span></span>



| <span data-ttu-id="4a323-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="4a323-147">Order</span></span> | <span data-ttu-id="4a323-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="4a323-148">Path</span></span>                        | <span data-ttu-id="4a323-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4a323-149">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="4a323-150">1</span><span class="sxs-lookup"><span data-stu-id="4a323-150">1</span></span>     | <span data-ttu-id="4a323-151">/IFD/GPS/{UShort = 8}</span><span class="sxs-lookup"><span data-stu-id="4a323-151">/ifd/gps/{ushort=8}</span></span>         | <span data-ttu-id="4a323-152">ascii</span><span class="sxs-lookup"><span data-stu-id="4a323-152">ascii</span></span>       |
| <span data-ttu-id="4a323-153">2</span><span class="sxs-lookup"><span data-stu-id="4a323-153">2</span></span>     | <span data-ttu-id="4a323-154">/ifd/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="4a323-154">/ifd/xmp/exif:GPSSatellites</span></span> | <span data-ttu-id="4a323-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="4a323-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="4a323-156">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="4a323-156">Write Paths</span></span>



| <span data-ttu-id="4a323-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="4a323-157">Order</span></span> | <span data-ttu-id="4a323-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="4a323-158">Path</span></span>                        | <span data-ttu-id="4a323-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4a323-159">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="4a323-160">1</span><span class="sxs-lookup"><span data-stu-id="4a323-160">1</span></span>     | <span data-ttu-id="4a323-161">/IFD/GPS/{UShort = 8}</span><span class="sxs-lookup"><span data-stu-id="4a323-161">/ifd/gps/{ushort=8}</span></span>         | <span data-ttu-id="4a323-162">ascii</span><span class="sxs-lookup"><span data-stu-id="4a323-162">ascii</span></span>       |
| <span data-ttu-id="4a323-163">2</span><span class="sxs-lookup"><span data-stu-id="4a323-163">2</span></span>     | <span data-ttu-id="4a323-164">/ifd/xmp/exif:GPSSatellites</span><span class="sxs-lookup"><span data-stu-id="4a323-164">/ifd/xmp/exif:GPSSatellites</span></span> | <span data-ttu-id="4a323-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="4a323-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="4a323-166">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="4a323-166">Remove Paths</span></span>



| <span data-ttu-id="4a323-167">Ordem</span><span class="sxs-lookup"><span data-stu-id="4a323-167">Order</span></span> | <span data-ttu-id="4a323-168">Caminho</span><span class="sxs-lookup"><span data-stu-id="4a323-168">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="4a323-169">1</span><span class="sxs-lookup"><span data-stu-id="4a323-169">1</span></span>     | <span data-ttu-id="4a323-170">/IFD/GPS/{UShort = 8}</span><span class="sxs-lookup"><span data-stu-id="4a323-170">/ifd/gps/{ushort=8}</span></span>         |
| <span data-ttu-id="4a323-171">2</span><span class="sxs-lookup"><span data-stu-id="4a323-171">2</span></span>     | <span data-ttu-id="4a323-172">/ifd/xmp/exif:gpssatellites</span><span class="sxs-lookup"><span data-stu-id="4a323-172">/ifd/xmp/exif:gpssatellites</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4a323-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a323-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a323-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a323-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a323-175">System. GPS. satélites</span><span class="sxs-lookup"><span data-stu-id="4a323-175">System.GPS.Satellites</span></span>](../properties/props-system-gps-satellites.md)
</dt> </dl>

 

 
