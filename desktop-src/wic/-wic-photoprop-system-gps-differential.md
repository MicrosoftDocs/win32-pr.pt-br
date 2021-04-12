---
description: A política de metadados de foto para a propriedade System. GPS. diferencial.
ms.assetid: 330d1f88-5f54-4e29-b57f-eb7112203e04
title: Política de metadados de foto System. GPS. diferencial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc3f114683d324a067fe4ce4034e2de5cfc88da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297364"
---
# <a name="systemgpsdifferential-photo-metadata-policy"></a><span data-ttu-id="cb688-103">Política de metadados de foto System. GPS. diferencial</span><span class="sxs-lookup"><span data-stu-id="cb688-103">System.GPS.Differential Photo Metadata Policy</span></span>

<span data-ttu-id="cb688-104">A política de metadados de foto para a propriedade [System. GPS. diferencial](../properties/props-system-gps-differential.md) .</span><span class="sxs-lookup"><span data-stu-id="cb688-104">The photo metadata policy for the [System.GPS.Differential](../properties/props-system-gps-differential.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="cb688-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="cb688-105">PKEY</span></span>

<span data-ttu-id="cb688-106">\_Diferencial do GPS PKEY \_</span><span class="sxs-lookup"><span data-stu-id="cb688-106">PKEY\_GPS\_Differential</span></span>

### <a name="containers"></a><span data-ttu-id="cb688-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="cb688-107">Containers</span></span>

<span data-ttu-id="cb688-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="cb688-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="cb688-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cb688-109">Read-Only</span></span>

<span data-ttu-id="cb688-110">No</span><span class="sxs-lookup"><span data-stu-id="cb688-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="cb688-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="cb688-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="cb688-112">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="cb688-112">VT\_UI2</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="cb688-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="cb688-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="cb688-114">VT \_ UI1, VT \_ UI2 e VT \_ UI4 são todos aceitos.</span><span class="sxs-lookup"><span data-stu-id="cb688-114">VT\_UI1, VT\_UI2, and VT\_UI4 are all accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="cb688-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="cb688-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="cb688-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="cb688-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="cb688-117">Políticas JPEG</span><span class="sxs-lookup"><span data-stu-id="cb688-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="cb688-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="cb688-118">Read Paths</span></span>



| <span data-ttu-id="cb688-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="cb688-119">Order</span></span> | <span data-ttu-id="cb688-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="cb688-120">Path</span></span>                      | <span data-ttu-id="cb688-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="cb688-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="cb688-122">1</span><span class="sxs-lookup"><span data-stu-id="cb688-122">1</span></span>     | <span data-ttu-id="cb688-123">/App1/IFD/GPS/{UShort = 30}</span><span class="sxs-lookup"><span data-stu-id="cb688-123">/app1/ifd/gps/{ushort=30}</span></span> | <span data-ttu-id="cb688-124">ushort</span><span class="sxs-lookup"><span data-stu-id="cb688-124">ushort</span></span>      |
| <span data-ttu-id="cb688-125">2</span><span class="sxs-lookup"><span data-stu-id="cb688-125">2</span></span>     | <span data-ttu-id="cb688-126">/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="cb688-126">/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="cb688-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="cb688-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="cb688-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="cb688-128">Write Paths</span></span>



| <span data-ttu-id="cb688-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="cb688-129">Order</span></span> | <span data-ttu-id="cb688-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="cb688-130">Path</span></span>                      | <span data-ttu-id="cb688-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="cb688-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="cb688-132">1</span><span class="sxs-lookup"><span data-stu-id="cb688-132">1</span></span>     | <span data-ttu-id="cb688-133">/App1/IFD/GPS/{UShort = 30}</span><span class="sxs-lookup"><span data-stu-id="cb688-133">/app1/ifd/gps/{ushort=30}</span></span> | <span data-ttu-id="cb688-134">ushort</span><span class="sxs-lookup"><span data-stu-id="cb688-134">ushort</span></span>      |
| <span data-ttu-id="cb688-135">2</span><span class="sxs-lookup"><span data-stu-id="cb688-135">2</span></span>     | <span data-ttu-id="cb688-136">/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="cb688-136">/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="cb688-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="cb688-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="cb688-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="cb688-138">Remove Paths</span></span>



| <span data-ttu-id="cb688-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="cb688-139">Order</span></span> | <span data-ttu-id="cb688-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="cb688-140">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="cb688-141">1</span><span class="sxs-lookup"><span data-stu-id="cb688-141">1</span></span>     | <span data-ttu-id="cb688-142">/App1/IFD/GPS/{UShort = 30}</span><span class="sxs-lookup"><span data-stu-id="cb688-142">/app1/ifd/gps/{ushort=30}</span></span> |
| <span data-ttu-id="cb688-143">2</span><span class="sxs-lookup"><span data-stu-id="cb688-143">2</span></span>     | <span data-ttu-id="cb688-144">/xmp/exif:gpsdifferential</span><span class="sxs-lookup"><span data-stu-id="cb688-144">/xmp/exif:gpsdifferential</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="cb688-145">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="cb688-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="cb688-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="cb688-146">Read Paths</span></span>



| <span data-ttu-id="cb688-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="cb688-147">Order</span></span> | <span data-ttu-id="cb688-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="cb688-148">Path</span></span>                          | <span data-ttu-id="cb688-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="cb688-149">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="cb688-150">1</span><span class="sxs-lookup"><span data-stu-id="cb688-150">1</span></span>     | <span data-ttu-id="cb688-151">/IFD/GPS/{UShort = 30}</span><span class="sxs-lookup"><span data-stu-id="cb688-151">/ifd/gps/{ushort=30}</span></span>          | <span data-ttu-id="cb688-152">ushort</span><span class="sxs-lookup"><span data-stu-id="cb688-152">ushort</span></span>      |
| <span data-ttu-id="cb688-153">2</span><span class="sxs-lookup"><span data-stu-id="cb688-153">2</span></span>     | <span data-ttu-id="cb688-154">/ifd/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="cb688-154">/ifd/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="cb688-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="cb688-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="cb688-156">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="cb688-156">Write Paths</span></span>



| <span data-ttu-id="cb688-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="cb688-157">Order</span></span> | <span data-ttu-id="cb688-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="cb688-158">Path</span></span>                          | <span data-ttu-id="cb688-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="cb688-159">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="cb688-160">1</span><span class="sxs-lookup"><span data-stu-id="cb688-160">1</span></span>     | <span data-ttu-id="cb688-161">/IFD/GPS/{UShort = 30}</span><span class="sxs-lookup"><span data-stu-id="cb688-161">/ifd/gps/{ushort=30}</span></span>          | <span data-ttu-id="cb688-162">ushort</span><span class="sxs-lookup"><span data-stu-id="cb688-162">ushort</span></span>      |
| <span data-ttu-id="cb688-163">2</span><span class="sxs-lookup"><span data-stu-id="cb688-163">2</span></span>     | <span data-ttu-id="cb688-164">/ifd/xmp/exif:GPSDifferential</span><span class="sxs-lookup"><span data-stu-id="cb688-164">/ifd/xmp/exif:GPSDifferential</span></span> | <span data-ttu-id="cb688-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="cb688-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="cb688-166">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="cb688-166">Remove Paths</span></span>



| <span data-ttu-id="cb688-167">Ordem</span><span class="sxs-lookup"><span data-stu-id="cb688-167">Order</span></span> | <span data-ttu-id="cb688-168">Caminho</span><span class="sxs-lookup"><span data-stu-id="cb688-168">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="cb688-169">1</span><span class="sxs-lookup"><span data-stu-id="cb688-169">1</span></span>     | <span data-ttu-id="cb688-170">/IFD/GPS/{UShort = 30}</span><span class="sxs-lookup"><span data-stu-id="cb688-170">/ifd/gps/{ushort=30}</span></span>          |
| <span data-ttu-id="cb688-171">2</span><span class="sxs-lookup"><span data-stu-id="cb688-171">2</span></span>     | <span data-ttu-id="cb688-172">/ifd/xmp/exif:gpsdifferential</span><span class="sxs-lookup"><span data-stu-id="cb688-172">/ifd/xmp/exif:gpsdifferential</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cb688-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb688-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb688-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cb688-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb688-175">System. GPS. diferencial</span><span class="sxs-lookup"><span data-stu-id="cb688-175">System.GPS.Differential</span></span>](../properties/props-system-gps-differential.md)
</dt> </dl>

 

 
