---
description: A política de metadados de foto para a propriedade System. Comment.
ms.assetid: 02a6ac18-ad69-4880-a267-8330d648c0d9
title: Política de metadados de foto System. Comment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9d7526e05a72b073ac32bd8286a621b33ee62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297368"
---
# <a name="systemcomment-photo-metadata-policy"></a><span data-ttu-id="94f2d-103">Política de metadados de foto System. Comment</span><span class="sxs-lookup"><span data-stu-id="94f2d-103">System.Comment Photo Metadata Policy</span></span>

<span data-ttu-id="94f2d-104">A política de metadados de foto para a propriedade [System. Comment](../properties/props-system-comment.md) .</span><span class="sxs-lookup"><span data-stu-id="94f2d-104">The photo metadata policy for the [System.Comment](../properties/props-system-comment.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="94f2d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="94f2d-105">PKEY</span></span>

<span data-ttu-id="94f2d-106">Comentário de PKEY \_</span><span class="sxs-lookup"><span data-stu-id="94f2d-106">PKEY\_Comment</span></span>

### <a name="containers"></a><span data-ttu-id="94f2d-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="94f2d-107">Containers</span></span>

<span data-ttu-id="94f2d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="94f2d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="94f2d-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="94f2d-109">Read-Only</span></span>

<span data-ttu-id="94f2d-110">No</span><span class="sxs-lookup"><span data-stu-id="94f2d-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="94f2d-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="94f2d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="94f2d-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="94f2d-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="94f2d-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="94f2d-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="94f2d-114">VT \_ LPWSTR ou VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="94f2d-114">VT\_LPWSTR or VT\_LPSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="94f2d-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="94f2d-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="94f2d-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="94f2d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="94f2d-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="94f2d-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="94f2d-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="94f2d-118">Read Paths</span></span>



| <span data-ttu-id="94f2d-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="94f2d-119">Order</span></span> | <span data-ttu-id="94f2d-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="94f2d-120">Path</span></span>                                | <span data-ttu-id="94f2d-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="94f2d-121">Disk Format</span></span>    |
|-------|-------------------------------------|----------------|
| <span data-ttu-id="94f2d-122">1</span><span class="sxs-lookup"><span data-stu-id="94f2d-122">1</span></span>     | <span data-ttu-id="94f2d-123">/App1/IFD/{UShort = 40092}</span><span class="sxs-lookup"><span data-stu-id="94f2d-123">/app1/ifd/{ushort=40092}</span></span>            | <span data-ttu-id="94f2d-124">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="94f2d-124">unicode\_bytes</span></span> |
| <span data-ttu-id="94f2d-125">2</span><span class="sxs-lookup"><span data-stu-id="94f2d-125">2</span></span>     | <span data-ttu-id="94f2d-126">/App1/IFD/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="94f2d-126">/app1/ifd/{ushort=37510}</span></span>            | <span data-ttu-id="94f2d-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="94f2d-127">unicode</span></span>        |
| <span data-ttu-id="94f2d-128">3</span><span class="sxs-lookup"><span data-stu-id="94f2d-128">3</span></span>     | <span data-ttu-id="94f2d-129">/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="94f2d-129">/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="94f2d-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="94f2d-130">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="94f2d-131">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="94f2d-131">Write Paths</span></span>



| <span data-ttu-id="94f2d-132">Ordem</span><span class="sxs-lookup"><span data-stu-id="94f2d-132">Order</span></span> | <span data-ttu-id="94f2d-133">Caminho</span><span class="sxs-lookup"><span data-stu-id="94f2d-133">Path</span></span>                     | <span data-ttu-id="94f2d-134">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="94f2d-134">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="94f2d-135">1</span><span class="sxs-lookup"><span data-stu-id="94f2d-135">1</span></span>     | <span data-ttu-id="94f2d-136">/App1/IFD/{UShort = 40092}</span><span class="sxs-lookup"><span data-stu-id="94f2d-136">/app1/ifd/{ushort=40092}</span></span> | <span data-ttu-id="94f2d-137">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="94f2d-137">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="94f2d-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="94f2d-138">Remove Paths</span></span>



| <span data-ttu-id="94f2d-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="94f2d-139">Order</span></span> | <span data-ttu-id="94f2d-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="94f2d-140">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="94f2d-141">1</span><span class="sxs-lookup"><span data-stu-id="94f2d-141">1</span></span>     | <span data-ttu-id="94f2d-142">/App1/IFD/{UShort = 40092}</span><span class="sxs-lookup"><span data-stu-id="94f2d-142">/app1/ifd/{ushort=40092}</span></span>      |
| <span data-ttu-id="94f2d-143">2</span><span class="sxs-lookup"><span data-stu-id="94f2d-143">2</span></span>     | <span data-ttu-id="94f2d-144">/App1/IFD/EXIF/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="94f2d-144">/app1/ifd/exif/{ushort=37510}</span></span> |
| <span data-ttu-id="94f2d-145">3</span><span class="sxs-lookup"><span data-stu-id="94f2d-145">3</span></span>     | <span data-ttu-id="94f2d-146">/XMP/EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="94f2d-146">/xmp/exif:UserComment</span></span>         |



 

### <a name="tiff-policy"></a><span data-ttu-id="94f2d-147">Política TIFF</span><span class="sxs-lookup"><span data-stu-id="94f2d-147">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="94f2d-148">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="94f2d-148">Read Paths</span></span>



| <span data-ttu-id="94f2d-149">Ordem</span><span class="sxs-lookup"><span data-stu-id="94f2d-149">Order</span></span> | <span data-ttu-id="94f2d-150">Caminho</span><span class="sxs-lookup"><span data-stu-id="94f2d-150">Path</span></span>                                    | <span data-ttu-id="94f2d-151">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="94f2d-151">Disk Format</span></span>    |
|-------|-----------------------------------------|----------------|
| <span data-ttu-id="94f2d-152">1</span><span class="sxs-lookup"><span data-stu-id="94f2d-152">1</span></span>     | <span data-ttu-id="94f2d-153">/IFD/{UShort = 40092}</span><span class="sxs-lookup"><span data-stu-id="94f2d-153">/ifd/{ushort=40092}</span></span>                     | <span data-ttu-id="94f2d-154">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="94f2d-154">unicode\_bytes</span></span> |
| <span data-ttu-id="94f2d-155">2</span><span class="sxs-lookup"><span data-stu-id="94f2d-155">2</span></span>     | <span data-ttu-id="94f2d-156">/IFD/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="94f2d-156">/ifd/{ushort=37510}</span></span>                     | <span data-ttu-id="94f2d-157">Unicode</span><span class="sxs-lookup"><span data-stu-id="94f2d-157">unicode</span></span>        |
| <span data-ttu-id="94f2d-158">3</span><span class="sxs-lookup"><span data-stu-id="94f2d-158">3</span></span>     | <span data-ttu-id="94f2d-159">/IFD/XMP/ <xmpalt> EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="94f2d-159">/ifd/xmp/<xmpalt>exif:UserComment</span></span> | <span data-ttu-id="94f2d-160">Unicode</span><span class="sxs-lookup"><span data-stu-id="94f2d-160">unicode</span></span>        |



 

### <a name="write-paths"></a><span data-ttu-id="94f2d-161">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="94f2d-161">Write Paths</span></span>



| <span data-ttu-id="94f2d-162">Ordem</span><span class="sxs-lookup"><span data-stu-id="94f2d-162">Order</span></span> | <span data-ttu-id="94f2d-163">Caminho</span><span class="sxs-lookup"><span data-stu-id="94f2d-163">Path</span></span>                | <span data-ttu-id="94f2d-164">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="94f2d-164">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="94f2d-165">1</span><span class="sxs-lookup"><span data-stu-id="94f2d-165">1</span></span>     | <span data-ttu-id="94f2d-166">/IFD/{UShort = 40092}</span><span class="sxs-lookup"><span data-stu-id="94f2d-166">/ifd/{ushort=40092}</span></span> | <span data-ttu-id="94f2d-167">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="94f2d-167">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="94f2d-168">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="94f2d-168">Remove Paths</span></span>



| <span data-ttu-id="94f2d-169">Ordem</span><span class="sxs-lookup"><span data-stu-id="94f2d-169">Order</span></span> | <span data-ttu-id="94f2d-170">Caminho</span><span class="sxs-lookup"><span data-stu-id="94f2d-170">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="94f2d-171">1</span><span class="sxs-lookup"><span data-stu-id="94f2d-171">1</span></span>     | <span data-ttu-id="94f2d-172">/IFD/{UShort = 40092}</span><span class="sxs-lookup"><span data-stu-id="94f2d-172">/ifd/{ushort=40092}</span></span>       |
| <span data-ttu-id="94f2d-173">2</span><span class="sxs-lookup"><span data-stu-id="94f2d-173">2</span></span>     | <span data-ttu-id="94f2d-174">/IFD/{UShort = 37510}</span><span class="sxs-lookup"><span data-stu-id="94f2d-174">/ifd/{ushort=37510}</span></span>       |
| <span data-ttu-id="94f2d-175">3</span><span class="sxs-lookup"><span data-stu-id="94f2d-175">3</span></span>     | <span data-ttu-id="94f2d-176">/IFD/XMP/EXIF: UserComment</span><span class="sxs-lookup"><span data-stu-id="94f2d-176">/ifd/xmp/exif:UserComment</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="94f2d-177">Comentários</span><span class="sxs-lookup"><span data-stu-id="94f2d-177">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="94f2d-178">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94f2d-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94f2d-179">Sistema. Comment</span><span class="sxs-lookup"><span data-stu-id="94f2d-179">System.Comment</span></span>](../properties/props-system-comment.md)
</dt> </dl>

 

 
