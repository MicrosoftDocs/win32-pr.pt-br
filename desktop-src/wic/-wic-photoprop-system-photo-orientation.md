---
description: A política de metadados de foto para a propriedade System. Photo. Orientation.
ms.assetid: 27e6d4f5-39d5-4cb4-88bc-b0d61ccaa2f3
title: Política de metadados de foto System. Photo. Orientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28f4f350cd1a4c24d71ec737b4679aea2f7cab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011537"
---
# <a name="systemphotoorientation-photo-metadata-policy"></a><span data-ttu-id="c6e37-103">Política de metadados de foto System. Photo. Orientation</span><span class="sxs-lookup"><span data-stu-id="c6e37-103">System.Photo.Orientation Photo Metadata Policy</span></span>

<span data-ttu-id="c6e37-104">A política de metadados de foto para a propriedade [System. Photo. Orientation](../properties/props-system-photo-meteringmode.md) .</span><span class="sxs-lookup"><span data-stu-id="c6e37-104">The photo metadata policy for the [System.Photo.Orientation](../properties/props-system-photo-meteringmode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c6e37-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="c6e37-105">PKEY</span></span>

<span data-ttu-id="c6e37-106">PKEY \_ a \_ orientação da foto</span><span class="sxs-lookup"><span data-stu-id="c6e37-106">PKEY\_Photo\_Orientation</span></span>

### <a name="containers"></a><span data-ttu-id="c6e37-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="c6e37-107">Containers</span></span>

<span data-ttu-id="c6e37-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c6e37-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c6e37-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c6e37-109">Read-Only</span></span>

<span data-ttu-id="c6e37-110">No</span><span class="sxs-lookup"><span data-stu-id="c6e37-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c6e37-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="c6e37-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c6e37-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="c6e37-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="c6e37-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="c6e37-113">Input Type</span></span>

<span data-ttu-id="c6e37-114">UShort</span><span class="sxs-lookup"><span data-stu-id="c6e37-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c6e37-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="c6e37-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="c6e37-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="c6e37-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="c6e37-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="c6e37-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="c6e37-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="c6e37-118">Read Paths</span></span>



| <span data-ttu-id="c6e37-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="c6e37-119">Order</span></span> | <span data-ttu-id="c6e37-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="c6e37-120">Path</span></span>                   | <span data-ttu-id="c6e37-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="c6e37-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="c6e37-122">1</span><span class="sxs-lookup"><span data-stu-id="c6e37-122">1</span></span>     | <span data-ttu-id="c6e37-123">/App1/IFD/{UShort = 274}</span><span class="sxs-lookup"><span data-stu-id="c6e37-123">/app1/ifd/{ushort=274}</span></span> | <span data-ttu-id="c6e37-124">ushort</span><span class="sxs-lookup"><span data-stu-id="c6e37-124">ushort</span></span>      |
| <span data-ttu-id="c6e37-125">2</span><span class="sxs-lookup"><span data-stu-id="c6e37-125">2</span></span>     | <span data-ttu-id="c6e37-126">/XMP/TIFF: orientação</span><span class="sxs-lookup"><span data-stu-id="c6e37-126">/xmp/tiff:Orientation</span></span>  | <span data-ttu-id="c6e37-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="c6e37-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c6e37-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="c6e37-128">Write Paths</span></span>



| <span data-ttu-id="c6e37-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="c6e37-129">Order</span></span> | <span data-ttu-id="c6e37-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="c6e37-130">Path</span></span>                   | <span data-ttu-id="c6e37-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="c6e37-131">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="c6e37-132">1</span><span class="sxs-lookup"><span data-stu-id="c6e37-132">1</span></span>     | <span data-ttu-id="c6e37-133">/App1/IFD/{UShort = 274}</span><span class="sxs-lookup"><span data-stu-id="c6e37-133">/app1/ifd/{ushort=274}</span></span> | <span data-ttu-id="c6e37-134">ushort</span><span class="sxs-lookup"><span data-stu-id="c6e37-134">ushort</span></span>      |
| <span data-ttu-id="c6e37-135">2</span><span class="sxs-lookup"><span data-stu-id="c6e37-135">2</span></span>     | <span data-ttu-id="c6e37-136">/XMP/TIFF: orientação</span><span class="sxs-lookup"><span data-stu-id="c6e37-136">/xmp/tiff:Orientation</span></span>  | <span data-ttu-id="c6e37-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="c6e37-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c6e37-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="c6e37-138">Remove Paths</span></span>



| <span data-ttu-id="c6e37-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="c6e37-139">Order</span></span> | <span data-ttu-id="c6e37-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="c6e37-140">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="c6e37-141">1</span><span class="sxs-lookup"><span data-stu-id="c6e37-141">1</span></span>     | <span data-ttu-id="c6e37-142">/App1/IFD/{UShort = 274}</span><span class="sxs-lookup"><span data-stu-id="c6e37-142">/app1/ifd/{ushort=274}</span></span> |
| <span data-ttu-id="c6e37-143">2</span><span class="sxs-lookup"><span data-stu-id="c6e37-143">2</span></span>     | <span data-ttu-id="c6e37-144">/XMP/TIFF: orientação</span><span class="sxs-lookup"><span data-stu-id="c6e37-144">/xmp/tiff:orientation</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="c6e37-145">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="c6e37-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="c6e37-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="c6e37-146">Read Paths</span></span>



| <span data-ttu-id="c6e37-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="c6e37-147">Order</span></span> | <span data-ttu-id="c6e37-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="c6e37-148">Path</span></span>                      | <span data-ttu-id="c6e37-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="c6e37-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="c6e37-150">1</span><span class="sxs-lookup"><span data-stu-id="c6e37-150">1</span></span>     | <span data-ttu-id="c6e37-151">/IFD/{UShort = 274}</span><span class="sxs-lookup"><span data-stu-id="c6e37-151">/ifd/{ushort=274}</span></span>         | <span data-ttu-id="c6e37-152">ushort</span><span class="sxs-lookup"><span data-stu-id="c6e37-152">ushort</span></span>      |
| <span data-ttu-id="c6e37-153">2</span><span class="sxs-lookup"><span data-stu-id="c6e37-153">2</span></span>     | <span data-ttu-id="c6e37-154">/IFD/XMP/TIFF: orientação</span><span class="sxs-lookup"><span data-stu-id="c6e37-154">/ifd/xmp/tiff:Orientation</span></span> | <span data-ttu-id="c6e37-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="c6e37-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="c6e37-156">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="c6e37-156">Write Paths</span></span>



| <span data-ttu-id="c6e37-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="c6e37-157">Order</span></span> | <span data-ttu-id="c6e37-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="c6e37-158">Path</span></span>                      | <span data-ttu-id="c6e37-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="c6e37-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="c6e37-160">1</span><span class="sxs-lookup"><span data-stu-id="c6e37-160">1</span></span>     | <span data-ttu-id="c6e37-161">/IFD/{UShort = 274}</span><span class="sxs-lookup"><span data-stu-id="c6e37-161">/ifd/{ushort=274}</span></span>         | <span data-ttu-id="c6e37-162">ushort</span><span class="sxs-lookup"><span data-stu-id="c6e37-162">ushort</span></span>      |
| <span data-ttu-id="c6e37-163">2</span><span class="sxs-lookup"><span data-stu-id="c6e37-163">2</span></span>     | <span data-ttu-id="c6e37-164">/IFD/XMP/TIFF: orientação</span><span class="sxs-lookup"><span data-stu-id="c6e37-164">/ifd/xmp/tiff:Orientation</span></span> | <span data-ttu-id="c6e37-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="c6e37-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="c6e37-166">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="c6e37-166">Remove Paths</span></span>



| <span data-ttu-id="c6e37-167">Ordem</span><span class="sxs-lookup"><span data-stu-id="c6e37-167">Order</span></span> | <span data-ttu-id="c6e37-168">Caminho</span><span class="sxs-lookup"><span data-stu-id="c6e37-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="c6e37-169">1</span><span class="sxs-lookup"><span data-stu-id="c6e37-169">1</span></span>     | <span data-ttu-id="c6e37-170">/IFD/{UShort = 274}</span><span class="sxs-lookup"><span data-stu-id="c6e37-170">/ifd/{ushort=274}</span></span>         |
| <span data-ttu-id="c6e37-171">2</span><span class="sxs-lookup"><span data-stu-id="c6e37-171">2</span></span>     | <span data-ttu-id="c6e37-172">/IFD/XMP/TIFF: orientação</span><span class="sxs-lookup"><span data-stu-id="c6e37-172">/ifd/xmp/tiff:orientation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c6e37-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6e37-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6e37-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c6e37-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6e37-175">System. Photo. Orientation</span><span class="sxs-lookup"><span data-stu-id="c6e37-175">System.Photo.Orientation</span></span>](../properties/props-system-photo-meteringmode.md)
</dt> </dl>

 

 
