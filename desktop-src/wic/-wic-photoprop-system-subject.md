---
description: A política de metadados de foto para a propriedade System. Subject.
ms.assetid: 5ab7c74b-8a5e-4329-8a49-291470d406cc
title: Política de metadados de foto System. Subject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceabbab95a52a1155db949dbc60b4525dd5f9d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789234"
---
# <a name="systemsubject-photo-metadata-policy"></a><span data-ttu-id="25351-103">Política de metadados de foto System. Subject</span><span class="sxs-lookup"><span data-stu-id="25351-103">System.Subject Photo Metadata Policy</span></span>

<span data-ttu-id="25351-104">A política de metadados de foto para a propriedade [System. Subject](../properties/props-system-subject.md) .</span><span class="sxs-lookup"><span data-stu-id="25351-104">The photo metadata policy for the [System.Subject](../properties/props-system-subject.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="25351-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="25351-105">PKEY</span></span>

<span data-ttu-id="25351-106">Assunto do PKEY \_</span><span class="sxs-lookup"><span data-stu-id="25351-106">PKEY\_Subject</span></span>

### <a name="containers"></a><span data-ttu-id="25351-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="25351-107">Containers</span></span>

<span data-ttu-id="25351-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="25351-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="25351-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25351-109">Read-Only</span></span>

<span data-ttu-id="25351-110">No</span><span class="sxs-lookup"><span data-stu-id="25351-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="25351-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="25351-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="25351-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="25351-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="25351-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="25351-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="25351-114">Uma VT \_ LPWSTR ou VT \_ LPWSTR</span><span class="sxs-lookup"><span data-stu-id="25351-114">Either VT\_LPWSTR or VT\_LPWSTR</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="25351-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="25351-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="25351-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="25351-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="25351-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="25351-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="25351-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="25351-118">Read Paths</span></span>



| <span data-ttu-id="25351-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="25351-119">Order</span></span> | <span data-ttu-id="25351-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="25351-120">Path</span></span>                     | <span data-ttu-id="25351-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="25351-121">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="25351-122">1</span><span class="sxs-lookup"><span data-stu-id="25351-122">1</span></span>     | <span data-ttu-id="25351-123">/App1/IFD/{UShort = 40095}</span><span class="sxs-lookup"><span data-stu-id="25351-123">/app1/ifd/{ushort=40095}</span></span> | <span data-ttu-id="25351-124">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="25351-124">unicode\_bytes</span></span> |
| <span data-ttu-id="25351-125">2</span><span class="sxs-lookup"><span data-stu-id="25351-125">2</span></span>     | <span data-ttu-id="25351-126">/App1/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="25351-126">/app1/ifd/{ushort=270}</span></span>   | <span data-ttu-id="25351-127">ascii</span><span class="sxs-lookup"><span data-stu-id="25351-127">ascii</span></span>          |



 

### <a name="write-paths"></a><span data-ttu-id="25351-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="25351-128">Write Paths</span></span>



| <span data-ttu-id="25351-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="25351-129">Order</span></span> | <span data-ttu-id="25351-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="25351-130">Path</span></span>                     | <span data-ttu-id="25351-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="25351-131">Disk Format</span></span>    |
|-------|--------------------------|----------------|
| <span data-ttu-id="25351-132">1</span><span class="sxs-lookup"><span data-stu-id="25351-132">1</span></span>     | <span data-ttu-id="25351-133">/App1/IFD/{UShort = 40095}</span><span class="sxs-lookup"><span data-stu-id="25351-133">/app1/ifd/{ushort=40095}</span></span> | <span data-ttu-id="25351-134">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="25351-134">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="25351-135">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="25351-135">Remove Paths</span></span>



| <span data-ttu-id="25351-136">Ordem</span><span class="sxs-lookup"><span data-stu-id="25351-136">Order</span></span> | <span data-ttu-id="25351-137">Caminho</span><span class="sxs-lookup"><span data-stu-id="25351-137">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="25351-138">1</span><span class="sxs-lookup"><span data-stu-id="25351-138">1</span></span>     | <span data-ttu-id="25351-139">/App1/IFD/{UShort = 40095}</span><span class="sxs-lookup"><span data-stu-id="25351-139">/app1/ifd/{ushort=40095}</span></span> |
| <span data-ttu-id="25351-140">2</span><span class="sxs-lookup"><span data-stu-id="25351-140">2</span></span>     | <span data-ttu-id="25351-141">/App1/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="25351-141">/app1/ifd/{ushort=270}</span></span>   |



 

### <a name="tiff-policy"></a><span data-ttu-id="25351-142">Política TIFF</span><span class="sxs-lookup"><span data-stu-id="25351-142">TIFF Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="25351-143">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="25351-143">Read Paths</span></span>



| <span data-ttu-id="25351-144">Ordem</span><span class="sxs-lookup"><span data-stu-id="25351-144">Order</span></span> | <span data-ttu-id="25351-145">Caminho</span><span class="sxs-lookup"><span data-stu-id="25351-145">Path</span></span>                | <span data-ttu-id="25351-146">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="25351-146">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="25351-147">1</span><span class="sxs-lookup"><span data-stu-id="25351-147">1</span></span>     | <span data-ttu-id="25351-148">/IFD/{UShort = 40095}</span><span class="sxs-lookup"><span data-stu-id="25351-148">/ifd/{ushort=40095}</span></span> | <span data-ttu-id="25351-149">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="25351-149">unicode\_bytes</span></span> |
| <span data-ttu-id="25351-150">2</span><span class="sxs-lookup"><span data-stu-id="25351-150">2</span></span>     | <span data-ttu-id="25351-151">/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="25351-151">/ifd/{ushort=270}</span></span>   | <span data-ttu-id="25351-152">ascii</span><span class="sxs-lookup"><span data-stu-id="25351-152">ascii</span></span>          |



 

### <a name="write-paths"></a><span data-ttu-id="25351-153">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="25351-153">Write Paths</span></span>



| <span data-ttu-id="25351-154">Ordem</span><span class="sxs-lookup"><span data-stu-id="25351-154">Order</span></span> | <span data-ttu-id="25351-155">Caminho</span><span class="sxs-lookup"><span data-stu-id="25351-155">Path</span></span>                | <span data-ttu-id="25351-156">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="25351-156">Disk Format</span></span>    |
|-------|---------------------|----------------|
| <span data-ttu-id="25351-157">1</span><span class="sxs-lookup"><span data-stu-id="25351-157">1</span></span>     | <span data-ttu-id="25351-158">/IFD/{UShort = 40095}</span><span class="sxs-lookup"><span data-stu-id="25351-158">/ifd/{ushort=40095}</span></span> | <span data-ttu-id="25351-159">\_bytes Unicode</span><span class="sxs-lookup"><span data-stu-id="25351-159">unicode\_bytes</span></span> |



 

### <a name="remove-paths"></a><span data-ttu-id="25351-160">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="25351-160">Remove Paths</span></span>



| <span data-ttu-id="25351-161">Ordem</span><span class="sxs-lookup"><span data-stu-id="25351-161">Order</span></span> | <span data-ttu-id="25351-162">Caminho</span><span class="sxs-lookup"><span data-stu-id="25351-162">Path</span></span>                |
|-------|---------------------|
| <span data-ttu-id="25351-163">1</span><span class="sxs-lookup"><span data-stu-id="25351-163">1</span></span>     | <span data-ttu-id="25351-164">/IFD/{UShort = 40095}</span><span class="sxs-lookup"><span data-stu-id="25351-164">/ifd/{ushort=40095}</span></span> |
| <span data-ttu-id="25351-165">2</span><span class="sxs-lookup"><span data-stu-id="25351-165">2</span></span>     | <span data-ttu-id="25351-166">/IFD/{UShort = 270}</span><span class="sxs-lookup"><span data-stu-id="25351-166">/ifd/{ushort=270}</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="25351-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="25351-167">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="25351-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="25351-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25351-169">Sistema. Subject</span><span class="sxs-lookup"><span data-stu-id="25351-169">System.Subject</span></span>](../properties/props-system-subject.md)
</dt> </dl>

 

 
