---
description: A política de metadados de foto para a propriedade System. GPS. DestBearing.
ms.assetid: ccc31b3d-27fd-4a8c-a304-852cf6114ec5
title: Política de metadados de foto System. GPS. DestBearing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a084a0633579afe646403fb4dcad0ca8a1b9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297366"
---
# <a name="systemgpsdestbearing-photo-metadata-policy"></a><span data-ttu-id="92b44-103">Política de metadados de foto System. GPS. DestBearing</span><span class="sxs-lookup"><span data-stu-id="92b44-103">System.GPS.DestBearing Photo Metadata Policy</span></span>

<span data-ttu-id="92b44-104">A política de metadados de foto para a propriedade [System. GPS. DestBearing](../properties/props-system-gps-destbearing.md) .</span><span class="sxs-lookup"><span data-stu-id="92b44-104">The photo metadata policy for the [System.GPS.DestBearing](../properties/props-system-gps-destbearing.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="92b44-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="92b44-105">PKEY</span></span>

<span data-ttu-id="92b44-106">PKEY \_ GPS \_ DestBearing</span><span class="sxs-lookup"><span data-stu-id="92b44-106">PKEY\_GPS\_DestBearing</span></span>

### <a name="containers"></a><span data-ttu-id="92b44-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="92b44-107">Containers</span></span>

<span data-ttu-id="92b44-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="92b44-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="92b44-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="92b44-109">Read-Only</span></span>

<span data-ttu-id="92b44-110">Yes</span><span class="sxs-lookup"><span data-stu-id="92b44-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="92b44-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="92b44-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="92b44-112">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="92b44-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="92b44-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="92b44-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="92b44-114">Esse valor pode ser gravado escrevendo em System. GPS. DestBearingNumerator e System. GPS. DestBearingDenominator.</span><span class="sxs-lookup"><span data-stu-id="92b44-114">This value can be written by writing to System.GPS.DestBearingNumerator and System.GPS.DestBearingDenominator.</span></span> <span data-ttu-id="92b44-115">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="92b44-115">It cannot be written directly.</span></span> <span data-ttu-id="92b44-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="92b44-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="92b44-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="92b44-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="92b44-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="92b44-118">Read Paths</span></span>



| <span data-ttu-id="92b44-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="92b44-119">Order</span></span> | <span data-ttu-id="92b44-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="92b44-120">Path</span></span>                      | <span data-ttu-id="92b44-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="92b44-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="92b44-122">1</span><span class="sxs-lookup"><span data-stu-id="92b44-122">1</span></span>     | <span data-ttu-id="92b44-123">/App1/IFD/GPS/{UShort = 24}</span><span class="sxs-lookup"><span data-stu-id="92b44-123">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="92b44-124">2</span><span class="sxs-lookup"><span data-stu-id="92b44-124">2</span></span>     | <span data-ttu-id="92b44-125">/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="92b44-125">/xmp/exif:GPSDestBearing</span></span>  |             |



 

### <a name="write-paths"></a><span data-ttu-id="92b44-126">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="92b44-126">Write Paths</span></span>



| <span data-ttu-id="92b44-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="92b44-127">Order</span></span> | <span data-ttu-id="92b44-128">Caminho</span><span class="sxs-lookup"><span data-stu-id="92b44-128">Path</span></span>                      | <span data-ttu-id="92b44-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="92b44-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="92b44-130">1</span><span class="sxs-lookup"><span data-stu-id="92b44-130">1</span></span>     | <span data-ttu-id="92b44-131">/App1/IFD/GPS/{UShort = 24}</span><span class="sxs-lookup"><span data-stu-id="92b44-131">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="92b44-132">2</span><span class="sxs-lookup"><span data-stu-id="92b44-132">2</span></span>     | <span data-ttu-id="92b44-133">/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="92b44-133">/xmp/exif:GPSDestBearing</span></span>  |             |



 

### <a name="remove-paths"></a><span data-ttu-id="92b44-134">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="92b44-134">Remove Paths</span></span>



| <span data-ttu-id="92b44-135">Ordem</span><span class="sxs-lookup"><span data-stu-id="92b44-135">Order</span></span> | <span data-ttu-id="92b44-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="92b44-136">Path</span></span>                      | <span data-ttu-id="92b44-137">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="92b44-137">Disk format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="92b44-138">1</span><span class="sxs-lookup"><span data-stu-id="92b44-138">1</span></span>     | <span data-ttu-id="92b44-139">/App1/IFD/GPS/{UShort = 24}</span><span class="sxs-lookup"><span data-stu-id="92b44-139">/app1/ifd/gps/{ushort=24}</span></span> |             |
| <span data-ttu-id="92b44-140">2</span><span class="sxs-lookup"><span data-stu-id="92b44-140">2</span></span>     | <span data-ttu-id="92b44-141">/xmp/exif:gpsdestbearing</span><span class="sxs-lookup"><span data-stu-id="92b44-141">/xmp/exif:gpsdestbearing</span></span>  |             |



 

### <a name="tiff-policies"></a><span data-ttu-id="92b44-142">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="92b44-142">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="92b44-143">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="92b44-143">Read Paths</span></span>



| <span data-ttu-id="92b44-144">Ordem</span><span class="sxs-lookup"><span data-stu-id="92b44-144">Order</span></span> | <span data-ttu-id="92b44-145">Caminho</span><span class="sxs-lookup"><span data-stu-id="92b44-145">Path</span></span>                         | <span data-ttu-id="92b44-146">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="92b44-146">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="92b44-147">1</span><span class="sxs-lookup"><span data-stu-id="92b44-147">1</span></span>     | <span data-ttu-id="92b44-148">/IFD/GPS/{UShort = 24}</span><span class="sxs-lookup"><span data-stu-id="92b44-148">/ifd/gps/{ushort=24}</span></span>         |             |
| <span data-ttu-id="92b44-149">2</span><span class="sxs-lookup"><span data-stu-id="92b44-149">2</span></span>     | <span data-ttu-id="92b44-150">/ifd/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="92b44-150">/ifd/xmp/exif:GPSDestBearing</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="92b44-151">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="92b44-151">Write Paths</span></span>



| <span data-ttu-id="92b44-152">Ordem</span><span class="sxs-lookup"><span data-stu-id="92b44-152">Order</span></span> | <span data-ttu-id="92b44-153">Caminho</span><span class="sxs-lookup"><span data-stu-id="92b44-153">Path</span></span>                         | <span data-ttu-id="92b44-154">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="92b44-154">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="92b44-155">1</span><span class="sxs-lookup"><span data-stu-id="92b44-155">1</span></span>     | <span data-ttu-id="92b44-156">/IFD/GPS/{UShort = 24}</span><span class="sxs-lookup"><span data-stu-id="92b44-156">/ifd/gps/{ushort=24}</span></span>         |             |
| <span data-ttu-id="92b44-157">2</span><span class="sxs-lookup"><span data-stu-id="92b44-157">2</span></span>     | <span data-ttu-id="92b44-158">/ifd/xmp/exif:GPSDestBearing</span><span class="sxs-lookup"><span data-stu-id="92b44-158">/ifd/xmp/exif:GPSDestBearing</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="92b44-159">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="92b44-159">Remove Paths</span></span>



| <span data-ttu-id="92b44-160">Ordem</span><span class="sxs-lookup"><span data-stu-id="92b44-160">Order</span></span> | <span data-ttu-id="92b44-161">Caminho</span><span class="sxs-lookup"><span data-stu-id="92b44-161">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="92b44-162">1</span><span class="sxs-lookup"><span data-stu-id="92b44-162">1</span></span>     | <span data-ttu-id="92b44-163">/IFD/GPS/{UShort = 24}</span><span class="sxs-lookup"><span data-stu-id="92b44-163">/ifd/gps/{ushort=24}</span></span>         |
| <span data-ttu-id="92b44-164">2</span><span class="sxs-lookup"><span data-stu-id="92b44-164">2</span></span>     | <span data-ttu-id="92b44-165">/ifd/xmp/exif:gpsdestbearing</span><span class="sxs-lookup"><span data-stu-id="92b44-165">/ifd/xmp/exif:gpsdestbearing</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="92b44-166">Comentários</span><span class="sxs-lookup"><span data-stu-id="92b44-166">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="92b44-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="92b44-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92b44-168">System. GPS. DestBearing</span><span class="sxs-lookup"><span data-stu-id="92b44-168">System.GPS.DestBearing</span></span>](../properties/props-system-gps-destbearing.md)
</dt> </dl>

 

 
