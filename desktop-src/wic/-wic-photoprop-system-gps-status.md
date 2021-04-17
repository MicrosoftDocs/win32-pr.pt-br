---
description: A política de metadados de foto para a propriedade System. GPS. status.
ms.assetid: 74ea0384-3b1f-4d5e-8713-7b3936813a3a
title: Política de metadados de foto System. GPS. status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac08139a267052f8d6dd3dc463e2a2768309a41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761835"
---
# <a name="systemgpsstatus-photo-metadata-policy"></a><span data-ttu-id="0c7b8-103">Política de metadados de foto System. GPS. status</span><span class="sxs-lookup"><span data-stu-id="0c7b8-103">System.GPS.Status Photo Metadata Policy</span></span>

<span data-ttu-id="0c7b8-104">A política de metadados de foto para a propriedade [System. GPS. status](../properties/props-system-gps-status.md) .</span><span class="sxs-lookup"><span data-stu-id="0c7b8-104">The photo metadata policy for the [System.GPS.Status](../properties/props-system-gps-status.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="0c7b8-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="0c7b8-105">PKEY</span></span>

<span data-ttu-id="0c7b8-106">\_Status de GPS PKEY \_</span><span class="sxs-lookup"><span data-stu-id="0c7b8-106">PKEY\_GPS\_Status</span></span>

### <a name="containers"></a><span data-ttu-id="0c7b8-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="0c7b8-107">Containers</span></span>

<span data-ttu-id="0c7b8-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="0c7b8-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="0c7b8-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0c7b8-109">Read-Only</span></span>

<span data-ttu-id="0c7b8-110">No</span><span class="sxs-lookup"><span data-stu-id="0c7b8-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="0c7b8-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="0c7b8-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="0c7b8-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="0c7b8-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="0c7b8-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="0c7b8-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="0c7b8-114">VT \_ LPWSTR é preferível, mas VT \_ LPSTR também é aceito.</span><span class="sxs-lookup"><span data-stu-id="0c7b8-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="0c7b8-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="0c7b8-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="0c7b8-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="0c7b8-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="0c7b8-117">Políticas JPEG</span><span class="sxs-lookup"><span data-stu-id="0c7b8-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0c7b8-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="0c7b8-118">Read Paths</span></span>



| <span data-ttu-id="0c7b8-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="0c7b8-119">Order</span></span> | <span data-ttu-id="0c7b8-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="0c7b8-120">Path</span></span>                     | <span data-ttu-id="0c7b8-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="0c7b8-121">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="0c7b8-122">1</span><span class="sxs-lookup"><span data-stu-id="0c7b8-122">1</span></span>     | <span data-ttu-id="0c7b8-123">/App1/IFD/GPS/{UShort = 9}</span><span class="sxs-lookup"><span data-stu-id="0c7b8-123">/app1/ifd/gps/{ushort=9}</span></span> | <span data-ttu-id="0c7b8-124">ascii</span><span class="sxs-lookup"><span data-stu-id="0c7b8-124">ascii</span></span>       |
| <span data-ttu-id="0c7b8-125">2</span><span class="sxs-lookup"><span data-stu-id="0c7b8-125">2</span></span>     | <span data-ttu-id="0c7b8-126">/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="0c7b8-126">/xmp/exif:GPSStatus</span></span>      | <span data-ttu-id="0c7b8-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="0c7b8-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0c7b8-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="0c7b8-128">Write Paths</span></span>



| <span data-ttu-id="0c7b8-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="0c7b8-129">Order</span></span> | <span data-ttu-id="0c7b8-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="0c7b8-130">Path</span></span>                     | <span data-ttu-id="0c7b8-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="0c7b8-131">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="0c7b8-132">1</span><span class="sxs-lookup"><span data-stu-id="0c7b8-132">1</span></span>     | <span data-ttu-id="0c7b8-133">/App1/IFD/GPS/{UShort = 9}</span><span class="sxs-lookup"><span data-stu-id="0c7b8-133">/app1/ifd/gps/{ushort=9}</span></span> | <span data-ttu-id="0c7b8-134">ascii</span><span class="sxs-lookup"><span data-stu-id="0c7b8-134">ascii</span></span>       |
| <span data-ttu-id="0c7b8-135">2</span><span class="sxs-lookup"><span data-stu-id="0c7b8-135">2</span></span>     | <span data-ttu-id="0c7b8-136">/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="0c7b8-136">/xmp/exif:GPSStatus</span></span>      | <span data-ttu-id="0c7b8-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="0c7b8-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0c7b8-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="0c7b8-138">Remove Paths</span></span>



| <span data-ttu-id="0c7b8-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="0c7b8-139">Order</span></span> | <span data-ttu-id="0c7b8-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="0c7b8-140">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="0c7b8-141">1</span><span class="sxs-lookup"><span data-stu-id="0c7b8-141">1</span></span>     | <span data-ttu-id="0c7b8-142">/App1/IFD/GPS/{UShort = 9}</span><span class="sxs-lookup"><span data-stu-id="0c7b8-142">/app1/ifd/gps/{ushort=9}</span></span> |
| <span data-ttu-id="0c7b8-143">2</span><span class="sxs-lookup"><span data-stu-id="0c7b8-143">2</span></span>     | <span data-ttu-id="0c7b8-144">/xmp/exif:gpsstatus</span><span class="sxs-lookup"><span data-stu-id="0c7b8-144">/xmp/exif:gpsstatus</span></span>      |



 

### <a name="tiff-policies"></a><span data-ttu-id="0c7b8-145">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="0c7b8-145">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0c7b8-146">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="0c7b8-146">Read Paths</span></span>



| <span data-ttu-id="0c7b8-147">Ordem</span><span class="sxs-lookup"><span data-stu-id="0c7b8-147">Order</span></span> | <span data-ttu-id="0c7b8-148">Caminho</span><span class="sxs-lookup"><span data-stu-id="0c7b8-148">Path</span></span>                    | <span data-ttu-id="0c7b8-149">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="0c7b8-149">Disk Format</span></span> |
|-------|-------------------------|-------------|
| <span data-ttu-id="0c7b8-150">1</span><span class="sxs-lookup"><span data-stu-id="0c7b8-150">1</span></span>     | <span data-ttu-id="0c7b8-151">/IFD/GPS/{UShort = 9}</span><span class="sxs-lookup"><span data-stu-id="0c7b8-151">/ifd/gps/{ushort=9}</span></span>     | <span data-ttu-id="0c7b8-152">ascii</span><span class="sxs-lookup"><span data-stu-id="0c7b8-152">ascii</span></span>       |
| <span data-ttu-id="0c7b8-153">2</span><span class="sxs-lookup"><span data-stu-id="0c7b8-153">2</span></span>     | <span data-ttu-id="0c7b8-154">/ifd/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="0c7b8-154">/ifd/xmp/exif:GPSStatus</span></span> | <span data-ttu-id="0c7b8-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="0c7b8-155">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0c7b8-156">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="0c7b8-156">Write Paths</span></span>



| <span data-ttu-id="0c7b8-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="0c7b8-157">Order</span></span> | <span data-ttu-id="0c7b8-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="0c7b8-158">Path</span></span>                    | <span data-ttu-id="0c7b8-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="0c7b8-159">Disk Format</span></span> |
|-------|-------------------------|-------------|
| <span data-ttu-id="0c7b8-160">1</span><span class="sxs-lookup"><span data-stu-id="0c7b8-160">1</span></span>     | <span data-ttu-id="0c7b8-161">/IFD/GPS/{UShort = 9}</span><span class="sxs-lookup"><span data-stu-id="0c7b8-161">/ifd/gps/{ushort=9}</span></span>     | <span data-ttu-id="0c7b8-162">ascii</span><span class="sxs-lookup"><span data-stu-id="0c7b8-162">ascii</span></span>       |
| <span data-ttu-id="0c7b8-163">2</span><span class="sxs-lookup"><span data-stu-id="0c7b8-163">2</span></span>     | <span data-ttu-id="0c7b8-164">/ifd/xmp/exif:GPSStatus</span><span class="sxs-lookup"><span data-stu-id="0c7b8-164">/ifd/xmp/exif:GPSStatus</span></span> | <span data-ttu-id="0c7b8-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="0c7b8-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0c7b8-166">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="0c7b8-166">Remove Paths</span></span>



| <span data-ttu-id="0c7b8-167">Ordem</span><span class="sxs-lookup"><span data-stu-id="0c7b8-167">Order</span></span> | <span data-ttu-id="0c7b8-168">Caminho</span><span class="sxs-lookup"><span data-stu-id="0c7b8-168">Path</span></span>                    |
|-------|-------------------------|
| <span data-ttu-id="0c7b8-169">1</span><span class="sxs-lookup"><span data-stu-id="0c7b8-169">1</span></span>     | <span data-ttu-id="0c7b8-170">/IFD/GPS/{UShort = 9}</span><span class="sxs-lookup"><span data-stu-id="0c7b8-170">/ifd/gps/{ushort=9}</span></span>     |
| <span data-ttu-id="0c7b8-171">2</span><span class="sxs-lookup"><span data-stu-id="0c7b8-171">2</span></span>     | <span data-ttu-id="0c7b8-172">/ifd/xmp/exif:gpsstatus</span><span class="sxs-lookup"><span data-stu-id="0c7b8-172">/ifd/xmp/exif:gpsstatus</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0c7b8-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c7b8-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c7b8-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0c7b8-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c7b8-175">System. GPS. status</span><span class="sxs-lookup"><span data-stu-id="0c7b8-175">System.GPS.Status</span></span>](../properties/props-system-gps-status.md)
</dt> </dl>

 

 
