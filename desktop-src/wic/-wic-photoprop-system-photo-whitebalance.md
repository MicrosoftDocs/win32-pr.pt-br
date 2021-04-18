---
description: A política de metadados de foto para a propriedade System. Photo. WhiteBalance.
ms.assetid: 7b3a31e6-a929-41e4-b7f0-c5b3beac2519
title: Política de metadados de foto System. Photo. WhiteBalance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc333cedcd4665ace37033452ec3c7f0336f13e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764402"
---
# <a name="systemphotowhitebalance-photo-metadata-policy"></a><span data-ttu-id="1b4d2-103">Política de metadados de foto System. Photo. WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="1b4d2-103">System.Photo.WhiteBalance Photo Metadata Policy</span></span>

<span data-ttu-id="1b4d2-104">A política de metadados de foto para a propriedade [System. Photo. whitebalance](../properties/props-system-photo-whitebalance.md) .</span><span class="sxs-lookup"><span data-stu-id="1b4d2-104">The photo metadata policy for the [System.Photo.WhiteBalance](../properties/props-system-photo-whitebalance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1b4d2-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="1b4d2-105">PKEY</span></span>

<span data-ttu-id="1b4d2-106">PKEY \_ Photo \_ whitebalance</span><span class="sxs-lookup"><span data-stu-id="1b4d2-106">PKEY\_Photo\_WhiteBalance</span></span>

### <a name="containers"></a><span data-ttu-id="1b4d2-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="1b4d2-107">Containers</span></span>

<span data-ttu-id="1b4d2-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1b4d2-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1b4d2-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b4d2-109">Read-Only</span></span>

<span data-ttu-id="1b4d2-110">No</span><span class="sxs-lookup"><span data-stu-id="1b4d2-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1b4d2-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="1b4d2-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1b4d2-112">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="1b4d2-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="1b4d2-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="1b4d2-113">Input Type</span></span>

<span data-ttu-id="1b4d2-114">UShort</span><span class="sxs-lookup"><span data-stu-id="1b4d2-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1b4d2-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="1b4d2-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="1b4d2-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="1b4d2-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="1b4d2-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="1b4d2-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="1b4d2-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="1b4d2-118">Read Paths</span></span>



| <span data-ttu-id="1b4d2-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="1b4d2-119">Order</span></span> | <span data-ttu-id="1b4d2-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="1b4d2-120">Path</span></span>                          | <span data-ttu-id="1b4d2-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="1b4d2-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="1b4d2-122">1</span><span class="sxs-lookup"><span data-stu-id="1b4d2-122">1</span></span>     | <span data-ttu-id="1b4d2-123">/App1/IFD/EXIF/{UShort = 41987}</span><span class="sxs-lookup"><span data-stu-id="1b4d2-123">/app1/ifd/exif/{ushort=41987}</span></span> | <span data-ttu-id="1b4d2-124">ushort</span><span class="sxs-lookup"><span data-stu-id="1b4d2-124">ushort</span></span>      |
| <span data-ttu-id="1b4d2-125">2</span><span class="sxs-lookup"><span data-stu-id="1b4d2-125">2</span></span>     | <span data-ttu-id="1b4d2-126">/xmp/exif:WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="1b4d2-126">/xmp/exif:WhiteBalance</span></span>        | <span data-ttu-id="1b4d2-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="1b4d2-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="1b4d2-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="1b4d2-128">Write Paths</span></span>



| <span data-ttu-id="1b4d2-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="1b4d2-129">Order</span></span> | <span data-ttu-id="1b4d2-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="1b4d2-130">Path</span></span>                          | <span data-ttu-id="1b4d2-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="1b4d2-131">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="1b4d2-132">1</span><span class="sxs-lookup"><span data-stu-id="1b4d2-132">1</span></span>     | <span data-ttu-id="1b4d2-133">/App1/IFD/EXIF/{UShort = 41987}</span><span class="sxs-lookup"><span data-stu-id="1b4d2-133">/app1/ifd/exif/{ushort=41987}</span></span> | <span data-ttu-id="1b4d2-134">ushort</span><span class="sxs-lookup"><span data-stu-id="1b4d2-134">ushort</span></span>      |
| <span data-ttu-id="1b4d2-135">2</span><span class="sxs-lookup"><span data-stu-id="1b4d2-135">2</span></span>     | <span data-ttu-id="1b4d2-136">/xmp/exif:WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="1b4d2-136">/xmp/exif:WhiteBalance</span></span>        | <span data-ttu-id="1b4d2-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="1b4d2-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="1b4d2-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="1b4d2-138">Remove Paths</span></span>



| <span data-ttu-id="1b4d2-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="1b4d2-139">Order</span></span> | <span data-ttu-id="1b4d2-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="1b4d2-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="1b4d2-141">1</span><span class="sxs-lookup"><span data-stu-id="1b4d2-141">1</span></span>     | <span data-ttu-id="1b4d2-142">/App1/IFD/EXIF/{UShort = 41987}</span><span class="sxs-lookup"><span data-stu-id="1b4d2-142">/app1/ifd/exif/{ushort=41987}</span></span> |
| <span data-ttu-id="1b4d2-143">2</span><span class="sxs-lookup"><span data-stu-id="1b4d2-143">2</span></span>     | <span data-ttu-id="1b4d2-144">/xmp/exif:whitebalance</span><span class="sxs-lookup"><span data-stu-id="1b4d2-144">/xmp/exif:whitebalance</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="1b4d2-145">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="1b4d2-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="1b4d2-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="1b4d2-146">Read Paths</span></span>



| <span data-ttu-id="1b4d2-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="1b4d2-147">Order</span></span> | <span data-ttu-id="1b4d2-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="1b4d2-148">Path</span></span>                       | <span data-ttu-id="1b4d2-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="1b4d2-149">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="1b4d2-150">1</span><span class="sxs-lookup"><span data-stu-id="1b4d2-150">1</span></span>     | <span data-ttu-id="1b4d2-151">/IFD/EXIF/{UShort = 41987}</span><span class="sxs-lookup"><span data-stu-id="1b4d2-151">/ifd/exif/{ushort=41987}</span></span>   | <span data-ttu-id="1b4d2-152">ushort</span><span class="sxs-lookup"><span data-stu-id="1b4d2-152">ushort</span></span>      |
| <span data-ttu-id="1b4d2-153">2</span><span class="sxs-lookup"><span data-stu-id="1b4d2-153">2</span></span>     | <span data-ttu-id="1b4d2-154">/ifd/xmp/exif:WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="1b4d2-154">/ifd/xmp/exif:WhiteBalance</span></span> | <span data-ttu-id="1b4d2-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="1b4d2-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="1b4d2-156">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="1b4d2-156">Write Paths</span></span>



| <span data-ttu-id="1b4d2-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="1b4d2-157">Order</span></span> | <span data-ttu-id="1b4d2-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="1b4d2-158">Path</span></span>                       | <span data-ttu-id="1b4d2-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="1b4d2-159">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="1b4d2-160">1</span><span class="sxs-lookup"><span data-stu-id="1b4d2-160">1</span></span>     | <span data-ttu-id="1b4d2-161">/IFD/EXIF/{UShort = 41987}</span><span class="sxs-lookup"><span data-stu-id="1b4d2-161">/ifd/exif/{ushort=41987}</span></span>   | <span data-ttu-id="1b4d2-162">ushort</span><span class="sxs-lookup"><span data-stu-id="1b4d2-162">ushort</span></span>      |
| <span data-ttu-id="1b4d2-163">2</span><span class="sxs-lookup"><span data-stu-id="1b4d2-163">2</span></span>     | <span data-ttu-id="1b4d2-164">/ifd/xmp/exif:WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="1b4d2-164">/ifd/xmp/exif:WhiteBalance</span></span> | <span data-ttu-id="1b4d2-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="1b4d2-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="1b4d2-166">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="1b4d2-166">Remove Paths</span></span>



| <span data-ttu-id="1b4d2-167">Ordem</span><span class="sxs-lookup"><span data-stu-id="1b4d2-167">Order</span></span> | <span data-ttu-id="1b4d2-168">Caminho</span><span class="sxs-lookup"><span data-stu-id="1b4d2-168">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="1b4d2-169">1</span><span class="sxs-lookup"><span data-stu-id="1b4d2-169">1</span></span>     | <span data-ttu-id="1b4d2-170">/IFD/EXIF/{UShort = 41987}</span><span class="sxs-lookup"><span data-stu-id="1b4d2-170">/ifd/exif/{ushort=41987}</span></span>   |
| <span data-ttu-id="1b4d2-171">2</span><span class="sxs-lookup"><span data-stu-id="1b4d2-171">2</span></span>     | <span data-ttu-id="1b4d2-172">/ifd/xmp/exif:whitebalance</span><span class="sxs-lookup"><span data-stu-id="1b4d2-172">/ifd/xmp/exif:whitebalance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1b4d2-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b4d2-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b4d2-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b4d2-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b4d2-175">System. Photo. WhiteBalance</span><span class="sxs-lookup"><span data-stu-id="1b4d2-175">System.Photo.WhiteBalance</span></span>](../properties/props-system-photo-whitebalance.md)
</dt> </dl>

 

 
