---
description: A política de metadados de foto para a propriedade System. GPS. DestLatitude.
ms.assetid: 05284291-977d-49b8-ad92-365f68384960
title: Política de metadados de foto System. GPS. DestLatitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192db0f8efc868e9457e86d283d9967e4692c95b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796398"
---
# <a name="systemgpsdestlatitude-photo-metadata-policy"></a><span data-ttu-id="d88f6-103">Política de metadados de foto System. GPS. DestLatitude</span><span class="sxs-lookup"><span data-stu-id="d88f6-103">System.GPS.DestLatitude Photo Metadata Policy</span></span>

<span data-ttu-id="d88f6-104">A política de metadados de foto para a propriedade [System. GPS. DestLatitude](../properties/props-system-gps-destlatitude.md) .</span><span class="sxs-lookup"><span data-stu-id="d88f6-104">The photo metadata policy for the [System.GPS.DestLatitude](../properties/props-system-gps-destlatitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d88f6-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="d88f6-105">PKEY</span></span>

<span data-ttu-id="d88f6-106">PKEY \_ GPS \_ DestLatitude</span><span class="sxs-lookup"><span data-stu-id="d88f6-106">PKEY\_GPS\_DestLatitude</span></span>

### <a name="containers"></a><span data-ttu-id="d88f6-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="d88f6-107">Containers</span></span>

<span data-ttu-id="d88f6-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d88f6-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d88f6-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d88f6-109">Read-Only</span></span>

<span data-ttu-id="d88f6-110">Yes</span><span class="sxs-lookup"><span data-stu-id="d88f6-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d88f6-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="d88f6-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d88f6-112">\_R8 de \| VT de vetor VT \_</span><span class="sxs-lookup"><span data-stu-id="d88f6-112">VT\_VECTOR \| VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="d88f6-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="d88f6-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="d88f6-114">\_R8 de \| VT de vetor VT \_</span><span class="sxs-lookup"><span data-stu-id="d88f6-114">VT\_VECTOR \| VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d88f6-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="d88f6-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="d88f6-116">Esse valor é gerado de System. GPS. DestLatitudeNumerator e System. GPS. DestLatitudeDenominator.</span><span class="sxs-lookup"><span data-stu-id="d88f6-116">This value is generated from System.GPS.DestLatitudeNumerator and System.GPS.DestLatitudeDenominator.</span></span> <span data-ttu-id="d88f6-117">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="d88f6-117">It cannot be written directly.</span></span> <span data-ttu-id="d88f6-118">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="d88f6-118">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="d88f6-119">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="d88f6-119">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d88f6-120">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="d88f6-120">Read Paths</span></span>



| <span data-ttu-id="d88f6-121">Ordem</span><span class="sxs-lookup"><span data-stu-id="d88f6-121">Order</span></span> | <span data-ttu-id="d88f6-122">Caminho</span><span class="sxs-lookup"><span data-stu-id="d88f6-122">Path</span></span>                      | <span data-ttu-id="d88f6-123">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d88f6-123">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="d88f6-124">1</span><span class="sxs-lookup"><span data-stu-id="d88f6-124">1</span></span>     | <span data-ttu-id="d88f6-125">/App1/IFD/GPS/{UShort = 20}</span><span class="sxs-lookup"><span data-stu-id="d88f6-125">/app1/ifd/gps/{ushort=20}</span></span> |             |
| <span data-ttu-id="d88f6-126">2</span><span class="sxs-lookup"><span data-stu-id="d88f6-126">2</span></span>     | <span data-ttu-id="d88f6-127">/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="d88f6-127">/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="d88f6-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="d88f6-128">Write Paths</span></span>



| <span data-ttu-id="d88f6-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="d88f6-129">Order</span></span> | <span data-ttu-id="d88f6-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="d88f6-130">Path</span></span>                      | <span data-ttu-id="d88f6-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d88f6-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="d88f6-132">1</span><span class="sxs-lookup"><span data-stu-id="d88f6-132">1</span></span>     | <span data-ttu-id="d88f6-133">/App1/IFD/GPS/{UShort = 20}</span><span class="sxs-lookup"><span data-stu-id="d88f6-133">/app1/ifd/gps/{ushort=20}</span></span> |             |
| <span data-ttu-id="d88f6-134">2</span><span class="sxs-lookup"><span data-stu-id="d88f6-134">2</span></span>     | <span data-ttu-id="d88f6-135">/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="d88f6-135">/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="d88f6-136">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="d88f6-136">Remove Paths</span></span>



| <span data-ttu-id="d88f6-137">Ordem</span><span class="sxs-lookup"><span data-stu-id="d88f6-137">Order</span></span> | <span data-ttu-id="d88f6-138">Caminho</span><span class="sxs-lookup"><span data-stu-id="d88f6-138">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="d88f6-139">1</span><span class="sxs-lookup"><span data-stu-id="d88f6-139">1</span></span>     | <span data-ttu-id="d88f6-140">/App1/IFD/GPS/{UShort = 20}</span><span class="sxs-lookup"><span data-stu-id="d88f6-140">/app1/ifd/gps/{ushort=20}</span></span> |
| <span data-ttu-id="d88f6-141">2</span><span class="sxs-lookup"><span data-stu-id="d88f6-141">2</span></span>     | <span data-ttu-id="d88f6-142">/xmp/exif:gpsdestlatitude</span><span class="sxs-lookup"><span data-stu-id="d88f6-142">/xmp/exif:gpsdestlatitude</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="d88f6-143">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="d88f6-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="d88f6-144">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="d88f6-144">Read Paths</span></span>



| <span data-ttu-id="d88f6-145">Ordem</span><span class="sxs-lookup"><span data-stu-id="d88f6-145">Order</span></span> | <span data-ttu-id="d88f6-146">Caminho</span><span class="sxs-lookup"><span data-stu-id="d88f6-146">Path</span></span>                          | <span data-ttu-id="d88f6-147">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d88f6-147">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="d88f6-148">1</span><span class="sxs-lookup"><span data-stu-id="d88f6-148">1</span></span>     | <span data-ttu-id="d88f6-149">/IFD/GPS/{UShort = 20}</span><span class="sxs-lookup"><span data-stu-id="d88f6-149">/ifd/gps/{ushort=20}</span></span>          |             |
| <span data-ttu-id="d88f6-150">2</span><span class="sxs-lookup"><span data-stu-id="d88f6-150">2</span></span>     | <span data-ttu-id="d88f6-151">/ifd/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="d88f6-151">/ifd/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="d88f6-152">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="d88f6-152">Write Paths</span></span>



| <span data-ttu-id="d88f6-153">Ordem</span><span class="sxs-lookup"><span data-stu-id="d88f6-153">Order</span></span> | <span data-ttu-id="d88f6-154">Caminho</span><span class="sxs-lookup"><span data-stu-id="d88f6-154">Path</span></span>                          | <span data-ttu-id="d88f6-155">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d88f6-155">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="d88f6-156">1</span><span class="sxs-lookup"><span data-stu-id="d88f6-156">1</span></span>     | <span data-ttu-id="d88f6-157">/IFD/GPS/{UShort = 20}</span><span class="sxs-lookup"><span data-stu-id="d88f6-157">/ifd/gps/{ushort=20}</span></span>          |             |
| <span data-ttu-id="d88f6-158">2</span><span class="sxs-lookup"><span data-stu-id="d88f6-158">2</span></span>     | <span data-ttu-id="d88f6-159">/ifd/xmp/exif:GPSDestLatitude</span><span class="sxs-lookup"><span data-stu-id="d88f6-159">/ifd/xmp/exif:GPSDestLatitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="d88f6-160">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="d88f6-160">Remove Paths</span></span>



| <span data-ttu-id="d88f6-161">Ordem</span><span class="sxs-lookup"><span data-stu-id="d88f6-161">Order</span></span> | <span data-ttu-id="d88f6-162">Caminho</span><span class="sxs-lookup"><span data-stu-id="d88f6-162">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="d88f6-163">1</span><span class="sxs-lookup"><span data-stu-id="d88f6-163">1</span></span>     | <span data-ttu-id="d88f6-164">/IFD/GPS/{UShort = 20}</span><span class="sxs-lookup"><span data-stu-id="d88f6-164">/ifd/gps/{ushort=20}</span></span>          |
| <span data-ttu-id="d88f6-165">2</span><span class="sxs-lookup"><span data-stu-id="d88f6-165">2</span></span>     | <span data-ttu-id="d88f6-166">/ifd/xmp/exif:gpsdestlatitude</span><span class="sxs-lookup"><span data-stu-id="d88f6-166">/ifd/xmp/exif:gpsdestlatitude</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d88f6-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="d88f6-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d88f6-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d88f6-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d88f6-169">System. GPS. DestLatitude</span><span class="sxs-lookup"><span data-stu-id="d88f6-169">System.GPS.DestLatitude</span></span>](../properties/props-system-gps-destlatitude.md)
</dt> </dl>

 

 
