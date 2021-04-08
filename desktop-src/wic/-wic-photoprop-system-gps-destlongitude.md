---
description: A política de metadados de foto para a propriedade System. GPS. DestLongitude.
ms.assetid: 885a522d-e1bf-43fb-a996-97e725b6cf0c
title: Política de metadados de foto System. GPS. DestLongitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72e0a4f56e49dfbb3397b96cf7fae35a6065b7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011542"
---
# <a name="systemgpsdestlongitude-photo-metadata-policy"></a><span data-ttu-id="9c486-103">Política de metadados de foto System. GPS. DestLongitude</span><span class="sxs-lookup"><span data-stu-id="9c486-103">System.GPS.DestLongitude Photo Metadata Policy</span></span>

<span data-ttu-id="9c486-104">A política de metadados de foto para a propriedade [System. GPS. DestLongitude](../properties/props-system-gps-destlongitude.md) .</span><span class="sxs-lookup"><span data-stu-id="9c486-104">The photo metadata policy for the [System.GPS.DestLongitude](../properties/props-system-gps-destlongitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9c486-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="9c486-105">PKEY</span></span>

<span data-ttu-id="9c486-106">PKEY \_ GPS \_ DestLongitude</span><span class="sxs-lookup"><span data-stu-id="9c486-106">PKEY\_GPS\_DestLongitude</span></span>

### <a name="containers"></a><span data-ttu-id="9c486-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="9c486-107">Containers</span></span>

<span data-ttu-id="9c486-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9c486-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9c486-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9c486-109">Read-Only</span></span>

<span data-ttu-id="9c486-110">Yes</span><span class="sxs-lookup"><span data-stu-id="9c486-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="9c486-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="9c486-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="9c486-112">\_R8 de \| VT de vetor VT \_</span><span class="sxs-lookup"><span data-stu-id="9c486-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="9c486-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="9c486-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="9c486-114">\_R8 de \| VT de vetor VT \_</span><span class="sxs-lookup"><span data-stu-id="9c486-114">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9c486-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="9c486-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="9c486-116">Esse valor é gerado de System. GPS. DestLongitudeNumerator e System. GPS. DestLongitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="9c486-116">This value is generated from System.GPS.DestLongitudeNumerator and System.GPS.DestLongitudeDenominator.</span></span> <span data-ttu-id="9c486-117">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="9c486-117">It cannot be written directly.</span></span> <span data-ttu-id="9c486-118">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="9c486-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="9c486-119">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="9c486-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="9c486-120">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="9c486-120">Read Paths</span></span>



| <span data-ttu-id="9c486-121">Ordem</span><span class="sxs-lookup"><span data-stu-id="9c486-121">Order</span></span> | <span data-ttu-id="9c486-122">Caminho</span><span class="sxs-lookup"><span data-stu-id="9c486-122">Path</span></span>                       | <span data-ttu-id="9c486-123">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9c486-123">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="9c486-124">1</span><span class="sxs-lookup"><span data-stu-id="9c486-124">1</span></span>     | <span data-ttu-id="9c486-125">/App1/IFD/GPS/{UShort = 22}</span><span class="sxs-lookup"><span data-stu-id="9c486-125">/app1/ifd/gps/{ushort=22}</span></span>  |             |
| <span data-ttu-id="9c486-126">2</span><span class="sxs-lookup"><span data-stu-id="9c486-126">2</span></span>     | <span data-ttu-id="9c486-127">/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="9c486-127">/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="9c486-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="9c486-128">Write Paths</span></span>



| <span data-ttu-id="9c486-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="9c486-129">Order</span></span> | <span data-ttu-id="9c486-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="9c486-130">Path</span></span>                       | <span data-ttu-id="9c486-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9c486-131">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="9c486-132">1</span><span class="sxs-lookup"><span data-stu-id="9c486-132">1</span></span>     | <span data-ttu-id="9c486-133">/App1/IFD/GPS/{UShort = 22}</span><span class="sxs-lookup"><span data-stu-id="9c486-133">/app1/ifd/gps/{ushort=22}</span></span>  |             |
| <span data-ttu-id="9c486-134">2</span><span class="sxs-lookup"><span data-stu-id="9c486-134">2</span></span>     | <span data-ttu-id="9c486-135">/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="9c486-135">/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="9c486-136">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="9c486-136">Remove Paths</span></span>



| <span data-ttu-id="9c486-137">Ordem</span><span class="sxs-lookup"><span data-stu-id="9c486-137">Order</span></span> | <span data-ttu-id="9c486-138">Caminho</span><span class="sxs-lookup"><span data-stu-id="9c486-138">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="9c486-139">1</span><span class="sxs-lookup"><span data-stu-id="9c486-139">1</span></span>     | <span data-ttu-id="9c486-140">/App1/IFD/GPS/{UShort = 22}</span><span class="sxs-lookup"><span data-stu-id="9c486-140">/app1/ifd/gps/{ushort=22}</span></span>  |
| <span data-ttu-id="9c486-141">2</span><span class="sxs-lookup"><span data-stu-id="9c486-141">2</span></span>     | <span data-ttu-id="9c486-142">/xmp/exif:gpsdestlongitude</span><span class="sxs-lookup"><span data-stu-id="9c486-142">/xmp/exif:gpsdestlongitude</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="9c486-143">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="9c486-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="9c486-144">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="9c486-144">Read Paths</span></span>



| <span data-ttu-id="9c486-145">Ordem</span><span class="sxs-lookup"><span data-stu-id="9c486-145">Order</span></span> | <span data-ttu-id="9c486-146">Caminho</span><span class="sxs-lookup"><span data-stu-id="9c486-146">Path</span></span>                           | <span data-ttu-id="9c486-147">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9c486-147">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="9c486-148">1</span><span class="sxs-lookup"><span data-stu-id="9c486-148">1</span></span>     | <span data-ttu-id="9c486-149">/IFD/GPS/{UShort = 22}</span><span class="sxs-lookup"><span data-stu-id="9c486-149">/ifd/gps/{ushort=22}</span></span>           |             |
| <span data-ttu-id="9c486-150">2</span><span class="sxs-lookup"><span data-stu-id="9c486-150">2</span></span>     | <span data-ttu-id="9c486-151">/ifd/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="9c486-151">/ifd/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="9c486-152">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="9c486-152">Write Paths</span></span>



| <span data-ttu-id="9c486-153">Ordem</span><span class="sxs-lookup"><span data-stu-id="9c486-153">Order</span></span> | <span data-ttu-id="9c486-154">Caminho</span><span class="sxs-lookup"><span data-stu-id="9c486-154">Path</span></span>                           | <span data-ttu-id="9c486-155">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9c486-155">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="9c486-156">1</span><span class="sxs-lookup"><span data-stu-id="9c486-156">1</span></span>     | <span data-ttu-id="9c486-157">/IFD/GPS/{UShort = 22}</span><span class="sxs-lookup"><span data-stu-id="9c486-157">/ifd/gps/{ushort=22}</span></span>           |             |
| <span data-ttu-id="9c486-158">2</span><span class="sxs-lookup"><span data-stu-id="9c486-158">2</span></span>     | <span data-ttu-id="9c486-159">/ifd/xmp/exif:GPSDestLongitude</span><span class="sxs-lookup"><span data-stu-id="9c486-159">/ifd/xmp/exif:GPSDestLongitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="9c486-160">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="9c486-160">Remove Paths</span></span>



| <span data-ttu-id="9c486-161">Ordem</span><span class="sxs-lookup"><span data-stu-id="9c486-161">Order</span></span> | <span data-ttu-id="9c486-162">Caminho</span><span class="sxs-lookup"><span data-stu-id="9c486-162">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="9c486-163">1</span><span class="sxs-lookup"><span data-stu-id="9c486-163">1</span></span>     | <span data-ttu-id="9c486-164">/IFD/GPS/{UShort = 22}</span><span class="sxs-lookup"><span data-stu-id="9c486-164">/ifd/gps/{ushort=22}</span></span>           |
| <span data-ttu-id="9c486-165">2</span><span class="sxs-lookup"><span data-stu-id="9c486-165">2</span></span>     | <span data-ttu-id="9c486-166">/ifd/xmp/exif:gpsdestlongitude</span><span class="sxs-lookup"><span data-stu-id="9c486-166">/ifd/xmp/exif:gpsdestlongitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9c486-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c486-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c486-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9c486-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c486-169">System. GPS. DestLongitude</span><span class="sxs-lookup"><span data-stu-id="9c486-169">System.GPS.DestLongitude</span></span>](../properties/props-system-gps-destlongitude.md)
</dt> </dl>

 

 
