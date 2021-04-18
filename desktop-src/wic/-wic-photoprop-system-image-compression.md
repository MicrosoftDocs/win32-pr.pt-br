---
description: A política de metadados de foto para a propriedade System. Image. Compression.
ms.assetid: 0fada41f-f6f8-43b3-ad65-79785e859c9c
title: Política de metadados de foto System. Image. Compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32fdc55e2a6a962b1a3dfd9057ef25c89d942f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813091"
---
# <a name="systemimagecompression-photo-metadata-policy"></a><span data-ttu-id="3fbdd-103">Política de metadados de foto System. Image. Compression</span><span class="sxs-lookup"><span data-stu-id="3fbdd-103">System.Image.Compression Photo Metadata Policy</span></span>

<span data-ttu-id="3fbdd-104">A política de metadados de foto para a propriedade [System. Image. Compression](../properties/props-system-image-compression.md) .</span><span class="sxs-lookup"><span data-stu-id="3fbdd-104">The photo metadata policy for the [System.Image.Compression](../properties/props-system-image-compression.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="3fbdd-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="3fbdd-105">PKEY</span></span>

<span data-ttu-id="3fbdd-106">\_Compactação de imagem PKEY \_</span><span class="sxs-lookup"><span data-stu-id="3fbdd-106">PKEY\_Image\_Compression</span></span>

### <a name="containers"></a><span data-ttu-id="3fbdd-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="3fbdd-107">Containers</span></span>

<span data-ttu-id="3fbdd-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="3fbdd-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="3fbdd-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3fbdd-109">Read-Only</span></span>

<span data-ttu-id="3fbdd-110">Yes</span><span class="sxs-lookup"><span data-stu-id="3fbdd-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="3fbdd-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="3fbdd-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="3fbdd-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="3fbdd-112">VT\_UI2</span></span>

### <a name="input-type"></a><span data-ttu-id="3fbdd-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="3fbdd-113">Input Type</span></span>

<span data-ttu-id="3fbdd-114">UShort</span><span class="sxs-lookup"><span data-stu-id="3fbdd-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="3fbdd-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="3fbdd-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="3fbdd-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="3fbdd-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="3fbdd-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="3fbdd-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="3fbdd-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="3fbdd-118">Read Paths</span></span>



| <span data-ttu-id="3fbdd-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="3fbdd-119">Order</span></span> | <span data-ttu-id="3fbdd-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="3fbdd-120">Path</span></span>                   | <span data-ttu-id="3fbdd-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="3fbdd-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="3fbdd-122">1</span><span class="sxs-lookup"><span data-stu-id="3fbdd-122">1</span></span>     | <span data-ttu-id="3fbdd-123">/App1/IFD/{UShort = 259}</span><span class="sxs-lookup"><span data-stu-id="3fbdd-123">/app1/ifd/{ushort=259}</span></span> | <span data-ttu-id="3fbdd-124">ushort</span><span class="sxs-lookup"><span data-stu-id="3fbdd-124">ushort</span></span>      |
| <span data-ttu-id="3fbdd-125">2</span><span class="sxs-lookup"><span data-stu-id="3fbdd-125">2</span></span>     | <span data-ttu-id="3fbdd-126">/XMP/TIFF: compactação</span><span class="sxs-lookup"><span data-stu-id="3fbdd-126">/xmp/tiff:Compression</span></span>  | <span data-ttu-id="3fbdd-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="3fbdd-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3fbdd-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="3fbdd-128">Write Paths</span></span>



| <span data-ttu-id="3fbdd-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="3fbdd-129">Order</span></span> | <span data-ttu-id="3fbdd-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="3fbdd-130">Path</span></span>                   | <span data-ttu-id="3fbdd-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="3fbdd-131">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="3fbdd-132">1</span><span class="sxs-lookup"><span data-stu-id="3fbdd-132">1</span></span>     | <span data-ttu-id="3fbdd-133">/App1/IFD/{UShort = 259}</span><span class="sxs-lookup"><span data-stu-id="3fbdd-133">/app1/ifd/{ushort=259}</span></span> | <span data-ttu-id="3fbdd-134">ushort</span><span class="sxs-lookup"><span data-stu-id="3fbdd-134">ushort</span></span>      |
| <span data-ttu-id="3fbdd-135">2</span><span class="sxs-lookup"><span data-stu-id="3fbdd-135">2</span></span>     | <span data-ttu-id="3fbdd-136">/XMP/TIFF: compactação</span><span class="sxs-lookup"><span data-stu-id="3fbdd-136">/xmp/tiff:Compression</span></span>  | <span data-ttu-id="3fbdd-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="3fbdd-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3fbdd-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="3fbdd-138">Remove Paths</span></span>



| <span data-ttu-id="3fbdd-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="3fbdd-139">Order</span></span> | <span data-ttu-id="3fbdd-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="3fbdd-140">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="3fbdd-141">1</span><span class="sxs-lookup"><span data-stu-id="3fbdd-141">1</span></span>     | <span data-ttu-id="3fbdd-142">/App1/IFD/{UShort = 259}</span><span class="sxs-lookup"><span data-stu-id="3fbdd-142">/app1/ifd/{ushort=259}</span></span> |
| <span data-ttu-id="3fbdd-143">2</span><span class="sxs-lookup"><span data-stu-id="3fbdd-143">2</span></span>     | <span data-ttu-id="3fbdd-144">/XMP/TIFF: compactação</span><span class="sxs-lookup"><span data-stu-id="3fbdd-144">/xmp/tiff:compression</span></span>  |



 

### <a name="tiff-policies"></a><span data-ttu-id="3fbdd-145">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="3fbdd-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="3fbdd-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="3fbdd-146">Read Paths</span></span>



| <span data-ttu-id="3fbdd-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="3fbdd-147">Order</span></span> | <span data-ttu-id="3fbdd-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="3fbdd-148">Path</span></span>                      | <span data-ttu-id="3fbdd-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="3fbdd-149">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="3fbdd-150">1</span><span class="sxs-lookup"><span data-stu-id="3fbdd-150">1</span></span>     | <span data-ttu-id="3fbdd-151">/IFD/{UShort = 259}</span><span class="sxs-lookup"><span data-stu-id="3fbdd-151">/ifd/{ushort=259}</span></span>         | <span data-ttu-id="3fbdd-152">ushort</span><span class="sxs-lookup"><span data-stu-id="3fbdd-152">ushort</span></span>      |
| <span data-ttu-id="3fbdd-153">2</span><span class="sxs-lookup"><span data-stu-id="3fbdd-153">2</span></span>     | <span data-ttu-id="3fbdd-154">/IFD/XMP/TIFF: compactação</span><span class="sxs-lookup"><span data-stu-id="3fbdd-154">/ifd/xmp/tiff:Compression</span></span> | <span data-ttu-id="3fbdd-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="3fbdd-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="3fbdd-156">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="3fbdd-156">Write Paths</span></span>



| <span data-ttu-id="3fbdd-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="3fbdd-157">Order</span></span> | <span data-ttu-id="3fbdd-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="3fbdd-158">Path</span></span>                      | <span data-ttu-id="3fbdd-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="3fbdd-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="3fbdd-160">1</span><span class="sxs-lookup"><span data-stu-id="3fbdd-160">1</span></span>     | <span data-ttu-id="3fbdd-161">/IFD/{UShort = 259}</span><span class="sxs-lookup"><span data-stu-id="3fbdd-161">/ifd/{ushort=259}</span></span>         | <span data-ttu-id="3fbdd-162">ushort</span><span class="sxs-lookup"><span data-stu-id="3fbdd-162">ushort</span></span>      |
| <span data-ttu-id="3fbdd-163">2</span><span class="sxs-lookup"><span data-stu-id="3fbdd-163">2</span></span>     | <span data-ttu-id="3fbdd-164">/IFD/XMP/TIFF: compactação</span><span class="sxs-lookup"><span data-stu-id="3fbdd-164">/ifd/xmp/tiff:Compression</span></span> | <span data-ttu-id="3fbdd-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="3fbdd-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="3fbdd-166">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="3fbdd-166">Remove Paths</span></span>



| <span data-ttu-id="3fbdd-167">Ordem</span><span class="sxs-lookup"><span data-stu-id="3fbdd-167">Order</span></span> | <span data-ttu-id="3fbdd-168">Caminho</span><span class="sxs-lookup"><span data-stu-id="3fbdd-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="3fbdd-169">1</span><span class="sxs-lookup"><span data-stu-id="3fbdd-169">1</span></span>     | <span data-ttu-id="3fbdd-170">/IFD/{UShort = 259}</span><span class="sxs-lookup"><span data-stu-id="3fbdd-170">/ifd/{ushort=259}</span></span>         |
| <span data-ttu-id="3fbdd-171">2</span><span class="sxs-lookup"><span data-stu-id="3fbdd-171">2</span></span>     | <span data-ttu-id="3fbdd-172">/IFD/XMP/TIFF: compactação</span><span class="sxs-lookup"><span data-stu-id="3fbdd-172">/ifd/xmp/tiff:compression</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3fbdd-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fbdd-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fbdd-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3fbdd-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fbdd-175">System. Image. Compression</span><span class="sxs-lookup"><span data-stu-id="3fbdd-175">System.Image.Compression</span></span>](../properties/props-system-image-compression.md)
</dt> </dl>

 

 
