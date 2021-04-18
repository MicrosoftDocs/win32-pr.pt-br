---
description: A política de metadados de foto para a propriedade System. GPS. ImgDirection.
ms.assetid: c9a0f5de-4010-4251-a5d5-8728b7ae6d33
title: Política de metadados de foto System. GPS. ImgDirection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013edd632f98f1359c4f3c04856b0409c70eaa56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771341"
---
# <a name="systemgpsimgdirection-photo-metadata-policy"></a><span data-ttu-id="c8efb-103">Política de metadados de foto System. GPS. ImgDirection</span><span class="sxs-lookup"><span data-stu-id="c8efb-103">System.GPS.ImgDirection Photo Metadata Policy</span></span>

<span data-ttu-id="c8efb-104">A política de metadados de foto para a propriedade [System. GPS. ImgDirection](../properties/props-system-gps-imgdirection.md) .</span><span class="sxs-lookup"><span data-stu-id="c8efb-104">The photo metadata policy for the [System.GPS.ImgDirection](../properties/props-system-gps-imgdirection.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c8efb-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="c8efb-105">PKEY</span></span>

<span data-ttu-id="c8efb-106">PKEY \_ GPS \_ ImgDirection</span><span class="sxs-lookup"><span data-stu-id="c8efb-106">PKEY\_GPS\_ImgDirection</span></span>

### <a name="containers"></a><span data-ttu-id="c8efb-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="c8efb-107">Containers</span></span>

<span data-ttu-id="c8efb-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c8efb-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c8efb-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8efb-109">Read-Only</span></span>

<span data-ttu-id="c8efb-110">Yes</span><span class="sxs-lookup"><span data-stu-id="c8efb-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c8efb-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="c8efb-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c8efb-112">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="c8efb-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c8efb-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="c8efb-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="c8efb-114">Esse valor pode ser gravado escrevendo em System. GPS. ImgDirectionNumerator e System. GPS. ImgDirectionDenominator.</span><span class="sxs-lookup"><span data-stu-id="c8efb-114">This value can be written by writing to System.GPS.ImgDirectionNumerator and System.GPS.ImgDirectionDenominator.</span></span> <span data-ttu-id="c8efb-115">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="c8efb-115">It cannot be written directly.</span></span> <span data-ttu-id="c8efb-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="c8efb-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="c8efb-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="c8efb-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="c8efb-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="c8efb-118">Read Paths</span></span>



| <span data-ttu-id="c8efb-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="c8efb-119">Order</span></span> | <span data-ttu-id="c8efb-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="c8efb-120">Path</span></span>                      | <span data-ttu-id="c8efb-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="c8efb-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="c8efb-122">1</span><span class="sxs-lookup"><span data-stu-id="c8efb-122">1</span></span>     | <span data-ttu-id="c8efb-123">/App1/IFD/GPS/{UShort = 17}</span><span class="sxs-lookup"><span data-stu-id="c8efb-123">/app1/ifd/gps/{ushort=17}</span></span> |             |
| <span data-ttu-id="c8efb-124">2</span><span class="sxs-lookup"><span data-stu-id="c8efb-124">2</span></span>     | <span data-ttu-id="c8efb-125">/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="c8efb-125">/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="c8efb-126">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="c8efb-126">Write Paths</span></span>



| <span data-ttu-id="c8efb-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="c8efb-127">Order</span></span> | <span data-ttu-id="c8efb-128">Caminho</span><span class="sxs-lookup"><span data-stu-id="c8efb-128">Path</span></span>                      | <span data-ttu-id="c8efb-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="c8efb-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="c8efb-130">1</span><span class="sxs-lookup"><span data-stu-id="c8efb-130">1</span></span>     | <span data-ttu-id="c8efb-131">/App1/IFD/GPS/{UShort = 17}</span><span class="sxs-lookup"><span data-stu-id="c8efb-131">/app1/ifd/gps/{ushort=17}</span></span> |             |
| <span data-ttu-id="c8efb-132">2</span><span class="sxs-lookup"><span data-stu-id="c8efb-132">2</span></span>     | <span data-ttu-id="c8efb-133">/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="c8efb-133">/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="c8efb-134">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="c8efb-134">Remove Paths</span></span>



| <span data-ttu-id="c8efb-135">Ordem</span><span class="sxs-lookup"><span data-stu-id="c8efb-135">Order</span></span> | <span data-ttu-id="c8efb-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="c8efb-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="c8efb-137">1</span><span class="sxs-lookup"><span data-stu-id="c8efb-137">1</span></span>     | <span data-ttu-id="c8efb-138">/App1/IFD/GPS/{UShort = 17}</span><span class="sxs-lookup"><span data-stu-id="c8efb-138">/app1/ifd/gps/{ushort=17}</span></span> |
| <span data-ttu-id="c8efb-139">2</span><span class="sxs-lookup"><span data-stu-id="c8efb-139">2</span></span>     | <span data-ttu-id="c8efb-140">/xmp/exif:gpsimgdirection</span><span class="sxs-lookup"><span data-stu-id="c8efb-140">/xmp/exif:gpsimgdirection</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="c8efb-141">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="c8efb-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c8efb-142">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="c8efb-142">Read Paths</span></span>



| <span data-ttu-id="c8efb-143">Ordem</span><span class="sxs-lookup"><span data-stu-id="c8efb-143">Order</span></span> | <span data-ttu-id="c8efb-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="c8efb-144">Path</span></span>                          | <span data-ttu-id="c8efb-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="c8efb-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="c8efb-146">1</span><span class="sxs-lookup"><span data-stu-id="c8efb-146">1</span></span>     | <span data-ttu-id="c8efb-147">/IFD/GPS/{UShort = 17}</span><span class="sxs-lookup"><span data-stu-id="c8efb-147">/ifd/gps/{ushort=17}</span></span>          |             |
| <span data-ttu-id="c8efb-148">2</span><span class="sxs-lookup"><span data-stu-id="c8efb-148">2</span></span>     | <span data-ttu-id="c8efb-149">/ifd/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="c8efb-149">/ifd/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="c8efb-150">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="c8efb-150">Write Paths</span></span>



| <span data-ttu-id="c8efb-151">Ordem</span><span class="sxs-lookup"><span data-stu-id="c8efb-151">Order</span></span> | <span data-ttu-id="c8efb-152">Caminho</span><span class="sxs-lookup"><span data-stu-id="c8efb-152">Path</span></span>                          | <span data-ttu-id="c8efb-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="c8efb-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="c8efb-154">1</span><span class="sxs-lookup"><span data-stu-id="c8efb-154">1</span></span>     | <span data-ttu-id="c8efb-155">/IFD/GPS/{UShort = 17}</span><span class="sxs-lookup"><span data-stu-id="c8efb-155">/ifd/gps/{ushort=17}</span></span>          |             |
| <span data-ttu-id="c8efb-156">2</span><span class="sxs-lookup"><span data-stu-id="c8efb-156">2</span></span>     | <span data-ttu-id="c8efb-157">/ifd/xmp/exif:GPSImgDirection</span><span class="sxs-lookup"><span data-stu-id="c8efb-157">/ifd/xmp/exif:GPSImgDirection</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="c8efb-158">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="c8efb-158">Remove Paths</span></span>



| <span data-ttu-id="c8efb-159">Ordem</span><span class="sxs-lookup"><span data-stu-id="c8efb-159">Order</span></span> | <span data-ttu-id="c8efb-160">Caminho</span><span class="sxs-lookup"><span data-stu-id="c8efb-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="c8efb-161">1</span><span class="sxs-lookup"><span data-stu-id="c8efb-161">1</span></span>     | <span data-ttu-id="c8efb-162">/IFD/GPS/{UShort = 17}</span><span class="sxs-lookup"><span data-stu-id="c8efb-162">/ifd/gps/{ushort=17}</span></span>          |
| <span data-ttu-id="c8efb-163">2</span><span class="sxs-lookup"><span data-stu-id="c8efb-163">2</span></span>     | <span data-ttu-id="c8efb-164">/ifd/xmp/exif:gpsimgdirection</span><span class="sxs-lookup"><span data-stu-id="c8efb-164">/ifd/xmp/exif:gpsimgdirection</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c8efb-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8efb-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8efb-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c8efb-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8efb-167">System. GPS. ImgDirection</span><span class="sxs-lookup"><span data-stu-id="c8efb-167">System.GPS.ImgDirection</span></span>](../properties/props-system-gps-imgdirection.md)
</dt> </dl>

 

 
