---
description: A política de metadados de foto para a propriedade System. GPS. altitude.
ms.assetid: 63d59aa3-52a6-4b6f-b6ec-a1c4abcee83f
title: Política de metadados de foto System. GPS. altitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003d39d135c625a01035c023b5d7dc8d890b3b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791278"
---
# <a name="systemgpsaltitude-photo-metadata-policy"></a><span data-ttu-id="5cf19-103">Política de metadados de foto System. GPS. altitude</span><span class="sxs-lookup"><span data-stu-id="5cf19-103">System.GPS.Altitude Photo Metadata Policy</span></span>

<span data-ttu-id="5cf19-104">A política de metadados de foto para a propriedade [System. GPS. altitude](../properties/props-system-gps-altitude.md) .</span><span class="sxs-lookup"><span data-stu-id="5cf19-104">The photo metadata policy for the [System.GPS.Altitude](../properties/props-system-gps-altitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="5cf19-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="5cf19-105">PKEY</span></span>

<span data-ttu-id="5cf19-106">\_Altitude de GPS PKEY \_</span><span class="sxs-lookup"><span data-stu-id="5cf19-106">PKEY\_GPS\_Altitude</span></span>

### <a name="description"></a><span data-ttu-id="5cf19-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5cf19-107">Description</span></span>

<span data-ttu-id="5cf19-108">A altitude é indicada como um valor absoluto referenciado em metros.</span><span class="sxs-lookup"><span data-stu-id="5cf19-108">The altitude is indicated as an absolute value referenced in meters.</span></span>

### <a name="containers"></a><span data-ttu-id="5cf19-109">Contêineres</span><span class="sxs-lookup"><span data-stu-id="5cf19-109">Containers</span></span>

<span data-ttu-id="5cf19-110">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="5cf19-110">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="5cf19-111">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5cf19-111">Read-Only</span></span>

<span data-ttu-id="5cf19-112">Yes</span><span class="sxs-lookup"><span data-stu-id="5cf19-112">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="5cf19-113">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="5cf19-113">Output PROPVARIANT Type</span></span>

<span data-ttu-id="5cf19-114">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="5cf19-114">VT\_R8</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="5cf19-115">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="5cf19-115">Input PROPVARIANT Type</span></span>

<span data-ttu-id="5cf19-116">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="5cf19-116">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="5cf19-117">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="5cf19-117">Conflict Resolution Policy</span></span>

<span data-ttu-id="5cf19-118">Esse valor pode ser gravado escrevendo em System. GPS. altitude. Numerator e System. GPS. altitude. denominador.</span><span class="sxs-lookup"><span data-stu-id="5cf19-118">This value can be written by writing to System.GPS.Altitude.Numerator and System.GPS.Altitude.Denominator.</span></span> <span data-ttu-id="5cf19-119">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="5cf19-119">It cannot be written directly.</span></span> <span data-ttu-id="5cf19-120">Os caminhos de gravação nas tabelas a seguir indicam onde o valor pode ser salvo quando é gerado, não quando ele é gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="5cf19-120">The write paths in the following tables indicate where the value may be saved when it is generated, not when it is written directly.</span></span> <span data-ttu-id="5cf19-121">Quando o valor é lido, os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="5cf19-121">When the value is read, values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="5cf19-122">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="5cf19-122">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="5cf19-123">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="5cf19-123">Read Paths</span></span>



| <span data-ttu-id="5cf19-124">Ordem</span><span class="sxs-lookup"><span data-stu-id="5cf19-124">Order</span></span> | <span data-ttu-id="5cf19-125">Caminho</span><span class="sxs-lookup"><span data-stu-id="5cf19-125">Path</span></span>                     | <span data-ttu-id="5cf19-126">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5cf19-126">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="5cf19-127">1</span><span class="sxs-lookup"><span data-stu-id="5cf19-127">1</span></span>     | <span data-ttu-id="5cf19-128">/App1/IFD/GPS/{UShort = 6}</span><span class="sxs-lookup"><span data-stu-id="5cf19-128">/app1/ifd/gps/{ushort=6}</span></span> |             |
| <span data-ttu-id="5cf19-129">2</span><span class="sxs-lookup"><span data-stu-id="5cf19-129">2</span></span>     | <span data-ttu-id="5cf19-130">/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="5cf19-130">/xmp/exif:GPSAltitude</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="5cf19-131">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="5cf19-131">Write Paths</span></span>



| <span data-ttu-id="5cf19-132">Ordem</span><span class="sxs-lookup"><span data-stu-id="5cf19-132">Order</span></span> | <span data-ttu-id="5cf19-133">Caminho</span><span class="sxs-lookup"><span data-stu-id="5cf19-133">Path</span></span>                     | <span data-ttu-id="5cf19-134">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5cf19-134">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="5cf19-135">1</span><span class="sxs-lookup"><span data-stu-id="5cf19-135">1</span></span>     | <span data-ttu-id="5cf19-136">/App1/IFD/GPS/{UShort = 6}</span><span class="sxs-lookup"><span data-stu-id="5cf19-136">/app1/ifd/gps/{ushort=6}</span></span> |             |
| <span data-ttu-id="5cf19-137">2</span><span class="sxs-lookup"><span data-stu-id="5cf19-137">2</span></span>     | <span data-ttu-id="5cf19-138">/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="5cf19-138">/xmp/exif:GPSAltitude</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="5cf19-139">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="5cf19-139">Remove Paths</span></span>



| <span data-ttu-id="5cf19-140">Ordem</span><span class="sxs-lookup"><span data-stu-id="5cf19-140">Order</span></span> | <span data-ttu-id="5cf19-141">Caminho</span><span class="sxs-lookup"><span data-stu-id="5cf19-141">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="5cf19-142">1</span><span class="sxs-lookup"><span data-stu-id="5cf19-142">1</span></span>     | <span data-ttu-id="5cf19-143">/App1/IFD/GPS/{UShort = 6}</span><span class="sxs-lookup"><span data-stu-id="5cf19-143">/app1/ifd/gps/{ushort=6}</span></span> |
| <span data-ttu-id="5cf19-144">2</span><span class="sxs-lookup"><span data-stu-id="5cf19-144">2</span></span>     | <span data-ttu-id="5cf19-145">/xmp/exif:gpsaltitude</span><span class="sxs-lookup"><span data-stu-id="5cf19-145">/xmp/exif:gpsaltitude</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="5cf19-146">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="5cf19-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="5cf19-147">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="5cf19-147">Read Paths</span></span>



| <span data-ttu-id="5cf19-148">Ordem</span><span class="sxs-lookup"><span data-stu-id="5cf19-148">Order</span></span> | <span data-ttu-id="5cf19-149">Caminho</span><span class="sxs-lookup"><span data-stu-id="5cf19-149">Path</span></span>                      | <span data-ttu-id="5cf19-150">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5cf19-150">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="5cf19-151">1</span><span class="sxs-lookup"><span data-stu-id="5cf19-151">1</span></span>     | <span data-ttu-id="5cf19-152">/IFD/GPS/{UShort = 6}</span><span class="sxs-lookup"><span data-stu-id="5cf19-152">/ifd/gps/{ushort=6}</span></span>       |             |
| <span data-ttu-id="5cf19-153">2</span><span class="sxs-lookup"><span data-stu-id="5cf19-153">2</span></span>     | <span data-ttu-id="5cf19-154">/ifd/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="5cf19-154">/ifd/xmp/exif:GPSAltitude</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="5cf19-155">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="5cf19-155">Write Paths</span></span>



| <span data-ttu-id="5cf19-156">Ordem</span><span class="sxs-lookup"><span data-stu-id="5cf19-156">Order</span></span> | <span data-ttu-id="5cf19-157">Caminho</span><span class="sxs-lookup"><span data-stu-id="5cf19-157">Path</span></span>                      | <span data-ttu-id="5cf19-158">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="5cf19-158">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="5cf19-159">1</span><span class="sxs-lookup"><span data-stu-id="5cf19-159">1</span></span>     | <span data-ttu-id="5cf19-160">/IFD/GPS/{UShort = 6}</span><span class="sxs-lookup"><span data-stu-id="5cf19-160">/ifd/gps/{ushort=6}</span></span>       |             |
| <span data-ttu-id="5cf19-161">2</span><span class="sxs-lookup"><span data-stu-id="5cf19-161">2</span></span>     | <span data-ttu-id="5cf19-162">/ifd/xmp/exif:GPSAltitude</span><span class="sxs-lookup"><span data-stu-id="5cf19-162">/ifd/xmp/exif:GPSAltitude</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="5cf19-163">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="5cf19-163">Remove Paths</span></span>



| <span data-ttu-id="5cf19-164">Ordem</span><span class="sxs-lookup"><span data-stu-id="5cf19-164">Order</span></span> | <span data-ttu-id="5cf19-165">Caminho</span><span class="sxs-lookup"><span data-stu-id="5cf19-165">Path</span></span>                      |     |
|-------|---------------------------|-----|
| <span data-ttu-id="5cf19-166">1</span><span class="sxs-lookup"><span data-stu-id="5cf19-166">1</span></span>     | <span data-ttu-id="5cf19-167">/IFD/GPS/{UShort = 6}</span><span class="sxs-lookup"><span data-stu-id="5cf19-167">/ifd/gps/{ushort=6}</span></span>       |     |
| <span data-ttu-id="5cf19-168">2</span><span class="sxs-lookup"><span data-stu-id="5cf19-168">2</span></span>     | <span data-ttu-id="5cf19-169">/ifd/xmp/exif:gpsaltitude</span><span class="sxs-lookup"><span data-stu-id="5cf19-169">/ifd/xmp/exif:gpsaltitude</span></span> |     |



 

## <a name="remarks"></a><span data-ttu-id="5cf19-170">Comentários</span><span class="sxs-lookup"><span data-stu-id="5cf19-170">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cf19-171">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5cf19-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cf19-172">System. GPS. altitude</span><span class="sxs-lookup"><span data-stu-id="5cf19-172">System.GPS.Altitude</span></span>](../properties/props-system-gps-altitude.md)
</dt> </dl>

 

 
