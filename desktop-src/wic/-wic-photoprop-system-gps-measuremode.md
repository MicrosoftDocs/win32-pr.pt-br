---
description: A política de metadados de foto para a propriedade System. GPS. Measuremode.
ms.assetid: 911a0d81-bd12-4155-b45a-ae1a18f2dd07
title: Política de metadados de foto System. GPS. Measuremode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a9449ca9a7d1ee5ef213c37562392be2842a09f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921864"
---
# <a name="systemgpsmeasuremode-photo-metadata-policy"></a><span data-ttu-id="4a7b3-103">Política de metadados de foto System. GPS. Measuremode</span><span class="sxs-lookup"><span data-stu-id="4a7b3-103">System.GPS.MeasureMode Photo Metadata Policy</span></span>

<span data-ttu-id="4a7b3-104">A política de metadados de foto para a propriedade [System. GPS. measuremode](../properties/props-system-gps-measuremode.md) .</span><span class="sxs-lookup"><span data-stu-id="4a7b3-104">The photo metadata policy for the [System.GPS.MeasureMode](../properties/props-system-gps-measuremode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="4a7b3-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="4a7b3-105">PKEY</span></span>

<span data-ttu-id="4a7b3-106">PKEY \_ de \_ medida de GPS</span><span class="sxs-lookup"><span data-stu-id="4a7b3-106">PKEY\_GPS\_MeasureMode</span></span>

### <a name="containers"></a><span data-ttu-id="4a7b3-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="4a7b3-107">Containers</span></span>

<span data-ttu-id="4a7b3-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="4a7b3-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="4a7b3-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4a7b3-109">Read-Only</span></span>

<span data-ttu-id="4a7b3-110">Não</span><span class="sxs-lookup"><span data-stu-id="4a7b3-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="4a7b3-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="4a7b3-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="4a7b3-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="4a7b3-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="4a7b3-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="4a7b3-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="4a7b3-114">VT \_ LPWSTR é preferível, mas VT \_ LPSTR também é aceito.</span><span class="sxs-lookup"><span data-stu-id="4a7b3-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="4a7b3-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="4a7b3-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="4a7b3-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="4a7b3-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="4a7b3-117">Políticas JPEG</span><span class="sxs-lookup"><span data-stu-id="4a7b3-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="4a7b3-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="4a7b3-118">Read Paths</span></span>



| <span data-ttu-id="4a7b3-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="4a7b3-119">Order</span></span> | <span data-ttu-id="4a7b3-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="4a7b3-120">Path</span></span>                      | <span data-ttu-id="4a7b3-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4a7b3-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="4a7b3-122">1</span><span class="sxs-lookup"><span data-stu-id="4a7b3-122">1</span></span>     | <span data-ttu-id="4a7b3-123">/App1/IFD/GPS/{UShort = 10}</span><span class="sxs-lookup"><span data-stu-id="4a7b3-123">/app1/ifd/gps/{ushort=10}</span></span> | <span data-ttu-id="4a7b3-124">ascii</span><span class="sxs-lookup"><span data-stu-id="4a7b3-124">ascii</span></span>       |
| <span data-ttu-id="4a7b3-125">2</span><span class="sxs-lookup"><span data-stu-id="4a7b3-125">2</span></span>     | <span data-ttu-id="4a7b3-126">/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="4a7b3-126">/xmp/exif:GPSMeasureMode</span></span>  | <span data-ttu-id="4a7b3-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="4a7b3-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="4a7b3-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="4a7b3-128">Write Paths</span></span>



| <span data-ttu-id="4a7b3-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="4a7b3-129">Order</span></span> | <span data-ttu-id="4a7b3-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="4a7b3-130">Path</span></span>                      | <span data-ttu-id="4a7b3-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4a7b3-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="4a7b3-132">1</span><span class="sxs-lookup"><span data-stu-id="4a7b3-132">1</span></span>     | <span data-ttu-id="4a7b3-133">/App1/IFD/GPS/{UShort = 10}</span><span class="sxs-lookup"><span data-stu-id="4a7b3-133">/app1/ifd/gps/{ushort=10}</span></span> | <span data-ttu-id="4a7b3-134">ascii</span><span class="sxs-lookup"><span data-stu-id="4a7b3-134">ascii</span></span>       |
| <span data-ttu-id="4a7b3-135">2</span><span class="sxs-lookup"><span data-stu-id="4a7b3-135">2</span></span>     | <span data-ttu-id="4a7b3-136">/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="4a7b3-136">/xmp/exif:GPSMeasureMode</span></span>  | <span data-ttu-id="4a7b3-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="4a7b3-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="4a7b3-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="4a7b3-138">Remove Paths</span></span>



| <span data-ttu-id="4a7b3-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="4a7b3-139">Order</span></span> | <span data-ttu-id="4a7b3-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="4a7b3-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="4a7b3-141">1</span><span class="sxs-lookup"><span data-stu-id="4a7b3-141">1</span></span>     | <span data-ttu-id="4a7b3-142">/App1/IFD/GPS/{UShort = 10}</span><span class="sxs-lookup"><span data-stu-id="4a7b3-142">/app1/ifd/gps/{ushort=10}</span></span> |
| <span data-ttu-id="4a7b3-143">2</span><span class="sxs-lookup"><span data-stu-id="4a7b3-143">2</span></span>     | <span data-ttu-id="4a7b3-144">/xmp/exif:gpsmeasuremode</span><span class="sxs-lookup"><span data-stu-id="4a7b3-144">/xmp/exif:gpsmeasuremode</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="4a7b3-145">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="4a7b3-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="4a7b3-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="4a7b3-146">Read Paths</span></span>



| <span data-ttu-id="4a7b3-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="4a7b3-147">Order</span></span> | <span data-ttu-id="4a7b3-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="4a7b3-148">Path</span></span>                         | <span data-ttu-id="4a7b3-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4a7b3-149">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="4a7b3-150">1</span><span class="sxs-lookup"><span data-stu-id="4a7b3-150">1</span></span>     | <span data-ttu-id="4a7b3-151">/IFD/GPS/{UShort = 10}</span><span class="sxs-lookup"><span data-stu-id="4a7b3-151">/ifd/gps/{ushort=10}</span></span>         | <span data-ttu-id="4a7b3-152">ascii</span><span class="sxs-lookup"><span data-stu-id="4a7b3-152">ascii</span></span>       |
| <span data-ttu-id="4a7b3-153">2</span><span class="sxs-lookup"><span data-stu-id="4a7b3-153">2</span></span>     | <span data-ttu-id="4a7b3-154">/ifd/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="4a7b3-154">/ifd/xmp/exif:GPSMeasureMode</span></span> | <span data-ttu-id="4a7b3-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="4a7b3-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="4a7b3-156">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="4a7b3-156">Write Paths</span></span>



| <span data-ttu-id="4a7b3-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="4a7b3-157">Order</span></span> | <span data-ttu-id="4a7b3-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="4a7b3-158">Path</span></span>                         | <span data-ttu-id="4a7b3-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="4a7b3-159">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="4a7b3-160">1</span><span class="sxs-lookup"><span data-stu-id="4a7b3-160">1</span></span>     | <span data-ttu-id="4a7b3-161">/IFD/GPS/{UShort = 10}</span><span class="sxs-lookup"><span data-stu-id="4a7b3-161">/ifd/gps/{ushort=10}</span></span>         | <span data-ttu-id="4a7b3-162">ascii</span><span class="sxs-lookup"><span data-stu-id="4a7b3-162">ascii</span></span>       |
| <span data-ttu-id="4a7b3-163">2</span><span class="sxs-lookup"><span data-stu-id="4a7b3-163">2</span></span>     | <span data-ttu-id="4a7b3-164">/ifd/xmp/exif:GPSMeasureMode</span><span class="sxs-lookup"><span data-stu-id="4a7b3-164">/ifd/xmp/exif:GPSMeasureMode</span></span> | <span data-ttu-id="4a7b3-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="4a7b3-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="4a7b3-166">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="4a7b3-166">Remove Paths</span></span>



| <span data-ttu-id="4a7b3-167">Ordem</span><span class="sxs-lookup"><span data-stu-id="4a7b3-167">Order</span></span> | <span data-ttu-id="4a7b3-168">Caminho</span><span class="sxs-lookup"><span data-stu-id="4a7b3-168">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="4a7b3-169">1</span><span class="sxs-lookup"><span data-stu-id="4a7b3-169">1</span></span>     | <span data-ttu-id="4a7b3-170">/IFD/GPS/{UShort = 10}</span><span class="sxs-lookup"><span data-stu-id="4a7b3-170">/ifd/gps/{ushort=10}</span></span>         |
| <span data-ttu-id="4a7b3-171">2</span><span class="sxs-lookup"><span data-stu-id="4a7b3-171">2</span></span>     | <span data-ttu-id="4a7b3-172">/ifd/xmp/exif:gpsmeasuremode</span><span class="sxs-lookup"><span data-stu-id="4a7b3-172">/ifd/xmp/exif:gpsmeasuremode</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4a7b3-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a7b3-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a7b3-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a7b3-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a7b3-175">System. GPS. Measuremode</span><span class="sxs-lookup"><span data-stu-id="4a7b3-175">System.GPS.MeasureMode</span></span>](../properties/props-system-gps-measuremode.md)
</dt> </dl>

 

 
