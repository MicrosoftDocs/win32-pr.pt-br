---
description: A política de metadados de foto para a propriedade System. Photo. FlashEnergy.
ms.assetid: d10a4de9-16fe-4920-aa7f-b2f95fb23045
title: Política de metadados de foto System. Photo. FlashEnergy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c272b4d6d14bf2f2e81d0964a3dc4395ba62dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011678"
---
# <a name="systemphotoflashenergy-photo-metadata-policy"></a><span data-ttu-id="88e20-103">Política de metadados de foto System. Photo. FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="88e20-103">System.Photo.FlashEnergy Photo Metadata Policy</span></span>

<span data-ttu-id="88e20-104">A política de metadados de foto para a propriedade [System. Photo. FlashEnergy](../properties/props-system-photo-flashenergy.md) .</span><span class="sxs-lookup"><span data-stu-id="88e20-104">The photo metadata policy for the [System.Photo.FlashEnergy](../properties/props-system-photo-flashenergy.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="88e20-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="88e20-105">PKEY</span></span>

<span data-ttu-id="88e20-106">PKEY \_ Photo \_ FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="88e20-106">PKEY\_Photo\_FlashEnergy</span></span>

### <a name="containers"></a><span data-ttu-id="88e20-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="88e20-107">Containers</span></span>

<span data-ttu-id="88e20-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="88e20-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="88e20-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="88e20-109">Read-Only</span></span>

<span data-ttu-id="88e20-110">Yes</span><span class="sxs-lookup"><span data-stu-id="88e20-110">Yes</span></span>

### <a name="input-type"></a><span data-ttu-id="88e20-111">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="88e20-111">Input Type</span></span>

<span data-ttu-id="88e20-112">Double</span><span class="sxs-lookup"><span data-stu-id="88e20-112">Double</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="88e20-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="88e20-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="88e20-114">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="88e20-114">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="88e20-115">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="88e20-115">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="88e20-116">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="88e20-116">Read Paths</span></span>



| <span data-ttu-id="88e20-117">Ordem</span><span class="sxs-lookup"><span data-stu-id="88e20-117">Order</span></span> | <span data-ttu-id="88e20-118">Caminho</span><span class="sxs-lookup"><span data-stu-id="88e20-118">Path</span></span>                          | <span data-ttu-id="88e20-119">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="88e20-119">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="88e20-120">1</span><span class="sxs-lookup"><span data-stu-id="88e20-120">1</span></span>     | <span data-ttu-id="88e20-121">/App1/IFD/EXIF/{UShort = 41483}</span><span class="sxs-lookup"><span data-stu-id="88e20-121">/app1/ifd/exif/{ushort=41483}</span></span> |             |
| <span data-ttu-id="88e20-122">2</span><span class="sxs-lookup"><span data-stu-id="88e20-122">2</span></span>     | <span data-ttu-id="88e20-123">/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="88e20-123">/xmp/exif:FlashEnergy</span></span>         |             |



 

### <a name="write-paths"></a><span data-ttu-id="88e20-124">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="88e20-124">Write Paths</span></span>



| <span data-ttu-id="88e20-125">Ordem</span><span class="sxs-lookup"><span data-stu-id="88e20-125">Order</span></span> | <span data-ttu-id="88e20-126">Caminho</span><span class="sxs-lookup"><span data-stu-id="88e20-126">Path</span></span>                          | <span data-ttu-id="88e20-127">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="88e20-127">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="88e20-128">1</span><span class="sxs-lookup"><span data-stu-id="88e20-128">1</span></span>     | <span data-ttu-id="88e20-129">/App1/IFD/EXIF/{UShort = 41483}</span><span class="sxs-lookup"><span data-stu-id="88e20-129">/app1/ifd/exif/{ushort=41483}</span></span> |             |
| <span data-ttu-id="88e20-130">2</span><span class="sxs-lookup"><span data-stu-id="88e20-130">2</span></span>     | <span data-ttu-id="88e20-131">/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="88e20-131">/xmp/exif:FlashEnergy</span></span>         |             |



 

### <a name="remove-paths"></a><span data-ttu-id="88e20-132">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="88e20-132">Remove Paths</span></span>



| <span data-ttu-id="88e20-133">Ordem</span><span class="sxs-lookup"><span data-stu-id="88e20-133">Order</span></span> | <span data-ttu-id="88e20-134">Caminho</span><span class="sxs-lookup"><span data-stu-id="88e20-134">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="88e20-135">1</span><span class="sxs-lookup"><span data-stu-id="88e20-135">1</span></span>     | <span data-ttu-id="88e20-136">/App1/IFD/EXIF/{UShort = 41483}</span><span class="sxs-lookup"><span data-stu-id="88e20-136">/app1/ifd/exif/{ushort=41483}</span></span> |
| <span data-ttu-id="88e20-137">2</span><span class="sxs-lookup"><span data-stu-id="88e20-137">2</span></span>     | <span data-ttu-id="88e20-138">/xmp/exif:flashenergy</span><span class="sxs-lookup"><span data-stu-id="88e20-138">/xmp/exif:flashenergy</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="88e20-139">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="88e20-139">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="88e20-140">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="88e20-140">Read Paths</span></span>



| <span data-ttu-id="88e20-141">Ordem</span><span class="sxs-lookup"><span data-stu-id="88e20-141">Order</span></span> | <span data-ttu-id="88e20-142">Caminho</span><span class="sxs-lookup"><span data-stu-id="88e20-142">Path</span></span>                      | <span data-ttu-id="88e20-143">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="88e20-143">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="88e20-144">1</span><span class="sxs-lookup"><span data-stu-id="88e20-144">1</span></span>     | <span data-ttu-id="88e20-145">/IFD/EXIF/{UShort = 41483}</span><span class="sxs-lookup"><span data-stu-id="88e20-145">/ifd/exif/{ushort=41483}</span></span>  |             |
| <span data-ttu-id="88e20-146">2</span><span class="sxs-lookup"><span data-stu-id="88e20-146">2</span></span>     | <span data-ttu-id="88e20-147">/ifd/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="88e20-147">/ifd/xmp/exif:FlashEnergy</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="88e20-148">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="88e20-148">Write Paths</span></span>



| <span data-ttu-id="88e20-149">Ordem</span><span class="sxs-lookup"><span data-stu-id="88e20-149">Order</span></span> | <span data-ttu-id="88e20-150">Caminho</span><span class="sxs-lookup"><span data-stu-id="88e20-150">Path</span></span>                      | <span data-ttu-id="88e20-151">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="88e20-151">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="88e20-152">1</span><span class="sxs-lookup"><span data-stu-id="88e20-152">1</span></span>     | <span data-ttu-id="88e20-153">/IFD/EXIF/{UShort = 41483}</span><span class="sxs-lookup"><span data-stu-id="88e20-153">/ifd/exif/{ushort=41483}</span></span>  |             |
| <span data-ttu-id="88e20-154">2</span><span class="sxs-lookup"><span data-stu-id="88e20-154">2</span></span>     | <span data-ttu-id="88e20-155">/ifd/xmp/exif:FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="88e20-155">/ifd/xmp/exif:FlashEnergy</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="88e20-156">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="88e20-156">Remove Paths</span></span>



| <span data-ttu-id="88e20-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="88e20-157">Order</span></span> | <span data-ttu-id="88e20-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="88e20-158">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="88e20-159">1</span><span class="sxs-lookup"><span data-stu-id="88e20-159">1</span></span>     | <span data-ttu-id="88e20-160">/IFD/EXIF/{UShort = 41483}</span><span class="sxs-lookup"><span data-stu-id="88e20-160">/ifd/exif/{ushort=41483}</span></span>  |
| <span data-ttu-id="88e20-161">2</span><span class="sxs-lookup"><span data-stu-id="88e20-161">2</span></span>     | <span data-ttu-id="88e20-162">/ifd/xmp/exif:flashenergy</span><span class="sxs-lookup"><span data-stu-id="88e20-162">/ifd/xmp/exif:flashenergy</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="88e20-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="88e20-163">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="88e20-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="88e20-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88e20-165">System. Photo. FlashEnergy</span><span class="sxs-lookup"><span data-stu-id="88e20-165">System.Photo.FlashEnergy</span></span>](../properties/props-system-photo-flashenergy.md)
</dt> </dl>

 

 
