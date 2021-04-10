---
description: A política de metadados de foto para a propriedade System. SimpleRating.
ms.assetid: d932a251-f238-4582-a1c4-cf4855f26fb3
title: Política de metadados de foto System. SimpleRating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b91e41a0684c8e395992683e0a1d4fe43306a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011532"
---
# <a name="systemsimplerating-photo-metadata-policy"></a><span data-ttu-id="b1091-103">Política de metadados de foto System. SimpleRating</span><span class="sxs-lookup"><span data-stu-id="b1091-103">System.SimpleRating Photo Metadata Policy</span></span>

<span data-ttu-id="b1091-104">A política de metadados de foto para a propriedade [System. SimpleRating](../properties/props-system-simplerating.md) .</span><span class="sxs-lookup"><span data-stu-id="b1091-104">The photo metadata policy for the [System.SimpleRating](../properties/props-system-simplerating.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b1091-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="b1091-105">PKEY</span></span>

<span data-ttu-id="b1091-106">PKEY \_ SimpleRating</span><span class="sxs-lookup"><span data-stu-id="b1091-106">PKEY\_SimpleRating</span></span>

### <a name="containers"></a><span data-ttu-id="b1091-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="b1091-107">Containers</span></span>

<span data-ttu-id="b1091-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b1091-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b1091-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1091-109">Read-Only</span></span>

<span data-ttu-id="b1091-110">No</span><span class="sxs-lookup"><span data-stu-id="b1091-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b1091-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="b1091-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b1091-112">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="b1091-112">VT\_UI4</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="b1091-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="b1091-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="b1091-114">Pode ser VT \_ UI1, VT \_ UI2 ou VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="b1091-114">May be VT\_UI1, VT\_UI2, or VT\_UI4.</span></span> <span data-ttu-id="b1091-115">O valor inteiro pode variar de 0 a 5.</span><span class="sxs-lookup"><span data-stu-id="b1091-115">The integer value may range from 0 to 5.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b1091-116">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="b1091-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="b1091-117">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="b1091-117">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="b1091-118">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="b1091-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="b1091-119">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="b1091-119">Read Paths</span></span>



| <span data-ttu-id="b1091-120">Ordem</span><span class="sxs-lookup"><span data-stu-id="b1091-120">Order</span></span> | <span data-ttu-id="b1091-121">Caminho</span><span class="sxs-lookup"><span data-stu-id="b1091-121">Path</span></span>                     | <span data-ttu-id="b1091-122">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b1091-122">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="b1091-123">1</span><span class="sxs-lookup"><span data-stu-id="b1091-123">1</span></span>     | <span data-ttu-id="b1091-124">/App1/IFD/{UShort = 18246}</span><span class="sxs-lookup"><span data-stu-id="b1091-124">/app1/ifd/{ushort=18246}</span></span> | <span data-ttu-id="b1091-125">ushort</span><span class="sxs-lookup"><span data-stu-id="b1091-125">ushort</span></span>      |
| <span data-ttu-id="b1091-126">2</span><span class="sxs-lookup"><span data-stu-id="b1091-126">2</span></span>     | <span data-ttu-id="b1091-127">/XMP/XMP: classificação</span><span class="sxs-lookup"><span data-stu-id="b1091-127">/xmp/xmp:Rating</span></span>          | <span data-ttu-id="b1091-128">Unicode</span><span class="sxs-lookup"><span data-stu-id="b1091-128">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="b1091-129">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="b1091-129">Write Paths</span></span>



| <span data-ttu-id="b1091-130">Ordem</span><span class="sxs-lookup"><span data-stu-id="b1091-130">Order</span></span> | <span data-ttu-id="b1091-131">Caminho</span><span class="sxs-lookup"><span data-stu-id="b1091-131">Path</span></span>                     | <span data-ttu-id="b1091-132">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b1091-132">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="b1091-133">1</span><span class="sxs-lookup"><span data-stu-id="b1091-133">1</span></span>     | <span data-ttu-id="b1091-134">/App1/IFD/{UShort = 18246}</span><span class="sxs-lookup"><span data-stu-id="b1091-134">/app1/ifd/{ushort=18246}</span></span> | <span data-ttu-id="b1091-135">ushort</span><span class="sxs-lookup"><span data-stu-id="b1091-135">ushort</span></span>      |
| <span data-ttu-id="b1091-136">2</span><span class="sxs-lookup"><span data-stu-id="b1091-136">2</span></span>     | <span data-ttu-id="b1091-137">/XMP/XMP: classificação</span><span class="sxs-lookup"><span data-stu-id="b1091-137">/xmp/xmp:Rating</span></span>          | <span data-ttu-id="b1091-138">Unicode</span><span class="sxs-lookup"><span data-stu-id="b1091-138">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="b1091-139">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="b1091-139">Remove Paths</span></span>



| <span data-ttu-id="b1091-140">Ordem</span><span class="sxs-lookup"><span data-stu-id="b1091-140">Order</span></span> | <span data-ttu-id="b1091-141">Caminho</span><span class="sxs-lookup"><span data-stu-id="b1091-141">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="b1091-142">1</span><span class="sxs-lookup"><span data-stu-id="b1091-142">1</span></span>     | <span data-ttu-id="b1091-143">/App1/IFD/{UShort = 18246}</span><span class="sxs-lookup"><span data-stu-id="b1091-143">/app1/ifd/{ushort=18246}</span></span> |
| <span data-ttu-id="b1091-144">2</span><span class="sxs-lookup"><span data-stu-id="b1091-144">2</span></span>     | <span data-ttu-id="b1091-145">/XMP/XMP: classificação</span><span class="sxs-lookup"><span data-stu-id="b1091-145">/xmp/xmp:rating</span></span>          |



 

### <a name="tiff-policies"></a><span data-ttu-id="b1091-146">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="b1091-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="b1091-147">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="b1091-147">Read Paths</span></span>



| <span data-ttu-id="b1091-148">Ordem</span><span class="sxs-lookup"><span data-stu-id="b1091-148">Order</span></span> | <span data-ttu-id="b1091-149">Caminho</span><span class="sxs-lookup"><span data-stu-id="b1091-149">Path</span></span>                | <span data-ttu-id="b1091-150">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b1091-150">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="b1091-151">1</span><span class="sxs-lookup"><span data-stu-id="b1091-151">1</span></span>     | <span data-ttu-id="b1091-152">/IFD/{UShort = 18246}</span><span class="sxs-lookup"><span data-stu-id="b1091-152">/ifd/{ushort=18246}</span></span> | <span data-ttu-id="b1091-153">ushort</span><span class="sxs-lookup"><span data-stu-id="b1091-153">ushort</span></span>      |
| <span data-ttu-id="b1091-154">2</span><span class="sxs-lookup"><span data-stu-id="b1091-154">2</span></span>     | <span data-ttu-id="b1091-155">/IFD/XMP/XMP: classificação</span><span class="sxs-lookup"><span data-stu-id="b1091-155">/ifd/xmp/xmp:Rating</span></span> | <span data-ttu-id="b1091-156">Unicode</span><span class="sxs-lookup"><span data-stu-id="b1091-156">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="b1091-157">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="b1091-157">Write Paths</span></span>



| <span data-ttu-id="b1091-158">Ordem</span><span class="sxs-lookup"><span data-stu-id="b1091-158">Order</span></span> | <span data-ttu-id="b1091-159">Caminho</span><span class="sxs-lookup"><span data-stu-id="b1091-159">Path</span></span>                | <span data-ttu-id="b1091-160">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b1091-160">Disk Format</span></span> |
|-------|---------------------|-------------|
| <span data-ttu-id="b1091-161">1</span><span class="sxs-lookup"><span data-stu-id="b1091-161">1</span></span>     | <span data-ttu-id="b1091-162">/IFD/{UShort = 18246}</span><span class="sxs-lookup"><span data-stu-id="b1091-162">/ifd/{ushort=18246}</span></span> | <span data-ttu-id="b1091-163">ushort</span><span class="sxs-lookup"><span data-stu-id="b1091-163">ushort</span></span>      |
| <span data-ttu-id="b1091-164">2</span><span class="sxs-lookup"><span data-stu-id="b1091-164">2</span></span>     | <span data-ttu-id="b1091-165">/IFD/XMP/XMP: classificação</span><span class="sxs-lookup"><span data-stu-id="b1091-165">/ifd/xmp/xmp:Rating</span></span> | <span data-ttu-id="b1091-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="b1091-166">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="b1091-167">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="b1091-167">Remove Paths</span></span>



| <span data-ttu-id="b1091-168">Ordem</span><span class="sxs-lookup"><span data-stu-id="b1091-168">Order</span></span> | <span data-ttu-id="b1091-169">Caminho</span><span class="sxs-lookup"><span data-stu-id="b1091-169">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="b1091-170">1</span><span class="sxs-lookup"><span data-stu-id="b1091-170">1</span></span>     | <span data-ttu-id="b1091-171">/IFD/{UShort = 18246}</span><span class="sxs-lookup"><span data-stu-id="b1091-171">/ifd/{ushort=18246}</span></span> |
| <span data-ttu-id="b1091-172">2</span><span class="sxs-lookup"><span data-stu-id="b1091-172">2</span></span>     | <span data-ttu-id="b1091-173">/IFD/XMP/XMP: classificação</span><span class="sxs-lookup"><span data-stu-id="b1091-173">/ifd/xmp/xmp:rating</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b1091-174">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1091-174">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1091-175">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1091-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1091-176">System. SimpleRating</span><span class="sxs-lookup"><span data-stu-id="b1091-176">System.SimpleRating</span></span>](../properties/props-system-simplerating.md)
</dt> </dl>

 

 
