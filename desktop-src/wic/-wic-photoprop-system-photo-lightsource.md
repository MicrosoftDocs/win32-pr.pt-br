---
description: A política de metadados de foto para a propriedade System. Photo. claridade.
ms.assetid: 051a49ad-bb4c-459f-ae52-dc359a03a14a
title: Política de metadados de foto System. Photo. Lightexception
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9b3d31f01cdd2bea8d3fabbbc730a41f1fb0da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506155"
---
# <a name="systemphotolightsource-photo-metadata-policy"></a><span data-ttu-id="59b97-103">Política de metadados de foto System. Photo. Lightexception</span><span class="sxs-lookup"><span data-stu-id="59b97-103">System.Photo.LightSource Photo Metadata Policy</span></span>

<span data-ttu-id="59b97-104">A política de metadados de foto para a propriedade [System. Photo. claridade](../properties/props-system-photo-lightsource.md) .</span><span class="sxs-lookup"><span data-stu-id="59b97-104">The photo metadata policy for the [System.Photo.LightSource](../properties/props-system-photo-lightsource.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="59b97-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="59b97-105">PKEY</span></span>

<span data-ttu-id="59b97-106">\_Claridade da foto PKEY \_</span><span class="sxs-lookup"><span data-stu-id="59b97-106">PKEY\_Photo\_LightSource</span></span>

### <a name="containers"></a><span data-ttu-id="59b97-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="59b97-107">Containers</span></span>

<span data-ttu-id="59b97-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="59b97-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="59b97-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="59b97-109">Read-Only</span></span>

<span data-ttu-id="59b97-110">No</span><span class="sxs-lookup"><span data-stu-id="59b97-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="59b97-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="59b97-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="59b97-112">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="59b97-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="59b97-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="59b97-113">Input Type</span></span>

<span data-ttu-id="59b97-114">UShort</span><span class="sxs-lookup"><span data-stu-id="59b97-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="59b97-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="59b97-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="59b97-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="59b97-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="59b97-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="59b97-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="59b97-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="59b97-118">Read Paths</span></span>



| <span data-ttu-id="59b97-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="59b97-119">Order</span></span> | <span data-ttu-id="59b97-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="59b97-120">Path</span></span>                          | <span data-ttu-id="59b97-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="59b97-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="59b97-122">1</span><span class="sxs-lookup"><span data-stu-id="59b97-122">1</span></span>     | <span data-ttu-id="59b97-123">/App1/IFD/EXIF/{UShort = 37384}</span><span class="sxs-lookup"><span data-stu-id="59b97-123">/app1/ifd/exif/{ushort=37384}</span></span> | <span data-ttu-id="59b97-124">ushort</span><span class="sxs-lookup"><span data-stu-id="59b97-124">ushort</span></span>      |
| <span data-ttu-id="59b97-125">2</span><span class="sxs-lookup"><span data-stu-id="59b97-125">2</span></span>     | <span data-ttu-id="59b97-126">/XMP/EXIF: claridade</span><span class="sxs-lookup"><span data-stu-id="59b97-126">/xmp/exif:LightSource</span></span>         | <span data-ttu-id="59b97-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="59b97-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="59b97-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="59b97-128">Write Paths</span></span>



| <span data-ttu-id="59b97-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="59b97-129">Order</span></span> | <span data-ttu-id="59b97-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="59b97-130">Path</span></span>                          | <span data-ttu-id="59b97-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="59b97-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="59b97-132">1</span><span class="sxs-lookup"><span data-stu-id="59b97-132">1</span></span>     | <span data-ttu-id="59b97-133">/App1/IFD/EXIF/{UShort = 37384}</span><span class="sxs-lookup"><span data-stu-id="59b97-133">/app1/ifd/exif/{ushort=37384}</span></span> | <span data-ttu-id="59b97-134">ushort</span><span class="sxs-lookup"><span data-stu-id="59b97-134">ushort</span></span>      |
| <span data-ttu-id="59b97-135">2</span><span class="sxs-lookup"><span data-stu-id="59b97-135">2</span></span>     | <span data-ttu-id="59b97-136">/XMP/EXIF: claridade</span><span class="sxs-lookup"><span data-stu-id="59b97-136">/xmp/exif:LightSource</span></span>         | <span data-ttu-id="59b97-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="59b97-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="59b97-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="59b97-138">Remove Paths</span></span>



| <span data-ttu-id="59b97-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="59b97-139">Order</span></span> | <span data-ttu-id="59b97-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="59b97-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="59b97-141">1</span><span class="sxs-lookup"><span data-stu-id="59b97-141">1</span></span>     | <span data-ttu-id="59b97-142">/App1/IFD/EXIF/{UShort = 37384}</span><span class="sxs-lookup"><span data-stu-id="59b97-142">/app1/ifd/exif/{ushort=37384}</span></span> |
| <span data-ttu-id="59b97-143">2</span><span class="sxs-lookup"><span data-stu-id="59b97-143">2</span></span>     | <span data-ttu-id="59b97-144">/XMP/EXIF: claridade</span><span class="sxs-lookup"><span data-stu-id="59b97-144">/xmp/exif:lightsource</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="59b97-145">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="59b97-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="59b97-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="59b97-146">Read Paths</span></span>



| <span data-ttu-id="59b97-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="59b97-147">Order</span></span> | <span data-ttu-id="59b97-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="59b97-148">Path</span></span>                      | <span data-ttu-id="59b97-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="59b97-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="59b97-150">1</span><span class="sxs-lookup"><span data-stu-id="59b97-150">1</span></span>     | <span data-ttu-id="59b97-151">/IFD/EXIF/{UShort = 37384}</span><span class="sxs-lookup"><span data-stu-id="59b97-151">/ifd/exif/{ushort=37384}</span></span>  | <span data-ttu-id="59b97-152">ushort</span><span class="sxs-lookup"><span data-stu-id="59b97-152">ushort</span></span>      |
| <span data-ttu-id="59b97-153">2</span><span class="sxs-lookup"><span data-stu-id="59b97-153">2</span></span>     | <span data-ttu-id="59b97-154">/IFD/XMP/EXIF: claridade</span><span class="sxs-lookup"><span data-stu-id="59b97-154">/ifd/xmp/exif:LightSource</span></span> | <span data-ttu-id="59b97-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="59b97-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="59b97-156">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="59b97-156">Write Paths</span></span>



| <span data-ttu-id="59b97-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="59b97-157">Order</span></span> | <span data-ttu-id="59b97-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="59b97-158">Path</span></span>                      | <span data-ttu-id="59b97-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="59b97-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="59b97-160">1</span><span class="sxs-lookup"><span data-stu-id="59b97-160">1</span></span>     | <span data-ttu-id="59b97-161">/IFD/EXIF/{UShort = 37384}</span><span class="sxs-lookup"><span data-stu-id="59b97-161">/ifd/exif/{ushort=37384}</span></span>  | <span data-ttu-id="59b97-162">ushort</span><span class="sxs-lookup"><span data-stu-id="59b97-162">ushort</span></span>      |
| <span data-ttu-id="59b97-163">2</span><span class="sxs-lookup"><span data-stu-id="59b97-163">2</span></span>     | <span data-ttu-id="59b97-164">/IFD/XMP/EXIF: claridade</span><span class="sxs-lookup"><span data-stu-id="59b97-164">/ifd/xmp/exif:LightSource</span></span> | <span data-ttu-id="59b97-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="59b97-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="59b97-166">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="59b97-166">Remove Paths</span></span>



| <span data-ttu-id="59b97-167">Ordem</span><span class="sxs-lookup"><span data-stu-id="59b97-167">Order</span></span> | <span data-ttu-id="59b97-168">Caminho</span><span class="sxs-lookup"><span data-stu-id="59b97-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="59b97-169">1</span><span class="sxs-lookup"><span data-stu-id="59b97-169">1</span></span>     | <span data-ttu-id="59b97-170">/IFD/EXIF/{UShort = 37384}</span><span class="sxs-lookup"><span data-stu-id="59b97-170">/ifd/exif/{ushort=37384}</span></span>  |
| <span data-ttu-id="59b97-171">2</span><span class="sxs-lookup"><span data-stu-id="59b97-171">2</span></span>     | <span data-ttu-id="59b97-172">/IFD/XMP/EXIF: claridade</span><span class="sxs-lookup"><span data-stu-id="59b97-172">/ifd/xmp/exif:lightsource</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="59b97-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="59b97-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="59b97-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="59b97-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59b97-175">Sistema. foto. Lightname</span><span class="sxs-lookup"><span data-stu-id="59b97-175">System.Photo.LightSource</span></span>](../properties/props-system-photo-lightsource.md)
</dt> </dl>

 

 
