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
# <a name="systemphotocameramodel-photo-metadata-policy"></a><span data-ttu-id="d4e5e-103">Política de metadados de foto System. Photo. CameraModel</span><span class="sxs-lookup"><span data-stu-id="d4e5e-103">System.Photo.CameraModel Photo Metadata Policy</span></span>

<span data-ttu-id="d4e5e-104">A política de metadados de foto para a propriedade [System. Photo. CameraModel](../properties/props-system-photo-cameramodel.md) .</span><span class="sxs-lookup"><span data-stu-id="d4e5e-104">The photo metadata policy for the [System.Photo.CameraModel](../properties/props-system-photo-cameramodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d4e5e-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="d4e5e-105">PKEY</span></span>

<span data-ttu-id="d4e5e-106">PKEY \_ Photo \_ CameraModel</span><span class="sxs-lookup"><span data-stu-id="d4e5e-106">PKEY\_Photo\_CameraModel</span></span>

### <a name="containers"></a><span data-ttu-id="d4e5e-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="d4e5e-107">Containers</span></span>

<span data-ttu-id="d4e5e-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d4e5e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d4e5e-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4e5e-109">Read-Only</span></span>

<span data-ttu-id="d4e5e-110">Não</span><span class="sxs-lookup"><span data-stu-id="d4e5e-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d4e5e-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="d4e5e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d4e5e-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="d4e5e-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="d4e5e-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="d4e5e-113">Input Type</span></span>

<span data-ttu-id="d4e5e-114">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d4e5e-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d4e5e-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="d4e5e-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="d4e5e-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="d4e5e-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="d4e5e-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="d4e5e-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d4e5e-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="d4e5e-118">Read Paths</span></span>



| <span data-ttu-id="d4e5e-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="d4e5e-119">Order</span></span> | <span data-ttu-id="d4e5e-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="d4e5e-120">Path</span></span>                   | <span data-ttu-id="d4e5e-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d4e5e-121">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="d4e5e-122">1</span><span class="sxs-lookup"><span data-stu-id="d4e5e-122">1</span></span>     | <span data-ttu-id="d4e5e-123">/App1/IFD/{UShort = 272}</span><span class="sxs-lookup"><span data-stu-id="d4e5e-123">/app1/ifd/{ushort=272}</span></span> | <span data-ttu-id="d4e5e-124">ascii</span><span class="sxs-lookup"><span data-stu-id="d4e5e-124">ascii</span></span>       |
| <span data-ttu-id="d4e5e-125">2</span><span class="sxs-lookup"><span data-stu-id="d4e5e-125">2</span></span>     | <span data-ttu-id="d4e5e-126">/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="d4e5e-126">/xmp/tiff:Model</span></span>        | <span data-ttu-id="d4e5e-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="d4e5e-127">unicode</span></span>     |
| <span data-ttu-id="d4e5e-128">3</span><span class="sxs-lookup"><span data-stu-id="d4e5e-128">3</span></span>     | <span data-ttu-id="d4e5e-129">/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="d4e5e-129">/xmp/tiff:model</span></span>        | <span data-ttu-id="d4e5e-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="d4e5e-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="d4e5e-131">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="d4e5e-131">Write Paths</span></span>



| <span data-ttu-id="d4e5e-132">Ordem</span><span class="sxs-lookup"><span data-stu-id="d4e5e-132">Order</span></span> | <span data-ttu-id="d4e5e-133">Caminho</span><span class="sxs-lookup"><span data-stu-id="d4e5e-133">Path</span></span>                   | <span data-ttu-id="d4e5e-134">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d4e5e-134">Disk Format</span></span> |
|-------|------------------------|-------------|
| <span data-ttu-id="d4e5e-135">1</span><span class="sxs-lookup"><span data-stu-id="d4e5e-135">1</span></span>     | <span data-ttu-id="d4e5e-136">/App1/IFD/{UShort = 272}</span><span class="sxs-lookup"><span data-stu-id="d4e5e-136">/app1/ifd/{ushort=272}</span></span> | <span data-ttu-id="d4e5e-137">ascii</span><span class="sxs-lookup"><span data-stu-id="d4e5e-137">ascii</span></span>       |
| <span data-ttu-id="d4e5e-138">2</span><span class="sxs-lookup"><span data-stu-id="d4e5e-138">2</span></span>     | <span data-ttu-id="d4e5e-139">/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="d4e5e-139">/xmp/tiff:Model</span></span>        | <span data-ttu-id="d4e5e-140">Unicode</span><span class="sxs-lookup"><span data-stu-id="d4e5e-140">unicode</span></span>     |
| <span data-ttu-id="d4e5e-141">3</span><span class="sxs-lookup"><span data-stu-id="d4e5e-141">3</span></span>     | <span data-ttu-id="d4e5e-142">/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="d4e5e-142">/xmp/tiff:model</span></span>        | <span data-ttu-id="d4e5e-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="d4e5e-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="d4e5e-144">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="d4e5e-144">Remove Paths</span></span>



| <span data-ttu-id="d4e5e-145">Ordem</span><span class="sxs-lookup"><span data-stu-id="d4e5e-145">Order</span></span> | <span data-ttu-id="d4e5e-146">Caminho</span><span class="sxs-lookup"><span data-stu-id="d4e5e-146">Path</span></span>                   |
|-------|------------------------|
| <span data-ttu-id="d4e5e-147">1</span><span class="sxs-lookup"><span data-stu-id="d4e5e-147">1</span></span>     | <span data-ttu-id="d4e5e-148">/App1/IFD/{UShort = 272}</span><span class="sxs-lookup"><span data-stu-id="d4e5e-148">/app1/ifd/{ushort=272}</span></span> |
| <span data-ttu-id="d4e5e-149">2</span><span class="sxs-lookup"><span data-stu-id="d4e5e-149">2</span></span>     | <span data-ttu-id="d4e5e-150">/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="d4e5e-150">/xmp/tiff:Model</span></span>        |
| <span data-ttu-id="d4e5e-151">3</span><span class="sxs-lookup"><span data-stu-id="d4e5e-151">3</span></span>     | <span data-ttu-id="d4e5e-152">/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="d4e5e-152">/xmp/tiff:model</span></span>        |



 

### <a name="tiff-policy"></a><span data-ttu-id="d4e5e-153">Política TIFF</span><span class="sxs-lookup"><span data-stu-id="d4e5e-153">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="d4e5e-154">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="d4e5e-154">Read Paths</span></span>



| <span data-ttu-id="d4e5e-155">Ordem</span><span class="sxs-lookup"><span data-stu-id="d4e5e-155">Order</span></span> | <span data-ttu-id="d4e5e-156">Caminho</span><span class="sxs-lookup"><span data-stu-id="d4e5e-156">Path</span></span>                | <span data-ttu-id="d4e5e-157">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d4e5e-157">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="d4e5e-158">1</span><span class="sxs-lookup"><span data-stu-id="d4e5e-158">1</span></span>     | <span data-ttu-id="d4e5e-159">/IFD/{UShort = 272}</span><span class="sxs-lookup"><span data-stu-id="d4e5e-159">/ifd/{ushort=272}</span></span>   | <span data-ttu-id="d4e5e-160">ascii</span><span class="sxs-lookup"><span data-stu-id="d4e5e-160">ascii</span></span>       |
| <span data-ttu-id="d4e5e-161">2</span><span class="sxs-lookup"><span data-stu-id="d4e5e-161">2</span></span>     | <span data-ttu-id="d4e5e-162">/IFD/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="d4e5e-162">/ifd/xmp/tiff:Model</span></span> | <span data-ttu-id="d4e5e-163">Unicode</span><span class="sxs-lookup"><span data-stu-id="d4e5e-163">unicode</span></span>     |
| <span data-ttu-id="d4e5e-164">3</span><span class="sxs-lookup"><span data-stu-id="d4e5e-164">3</span></span>     | <span data-ttu-id="d4e5e-165">/IFD/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="d4e5e-165">/ifd/xmp/tiff:model</span></span> | <span data-ttu-id="d4e5e-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="d4e5e-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="d4e5e-167">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="d4e5e-167">Write Paths</span></span>



| <span data-ttu-id="d4e5e-168">Ordem</span><span class="sxs-lookup"><span data-stu-id="d4e5e-168">Order</span></span> | <span data-ttu-id="d4e5e-169">Caminho</span><span class="sxs-lookup"><span data-stu-id="d4e5e-169">Path</span></span>                | <span data-ttu-id="d4e5e-170">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d4e5e-170">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="d4e5e-171">1</span><span class="sxs-lookup"><span data-stu-id="d4e5e-171">1</span></span>     | <span data-ttu-id="d4e5e-172">/IFD/{UShort = 272}</span><span class="sxs-lookup"><span data-stu-id="d4e5e-172">/ifd/{ushort=272}</span></span>   | <span data-ttu-id="d4e5e-173">ascii</span><span class="sxs-lookup"><span data-stu-id="d4e5e-173">ascii</span></span>       |
| <span data-ttu-id="d4e5e-174">2</span><span class="sxs-lookup"><span data-stu-id="d4e5e-174">2</span></span>     | <span data-ttu-id="d4e5e-175">/IFD/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="d4e5e-175">/ifd/xmp/tiff:Model</span></span> | <span data-ttu-id="d4e5e-176">Unicode</span><span class="sxs-lookup"><span data-stu-id="d4e5e-176">unicode</span></span>     |
| <span data-ttu-id="d4e5e-177">3</span><span class="sxs-lookup"><span data-stu-id="d4e5e-177">3</span></span>     | <span data-ttu-id="d4e5e-178">/IFD/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="d4e5e-178">/ifd/xmp/tiff:model</span></span> | <span data-ttu-id="d4e5e-179">Unicode</span><span class="sxs-lookup"><span data-stu-id="d4e5e-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="d4e5e-180">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="d4e5e-180">Remove Paths</span></span>



| <span data-ttu-id="d4e5e-181">Ordem</span><span class="sxs-lookup"><span data-stu-id="d4e5e-181">Order</span></span> | <span data-ttu-id="d4e5e-182">Caminho</span><span class="sxs-lookup"><span data-stu-id="d4e5e-182">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="d4e5e-183">1</span><span class="sxs-lookup"><span data-stu-id="d4e5e-183">1</span></span>     | <span data-ttu-id="d4e5e-184">/IFD/{UShort = 272}</span><span class="sxs-lookup"><span data-stu-id="d4e5e-184">/ifd/{ushort=272}</span></span>   |
| <span data-ttu-id="d4e5e-185">2</span><span class="sxs-lookup"><span data-stu-id="d4e5e-185">2</span></span>     | <span data-ttu-id="d4e5e-186">/IFD/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="d4e5e-186">/ifd/xmp/tiff:Model</span></span> |
| <span data-ttu-id="d4e5e-187">3</span><span class="sxs-lookup"><span data-stu-id="d4e5e-187">3</span></span>     | <span data-ttu-id="d4e5e-188">/IFD/XMP/TIFF: modelo</span><span class="sxs-lookup"><span data-stu-id="d4e5e-188">/ifd/xmp/tiff:model</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d4e5e-189">Comentários</span><span class="sxs-lookup"><span data-stu-id="d4e5e-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4e5e-190">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4e5e-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4e5e-191">System. Photo. CameraModel</span><span class="sxs-lookup"><span data-stu-id="d4e5e-191">System.Photo.CameraModel</span></span>](../properties/props-system-photo-cameramodel.md)
</dt> </dl>

 

 
