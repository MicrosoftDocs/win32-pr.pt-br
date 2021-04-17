---
description: A política de metadados de foto para a propriedade System. GPS. AltitudeRef.
ms.assetid: abbb2441-25ca-484b-a744-620ff2794221
title: Política de metadados de foto System. GPS. AltitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db600d218d72014c49fd3f0a8b5eb11dd4c467d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790383"
---
# <a name="systemgpsaltituderef-photo-metadata-policy"></a><span data-ttu-id="6a51f-103">Política de metadados de foto System. GPS. AltitudeRef</span><span class="sxs-lookup"><span data-stu-id="6a51f-103">System.GPS.AltitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="6a51f-104">A política de metadados de foto para a propriedade [System. GPS. AltitudeRef](../properties/props-system-gps-altituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="6a51f-104">The photo metadata policy for the [System.GPS.AltitudeRef](../properties/props-system-gps-altituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="6a51f-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="6a51f-105">PKEY</span></span>

<span data-ttu-id="6a51f-106">PKEY \_ GPS \_ AltitudeRef</span><span class="sxs-lookup"><span data-stu-id="6a51f-106">PKEY\_GPS\_AltitudeRef</span></span>

### <a name="description"></a><span data-ttu-id="6a51f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a51f-107">Description</span></span>

<span data-ttu-id="6a51f-108">Indica a altitude usada como a altitude de referência.</span><span class="sxs-lookup"><span data-stu-id="6a51f-108">Indicates the altitude used as the reference altitude.</span></span> <span data-ttu-id="6a51f-109">Um valor de 0 indica que a altitude está acima do nível do mar.</span><span class="sxs-lookup"><span data-stu-id="6a51f-109">A value of 0 indicates the altitude is above sea level.</span></span> <span data-ttu-id="6a51f-110">Um valor de 1 indica uma altitude abaixo do nível do Sea.</span><span class="sxs-lookup"><span data-stu-id="6a51f-110">A value of 1 indicates an altitude below sea level.</span></span>

### <a name="containers"></a><span data-ttu-id="6a51f-111">Contêineres</span><span class="sxs-lookup"><span data-stu-id="6a51f-111">Containers</span></span>

<span data-ttu-id="6a51f-112">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="6a51f-112">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="6a51f-113">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6a51f-113">Read-Only</span></span>

<span data-ttu-id="6a51f-114">No</span><span class="sxs-lookup"><span data-stu-id="6a51f-114">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="6a51f-115">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="6a51f-115">Output PROPVARIANT Type</span></span>

<span data-ttu-id="6a51f-116">\_UI1 VT</span><span class="sxs-lookup"><span data-stu-id="6a51f-116">VT\_UI1</span></span>

### <a name="input-type"></a><span data-ttu-id="6a51f-117">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="6a51f-117">Input Type</span></span>

<span data-ttu-id="6a51f-118">Minuciosa.</span><span class="sxs-lookup"><span data-stu-id="6a51f-118">Byte.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="6a51f-119">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="6a51f-119">Conflict Resolution Policy</span></span>

<span data-ttu-id="6a51f-120">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="6a51f-120">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="6a51f-121">Políticas JPEG</span><span class="sxs-lookup"><span data-stu-id="6a51f-121">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="6a51f-122">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="6a51f-122">Read Paths</span></span>



| <span data-ttu-id="6a51f-123">Ordem</span><span class="sxs-lookup"><span data-stu-id="6a51f-123">Order</span></span> | <span data-ttu-id="6a51f-124">Caminho</span><span class="sxs-lookup"><span data-stu-id="6a51f-124">Path</span></span>                     | <span data-ttu-id="6a51f-125">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="6a51f-125">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="6a51f-126">1</span><span class="sxs-lookup"><span data-stu-id="6a51f-126">1</span></span>     | <span data-ttu-id="6a51f-127">/App1/IFD/GPS/{UShort = 5}</span><span class="sxs-lookup"><span data-stu-id="6a51f-127">/app1/ifd/gps/{ushort=5}</span></span> | <span data-ttu-id="6a51f-128">byte</span><span class="sxs-lookup"><span data-stu-id="6a51f-128">byte</span></span>        |
| <span data-ttu-id="6a51f-129">2</span><span class="sxs-lookup"><span data-stu-id="6a51f-129">2</span></span>     | <span data-ttu-id="6a51f-130">/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="6a51f-130">/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="6a51f-131">Unicode</span><span class="sxs-lookup"><span data-stu-id="6a51f-131">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="6a51f-132">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="6a51f-132">Write Paths</span></span>



| <span data-ttu-id="6a51f-133">Ordem</span><span class="sxs-lookup"><span data-stu-id="6a51f-133">Order</span></span> | <span data-ttu-id="6a51f-134">Caminho</span><span class="sxs-lookup"><span data-stu-id="6a51f-134">Path</span></span>                     | <span data-ttu-id="6a51f-135">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="6a51f-135">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="6a51f-136">1</span><span class="sxs-lookup"><span data-stu-id="6a51f-136">1</span></span>     | <span data-ttu-id="6a51f-137">/App1/IFD/GPS/{UShort = 5}</span><span class="sxs-lookup"><span data-stu-id="6a51f-137">/app1/ifd/gps/{ushort=5}</span></span> | <span data-ttu-id="6a51f-138">byte</span><span class="sxs-lookup"><span data-stu-id="6a51f-138">byte</span></span>        |
| <span data-ttu-id="6a51f-139">2</span><span class="sxs-lookup"><span data-stu-id="6a51f-139">2</span></span>     | <span data-ttu-id="6a51f-140">/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="6a51f-140">/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="6a51f-141">Unicode</span><span class="sxs-lookup"><span data-stu-id="6a51f-141">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="6a51f-142">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="6a51f-142">Remove Paths</span></span>



| <span data-ttu-id="6a51f-143">Ordem</span><span class="sxs-lookup"><span data-stu-id="6a51f-143">Order</span></span> | <span data-ttu-id="6a51f-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="6a51f-144">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="6a51f-145">1</span><span class="sxs-lookup"><span data-stu-id="6a51f-145">1</span></span>     | <span data-ttu-id="6a51f-146">/App1/IFD/GPS/{UShort = 5}</span><span class="sxs-lookup"><span data-stu-id="6a51f-146">/app1/ifd/gps/{ushort=5}</span></span> |
| <span data-ttu-id="6a51f-147">2</span><span class="sxs-lookup"><span data-stu-id="6a51f-147">2</span></span>     | <span data-ttu-id="6a51f-148">/xmp/exif:gpsaltituderef</span><span class="sxs-lookup"><span data-stu-id="6a51f-148">/xmp/exif:gpsaltituderef</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="6a51f-149">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="6a51f-149">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="6a51f-150">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="6a51f-150">Read Paths</span></span>



| <span data-ttu-id="6a51f-151">Ordem</span><span class="sxs-lookup"><span data-stu-id="6a51f-151">Order</span></span> | <span data-ttu-id="6a51f-152">Caminho</span><span class="sxs-lookup"><span data-stu-id="6a51f-152">Path</span></span>                         | <span data-ttu-id="6a51f-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="6a51f-153">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="6a51f-154">1</span><span class="sxs-lookup"><span data-stu-id="6a51f-154">1</span></span>     | <span data-ttu-id="6a51f-155">/IFD/GPS/{UShort = 5}</span><span class="sxs-lookup"><span data-stu-id="6a51f-155">/ifd/gps/{ushort=5}</span></span>          | <span data-ttu-id="6a51f-156">byte</span><span class="sxs-lookup"><span data-stu-id="6a51f-156">byte</span></span>        |
| <span data-ttu-id="6a51f-157">2</span><span class="sxs-lookup"><span data-stu-id="6a51f-157">2</span></span>     | <span data-ttu-id="6a51f-158">/ifd/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="6a51f-158">/ifd/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="6a51f-159">Unicode</span><span class="sxs-lookup"><span data-stu-id="6a51f-159">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="6a51f-160">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="6a51f-160">Write Paths</span></span>



| <span data-ttu-id="6a51f-161">Ordem</span><span class="sxs-lookup"><span data-stu-id="6a51f-161">Order</span></span> | <span data-ttu-id="6a51f-162">Caminho</span><span class="sxs-lookup"><span data-stu-id="6a51f-162">Path</span></span>                         | <span data-ttu-id="6a51f-163">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="6a51f-163">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="6a51f-164">1</span><span class="sxs-lookup"><span data-stu-id="6a51f-164">1</span></span>     | <span data-ttu-id="6a51f-165">/IFD/GPS/{UShort = 5}</span><span class="sxs-lookup"><span data-stu-id="6a51f-165">/ifd/gps/{ushort=5}</span></span>          | <span data-ttu-id="6a51f-166">byte</span><span class="sxs-lookup"><span data-stu-id="6a51f-166">byte</span></span>        |
| <span data-ttu-id="6a51f-167">2</span><span class="sxs-lookup"><span data-stu-id="6a51f-167">2</span></span>     | <span data-ttu-id="6a51f-168">/ifd/xmp/exif:GPSAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="6a51f-168">/ifd/xmp/exif:GPSAltitudeRef</span></span> | <span data-ttu-id="6a51f-169">Unicode</span><span class="sxs-lookup"><span data-stu-id="6a51f-169">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="6a51f-170">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="6a51f-170">Remove Paths</span></span>



| <span data-ttu-id="6a51f-171">Ordem</span><span class="sxs-lookup"><span data-stu-id="6a51f-171">Order</span></span> | <span data-ttu-id="6a51f-172">Caminho</span><span class="sxs-lookup"><span data-stu-id="6a51f-172">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="6a51f-173">1</span><span class="sxs-lookup"><span data-stu-id="6a51f-173">1</span></span>     | <span data-ttu-id="6a51f-174">/IFD/GPS/{UShort = 5}</span><span class="sxs-lookup"><span data-stu-id="6a51f-174">/ifd/gps/{ushort=5}</span></span>          |
| <span data-ttu-id="6a51f-175">2</span><span class="sxs-lookup"><span data-stu-id="6a51f-175">2</span></span>     | <span data-ttu-id="6a51f-176">/ifd/xmp/exif:gpsaltituderef</span><span class="sxs-lookup"><span data-stu-id="6a51f-176">/ifd/xmp/exif:gpsaltituderef</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6a51f-177">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a51f-177">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a51f-178">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a51f-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a51f-179">System. GPS. AltitudeRef</span><span class="sxs-lookup"><span data-stu-id="6a51f-179">System.GPS.AltitudeRef</span></span>](../properties/props-system-gps-altituderef.md)
</dt> </dl>

 

 
