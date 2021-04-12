---
description: A política de metadados de foto para a propriedade System. Photo. DigitalZoom.
ms.assetid: 22a69d3e-4ec3-4652-b4bb-dfcfffc2322b
title: Política de metadados de foto System. Photo. DigitalZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf440e92243eb2102ac6abaa349ea83e58d9a2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297134"
---
# <a name="systemphotodigitalzoom-photo-metadata-policy"></a><span data-ttu-id="07665-103">Política de metadados de foto System. Photo. DigitalZoom</span><span class="sxs-lookup"><span data-stu-id="07665-103">System.Photo.DigitalZoom Photo Metadata Policy</span></span>

<span data-ttu-id="07665-104">A política de metadados de foto para a propriedade [System. Photo. DigitalZoom](../properties/props-system-photo-digitalzoom.md) .</span><span class="sxs-lookup"><span data-stu-id="07665-104">The photo metadata policy for the [System.Photo.DigitalZoom](../properties/props-system-photo-digitalzoom.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="07665-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="07665-105">PKEY</span></span>

<span data-ttu-id="07665-106">PKEY \_ Photo \_ DigitalZoom</span><span class="sxs-lookup"><span data-stu-id="07665-106">PKEY\_Photo\_DigitalZoom</span></span>

### <a name="containers"></a><span data-ttu-id="07665-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="07665-107">Containers</span></span>

<span data-ttu-id="07665-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="07665-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="07665-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07665-109">Read-Only</span></span>

<span data-ttu-id="07665-110">Yes</span><span class="sxs-lookup"><span data-stu-id="07665-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="07665-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="07665-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="07665-112">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="07665-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="07665-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="07665-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="07665-114">Esse valor é gerado em System. Photo. DigitalZoomNumerator e System. Photo. DigitalZoomDenominator.</span><span class="sxs-lookup"><span data-stu-id="07665-114">This value is generated from System.Photo.DigitalZoomNumerator and System.Photo.DigitalZoomDenominator.</span></span> <span data-ttu-id="07665-115">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="07665-115">It cannot be written directly.</span></span> <span data-ttu-id="07665-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="07665-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="07665-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="07665-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="07665-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="07665-118">Read Paths</span></span>



| <span data-ttu-id="07665-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="07665-119">Order</span></span> | <span data-ttu-id="07665-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="07665-120">Path</span></span>                          | <span data-ttu-id="07665-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="07665-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="07665-122">1</span><span class="sxs-lookup"><span data-stu-id="07665-122">1</span></span>     | <span data-ttu-id="07665-123">/App1/IFD/EXIF/{UShort = 41988}</span><span class="sxs-lookup"><span data-stu-id="07665-123">/app1/ifd/exif/{ushort=41988}</span></span> |             |
| <span data-ttu-id="07665-124">2</span><span class="sxs-lookup"><span data-stu-id="07665-124">2</span></span>     | <span data-ttu-id="07665-125">/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="07665-125">/xmp/exif:DigitalZoomRatio</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="07665-126">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="07665-126">Write Paths</span></span>



| <span data-ttu-id="07665-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="07665-127">Order</span></span> | <span data-ttu-id="07665-128">Caminho</span><span class="sxs-lookup"><span data-stu-id="07665-128">Path</span></span>                          | <span data-ttu-id="07665-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="07665-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="07665-130">1</span><span class="sxs-lookup"><span data-stu-id="07665-130">1</span></span>     | <span data-ttu-id="07665-131">/App1/IFD/EXIF/{UShort = 41988}</span><span class="sxs-lookup"><span data-stu-id="07665-131">/app1/ifd/exif/{ushort=41988}</span></span> |             |
| <span data-ttu-id="07665-132">2</span><span class="sxs-lookup"><span data-stu-id="07665-132">2</span></span>     | <span data-ttu-id="07665-133">/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="07665-133">/xmp/exif:DigitalZoomRatio</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="07665-134">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="07665-134">Remove Paths</span></span>



| <span data-ttu-id="07665-135">Ordem</span><span class="sxs-lookup"><span data-stu-id="07665-135">Order</span></span> | <span data-ttu-id="07665-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="07665-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="07665-137">1</span><span class="sxs-lookup"><span data-stu-id="07665-137">1</span></span>     | <span data-ttu-id="07665-138">/App1/IFD/EXIF/{UShort = 41988}</span><span class="sxs-lookup"><span data-stu-id="07665-138">/app1/ifd/exif/{ushort=41988}</span></span> |
| <span data-ttu-id="07665-139">2</span><span class="sxs-lookup"><span data-stu-id="07665-139">2</span></span>     | <span data-ttu-id="07665-140">/xmp/exif:digitalzoomratio</span><span class="sxs-lookup"><span data-stu-id="07665-140">/xmp/exif:digitalzoomratio</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="07665-141">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="07665-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="07665-142">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="07665-142">Read Paths</span></span>



| <span data-ttu-id="07665-143">Ordem</span><span class="sxs-lookup"><span data-stu-id="07665-143">Order</span></span> | <span data-ttu-id="07665-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="07665-144">Path</span></span>                           | <span data-ttu-id="07665-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="07665-145">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="07665-146">1</span><span class="sxs-lookup"><span data-stu-id="07665-146">1</span></span>     | <span data-ttu-id="07665-147">/IFD/EXIF/{UShort = 41988}</span><span class="sxs-lookup"><span data-stu-id="07665-147">/ifd/exif/{ushort=41988}</span></span>       |             |
| <span data-ttu-id="07665-148">2</span><span class="sxs-lookup"><span data-stu-id="07665-148">2</span></span>     | <span data-ttu-id="07665-149">/ifd/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="07665-149">/ifd/xmp/exif:DigitalZoomRatio</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="07665-150">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="07665-150">Write Paths</span></span>



| <span data-ttu-id="07665-151">Ordem</span><span class="sxs-lookup"><span data-stu-id="07665-151">Order</span></span> | <span data-ttu-id="07665-152">Caminho</span><span class="sxs-lookup"><span data-stu-id="07665-152">Path</span></span>                           | <span data-ttu-id="07665-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="07665-153">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="07665-154">1</span><span class="sxs-lookup"><span data-stu-id="07665-154">1</span></span>     | <span data-ttu-id="07665-155">/IFD/EXIF/{UShort = 41988}</span><span class="sxs-lookup"><span data-stu-id="07665-155">/ifd/exif/{ushort=41988}</span></span>       |             |
| <span data-ttu-id="07665-156">2</span><span class="sxs-lookup"><span data-stu-id="07665-156">2</span></span>     | <span data-ttu-id="07665-157">/ifd/xmp/exif:DigitalZoomRatio</span><span class="sxs-lookup"><span data-stu-id="07665-157">/ifd/xmp/exif:DigitalZoomRatio</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="07665-158">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="07665-158">Remove Paths</span></span>



| <span data-ttu-id="07665-159">Ordem</span><span class="sxs-lookup"><span data-stu-id="07665-159">Order</span></span> | <span data-ttu-id="07665-160">Caminho</span><span class="sxs-lookup"><span data-stu-id="07665-160">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="07665-161">1</span><span class="sxs-lookup"><span data-stu-id="07665-161">1</span></span>     | <span data-ttu-id="07665-162">/IFD/EXIF/{UShort = 41988}</span><span class="sxs-lookup"><span data-stu-id="07665-162">/ifd/exif/{ushort=41988}</span></span>       |
| <span data-ttu-id="07665-163">2</span><span class="sxs-lookup"><span data-stu-id="07665-163">2</span></span>     | <span data-ttu-id="07665-164">/ifd/xmp/exif:digitalzoomratio</span><span class="sxs-lookup"><span data-stu-id="07665-164">/ifd/xmp/exif:digitalzoomratio</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="07665-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="07665-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="07665-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="07665-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07665-167">System. Photo. DigitalZoom</span><span class="sxs-lookup"><span data-stu-id="07665-167">System.Photo.DigitalZoom</span></span>](../properties/props-system-photo-digitalzoom.md)
</dt> </dl>

 

 
