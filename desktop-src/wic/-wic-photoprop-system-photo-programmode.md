---
description: A política de metadados de foto para a propriedade System. Photo. programmode.
ms.assetid: f1954dc7-d4df-4675-ab3b-a65f2354e57a
title: Política de metadados de foto System. Photo. programmode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f5dffa822454509134c485e4792f4be4270912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922345"
---
# <a name="systemphotoprogrammode-photo-metadata-policy"></a><span data-ttu-id="76008-103">Política de metadados de foto System. Photo. programmode</span><span class="sxs-lookup"><span data-stu-id="76008-103">System.Photo.ProgramMode Photo Metadata Policy</span></span>

<span data-ttu-id="76008-104">A política de metadados de foto para a propriedade [System. Photo. programmode](../properties/props-system-photo-programmode.md) .</span><span class="sxs-lookup"><span data-stu-id="76008-104">The photo metadata policy for the [System.Photo.ProgramMode](../properties/props-system-photo-programmode.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="76008-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="76008-105">PKEY</span></span>

<span data-ttu-id="76008-106">\_Programa de foto PKEY \_</span><span class="sxs-lookup"><span data-stu-id="76008-106">PKEY\_Photo\_ProgramMode</span></span>

### <a name="containers"></a><span data-ttu-id="76008-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="76008-107">Containers</span></span>

<span data-ttu-id="76008-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="76008-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="76008-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="76008-109">Read-Only</span></span>

<span data-ttu-id="76008-110">No</span><span class="sxs-lookup"><span data-stu-id="76008-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="76008-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="76008-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="76008-112">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="76008-112">VT\_UI4</span></span>

### <a name="input-type"></a><span data-ttu-id="76008-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="76008-113">Input Type</span></span>

<span data-ttu-id="76008-114">UShort</span><span class="sxs-lookup"><span data-stu-id="76008-114">UShort</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="76008-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="76008-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="76008-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="76008-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="76008-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="76008-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="76008-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="76008-118">Read Paths</span></span>



| <span data-ttu-id="76008-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="76008-119">Order</span></span> | <span data-ttu-id="76008-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="76008-120">Path</span></span>                          | <span data-ttu-id="76008-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="76008-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="76008-122">1</span><span class="sxs-lookup"><span data-stu-id="76008-122">1</span></span>     | <span data-ttu-id="76008-123">/App1/IFD/EXIF/{UShort = 34850}</span><span class="sxs-lookup"><span data-stu-id="76008-123">/app1/ifd/exif/{ushort=34850}</span></span> | <span data-ttu-id="76008-124">ushort</span><span class="sxs-lookup"><span data-stu-id="76008-124">ushort</span></span>      |
| <span data-ttu-id="76008-125">2</span><span class="sxs-lookup"><span data-stu-id="76008-125">2</span></span>     | <span data-ttu-id="76008-126">/xmp/exif:ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="76008-126">/xmp/exif:ExposureProgram</span></span>     | <span data-ttu-id="76008-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="76008-127">unicode</span></span>     |
| <span data-ttu-id="76008-128">3</span><span class="sxs-lookup"><span data-stu-id="76008-128">3</span></span>     | <span data-ttu-id="76008-129">/XMP/EXIF: programmode</span><span class="sxs-lookup"><span data-stu-id="76008-129">/xmp/exif:ProgramMode</span></span>         | <span data-ttu-id="76008-130">Unicode</span><span class="sxs-lookup"><span data-stu-id="76008-130">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="76008-131">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="76008-131">Write Paths</span></span>



| <span data-ttu-id="76008-132">Ordem</span><span class="sxs-lookup"><span data-stu-id="76008-132">Order</span></span> | <span data-ttu-id="76008-133">Caminho</span><span class="sxs-lookup"><span data-stu-id="76008-133">Path</span></span>                          | <span data-ttu-id="76008-134">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="76008-134">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="76008-135">1</span><span class="sxs-lookup"><span data-stu-id="76008-135">1</span></span>     | <span data-ttu-id="76008-136">/App1/IFD/EXIF/{UShort = 34850}</span><span class="sxs-lookup"><span data-stu-id="76008-136">/app1/ifd/exif/{ushort=34850}</span></span> | <span data-ttu-id="76008-137">ushort</span><span class="sxs-lookup"><span data-stu-id="76008-137">ushort</span></span>      |
| <span data-ttu-id="76008-138">2</span><span class="sxs-lookup"><span data-stu-id="76008-138">2</span></span>     | <span data-ttu-id="76008-139">/xmp/exif:ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="76008-139">/xmp/exif:ExposureProgram</span></span>     | <span data-ttu-id="76008-140">Unicode</span><span class="sxs-lookup"><span data-stu-id="76008-140">unicode</span></span>     |
| <span data-ttu-id="76008-141">3</span><span class="sxs-lookup"><span data-stu-id="76008-141">3</span></span>     | <span data-ttu-id="76008-142">/XMP/EXIF: programmode</span><span class="sxs-lookup"><span data-stu-id="76008-142">/xmp/exif:ProgramMode</span></span>         | <span data-ttu-id="76008-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="76008-143">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="76008-144">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="76008-144">Remove Paths</span></span>



| <span data-ttu-id="76008-145">Ordem</span><span class="sxs-lookup"><span data-stu-id="76008-145">Order</span></span> | <span data-ttu-id="76008-146">Caminho</span><span class="sxs-lookup"><span data-stu-id="76008-146">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="76008-147">1</span><span class="sxs-lookup"><span data-stu-id="76008-147">1</span></span>     | <span data-ttu-id="76008-148">/App1/IFD/EXIF/{UShort = 34850}</span><span class="sxs-lookup"><span data-stu-id="76008-148">/app1/ifd/exif/{ushort=34850}</span></span> |
| <span data-ttu-id="76008-149">2</span><span class="sxs-lookup"><span data-stu-id="76008-149">2</span></span>     | <span data-ttu-id="76008-150">/xmp/exif:exposureprogram</span><span class="sxs-lookup"><span data-stu-id="76008-150">/xmp/exif:exposureprogram</span></span>     |
| <span data-ttu-id="76008-151">3</span><span class="sxs-lookup"><span data-stu-id="76008-151">3</span></span>     | <span data-ttu-id="76008-152">/XMP/EXIF: programmode</span><span class="sxs-lookup"><span data-stu-id="76008-152">/xmp/exif:programmode</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="76008-153">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="76008-153">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="76008-154">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="76008-154">Read Paths</span></span>



| <span data-ttu-id="76008-155">Ordem</span><span class="sxs-lookup"><span data-stu-id="76008-155">Order</span></span> | <span data-ttu-id="76008-156">Caminho</span><span class="sxs-lookup"><span data-stu-id="76008-156">Path</span></span>                          | <span data-ttu-id="76008-157">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="76008-157">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="76008-158">1</span><span class="sxs-lookup"><span data-stu-id="76008-158">1</span></span>     | <span data-ttu-id="76008-159">/IFD/EXIF/{UShort = 34850}</span><span class="sxs-lookup"><span data-stu-id="76008-159">/ifd/exif/{ushort=34850}</span></span>      | <span data-ttu-id="76008-160">ushort</span><span class="sxs-lookup"><span data-stu-id="76008-160">ushort</span></span>      |
| <span data-ttu-id="76008-161">2</span><span class="sxs-lookup"><span data-stu-id="76008-161">2</span></span>     | <span data-ttu-id="76008-162">/ifd/xmp/exif:ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="76008-162">/ifd/xmp/exif:ExposureProgram</span></span> | <span data-ttu-id="76008-163">Unicode</span><span class="sxs-lookup"><span data-stu-id="76008-163">unicode</span></span>     |
| <span data-ttu-id="76008-164">3</span><span class="sxs-lookup"><span data-stu-id="76008-164">3</span></span>     | <span data-ttu-id="76008-165">/IFD/XMP/EXIF: programmode</span><span class="sxs-lookup"><span data-stu-id="76008-165">/ifd/xmp/exif:ProgramMode</span></span>     | <span data-ttu-id="76008-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="76008-166">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="76008-167">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="76008-167">Write Paths</span></span>



| <span data-ttu-id="76008-168">Ordem</span><span class="sxs-lookup"><span data-stu-id="76008-168">Order</span></span> | <span data-ttu-id="76008-169">Caminho</span><span class="sxs-lookup"><span data-stu-id="76008-169">Path</span></span>                          | <span data-ttu-id="76008-170">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="76008-170">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="76008-171">1</span><span class="sxs-lookup"><span data-stu-id="76008-171">1</span></span>     | <span data-ttu-id="76008-172">/IFD/EXIF/{UShort = 34850}</span><span class="sxs-lookup"><span data-stu-id="76008-172">/ifd/exif/{ushort=34850}</span></span>      | <span data-ttu-id="76008-173">ushort</span><span class="sxs-lookup"><span data-stu-id="76008-173">ushort</span></span>      |
| <span data-ttu-id="76008-174">2</span><span class="sxs-lookup"><span data-stu-id="76008-174">2</span></span>     | <span data-ttu-id="76008-175">/ifd/xmp/exif:ExposureProgram</span><span class="sxs-lookup"><span data-stu-id="76008-175">/ifd/xmp/exif:ExposureProgram</span></span> | <span data-ttu-id="76008-176">Unicode</span><span class="sxs-lookup"><span data-stu-id="76008-176">unicode</span></span>     |
| <span data-ttu-id="76008-177">3</span><span class="sxs-lookup"><span data-stu-id="76008-177">3</span></span>     | <span data-ttu-id="76008-178">/IFD/XMP/EXIF: programmode</span><span class="sxs-lookup"><span data-stu-id="76008-178">/ifd/xmp/exif:ProgramMode</span></span>     | <span data-ttu-id="76008-179">Unicode</span><span class="sxs-lookup"><span data-stu-id="76008-179">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="76008-180">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="76008-180">Remove Paths</span></span>



| <span data-ttu-id="76008-181">Ordem</span><span class="sxs-lookup"><span data-stu-id="76008-181">Order</span></span> | <span data-ttu-id="76008-182">Caminho</span><span class="sxs-lookup"><span data-stu-id="76008-182">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="76008-183">1</span><span class="sxs-lookup"><span data-stu-id="76008-183">1</span></span>     | <span data-ttu-id="76008-184">/IFD/EXIF/{UShort = 34850}</span><span class="sxs-lookup"><span data-stu-id="76008-184">/ifd/exif/{ushort=34850}</span></span>      |
| <span data-ttu-id="76008-185">2</span><span class="sxs-lookup"><span data-stu-id="76008-185">2</span></span>     | <span data-ttu-id="76008-186">/ifd/xmp/exif:exposureprogram</span><span class="sxs-lookup"><span data-stu-id="76008-186">/ifd/xmp/exif:exposureprogram</span></span> |
| <span data-ttu-id="76008-187">3</span><span class="sxs-lookup"><span data-stu-id="76008-187">3</span></span>     | <span data-ttu-id="76008-188">/IFD/XMP/EXIF: programmode</span><span class="sxs-lookup"><span data-stu-id="76008-188">/ifd/xmp/exif:programmode</span></span>     |



 

## <a name="remarks"></a><span data-ttu-id="76008-189">Comentários</span><span class="sxs-lookup"><span data-stu-id="76008-189">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="76008-190">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="76008-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76008-191">System. Photo. programmode</span><span class="sxs-lookup"><span data-stu-id="76008-191">System.Photo.ProgramMode</span></span>](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
