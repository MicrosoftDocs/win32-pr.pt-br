---
description: A política de metadados de foto para a propriedade System. DateAcquired.
ms.assetid: 04a61ecc-d168-4f93-b143-3e6ba8aaf322
title: Política de metadados de foto System. DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f126ccb4424d1489f671f61f719a505559a78c8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171522"
---
# <a name="systemdateacquired-photo-metadata-policy"></a><span data-ttu-id="82e5c-103">Política de metadados de foto System. DateAcquired</span><span class="sxs-lookup"><span data-stu-id="82e5c-103">System.DateAcquired Photo Metadata Policy</span></span>

<span data-ttu-id="82e5c-104">A política de metadados de foto para a propriedade [System. DateAcquired](../properties/props-system-dateacquired.md) .</span><span class="sxs-lookup"><span data-stu-id="82e5c-104">The photo metadata policy for the [System.DateAcquired](../properties/props-system-dateacquired.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="82e5c-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="82e5c-105">PKEY</span></span>

<span data-ttu-id="82e5c-106">PKEY \_ DateAcquired</span><span class="sxs-lookup"><span data-stu-id="82e5c-106">PKEY\_DateAcquired</span></span>

### <a name="containers"></a><span data-ttu-id="82e5c-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="82e5c-107">Containers</span></span>

<span data-ttu-id="82e5c-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="82e5c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="82e5c-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="82e5c-109">Read-Only</span></span>

<span data-ttu-id="82e5c-110">No</span><span class="sxs-lookup"><span data-stu-id="82e5c-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="82e5c-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="82e5c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="82e5c-112">FILETIME do VT \_</span><span class="sxs-lookup"><span data-stu-id="82e5c-112">VT\_FILETIME</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="82e5c-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="82e5c-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="82e5c-114">FILETIME do VT \_</span><span class="sxs-lookup"><span data-stu-id="82e5c-114">VT\_FILETIME</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="82e5c-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="82e5c-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="82e5c-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="82e5c-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="82e5c-117">Precedência de caminhos (JPEG)</span><span class="sxs-lookup"><span data-stu-id="82e5c-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="82e5c-118">Se o arquivo estiver no formato JPEG, o manipulador pesquisará os dados na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="82e5c-118">If the file is in JPEG format, the handler searches for the data in the following order:</span></span>



| <span data-ttu-id="82e5c-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="82e5c-119">Order</span></span> | <span data-ttu-id="82e5c-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="82e5c-120">Path</span></span>                             | <span data-ttu-id="82e5c-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="82e5c-121">Disk Format</span></span>                        | <span data-ttu-id="82e5c-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="82e5c-122">Required</span></span> |
|-------|----------------------------------|------------------------------------|----------|
| <span data-ttu-id="82e5c-123">1</span><span class="sxs-lookup"><span data-stu-id="82e5c-123">1</span></span>     | <span data-ttu-id="82e5c-124">/xmp/MicrosoftPhoto:DateAcquired</span><span class="sxs-lookup"><span data-stu-id="82e5c-124">/xmp/MicrosoftPhoto:DateAcquired</span></span> | <span data-ttu-id="82e5c-125">Cadeia de caracteres Unicode no formato de data XMP.</span><span class="sxs-lookup"><span data-stu-id="82e5c-125">Unicode string in XMP date format.</span></span> | <span data-ttu-id="82e5c-126">Yes</span><span class="sxs-lookup"><span data-stu-id="82e5c-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="82e5c-127">Precedência de caminhos (TIFF)</span><span class="sxs-lookup"><span data-stu-id="82e5c-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="82e5c-128">Se o arquivo estiver no formato TIFF, o manipulador pesquisará os dados na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="82e5c-128">If the file is in TIFF format, the handler searches for the data in the following order:</span></span>



| <span data-ttu-id="82e5c-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="82e5c-129">Order</span></span> | <span data-ttu-id="82e5c-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="82e5c-130">Path</span></span>                                 | <span data-ttu-id="82e5c-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="82e5c-131">Disk Format</span></span>                        | <span data-ttu-id="82e5c-132">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="82e5c-132">Required</span></span> |
|-------|--------------------------------------|------------------------------------|----------|
| <span data-ttu-id="82e5c-133">1</span><span class="sxs-lookup"><span data-stu-id="82e5c-133">1</span></span>     | <span data-ttu-id="82e5c-134">/ifd/xmp/MicrosoftPhoto:DateAcquired</span><span class="sxs-lookup"><span data-stu-id="82e5c-134">/ifd/xmp/MicrosoftPhoto:DateAcquired</span></span> | <span data-ttu-id="82e5c-135">Cadeia de caracteres Unicode no formato de data XMP.</span><span class="sxs-lookup"><span data-stu-id="82e5c-135">Unicode string in XMP date format.</span></span> | <span data-ttu-id="82e5c-136">Yes</span><span class="sxs-lookup"><span data-stu-id="82e5c-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="82e5c-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="82e5c-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="82e5c-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82e5c-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82e5c-139">System. DateAcquired</span><span class="sxs-lookup"><span data-stu-id="82e5c-139">System.DateAcquired</span></span>](../properties/props-system-dateacquired.md)
</dt> </dl>

 

 
