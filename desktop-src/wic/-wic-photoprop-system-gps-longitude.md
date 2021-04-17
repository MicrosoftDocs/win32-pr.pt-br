---
description: A política de metadados de foto para a propriedade System. GPS. longitude.
ms.assetid: 36539e20-d00c-4bbb-b9ee-1cf5e4b8df4b
title: Política de metadados de foto System. GPS. longitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25eb9869bc536f97adfc8f3c0f5b1f70c8bf030f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789659"
---
# <a name="systemgpslongitude-photo-metadata-policy"></a><span data-ttu-id="b18c5-103">Política de metadados de foto System. GPS. longitude</span><span class="sxs-lookup"><span data-stu-id="b18c5-103">System.GPS.Longitude Photo Metadata Policy</span></span>

<span data-ttu-id="b18c5-104">A política de metadados de foto para a propriedade [System. GPS. longitude](../properties/props-system-gps-longitude.md) .</span><span class="sxs-lookup"><span data-stu-id="b18c5-104">The photo metadata policy for the [System.GPS.Longitude](../properties/props-system-gps-longitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b18c5-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="b18c5-105">PKEY</span></span>

<span data-ttu-id="b18c5-106">\_Longitude de GPS PKEY \_</span><span class="sxs-lookup"><span data-stu-id="b18c5-106">PKEY\_GPS\_Longitude</span></span>

### <a name="containers"></a><span data-ttu-id="b18c5-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="b18c5-107">Containers</span></span>

<span data-ttu-id="b18c5-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b18c5-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b18c5-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b18c5-109">Read-Only</span></span>

<span data-ttu-id="b18c5-110">Yes</span><span class="sxs-lookup"><span data-stu-id="b18c5-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b18c5-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="b18c5-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b18c5-112">\_R8 de \| VT de vetor VT \_</span><span class="sxs-lookup"><span data-stu-id="b18c5-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b18c5-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="b18c5-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="b18c5-114">Esse valor pode ser gravado escrevendo em System. GPS. LongitudeNumerator e System. GPS. LongitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="b18c5-114">This value can be written by writing to System.GPS.LongitudeNumerator and System.GPS.LongitudeDenominator.</span></span> <span data-ttu-id="b18c5-115">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="b18c5-115">It cannot be written directly.</span></span> <span data-ttu-id="b18c5-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="b18c5-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b18c5-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="b18c5-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b18c5-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="b18c5-118">Read Paths</span></span>



| <span data-ttu-id="b18c5-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="b18c5-119">Order</span></span> | <span data-ttu-id="b18c5-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="b18c5-120">Path</span></span>                     | <span data-ttu-id="b18c5-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b18c5-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="b18c5-122">1</span><span class="sxs-lookup"><span data-stu-id="b18c5-122">1</span></span>     | <span data-ttu-id="b18c5-123">/App1/IFD/GPS/{UShort = 4}</span><span class="sxs-lookup"><span data-stu-id="b18c5-123">/app1/ifd/gps/{ushort=4}</span></span> |             |
| <span data-ttu-id="b18c5-124">2</span><span class="sxs-lookup"><span data-stu-id="b18c5-124">2</span></span>     | <span data-ttu-id="b18c5-125">/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="b18c5-125">/xmp/exif:GPSLongitude</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="b18c5-126">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="b18c5-126">Write Paths</span></span>



| <span data-ttu-id="b18c5-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="b18c5-127">Order</span></span> | <span data-ttu-id="b18c5-128">Caminho</span><span class="sxs-lookup"><span data-stu-id="b18c5-128">Path</span></span>                     | <span data-ttu-id="b18c5-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b18c5-129">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="b18c5-130">1</span><span class="sxs-lookup"><span data-stu-id="b18c5-130">1</span></span>     | <span data-ttu-id="b18c5-131">/App1/IFD/GPS/{UShort = 4}</span><span class="sxs-lookup"><span data-stu-id="b18c5-131">/app1/ifd/gps/{ushort=4}</span></span> |             |
| <span data-ttu-id="b18c5-132">2</span><span class="sxs-lookup"><span data-stu-id="b18c5-132">2</span></span>     | <span data-ttu-id="b18c5-133">/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="b18c5-133">/xmp/exif:GPSLongitude</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b18c5-134">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="b18c5-134">Remove Paths</span></span>



| <span data-ttu-id="b18c5-135">Ordem</span><span class="sxs-lookup"><span data-stu-id="b18c5-135">Order</span></span> | <span data-ttu-id="b18c5-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="b18c5-136">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="b18c5-137">1</span><span class="sxs-lookup"><span data-stu-id="b18c5-137">1</span></span>     | <span data-ttu-id="b18c5-138">/App1/IFD/GPS/{UShort = 4}</span><span class="sxs-lookup"><span data-stu-id="b18c5-138">/app1/ifd/gps/{ushort=4}</span></span> |
| <span data-ttu-id="b18c5-139">2</span><span class="sxs-lookup"><span data-stu-id="b18c5-139">2</span></span>     | <span data-ttu-id="b18c5-140">/xmp/exif:gpslongitude</span><span class="sxs-lookup"><span data-stu-id="b18c5-140">/xmp/exif:gpslongitude</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="b18c5-141">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="b18c5-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b18c5-142">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="b18c5-142">Read Paths</span></span>



| <span data-ttu-id="b18c5-143">Ordem</span><span class="sxs-lookup"><span data-stu-id="b18c5-143">Order</span></span> | <span data-ttu-id="b18c5-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="b18c5-144">Path</span></span>                       | <span data-ttu-id="b18c5-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b18c5-145">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="b18c5-146">1</span><span class="sxs-lookup"><span data-stu-id="b18c5-146">1</span></span>     | <span data-ttu-id="b18c5-147">/IFD/GPS/{UShort = 4}</span><span class="sxs-lookup"><span data-stu-id="b18c5-147">/ifd/gps/{ushort=4}</span></span>        |             |
| <span data-ttu-id="b18c5-148">2</span><span class="sxs-lookup"><span data-stu-id="b18c5-148">2</span></span>     | <span data-ttu-id="b18c5-149">/ifd/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="b18c5-149">/ifd/xmp/exif:GPSLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="b18c5-150">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="b18c5-150">Write Paths</span></span>



| <span data-ttu-id="b18c5-151">Ordem</span><span class="sxs-lookup"><span data-stu-id="b18c5-151">Order</span></span> | <span data-ttu-id="b18c5-152">Caminho</span><span class="sxs-lookup"><span data-stu-id="b18c5-152">Path</span></span>                       | <span data-ttu-id="b18c5-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b18c5-153">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="b18c5-154">1</span><span class="sxs-lookup"><span data-stu-id="b18c5-154">1</span></span>     | <span data-ttu-id="b18c5-155">/IFD/GPS/{UShort = 4}</span><span class="sxs-lookup"><span data-stu-id="b18c5-155">/ifd/gps/{ushort=4}</span></span>        |             |
| <span data-ttu-id="b18c5-156">2</span><span class="sxs-lookup"><span data-stu-id="b18c5-156">2</span></span>     | <span data-ttu-id="b18c5-157">/ifd/xmp/exif:GPSLongitude</span><span class="sxs-lookup"><span data-stu-id="b18c5-157">/ifd/xmp/exif:GPSLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b18c5-158">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="b18c5-158">Remove Paths</span></span>



| <span data-ttu-id="b18c5-159">Ordem</span><span class="sxs-lookup"><span data-stu-id="b18c5-159">Order</span></span> | <span data-ttu-id="b18c5-160">Caminho</span><span class="sxs-lookup"><span data-stu-id="b18c5-160">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="b18c5-161">1</span><span class="sxs-lookup"><span data-stu-id="b18c5-161">1</span></span>     | <span data-ttu-id="b18c5-162">/IFD/GPS/{UShort = 4}</span><span class="sxs-lookup"><span data-stu-id="b18c5-162">/ifd/gps/{ushort=4}</span></span>        |
| <span data-ttu-id="b18c5-163">2</span><span class="sxs-lookup"><span data-stu-id="b18c5-163">2</span></span>     | <span data-ttu-id="b18c5-164">/ifd/xmp/exif:gpslongitude</span><span class="sxs-lookup"><span data-stu-id="b18c5-164">/ifd/xmp/exif:gpslongitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b18c5-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="b18c5-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b18c5-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b18c5-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b18c5-167">System. GPS. longitude</span><span class="sxs-lookup"><span data-stu-id="b18c5-167">System.GPS.Longitude</span></span>](../properties/props-system-gps-longitude.md)
</dt> </dl>

 

 
