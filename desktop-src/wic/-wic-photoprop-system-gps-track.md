---
description: A política de metadados de foto para a propriedade System. GPS. Track.
ms.assetid: ac9e14a0-55f1-437e-9d27-df0fa09671c1
title: Política de metadados de foto System. GPS. Track
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 773c65eec8b165c51456f3871309644638c1e2da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764562"
---
# <a name="systemgpstrack-photo-metadata-policy"></a><span data-ttu-id="86e41-103">Política de metadados de foto System. GPS. Track</span><span class="sxs-lookup"><span data-stu-id="86e41-103">System.GPS.Track Photo Metadata Policy</span></span>

<span data-ttu-id="86e41-104">A política de metadados de foto para a propriedade [System. GPS. Track](../properties/props-system-gps-track.md) .</span><span class="sxs-lookup"><span data-stu-id="86e41-104">The photo metadata policy for the [System.GPS.Track](../properties/props-system-gps-track.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="86e41-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="86e41-105">PKEY</span></span>

<span data-ttu-id="86e41-106">\_Faixa de GPS PKEY \_</span><span class="sxs-lookup"><span data-stu-id="86e41-106">PKEY\_GPS\_Track</span></span>

### <a name="containers"></a><span data-ttu-id="86e41-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="86e41-107">Containers</span></span>

<span data-ttu-id="86e41-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="86e41-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="86e41-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="86e41-109">Read-Only</span></span>

<span data-ttu-id="86e41-110">Yes</span><span class="sxs-lookup"><span data-stu-id="86e41-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="86e41-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="86e41-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="86e41-112">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="86e41-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="86e41-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="86e41-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="86e41-114">Esse valor é gerado de System. GPS. TrackNumerator e System. GPS. TrackDenominator.</span><span class="sxs-lookup"><span data-stu-id="86e41-114">This value is generated from System.GPS.TrackNumerator and System.GPS.TrackDenominator.</span></span> <span data-ttu-id="86e41-115">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="86e41-115">It cannot be written directly.</span></span> <span data-ttu-id="86e41-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="86e41-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="86e41-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="86e41-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="86e41-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="86e41-118">Read Paths</span></span>



| <span data-ttu-id="86e41-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="86e41-119">Order</span></span> | <span data-ttu-id="86e41-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="86e41-120">Path</span></span>                      | <span data-ttu-id="86e41-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="86e41-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="86e41-122">1</span><span class="sxs-lookup"><span data-stu-id="86e41-122">1</span></span>     | <span data-ttu-id="86e41-123">/App1/IFD/GPS/{UShort = 15}</span><span class="sxs-lookup"><span data-stu-id="86e41-123">/app1/ifd/gps/{ushort=15}</span></span> |             |
| <span data-ttu-id="86e41-124">2</span><span class="sxs-lookup"><span data-stu-id="86e41-124">2</span></span>     | <span data-ttu-id="86e41-125">/xmp/exif:GPSTrack</span><span class="sxs-lookup"><span data-stu-id="86e41-125">/xmp/exif:GPSTrack</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="86e41-126">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="86e41-126">Write Paths</span></span>



| <span data-ttu-id="86e41-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="86e41-127">Order</span></span> | <span data-ttu-id="86e41-128">Caminho</span><span class="sxs-lookup"><span data-stu-id="86e41-128">Path</span></span>                      | <span data-ttu-id="86e41-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="86e41-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="86e41-130">1</span><span class="sxs-lookup"><span data-stu-id="86e41-130">1</span></span>     | <span data-ttu-id="86e41-131">/App1/IFD/GPS/{UShort = 15}</span><span class="sxs-lookup"><span data-stu-id="86e41-131">/app1/ifd/gps/{ushort=15}</span></span> |             |
| <span data-ttu-id="86e41-132">2</span><span class="sxs-lookup"><span data-stu-id="86e41-132">2</span></span>     | <span data-ttu-id="86e41-133">/xmp/exif:GPSTrack</span><span class="sxs-lookup"><span data-stu-id="86e41-133">/xmp/exif:GPSTrack</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="86e41-134">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="86e41-134">Remove Paths</span></span>



| <span data-ttu-id="86e41-135">Ordem</span><span class="sxs-lookup"><span data-stu-id="86e41-135">Order</span></span> | <span data-ttu-id="86e41-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="86e41-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="86e41-137">1</span><span class="sxs-lookup"><span data-stu-id="86e41-137">1</span></span>     | <span data-ttu-id="86e41-138">/App1/IFD/GPS/{UShort = 15}</span><span class="sxs-lookup"><span data-stu-id="86e41-138">/app1/ifd/gps/{ushort=15}</span></span> |
| <span data-ttu-id="86e41-139">2</span><span class="sxs-lookup"><span data-stu-id="86e41-139">2</span></span>     | <span data-ttu-id="86e41-140">/xmp/exif:gpstrack</span><span class="sxs-lookup"><span data-stu-id="86e41-140">/xmp/exif:gpstrack</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="86e41-141">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="86e41-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="86e41-142">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="86e41-142">Read Paths</span></span>



| <span data-ttu-id="86e41-143">Ordem</span><span class="sxs-lookup"><span data-stu-id="86e41-143">Order</span></span> | <span data-ttu-id="86e41-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="86e41-144">Path</span></span>                   | <span data-ttu-id="86e41-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="86e41-145">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="86e41-146">1</span><span class="sxs-lookup"><span data-stu-id="86e41-146">1</span></span>     | <span data-ttu-id="86e41-147">/IFD/GPS/{UShort = 15}</span><span class="sxs-lookup"><span data-stu-id="86e41-147">/ifd/gps/{ushort=15}</span></span>   |             |
| <span data-ttu-id="86e41-148">2</span><span class="sxs-lookup"><span data-stu-id="86e41-148">2</span></span>     | <span data-ttu-id="86e41-149">/ifd/xmp/exif:GPSTrack</span><span class="sxs-lookup"><span data-stu-id="86e41-149">/ifd/xmp/exif:GPSTrack</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="86e41-150">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="86e41-150">Write Paths</span></span>



| <span data-ttu-id="86e41-151">Ordem</span><span class="sxs-lookup"><span data-stu-id="86e41-151">Order</span></span> | <span data-ttu-id="86e41-152">Caminho</span><span class="sxs-lookup"><span data-stu-id="86e41-152">Path</span></span>                   | <span data-ttu-id="86e41-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="86e41-153">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="86e41-154">1</span><span class="sxs-lookup"><span data-stu-id="86e41-154">1</span></span>     | <span data-ttu-id="86e41-155">/IFD/GPS/{UShort = 15}</span><span class="sxs-lookup"><span data-stu-id="86e41-155">/ifd/gps/{ushort=15}</span></span>   |             |
| <span data-ttu-id="86e41-156">2</span><span class="sxs-lookup"><span data-stu-id="86e41-156">2</span></span>     | <span data-ttu-id="86e41-157">/ifd/xmp/exif:GPSTrack</span><span class="sxs-lookup"><span data-stu-id="86e41-157">/ifd/xmp/exif:GPSTrack</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="86e41-158">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="86e41-158">Remove Paths</span></span>



| <span data-ttu-id="86e41-159">Ordem</span><span class="sxs-lookup"><span data-stu-id="86e41-159">Order</span></span> | <span data-ttu-id="86e41-160">Caminho</span><span class="sxs-lookup"><span data-stu-id="86e41-160">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="86e41-161">1</span><span class="sxs-lookup"><span data-stu-id="86e41-161">1</span></span>     | <span data-ttu-id="86e41-162">/IFD/GPS/{UShort = 15}</span><span class="sxs-lookup"><span data-stu-id="86e41-162">/ifd/gps/{ushort=15}</span></span>   |
| <span data-ttu-id="86e41-163">2</span><span class="sxs-lookup"><span data-stu-id="86e41-163">2</span></span>     | <span data-ttu-id="86e41-164">/ifd/xmp/exif:gpstrack</span><span class="sxs-lookup"><span data-stu-id="86e41-164">/ifd/xmp/exif:gpstrack</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="86e41-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="86e41-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="86e41-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="86e41-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86e41-167">Sistema. GPS. Track</span><span class="sxs-lookup"><span data-stu-id="86e41-167">System.GPS.Track</span></span>](../properties/props-system-gps-track.md)
</dt> </dl>

 

 
