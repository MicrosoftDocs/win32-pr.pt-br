---
description: A política de metadados de foto para a propriedade System. GPS. Speed.
ms.assetid: 278826c2-3057-4da2-8c86-0e44471ad7b0
title: Política de metadados de foto System. GPS. Speed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26d89f755114a73ab17388a1718d5ad0cbdf5a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763845"
---
# <a name="systemgpsspeed-photo-metadata-policy"></a><span data-ttu-id="b3e0f-103">Política de metadados de foto System. GPS. Speed</span><span class="sxs-lookup"><span data-stu-id="b3e0f-103">System.GPS.Speed Photo Metadata Policy</span></span>

<span data-ttu-id="b3e0f-104">A política de metadados de foto para a propriedade [System. GPS. Speed](../properties/props-system-gps-speed.md) .</span><span class="sxs-lookup"><span data-stu-id="b3e0f-104">The photo metadata policy for the [System.GPS.Speed](../properties/props-system-gps-speed.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b3e0f-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="b3e0f-105">PKEY</span></span>

<span data-ttu-id="b3e0f-106">\_Velocidade de GPS PKEY \_</span><span class="sxs-lookup"><span data-stu-id="b3e0f-106">PKEY\_GPS\_Speed</span></span>

### <a name="containers"></a><span data-ttu-id="b3e0f-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="b3e0f-107">Containers</span></span>

<span data-ttu-id="b3e0f-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b3e0f-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b3e0f-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3e0f-109">Read-Only</span></span>

<span data-ttu-id="b3e0f-110">Yes</span><span class="sxs-lookup"><span data-stu-id="b3e0f-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b3e0f-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="b3e0f-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b3e0f-112">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="b3e0f-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b3e0f-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="b3e0f-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="b3e0f-114">Esse valor é gerado de System. GPS. SpeedNumerator e System. GPS. SpeedDenominator.</span><span class="sxs-lookup"><span data-stu-id="b3e0f-114">This value is generated from System.GPS.SpeedNumerator and System.GPS.SpeedDenominator.</span></span> <span data-ttu-id="b3e0f-115">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="b3e0f-115">It cannot be written directly.</span></span> <span data-ttu-id="b3e0f-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="b3e0f-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b3e0f-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="b3e0f-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b3e0f-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="b3e0f-118">Read Paths</span></span>



| <span data-ttu-id="b3e0f-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="b3e0f-119">Order</span></span> | <span data-ttu-id="b3e0f-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="b3e0f-120">Path</span></span>                      | <span data-ttu-id="b3e0f-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b3e0f-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="b3e0f-122">1</span><span class="sxs-lookup"><span data-stu-id="b3e0f-122">1</span></span>     | <span data-ttu-id="b3e0f-123">/App1/IFD/GPS/{UShort = 13}</span><span class="sxs-lookup"><span data-stu-id="b3e0f-123">/app1/ifd/gps/{ushort=13}</span></span> |             |
| <span data-ttu-id="b3e0f-124">2</span><span class="sxs-lookup"><span data-stu-id="b3e0f-124">2</span></span>     | <span data-ttu-id="b3e0f-125">/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="b3e0f-125">/xmp/exif:GPSSpeed</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="b3e0f-126">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="b3e0f-126">Write Paths</span></span>



| <span data-ttu-id="b3e0f-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="b3e0f-127">Order</span></span> | <span data-ttu-id="b3e0f-128">Caminho</span><span class="sxs-lookup"><span data-stu-id="b3e0f-128">Path</span></span>                      | <span data-ttu-id="b3e0f-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b3e0f-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="b3e0f-130">1</span><span class="sxs-lookup"><span data-stu-id="b3e0f-130">1</span></span>     | <span data-ttu-id="b3e0f-131">/App1/IFD/GPS/{UShort = 13}</span><span class="sxs-lookup"><span data-stu-id="b3e0f-131">/app1/ifd/gps/{ushort=13}</span></span> |             |
| <span data-ttu-id="b3e0f-132">2</span><span class="sxs-lookup"><span data-stu-id="b3e0f-132">2</span></span>     | <span data-ttu-id="b3e0f-133">/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="b3e0f-133">/xmp/exif:GPSSpeed</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b3e0f-134">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="b3e0f-134">Remove Paths</span></span>



| <span data-ttu-id="b3e0f-135">Ordem</span><span class="sxs-lookup"><span data-stu-id="b3e0f-135">Order</span></span> | <span data-ttu-id="b3e0f-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="b3e0f-136">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="b3e0f-137">1</span><span class="sxs-lookup"><span data-stu-id="b3e0f-137">1</span></span>     | <span data-ttu-id="b3e0f-138">/App1/IFD/GPS/{UShort = 13}</span><span class="sxs-lookup"><span data-stu-id="b3e0f-138">/app1/ifd/gps/{ushort=13}</span></span> |
| <span data-ttu-id="b3e0f-139">2</span><span class="sxs-lookup"><span data-stu-id="b3e0f-139">2</span></span>     | <span data-ttu-id="b3e0f-140">/xmp/exif:gpsspeed</span><span class="sxs-lookup"><span data-stu-id="b3e0f-140">/xmp/exif:gpsspeed</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="b3e0f-141">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="b3e0f-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b3e0f-142">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="b3e0f-142">Read Paths</span></span>



| <span data-ttu-id="b3e0f-143">Ordem</span><span class="sxs-lookup"><span data-stu-id="b3e0f-143">Order</span></span> | <span data-ttu-id="b3e0f-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="b3e0f-144">Path</span></span>                   | <span data-ttu-id="b3e0f-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b3e0f-145">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="b3e0f-146">1</span><span class="sxs-lookup"><span data-stu-id="b3e0f-146">1</span></span>     | <span data-ttu-id="b3e0f-147">/IFD/GPS/{UShort = 13}</span><span class="sxs-lookup"><span data-stu-id="b3e0f-147">/ifd/gps/{ushort=13}</span></span>   |             |
| <span data-ttu-id="b3e0f-148">2</span><span class="sxs-lookup"><span data-stu-id="b3e0f-148">2</span></span>     | <span data-ttu-id="b3e0f-149">/ifd/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="b3e0f-149">/ifd/xmp/exif:GPSSpeed</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="b3e0f-150">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="b3e0f-150">Write Paths</span></span>



| <span data-ttu-id="b3e0f-151">Ordem</span><span class="sxs-lookup"><span data-stu-id="b3e0f-151">Order</span></span> | <span data-ttu-id="b3e0f-152">Caminho</span><span class="sxs-lookup"><span data-stu-id="b3e0f-152">Path</span></span>                   | <span data-ttu-id="b3e0f-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b3e0f-153">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="b3e0f-154">1</span><span class="sxs-lookup"><span data-stu-id="b3e0f-154">1</span></span>     | <span data-ttu-id="b3e0f-155">/IFD/GPS/{UShort = 13}</span><span class="sxs-lookup"><span data-stu-id="b3e0f-155">/ifd/gps/{ushort=13}</span></span>   |             |
| <span data-ttu-id="b3e0f-156">2</span><span class="sxs-lookup"><span data-stu-id="b3e0f-156">2</span></span>     | <span data-ttu-id="b3e0f-157">/ifd/xmp/exif:GPSSpeed</span><span class="sxs-lookup"><span data-stu-id="b3e0f-157">/ifd/xmp/exif:GPSSpeed</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="b3e0f-158">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="b3e0f-158">Remove Paths</span></span>



| <span data-ttu-id="b3e0f-159">Ordem</span><span class="sxs-lookup"><span data-stu-id="b3e0f-159">Order</span></span> | <span data-ttu-id="b3e0f-160">Caminho</span><span class="sxs-lookup"><span data-stu-id="b3e0f-160">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="b3e0f-161">1</span><span class="sxs-lookup"><span data-stu-id="b3e0f-161">1</span></span>     | <span data-ttu-id="b3e0f-162">/IFD/GPS/{UShort = 13}</span><span class="sxs-lookup"><span data-stu-id="b3e0f-162">/ifd/gps/{ushort=13}</span></span>   |
| <span data-ttu-id="b3e0f-163">2</span><span class="sxs-lookup"><span data-stu-id="b3e0f-163">2</span></span>     | <span data-ttu-id="b3e0f-164">/ifd/xmp/exif:gpsspeed</span><span class="sxs-lookup"><span data-stu-id="b3e0f-164">/ifd/xmp/exif:gpsspeed</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b3e0f-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3e0f-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3e0f-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3e0f-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3e0f-167">Sistema. GPS. Speed</span><span class="sxs-lookup"><span data-stu-id="b3e0f-167">System.GPS.Speed</span></span>](../properties/props-system-gps-speed.md)
</dt> </dl>

 

 
