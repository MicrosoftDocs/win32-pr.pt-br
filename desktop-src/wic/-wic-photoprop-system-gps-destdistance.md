---
description: A política de metadados de foto para a propriedade System. GPS. DestDistance.
ms.assetid: 1bd72acb-f462-454d-aec2-72d5b4517de3
title: Política de metadados de foto System. GPS. DestDistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc71c89ae6270f5babf08637f54baaf2cb57aae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760415"
---
# <a name="systemgpsdestdistance-photo-metadata-policy"></a><span data-ttu-id="db33a-103">Política de metadados de foto System. GPS. DestDistance</span><span class="sxs-lookup"><span data-stu-id="db33a-103">System.GPS.DestDistance Photo Metadata Policy</span></span>

<span data-ttu-id="db33a-104">A política de metadados de foto para a propriedade [System. GPS. DestDistance](../properties/props-system-gps-destdistance.md) .</span><span class="sxs-lookup"><span data-stu-id="db33a-104">The photo metadata policy for the [System.GPS.DestDistance](../properties/props-system-gps-destdistance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="db33a-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="db33a-105">PKEY</span></span>

<span data-ttu-id="db33a-106">PKEY \_ GPS \_ DestDistance</span><span class="sxs-lookup"><span data-stu-id="db33a-106">PKEY\_GPS\_DestDistance</span></span>

### <a name="containers"></a><span data-ttu-id="db33a-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="db33a-107">Containers</span></span>

<span data-ttu-id="db33a-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="db33a-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="db33a-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="db33a-109">Read-Only</span></span>

<span data-ttu-id="db33a-110">Yes</span><span class="sxs-lookup"><span data-stu-id="db33a-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="db33a-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="db33a-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="db33a-112">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="db33a-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="db33a-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="db33a-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="db33a-114">Esse valor é gerado de System. GPS. DestDistanceNumerator e System. GPS. DestDistanceDenominator.</span><span class="sxs-lookup"><span data-stu-id="db33a-114">This value is generated from System.GPS.DestDistanceNumerator and System.GPS.DestDistanceDenominator.</span></span> <span data-ttu-id="db33a-115">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="db33a-115">It cannot be written directly.</span></span> <span data-ttu-id="db33a-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="db33a-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="db33a-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="db33a-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="db33a-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="db33a-118">Read Paths</span></span>



| <span data-ttu-id="db33a-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="db33a-119">Order</span></span> | <span data-ttu-id="db33a-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="db33a-120">Path</span></span>                      | <span data-ttu-id="db33a-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="db33a-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="db33a-122">1</span><span class="sxs-lookup"><span data-stu-id="db33a-122">1</span></span>     | <span data-ttu-id="db33a-123">/App1/IFD/GPS/{UShort = 26}</span><span class="sxs-lookup"><span data-stu-id="db33a-123">/app1/ifd/gps/{ushort=26}</span></span> |             |
| <span data-ttu-id="db33a-124">2</span><span class="sxs-lookup"><span data-stu-id="db33a-124">2</span></span>     | <span data-ttu-id="db33a-125">/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="db33a-125">/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="db33a-126">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="db33a-126">Write Paths</span></span>



| <span data-ttu-id="db33a-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="db33a-127">Order</span></span> | <span data-ttu-id="db33a-128">Caminho</span><span class="sxs-lookup"><span data-stu-id="db33a-128">Path</span></span>                      | <span data-ttu-id="db33a-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="db33a-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="db33a-130">1</span><span class="sxs-lookup"><span data-stu-id="db33a-130">1</span></span>     | <span data-ttu-id="db33a-131">/App1/IFD/GPS/{UShort = 26}</span><span class="sxs-lookup"><span data-stu-id="db33a-131">/app1/ifd/gps/{ushort=26}</span></span> |             |
| <span data-ttu-id="db33a-132">2</span><span class="sxs-lookup"><span data-stu-id="db33a-132">2</span></span>     | <span data-ttu-id="db33a-133">/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="db33a-133">/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="db33a-134">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="db33a-134">Remove Paths</span></span>



| <span data-ttu-id="db33a-135">Ordem</span><span class="sxs-lookup"><span data-stu-id="db33a-135">Order</span></span> | <span data-ttu-id="db33a-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="db33a-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="db33a-137">1</span><span class="sxs-lookup"><span data-stu-id="db33a-137">1</span></span>     | <span data-ttu-id="db33a-138">/App1/IFD/GPS/{UShort = 26}</span><span class="sxs-lookup"><span data-stu-id="db33a-138">/app1/ifd/gps/{ushort=26}</span></span> |
| <span data-ttu-id="db33a-139">2</span><span class="sxs-lookup"><span data-stu-id="db33a-139">2</span></span>     | <span data-ttu-id="db33a-140">/xmp/exif:gpsdestdistance</span><span class="sxs-lookup"><span data-stu-id="db33a-140">/xmp/exif:gpsdestdistance</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="db33a-141">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="db33a-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="db33a-142">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="db33a-142">Read Paths</span></span>



| <span data-ttu-id="db33a-143">Ordem</span><span class="sxs-lookup"><span data-stu-id="db33a-143">Order</span></span> | <span data-ttu-id="db33a-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="db33a-144">Path</span></span>                          | <span data-ttu-id="db33a-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="db33a-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="db33a-146">1</span><span class="sxs-lookup"><span data-stu-id="db33a-146">1</span></span>     | <span data-ttu-id="db33a-147">/IFD/GPS/{UShort = 26}</span><span class="sxs-lookup"><span data-stu-id="db33a-147">/ifd/gps/{ushort=26}</span></span>          |             |
| <span data-ttu-id="db33a-148">2</span><span class="sxs-lookup"><span data-stu-id="db33a-148">2</span></span>     | <span data-ttu-id="db33a-149">/ifd/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="db33a-149">/ifd/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="db33a-150">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="db33a-150">Write Paths</span></span>



| <span data-ttu-id="db33a-151">Ordem</span><span class="sxs-lookup"><span data-stu-id="db33a-151">Order</span></span> | <span data-ttu-id="db33a-152">Caminho</span><span class="sxs-lookup"><span data-stu-id="db33a-152">Path</span></span>                          | <span data-ttu-id="db33a-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="db33a-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="db33a-154">1</span><span class="sxs-lookup"><span data-stu-id="db33a-154">1</span></span>     | <span data-ttu-id="db33a-155">/IFD/GPS/{UShort = 26}</span><span class="sxs-lookup"><span data-stu-id="db33a-155">/ifd/gps/{ushort=26}</span></span>          |             |
| <span data-ttu-id="db33a-156">2</span><span class="sxs-lookup"><span data-stu-id="db33a-156">2</span></span>     | <span data-ttu-id="db33a-157">/ifd/xmp/exif:GPSDestDistance</span><span class="sxs-lookup"><span data-stu-id="db33a-157">/ifd/xmp/exif:GPSDestDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="db33a-158">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="db33a-158">Remove Paths</span></span>



| <span data-ttu-id="db33a-159">Ordem</span><span class="sxs-lookup"><span data-stu-id="db33a-159">Order</span></span> | <span data-ttu-id="db33a-160">Caminho</span><span class="sxs-lookup"><span data-stu-id="db33a-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="db33a-161">1</span><span class="sxs-lookup"><span data-stu-id="db33a-161">1</span></span>     | <span data-ttu-id="db33a-162">/IFD/GPS/{UShort = 26}</span><span class="sxs-lookup"><span data-stu-id="db33a-162">/ifd/gps/{ushort=26}</span></span>          |
| <span data-ttu-id="db33a-163">2</span><span class="sxs-lookup"><span data-stu-id="db33a-163">2</span></span>     | <span data-ttu-id="db33a-164">/ifd/xmp/exif:gpsdestdistance</span><span class="sxs-lookup"><span data-stu-id="db33a-164">/ifd/xmp/exif:gpsdestdistance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="db33a-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="db33a-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="db33a-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="db33a-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db33a-167">System. GPS. DestDistance</span><span class="sxs-lookup"><span data-stu-id="db33a-167">System.GPS.DestDistance</span></span>](../properties/props-system-gps-destdistance.md)
</dt> </dl>

 

 
