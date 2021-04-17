---
description: A política de metadados de foto para a propriedade System. GPS. VersionId.
ms.assetid: d3c88243-8744-4bb3-ab47-38b5354f6f7e
title: Política de metadados de foto System. GPS. VersionId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ca5bd1885f0ac5c3dc14dbb5e859de3f8a26cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797646"
---
# <a name="systemgpsversionid-photo-metadata-policy"></a><span data-ttu-id="d2f68-103">Política de metadados de foto System. GPS. VersionId</span><span class="sxs-lookup"><span data-stu-id="d2f68-103">System.GPS.VersionID Photo Metadata Policy</span></span>

<span data-ttu-id="d2f68-104">A política de metadados de foto para a propriedade [System. GPS. VersionId](../properties/props-system-gps-versionid.md) .</span><span class="sxs-lookup"><span data-stu-id="d2f68-104">The photo metadata policy for the [System.GPS.VersionID](../properties/props-system-gps-versionid.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="d2f68-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="d2f68-105">PKEY</span></span>

<span data-ttu-id="d2f68-106">PKEY \_ GPS \_ VersionId</span><span class="sxs-lookup"><span data-stu-id="d2f68-106">PKEY\_GPS\_VersionID</span></span>

### <a name="containers"></a><span data-ttu-id="d2f68-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="d2f68-107">Containers</span></span>

<span data-ttu-id="d2f68-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="d2f68-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="d2f68-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d2f68-109">Read-Only</span></span>

<span data-ttu-id="d2f68-110">No</span><span class="sxs-lookup"><span data-stu-id="d2f68-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="d2f68-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="d2f68-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="d2f68-112">\_ \| \_ interface do usuário VT de vetor VT</span><span class="sxs-lookup"><span data-stu-id="d2f68-112">VT\_VECTOR \| VT\_UI</span></span>

### <a name="input-type"></a><span data-ttu-id="d2f68-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="d2f68-113">Input Type</span></span>

<span data-ttu-id="d2f68-114">Buffer</span><span class="sxs-lookup"><span data-stu-id="d2f68-114">Buffer</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="d2f68-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="d2f68-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="d2f68-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="d2f68-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="d2f68-117">Políticas JPEG</span><span class="sxs-lookup"><span data-stu-id="d2f68-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="d2f68-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="d2f68-118">Read Paths</span></span>



| <span data-ttu-id="d2f68-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="d2f68-119">Order</span></span> | <span data-ttu-id="d2f68-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="d2f68-120">Path</span></span>                     | <span data-ttu-id="d2f68-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d2f68-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="d2f68-122">1</span><span class="sxs-lookup"><span data-stu-id="d2f68-122">1</span></span>     | <span data-ttu-id="d2f68-123">/App1/IFD/GPS/{UShort = 0}</span><span class="sxs-lookup"><span data-stu-id="d2f68-123">/app1/ifd/gps/{ushort=0}</span></span> |             |
| <span data-ttu-id="d2f68-124">2</span><span class="sxs-lookup"><span data-stu-id="d2f68-124">2</span></span>     | <span data-ttu-id="d2f68-125">/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="d2f68-125">/xmp/exif:GPSVersionID</span></span>   | <span data-ttu-id="d2f68-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2f68-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="d2f68-127">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="d2f68-127">Write Paths</span></span>



| <span data-ttu-id="d2f68-128">Ordem</span><span class="sxs-lookup"><span data-stu-id="d2f68-128">Order</span></span> | <span data-ttu-id="d2f68-129">Caminho</span><span class="sxs-lookup"><span data-stu-id="d2f68-129">Path</span></span>                     | <span data-ttu-id="d2f68-130">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d2f68-130">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="d2f68-131">1</span><span class="sxs-lookup"><span data-stu-id="d2f68-131">1</span></span>     | <span data-ttu-id="d2f68-132">/App1/IFD/GPS/{UShort = 0}</span><span class="sxs-lookup"><span data-stu-id="d2f68-132">/app1/ifd/gps/{ushort=0}</span></span> |             |
| <span data-ttu-id="d2f68-133">2</span><span class="sxs-lookup"><span data-stu-id="d2f68-133">2</span></span>     | <span data-ttu-id="d2f68-134">/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="d2f68-134">/xmp/exif:GPSVersionID</span></span>   | <span data-ttu-id="d2f68-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2f68-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="d2f68-136">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="d2f68-136">Remove Paths</span></span>



| <span data-ttu-id="d2f68-137">Ordem</span><span class="sxs-lookup"><span data-stu-id="d2f68-137">Order</span></span> | <span data-ttu-id="d2f68-138">Caminho</span><span class="sxs-lookup"><span data-stu-id="d2f68-138">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="d2f68-139">1</span><span class="sxs-lookup"><span data-stu-id="d2f68-139">1</span></span>     | <span data-ttu-id="d2f68-140">/App1/IFD/GPS/{UShort = 0}</span><span class="sxs-lookup"><span data-stu-id="d2f68-140">/app1/ifd/gps/{ushort=0}</span></span> |
| <span data-ttu-id="d2f68-141">2</span><span class="sxs-lookup"><span data-stu-id="d2f68-141">2</span></span>     | <span data-ttu-id="d2f68-142">/xmp/exif:gpsversionid</span><span class="sxs-lookup"><span data-stu-id="d2f68-142">/xmp/exif:gpsversionid</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="d2f68-143">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="d2f68-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="d2f68-144">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="d2f68-144">Read Paths</span></span>



| <span data-ttu-id="d2f68-145">Ordem</span><span class="sxs-lookup"><span data-stu-id="d2f68-145">Order</span></span> | <span data-ttu-id="d2f68-146">Caminho</span><span class="sxs-lookup"><span data-stu-id="d2f68-146">Path</span></span>                       | <span data-ttu-id="d2f68-147">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d2f68-147">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="d2f68-148">1</span><span class="sxs-lookup"><span data-stu-id="d2f68-148">1</span></span>     | <span data-ttu-id="d2f68-149">/IFD/GPS/{UShort = 0}</span><span class="sxs-lookup"><span data-stu-id="d2f68-149">/ifd/gps/{ushort=0}</span></span>        |             |
| <span data-ttu-id="d2f68-150">2</span><span class="sxs-lookup"><span data-stu-id="d2f68-150">2</span></span>     | <span data-ttu-id="d2f68-151">/ifd/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="d2f68-151">/ifd/xmp/exif:GPSVersionID</span></span> | <span data-ttu-id="d2f68-152">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2f68-152">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="d2f68-153">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="d2f68-153">Write Paths</span></span>



| <span data-ttu-id="d2f68-154">Ordem</span><span class="sxs-lookup"><span data-stu-id="d2f68-154">Order</span></span> | <span data-ttu-id="d2f68-155">Caminho</span><span class="sxs-lookup"><span data-stu-id="d2f68-155">Path</span></span>                       | <span data-ttu-id="d2f68-156">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="d2f68-156">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="d2f68-157">1</span><span class="sxs-lookup"><span data-stu-id="d2f68-157">1</span></span>     | <span data-ttu-id="d2f68-158">/IFD/GPS/{UShort = 0}</span><span class="sxs-lookup"><span data-stu-id="d2f68-158">/ifd/gps/{ushort=0}</span></span>        |             |
| <span data-ttu-id="d2f68-159">2</span><span class="sxs-lookup"><span data-stu-id="d2f68-159">2</span></span>     | <span data-ttu-id="d2f68-160">/ifd/xmp/exif:GPSVersionID</span><span class="sxs-lookup"><span data-stu-id="d2f68-160">/ifd/xmp/exif:GPSVersionID</span></span> | <span data-ttu-id="d2f68-161">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2f68-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="d2f68-162">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="d2f68-162">Remove Paths</span></span>



| <span data-ttu-id="d2f68-163">Ordem</span><span class="sxs-lookup"><span data-stu-id="d2f68-163">Order</span></span> | <span data-ttu-id="d2f68-164">Caminho</span><span class="sxs-lookup"><span data-stu-id="d2f68-164">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="d2f68-165">1</span><span class="sxs-lookup"><span data-stu-id="d2f68-165">1</span></span>     | <span data-ttu-id="d2f68-166">/IFD/GPS/{UShort = 0}</span><span class="sxs-lookup"><span data-stu-id="d2f68-166">/ifd/gps/{ushort=0}</span></span>        |
| <span data-ttu-id="d2f68-167">2</span><span class="sxs-lookup"><span data-stu-id="d2f68-167">2</span></span>     | <span data-ttu-id="d2f68-168">/ifd/xmp/exif:gpsversionid</span><span class="sxs-lookup"><span data-stu-id="d2f68-168">/ifd/xmp/exif:gpsversionid</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d2f68-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2f68-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2f68-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d2f68-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2f68-171">System. GPS. VersionId</span><span class="sxs-lookup"><span data-stu-id="d2f68-171">System.GPS.VersionID</span></span>](../properties/props-system-gps-versionid.md)
</dt> </dl>

 

 
