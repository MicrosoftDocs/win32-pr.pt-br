---
description: A política de metadados de foto para a propriedade System. Photo. TranscodedForSync.
ms.assetid: 1869d845-6264-425a-ab3e-e0a9f942961a
title: Política de metadados de foto System. Photo. TranscodedForSync
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5884ad469fcf7b5dffc8c4ad14f0ee5ff90cd07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829493"
---
# <a name="systemphototranscodedforsync-photo-metadata-policy"></a><span data-ttu-id="a4174-103">Política de metadados de foto System. Photo. TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="a4174-103">System.Photo.TranscodedForSync Photo Metadata Policy</span></span>

<span data-ttu-id="a4174-104">A política de metadados de foto para a propriedade [System. Photo. TranscodedForSync](../properties/props-system-photo-transcodedforsync.md) .</span><span class="sxs-lookup"><span data-stu-id="a4174-104">The photo metadata policy for the [System.Photo.TranscodedForSync](../properties/props-system-photo-transcodedforsync.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a4174-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a4174-105">PKEY</span></span>

<span data-ttu-id="a4174-106">PKEY \_ Photo \_ TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="a4174-106">PKEY\_Photo\_TranscodedForSync</span></span>

### <a name="containers"></a><span data-ttu-id="a4174-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="a4174-107">Containers</span></span>

<span data-ttu-id="a4174-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a4174-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a4174-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4174-109">Read-Only</span></span>

<span data-ttu-id="a4174-110">No</span><span class="sxs-lookup"><span data-stu-id="a4174-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a4174-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="a4174-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a4174-112">BOOL do VT \_</span><span class="sxs-lookup"><span data-stu-id="a4174-112">VT\_BOOL</span></span>

### <a name="input-type"></a><span data-ttu-id="a4174-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="a4174-113">Input Type</span></span>

<span data-ttu-id="a4174-114">Booliano.</span><span class="sxs-lookup"><span data-stu-id="a4174-114">Boolean.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a4174-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="a4174-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a4174-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="a4174-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a4174-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="a4174-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a4174-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="a4174-118">Read Paths</span></span>



| <span data-ttu-id="a4174-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4174-119">Order</span></span> | <span data-ttu-id="a4174-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4174-120">Path</span></span>                                  | <span data-ttu-id="a4174-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a4174-121">Disk Format</span></span>  |
|-------|---------------------------------------|--------------|
| <span data-ttu-id="a4174-122">1</span><span class="sxs-lookup"><span data-stu-id="a4174-122">1</span></span>     | <span data-ttu-id="a4174-123">/App1/IFD/{UShort = 18248}</span><span class="sxs-lookup"><span data-stu-id="a4174-123">/app1/ifd/{ushort=18248}</span></span>              | <span data-ttu-id="a4174-124">bool \_ ushort</span><span class="sxs-lookup"><span data-stu-id="a4174-124">bool\_ushort</span></span> |
| <span data-ttu-id="a4174-125">2</span><span class="sxs-lookup"><span data-stu-id="a4174-125">2</span></span>     | <span data-ttu-id="a4174-126">/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="a4174-126">/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="write-paths"></a><span data-ttu-id="a4174-127">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="a4174-127">Write Paths</span></span>



| <span data-ttu-id="a4174-128">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4174-128">Order</span></span> | <span data-ttu-id="a4174-129">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4174-129">Path</span></span>                                  | <span data-ttu-id="a4174-130">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a4174-130">Disk Format</span></span>  |
|-------|---------------------------------------|--------------|
| <span data-ttu-id="a4174-131">1</span><span class="sxs-lookup"><span data-stu-id="a4174-131">1</span></span>     | <span data-ttu-id="a4174-132">/App1/IFD/{UShort = 18248}</span><span class="sxs-lookup"><span data-stu-id="a4174-132">/app1/ifd/{ushort=18248}</span></span>              | <span data-ttu-id="a4174-133">bool \_ ushort</span><span class="sxs-lookup"><span data-stu-id="a4174-133">bool\_ushort</span></span> |
| <span data-ttu-id="a4174-134">2</span><span class="sxs-lookup"><span data-stu-id="a4174-134">2</span></span>     | <span data-ttu-id="a4174-135">/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="a4174-135">/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="remove-paths"></a><span data-ttu-id="a4174-136">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="a4174-136">Remove Paths</span></span>



| <span data-ttu-id="a4174-137">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4174-137">Order</span></span> | <span data-ttu-id="a4174-138">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4174-138">Path</span></span>                                  |
|-------|---------------------------------------|
| <span data-ttu-id="a4174-139">1</span><span class="sxs-lookup"><span data-stu-id="a4174-139">1</span></span>     | <span data-ttu-id="a4174-140">/App1/IFD/{UShort = 18248}</span><span class="sxs-lookup"><span data-stu-id="a4174-140">/app1/ifd/{ushort=18248}</span></span>              |
| <span data-ttu-id="a4174-141">2</span><span class="sxs-lookup"><span data-stu-id="a4174-141">2</span></span>     | <span data-ttu-id="a4174-142">/xmp/microsoftphoto:transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="a4174-142">/xmp/microsoftphoto:transcodedforsync</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="a4174-143">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="a4174-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a4174-144">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="a4174-144">Read Paths</span></span>



| <span data-ttu-id="a4174-145">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4174-145">Order</span></span> | <span data-ttu-id="a4174-146">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4174-146">Path</span></span>                                      | <span data-ttu-id="a4174-147">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a4174-147">Disk Format</span></span>  |
|-------|-------------------------------------------|--------------|
| <span data-ttu-id="a4174-148">1</span><span class="sxs-lookup"><span data-stu-id="a4174-148">1</span></span>     | <span data-ttu-id="a4174-149">/IFD/{UShort = 18248}</span><span class="sxs-lookup"><span data-stu-id="a4174-149">/ifd/{ushort=18248}</span></span>                       | <span data-ttu-id="a4174-150">bool \_ ushort</span><span class="sxs-lookup"><span data-stu-id="a4174-150">bool\_ushort</span></span> |
| <span data-ttu-id="a4174-151">2</span><span class="sxs-lookup"><span data-stu-id="a4174-151">2</span></span>     | <span data-ttu-id="a4174-152">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="a4174-152">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="write-paths"></a><span data-ttu-id="a4174-153">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="a4174-153">Write Paths</span></span>



| <span data-ttu-id="a4174-154">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4174-154">Order</span></span> | <span data-ttu-id="a4174-155">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4174-155">Path</span></span>                                      | <span data-ttu-id="a4174-156">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a4174-156">Disk Format</span></span>  |
|-------|-------------------------------------------|--------------|
| <span data-ttu-id="a4174-157">1</span><span class="sxs-lookup"><span data-stu-id="a4174-157">1</span></span>     | <span data-ttu-id="a4174-158">/IFD/{UShort = 18248}</span><span class="sxs-lookup"><span data-stu-id="a4174-158">/ifd/{ushort=18248}</span></span>                       | <span data-ttu-id="a4174-159">bool \_ ushort</span><span class="sxs-lookup"><span data-stu-id="a4174-159">bool\_ushort</span></span> |
| <span data-ttu-id="a4174-160">2</span><span class="sxs-lookup"><span data-stu-id="a4174-160">2</span></span>     | <span data-ttu-id="a4174-161">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="a4174-161">/ifd/xmp/MicrosoftPhoto:TranscodedForSync</span></span> |              |



 

### <a name="remove-paths"></a><span data-ttu-id="a4174-162">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="a4174-162">Remove Paths</span></span>



| <span data-ttu-id="a4174-163">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4174-163">Order</span></span> | <span data-ttu-id="a4174-164">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4174-164">Path</span></span>                                      |
|-------|-------------------------------------------|
| <span data-ttu-id="a4174-165">1</span><span class="sxs-lookup"><span data-stu-id="a4174-165">1</span></span>     | <span data-ttu-id="a4174-166">/IFD/{UShort = 18248}</span><span class="sxs-lookup"><span data-stu-id="a4174-166">/ifd/{ushort=18248}</span></span>                       |
| <span data-ttu-id="a4174-167">2</span><span class="sxs-lookup"><span data-stu-id="a4174-167">2</span></span>     | <span data-ttu-id="a4174-168">/ifd/xmp/microsoftphoto:transcodedforsync</span><span class="sxs-lookup"><span data-stu-id="a4174-168">/ifd/xmp/microsoftphoto:transcodedforsync</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a4174-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4174-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4174-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4174-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4174-171">System. Photo. TranscodedForSync</span><span class="sxs-lookup"><span data-stu-id="a4174-171">System.Photo.TranscodedForSync</span></span>](../properties/props-system-photo-transcodedforsync.md)
</dt> </dl>

 

 
