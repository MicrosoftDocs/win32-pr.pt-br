---
description: A política de metadados de foto para a propriedade System. Photo. CameraModel.
ms.assetid: ff85e6ee-dc75-45bc-a406-2290b012c22d
title: Política de metadados de foto System. Photo. CameraModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf9cbb2906f15d02e8d72219862c607d0f515a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836882"
---
# <a name="systemphotocameramodel-photo-metadata-policy"></a><span data-ttu-id="7d22b-103">Política de metadados de foto System. Photo. CameraModel</span><span class="sxs-lookup"><span data-stu-id="7d22b-103">System.Photo.CameraModel Photo Metadata Policy</span></span>

<span data-ttu-id="7d22b-104">A política de metadados de foto para a propriedade [System. Photo. CameraModel](../properties/props-system-photo-cameramodel.md) .</span><span class="sxs-lookup"><span data-stu-id="7d22b-104">The photo metadata policy for the [System.Photo.CameraModel](../properties/props-system-photo-cameramodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="7d22b-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="7d22b-105">PKEY</span></span>

<span data-ttu-id="7d22b-106">PKEY \_ Photo \_ CameraModel</span><span class="sxs-lookup"><span data-stu-id="7d22b-106">PKEY\_Photo\_CameraModel</span></span>

### <a name="containers"></a><span data-ttu-id="7d22b-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="7d22b-107">Containers</span></span>

<span data-ttu-id="7d22b-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7d22b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="7d22b-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d22b-109">Read-Only</span></span>

<span data-ttu-id="7d22b-110">No</span><span class="sxs-lookup"><span data-stu-id="7d22b-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="7d22b-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="7d22b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="7d22b-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="7d22b-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="7d22b-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="7d22b-113">Input Type</span></span>

<span data-ttu-id="7d22b-114">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7d22b-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="7d22b-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="7d22b-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="7d22b-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="7d22b-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="7d22b-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="7d22b-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="7d22b-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="7d22b-118">Read Paths</span></span>



| <span data-ttu-id="7d22b-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="7d22b-119">Order</span></span> | <span data-ttu-id="7d22b-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="7d22b-120">Path</span></span>                   | <span data-ttu-id="7d22b-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7d22b-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="7d22b-122">1</span><span class="sxs-lookup"><span data-stu-id="7d22b-122">1</span></span>     | <span data-ttu-id="7d22b-123">/App1/IFD/{UShort = 272}</span><span class="sxs-lookup"><span data-stu-id="7d22b-123">/app1/ifd/{ushort=272}</span></span> | <span data-ttu-id="7d22b-124">ascii</span><span class="sxs-lookup"><span data-stu-id="7d22b-124">ascii</span></span>       |
| <span data-ttu-id="7d22b-125">2</span><span class="sxs-lookup"><span data-stu-id="7d22b-125">2</span></span>     | <span data-ttu-id="7d22b-126">/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="7d22b-126">/xmp/tiff:Model</span></span>        | <span data-ttu-id="7d22b-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="7d22b-127">unicode</span></span>     |
| <span data-ttu-id="7d22b-128">3</span><span class="sxs-lookup"><span data-stu-id="7d22b-128">3</span></span>     | <span data-ttu-id="7d22b-129">/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="7d22b-129">/xmp/tiff:model</span></span>        | <span data-ttu-id="7d22b-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="7d22b-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="7d22b-131">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="7d22b-131">Write Paths</span></span>



| <span data-ttu-id="7d22b-132">Ordem</span><span class="sxs-lookup"><span data-stu-id="7d22b-132">Order</span></span> | <span data-ttu-id="7d22b-133">Caminho</span><span class="sxs-lookup"><span data-stu-id="7d22b-133">Path</span></span>                   | <span data-ttu-id="7d22b-134">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7d22b-134">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="7d22b-135">1</span><span class="sxs-lookup"><span data-stu-id="7d22b-135">1</span></span>     | <span data-ttu-id="7d22b-136">/App1/IFD/{UShort = 272}</span><span class="sxs-lookup"><span data-stu-id="7d22b-136">/app1/ifd/{ushort=272}</span></span> | <span data-ttu-id="7d22b-137">ascii</span><span class="sxs-lookup"><span data-stu-id="7d22b-137">ascii</span></span>       |
| <span data-ttu-id="7d22b-138">2</span><span class="sxs-lookup"><span data-stu-id="7d22b-138">2</span></span>     | <span data-ttu-id="7d22b-139">/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="7d22b-139">/xmp/tiff:Model</span></span>        | <span data-ttu-id="7d22b-140">Unicode</span><span class="sxs-lookup"><span data-stu-id="7d22b-140">unicode</span></span>     |
| <span data-ttu-id="7d22b-141">3</span><span class="sxs-lookup"><span data-stu-id="7d22b-141">3</span></span>     | <span data-ttu-id="7d22b-142">/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="7d22b-142">/xmp/tiff:model</span></span>        | <span data-ttu-id="7d22b-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="7d22b-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="7d22b-144">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="7d22b-144">Remove Paths</span></span>



| <span data-ttu-id="7d22b-145">Ordem</span><span class="sxs-lookup"><span data-stu-id="7d22b-145">Order</span></span> | <span data-ttu-id="7d22b-146">Caminho</span><span class="sxs-lookup"><span data-stu-id="7d22b-146">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="7d22b-147">1</span><span class="sxs-lookup"><span data-stu-id="7d22b-147">1</span></span>     | <span data-ttu-id="7d22b-148">/App1/IFD/{UShort = 272}</span><span class="sxs-lookup"><span data-stu-id="7d22b-148">/app1/ifd/{ushort=272}</span></span> |
| <span data-ttu-id="7d22b-149">2</span><span class="sxs-lookup"><span data-stu-id="7d22b-149">2</span></span>     | <span data-ttu-id="7d22b-150">/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="7d22b-150">/xmp/tiff:Model</span></span>        |
| <span data-ttu-id="7d22b-151">3</span><span class="sxs-lookup"><span data-stu-id="7d22b-151">3</span></span>     | <span data-ttu-id="7d22b-152">/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="7d22b-152">/xmp/tiff:model</span></span>        |



 

### <a name="tiff-policy"></a><span data-ttu-id="7d22b-153">Política TIFF</span><span class="sxs-lookup"><span data-stu-id="7d22b-153">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="7d22b-154">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="7d22b-154">Read Paths</span></span>



| <span data-ttu-id="7d22b-155">Ordem</span><span class="sxs-lookup"><span data-stu-id="7d22b-155">Order</span></span> | <span data-ttu-id="7d22b-156">Caminho</span><span class="sxs-lookup"><span data-stu-id="7d22b-156">Path</span></span>                | <span data-ttu-id="7d22b-157">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7d22b-157">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="7d22b-158">1</span><span class="sxs-lookup"><span data-stu-id="7d22b-158">1</span></span>     | <span data-ttu-id="7d22b-159">/IFD/{UShort = 272}</span><span class="sxs-lookup"><span data-stu-id="7d22b-159">/ifd/{ushort=272}</span></span>   | <span data-ttu-id="7d22b-160">ascii</span><span class="sxs-lookup"><span data-stu-id="7d22b-160">ascii</span></span>       |
| <span data-ttu-id="7d22b-161">2</span><span class="sxs-lookup"><span data-stu-id="7d22b-161">2</span></span>     | <span data-ttu-id="7d22b-162">/IFD/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="7d22b-162">/ifd/xmp/tiff:Model</span></span> | <span data-ttu-id="7d22b-163">Unicode</span><span class="sxs-lookup"><span data-stu-id="7d22b-163">unicode</span></span>     |
| <span data-ttu-id="7d22b-164">3</span><span class="sxs-lookup"><span data-stu-id="7d22b-164">3</span></span>     | <span data-ttu-id="7d22b-165">/IFD/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="7d22b-165">/ifd/xmp/tiff:model</span></span> | <span data-ttu-id="7d22b-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="7d22b-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="7d22b-167">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="7d22b-167">Write Paths</span></span>



| <span data-ttu-id="7d22b-168">Ordem</span><span class="sxs-lookup"><span data-stu-id="7d22b-168">Order</span></span> | <span data-ttu-id="7d22b-169">Caminho</span><span class="sxs-lookup"><span data-stu-id="7d22b-169">Path</span></span>                | <span data-ttu-id="7d22b-170">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7d22b-170">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="7d22b-171">1</span><span class="sxs-lookup"><span data-stu-id="7d22b-171">1</span></span>     | <span data-ttu-id="7d22b-172">/IFD/{UShort = 272}</span><span class="sxs-lookup"><span data-stu-id="7d22b-172">/ifd/{ushort=272}</span></span>   | <span data-ttu-id="7d22b-173">ascii</span><span class="sxs-lookup"><span data-stu-id="7d22b-173">ascii</span></span>       |
| <span data-ttu-id="7d22b-174">2</span><span class="sxs-lookup"><span data-stu-id="7d22b-174">2</span></span>     | <span data-ttu-id="7d22b-175">/IFD/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="7d22b-175">/ifd/xmp/tiff:Model</span></span> | <span data-ttu-id="7d22b-176">Unicode</span><span class="sxs-lookup"><span data-stu-id="7d22b-176">unicode</span></span>     |
| <span data-ttu-id="7d22b-177">3</span><span class="sxs-lookup"><span data-stu-id="7d22b-177">3</span></span>     | <span data-ttu-id="7d22b-178">/IFD/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="7d22b-178">/ifd/xmp/tiff:model</span></span> | <span data-ttu-id="7d22b-179">Unicode</span><span class="sxs-lookup"><span data-stu-id="7d22b-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="7d22b-180">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="7d22b-180">Remove Paths</span></span>



| <span data-ttu-id="7d22b-181">Ordem</span><span class="sxs-lookup"><span data-stu-id="7d22b-181">Order</span></span> | <span data-ttu-id="7d22b-182">Caminho</span><span class="sxs-lookup"><span data-stu-id="7d22b-182">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="7d22b-183">1</span><span class="sxs-lookup"><span data-stu-id="7d22b-183">1</span></span>     | <span data-ttu-id="7d22b-184">/IFD/{UShort = 272}</span><span class="sxs-lookup"><span data-stu-id="7d22b-184">/ifd/{ushort=272}</span></span>   |
| <span data-ttu-id="7d22b-185">2</span><span class="sxs-lookup"><span data-stu-id="7d22b-185">2</span></span>     | <span data-ttu-id="7d22b-186">/IFD/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="7d22b-186">/ifd/xmp/tiff:Model</span></span> |
| <span data-ttu-id="7d22b-187">3</span><span class="sxs-lookup"><span data-stu-id="7d22b-187">3</span></span>     | <span data-ttu-id="7d22b-188">/IFD/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="7d22b-188">/ifd/xmp/tiff:model</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7d22b-189">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d22b-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d22b-190">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d22b-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d22b-191">System. Photo. CameraModel</span><span class="sxs-lookup"><span data-stu-id="7d22b-191">System.Photo.CameraModel</span></span>](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
