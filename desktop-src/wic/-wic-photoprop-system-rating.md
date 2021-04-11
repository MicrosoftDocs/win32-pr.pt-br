---
description: A política de metadados de foto para a propriedade System. rating.
ms.assetid: e4d2c12e-617a-431e-9062-62acf6ef21c8
title: Política de metadados de foto System. rating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4f7d89b1ff1ea8326c2d26fba0d331db1eab1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297084"
---
# <a name="systemrating-photo-metadata-policy"></a><span data-ttu-id="2a23b-103">Política de metadados de foto System. rating</span><span class="sxs-lookup"><span data-stu-id="2a23b-103">System.Rating Photo Metadata Policy</span></span>

<span data-ttu-id="2a23b-104">A política de metadados de foto para a propriedade [System. rating](../properties/props-system-rating.md) .</span><span class="sxs-lookup"><span data-stu-id="2a23b-104">The photo metadata policy for the [System.Rating](../properties/props-system-rating.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="2a23b-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="2a23b-105">PKEY</span></span>

<span data-ttu-id="2a23b-106">Classificação de PKEY \_</span><span class="sxs-lookup"><span data-stu-id="2a23b-106">PKEY\_Rating</span></span>

### <a name="containers"></a><span data-ttu-id="2a23b-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="2a23b-107">Containers</span></span>

<span data-ttu-id="2a23b-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="2a23b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="2a23b-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2a23b-109">Read-Only</span></span>

<span data-ttu-id="2a23b-110">No</span><span class="sxs-lookup"><span data-stu-id="2a23b-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="2a23b-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="2a23b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="2a23b-112">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="2a23b-112">VT\_UI4</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="2a23b-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="2a23b-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="2a23b-114">Pode ser VT \_ UI1, VT \_ UI2 ou VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="2a23b-114">May be VT\_UI1, VT\_UI2, or VT\_UI4.</span></span> <span data-ttu-id="2a23b-115">O valor pode variar de 0 a 99.</span><span class="sxs-lookup"><span data-stu-id="2a23b-115">The value may range from 0 to 99.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="2a23b-116">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="2a23b-116">Conflict Resolution Policy</span></span>

<span data-ttu-id="2a23b-117">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="2a23b-117">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="2a23b-118">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="2a23b-118">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="2a23b-119">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="2a23b-119">Read Paths</span></span>



| <span data-ttu-id="2a23b-120">Ordem</span><span class="sxs-lookup"><span data-stu-id="2a23b-120">Order</span></span> | <span data-ttu-id="2a23b-121">Caminho</span><span class="sxs-lookup"><span data-stu-id="2a23b-121">Path</span></span>                       | <span data-ttu-id="2a23b-122">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="2a23b-122">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="2a23b-123">1</span><span class="sxs-lookup"><span data-stu-id="2a23b-123">1</span></span>     | <span data-ttu-id="2a23b-124">/App1/IFD/{UShort = 18249}</span><span class="sxs-lookup"><span data-stu-id="2a23b-124">/app1/ifd/{ushort=18249}</span></span>   | <span data-ttu-id="2a23b-125">ushort</span><span class="sxs-lookup"><span data-stu-id="2a23b-125">ushort</span></span>      |
| <span data-ttu-id="2a23b-126">2</span><span class="sxs-lookup"><span data-stu-id="2a23b-126">2</span></span>     | <span data-ttu-id="2a23b-127">/xmp/MicrosoftPhoto: classificação</span><span class="sxs-lookup"><span data-stu-id="2a23b-127">/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="2a23b-128">Unicode</span><span class="sxs-lookup"><span data-stu-id="2a23b-128">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="2a23b-129">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="2a23b-129">Write Paths</span></span>



| <span data-ttu-id="2a23b-130">Ordem</span><span class="sxs-lookup"><span data-stu-id="2a23b-130">Order</span></span> | <span data-ttu-id="2a23b-131">Caminho</span><span class="sxs-lookup"><span data-stu-id="2a23b-131">Path</span></span>                       | <span data-ttu-id="2a23b-132">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="2a23b-132">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="2a23b-133">1</span><span class="sxs-lookup"><span data-stu-id="2a23b-133">1</span></span>     | <span data-ttu-id="2a23b-134">/App1/IFD/{UShort = 18249}</span><span class="sxs-lookup"><span data-stu-id="2a23b-134">/app1/ifd/{ushort=18249}</span></span>   | <span data-ttu-id="2a23b-135">ushort</span><span class="sxs-lookup"><span data-stu-id="2a23b-135">ushort</span></span>      |
| <span data-ttu-id="2a23b-136">2</span><span class="sxs-lookup"><span data-stu-id="2a23b-136">2</span></span>     | <span data-ttu-id="2a23b-137">/xmp/MicrosoftPhoto: classificação</span><span class="sxs-lookup"><span data-stu-id="2a23b-137">/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="2a23b-138">Unicode</span><span class="sxs-lookup"><span data-stu-id="2a23b-138">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="2a23b-139">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="2a23b-139">Remove Paths</span></span>



| <span data-ttu-id="2a23b-140">Ordem</span><span class="sxs-lookup"><span data-stu-id="2a23b-140">Order</span></span> | <span data-ttu-id="2a23b-141">Caminho</span><span class="sxs-lookup"><span data-stu-id="2a23b-141">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="2a23b-142">1</span><span class="sxs-lookup"><span data-stu-id="2a23b-142">1</span></span>     | <span data-ttu-id="2a23b-143">/App1/IFD/{UShort = 18249}</span><span class="sxs-lookup"><span data-stu-id="2a23b-143">/app1/ifd/{ushort=18249}</span></span>   |
| <span data-ttu-id="2a23b-144">2</span><span class="sxs-lookup"><span data-stu-id="2a23b-144">2</span></span>     | <span data-ttu-id="2a23b-145">/XMP/microsoftphoto: classificação</span><span class="sxs-lookup"><span data-stu-id="2a23b-145">/xmp/microsoftphoto:rating</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="2a23b-146">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="2a23b-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="2a23b-147">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="2a23b-147">Read Paths</span></span>



| <span data-ttu-id="2a23b-148">Ordem</span><span class="sxs-lookup"><span data-stu-id="2a23b-148">Order</span></span> | <span data-ttu-id="2a23b-149">Caminho</span><span class="sxs-lookup"><span data-stu-id="2a23b-149">Path</span></span>                           | <span data-ttu-id="2a23b-150">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="2a23b-150">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="2a23b-151">1</span><span class="sxs-lookup"><span data-stu-id="2a23b-151">1</span></span>     | <span data-ttu-id="2a23b-152">/IFD/{UShort = 18249}</span><span class="sxs-lookup"><span data-stu-id="2a23b-152">/ifd/{ushort=18249}</span></span>            | <span data-ttu-id="2a23b-153">ushort</span><span class="sxs-lookup"><span data-stu-id="2a23b-153">ushort</span></span>      |
| <span data-ttu-id="2a23b-154">2</span><span class="sxs-lookup"><span data-stu-id="2a23b-154">2</span></span>     | <span data-ttu-id="2a23b-155">/ifd/xmp/MicrosoftPhoto: classificação</span><span class="sxs-lookup"><span data-stu-id="2a23b-155">/ifd/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="2a23b-156">Unicode</span><span class="sxs-lookup"><span data-stu-id="2a23b-156">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="2a23b-157">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="2a23b-157">Write Paths</span></span>



| <span data-ttu-id="2a23b-158">Ordem</span><span class="sxs-lookup"><span data-stu-id="2a23b-158">Order</span></span> | <span data-ttu-id="2a23b-159">Caminho</span><span class="sxs-lookup"><span data-stu-id="2a23b-159">Path</span></span>                           | <span data-ttu-id="2a23b-160">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="2a23b-160">Disk Format</span></span> |
|-------|--------------------------------|-------------|
| <span data-ttu-id="2a23b-161">1</span><span class="sxs-lookup"><span data-stu-id="2a23b-161">1</span></span>     | <span data-ttu-id="2a23b-162">/IFD/{UShort = 18249}</span><span class="sxs-lookup"><span data-stu-id="2a23b-162">/ifd/{ushort=18249}</span></span>            | <span data-ttu-id="2a23b-163">ushort</span><span class="sxs-lookup"><span data-stu-id="2a23b-163">ushort</span></span>      |
| <span data-ttu-id="2a23b-164">2</span><span class="sxs-lookup"><span data-stu-id="2a23b-164">2</span></span>     | <span data-ttu-id="2a23b-165">/ifd/xmp/MicrosoftPhoto: classificação</span><span class="sxs-lookup"><span data-stu-id="2a23b-165">/ifd/xmp/MicrosoftPhoto:Rating</span></span> | <span data-ttu-id="2a23b-166">Unicode</span><span class="sxs-lookup"><span data-stu-id="2a23b-166">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="2a23b-167">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="2a23b-167">Remove Paths</span></span>



| <span data-ttu-id="2a23b-168">Ordem</span><span class="sxs-lookup"><span data-stu-id="2a23b-168">Order</span></span> | <span data-ttu-id="2a23b-169">Caminho</span><span class="sxs-lookup"><span data-stu-id="2a23b-169">Path</span></span>                           |
|-------|--------------------------------|
| <span data-ttu-id="2a23b-170">1</span><span class="sxs-lookup"><span data-stu-id="2a23b-170">1</span></span>     | <span data-ttu-id="2a23b-171">/IFD/{UShort = 18249}</span><span class="sxs-lookup"><span data-stu-id="2a23b-171">/ifd/{ushort=18249}</span></span>            |
| <span data-ttu-id="2a23b-172">2</span><span class="sxs-lookup"><span data-stu-id="2a23b-172">2</span></span>     | <span data-ttu-id="2a23b-173">/IFD/XMP/microsoftphoto: classificação</span><span class="sxs-lookup"><span data-stu-id="2a23b-173">/ifd/xmp/microsoftphoto:rating</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2a23b-174">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a23b-174">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a23b-175">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a23b-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a23b-176">System. rating</span><span class="sxs-lookup"><span data-stu-id="2a23b-176">System.Rating</span></span>](../properties/props-system-rating.md)
</dt> </dl>

 

 
