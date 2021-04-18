---
description: A política de metadados de foto para a propriedade System. GPS. latitude.
ms.assetid: 0f8cea07-da96-4d2a-8444-6073b51e1236
title: Política de metadados de foto System. GPS. latitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5320869c1e8fd0d4b17bb17da455fc939bf44b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785094"
---
# <a name="systemgpslatitude-photo-metadata-policy"></a><span data-ttu-id="d7972-103">Política de metadados de foto System. GPS. latitude</span><span class="sxs-lookup"><span data-stu-id="d7972-103">System.GPS.Latitude Photo Metadata Policy</span></span>

<span data-ttu-id="d7972-104">A política de metadados de foto para a propriedade [System. GPS. latitude](../properties/props-system-gps-latitude.md) .</span><span class="sxs-lookup"><span data-stu-id="d7972-104">The photo metadata policy for the [System.GPS.Latitude](../properties/props-system-gps-latitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d7972-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="d7972-105">PKEY</span></span>

<span data-ttu-id="d7972-106">\_Latitude PKEY GPS \_</span><span class="sxs-lookup"><span data-stu-id="d7972-106">PKEY\_GPS\_Latitude</span></span>

### <a name="containers"></a><span data-ttu-id="d7972-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="d7972-107">Containers</span></span>

<span data-ttu-id="d7972-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d7972-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d7972-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7972-109">Read-Only</span></span>

<span data-ttu-id="d7972-110">Yes</span><span class="sxs-lookup"><span data-stu-id="d7972-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d7972-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="d7972-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d7972-112">\_R8 de \| VT de vetor VT \_</span><span class="sxs-lookup"><span data-stu-id="d7972-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d7972-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="d7972-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="d7972-114">Esse valor pode ser gravado escrevendo em System. GPS. LatitudeNumerator e System. GPS. LatitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="d7972-114">This value can be written by writing to System.GPS.LatitudeNumerator and System.GPS.LatitudeDenominator.</span></span> <span data-ttu-id="d7972-115">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="d7972-115">It cannot be written directly.</span></span> <span data-ttu-id="d7972-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="d7972-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="d7972-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="d7972-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d7972-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="d7972-118">Read Paths</span></span>



| <span data-ttu-id="d7972-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="d7972-119">Order</span></span> | <span data-ttu-id="d7972-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="d7972-120">Path</span></span>                     | <span data-ttu-id="d7972-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d7972-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="d7972-122">1</span><span class="sxs-lookup"><span data-stu-id="d7972-122">1</span></span>     | <span data-ttu-id="d7972-123">/App1/IFD/GPS/{UShort = 2}</span><span class="sxs-lookup"><span data-stu-id="d7972-123">/app1/ifd/gps/{ushort=2}</span></span> |             |
| <span data-ttu-id="d7972-124">2</span><span class="sxs-lookup"><span data-stu-id="d7972-124">2</span></span>     | <span data-ttu-id="d7972-125">/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="d7972-125">/xmp/exif:GPSLatitude</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="d7972-126">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="d7972-126">Write Paths</span></span>



| <span data-ttu-id="d7972-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="d7972-127">Order</span></span> | <span data-ttu-id="d7972-128">Caminho</span><span class="sxs-lookup"><span data-stu-id="d7972-128">Path</span></span>                     | <span data-ttu-id="d7972-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d7972-129">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="d7972-130">1</span><span class="sxs-lookup"><span data-stu-id="d7972-130">1</span></span>     | <span data-ttu-id="d7972-131">/App1/IFD/GPS/{UShort = 2}</span><span class="sxs-lookup"><span data-stu-id="d7972-131">/app1/ifd/gps/{ushort=2}</span></span> |             |
| <span data-ttu-id="d7972-132">2</span><span class="sxs-lookup"><span data-stu-id="d7972-132">2</span></span>     | <span data-ttu-id="d7972-133">/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="d7972-133">/xmp/exif:GPSLatitude</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="d7972-134">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="d7972-134">Remove Paths</span></span>



| <span data-ttu-id="d7972-135">Ordem</span><span class="sxs-lookup"><span data-stu-id="d7972-135">Order</span></span> | <span data-ttu-id="d7972-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="d7972-136">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="d7972-137">1</span><span class="sxs-lookup"><span data-stu-id="d7972-137">1</span></span>     | <span data-ttu-id="d7972-138">/App1/IFD/GPS/{UShort = 2}</span><span class="sxs-lookup"><span data-stu-id="d7972-138">/app1/ifd/gps/{ushort=2}</span></span> |
| <span data-ttu-id="d7972-139">2</span><span class="sxs-lookup"><span data-stu-id="d7972-139">2</span></span>     | <span data-ttu-id="d7972-140">/xmp/exif:gpslatitude</span><span class="sxs-lookup"><span data-stu-id="d7972-140">/xmp/exif:gpslatitude</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="d7972-141">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="d7972-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="d7972-142">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="d7972-142">Read Paths</span></span>



| <span data-ttu-id="d7972-143">Ordem</span><span class="sxs-lookup"><span data-stu-id="d7972-143">Order</span></span> | <span data-ttu-id="d7972-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="d7972-144">Path</span></span>                      | <span data-ttu-id="d7972-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d7972-145">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="d7972-146">1</span><span class="sxs-lookup"><span data-stu-id="d7972-146">1</span></span>     | <span data-ttu-id="d7972-147">/IFD/GPS/{UShort = 2}</span><span class="sxs-lookup"><span data-stu-id="d7972-147">/ifd/gps/{ushort=2}</span></span>       |             |
| <span data-ttu-id="d7972-148">2</span><span class="sxs-lookup"><span data-stu-id="d7972-148">2</span></span>     | <span data-ttu-id="d7972-149">/ifd/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="d7972-149">/ifd/xmp/exif:GPSLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="d7972-150">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="d7972-150">Write Paths</span></span>



| <span data-ttu-id="d7972-151">Ordem</span><span class="sxs-lookup"><span data-stu-id="d7972-151">Order</span></span> | <span data-ttu-id="d7972-152">Caminho</span><span class="sxs-lookup"><span data-stu-id="d7972-152">Path</span></span>                      | <span data-ttu-id="d7972-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d7972-153">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="d7972-154">1</span><span class="sxs-lookup"><span data-stu-id="d7972-154">1</span></span>     | <span data-ttu-id="d7972-155">/IFD/GPS/{UShort = 2}</span><span class="sxs-lookup"><span data-stu-id="d7972-155">/ifd/gps/{ushort=2}</span></span>       |             |
| <span data-ttu-id="d7972-156">2</span><span class="sxs-lookup"><span data-stu-id="d7972-156">2</span></span>     | <span data-ttu-id="d7972-157">/ifd/xmp/exif:GPSLatitude</span><span class="sxs-lookup"><span data-stu-id="d7972-157">/ifd/xmp/exif:GPSLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="d7972-158">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="d7972-158">Remove Paths</span></span>



| <span data-ttu-id="d7972-159">Ordem</span><span class="sxs-lookup"><span data-stu-id="d7972-159">Order</span></span> | <span data-ttu-id="d7972-160">Caminho</span><span class="sxs-lookup"><span data-stu-id="d7972-160">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="d7972-161">1</span><span class="sxs-lookup"><span data-stu-id="d7972-161">1</span></span>     | <span data-ttu-id="d7972-162">/IFD/GPS/{UShort = 2}</span><span class="sxs-lookup"><span data-stu-id="d7972-162">/ifd/gps/{ushort=2}</span></span>       |
| <span data-ttu-id="d7972-163">2</span><span class="sxs-lookup"><span data-stu-id="d7972-163">2</span></span>     | <span data-ttu-id="d7972-164">/ifd/xmp/exif:gpslatitude</span><span class="sxs-lookup"><span data-stu-id="d7972-164">/ifd/xmp/exif:gpslatitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d7972-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7972-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7972-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7972-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7972-167">System. GPS. latitude</span><span class="sxs-lookup"><span data-stu-id="d7972-167">System.GPS.Latitude</span></span>](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
