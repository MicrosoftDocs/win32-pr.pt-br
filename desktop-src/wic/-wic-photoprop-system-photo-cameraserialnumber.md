---
description: A política de metadados de foto para a propriedade System. Photo. CameraSerialNumber.
ms.assetid: 85f78f45-5e76-4d52-88a2-ac3c9e2b6a1e
title: Política de metadados de foto System. Photo. CameraSerialNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c329cd4c56b49e39de5da97ac9d9f8b14bffb64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759995"
---
# <a name="systemphotocameraserialnumber-photo-metadata-policy"></a><span data-ttu-id="7d072-103">Política de metadados de foto System. Photo. CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="7d072-103">System.Photo.CameraSerialNumber Photo Metadata Policy</span></span>

<span data-ttu-id="7d072-104">A política de metadados de foto para a propriedade [System. Photo. CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md) .</span><span class="sxs-lookup"><span data-stu-id="7d072-104">The photo metadata policy for the [System.Photo.CameraSerialNumber](../properties/props-system-photo-cameraserialnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="7d072-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="7d072-105">PKEY</span></span>

<span data-ttu-id="7d072-106">PKEY \_ Photo \_ CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="7d072-106">PKEY\_Photo\_CameraSerialNumber</span></span>

### <a name="containers"></a><span data-ttu-id="7d072-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="7d072-107">Containers</span></span>

<span data-ttu-id="7d072-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7d072-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="7d072-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7d072-109">Read-Only</span></span>

<span data-ttu-id="7d072-110">No</span><span class="sxs-lookup"><span data-stu-id="7d072-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="7d072-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="7d072-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="7d072-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="7d072-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="7d072-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="7d072-113">Input Type</span></span>

<span data-ttu-id="7d072-114">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7d072-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="7d072-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="7d072-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="7d072-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="7d072-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="7d072-117">Precedência de caminhos (JPEG)</span><span class="sxs-lookup"><span data-stu-id="7d072-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="7d072-118">Se o arquivo estiver no formato JPEG, o manipulador lerá, gravará e removerá os dados do seguinte caminho:</span><span class="sxs-lookup"><span data-stu-id="7d072-118">If the file is in JPEG format, the handler will read, write, and remove the data from the following path:</span></span>



| <span data-ttu-id="7d072-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="7d072-119">Order</span></span> | <span data-ttu-id="7d072-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="7d072-120">Path</span></span>                                   | <span data-ttu-id="7d072-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7d072-121">Disk Format</span></span> | <span data-ttu-id="7d072-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7d072-122">Required</span></span> |
|-------|----------------------------------------|-------------|----------|
| <span data-ttu-id="7d072-123">1</span><span class="sxs-lookup"><span data-stu-id="7d072-123">1</span></span>     | <span data-ttu-id="7d072-124">/xmp/MicrosoftPhoto:CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="7d072-124">/xmp/MicrosoftPhoto:CameraSerialNumber</span></span> | <span data-ttu-id="7d072-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="7d072-125">Unicode</span></span>     | <span data-ttu-id="7d072-126">Yes</span><span class="sxs-lookup"><span data-stu-id="7d072-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="7d072-127">Precedência de caminhos (TIFF)</span><span class="sxs-lookup"><span data-stu-id="7d072-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="7d072-128">Se o arquivo estiver no formato TIFF, o manipulador lerá, gravará e removerá os dados do seguinte caminho</span><span class="sxs-lookup"><span data-stu-id="7d072-128">If the file is in TIFF format, the handler will read, write, and remove the data from the following path</span></span>



| <span data-ttu-id="7d072-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="7d072-129">Order</span></span> | <span data-ttu-id="7d072-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="7d072-130">Path</span></span>                                       | <span data-ttu-id="7d072-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7d072-131">Disk Format</span></span> | <span data-ttu-id="7d072-132">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7d072-132">Required</span></span> |
|-------|--------------------------------------------|-------------|----------|
| <span data-ttu-id="7d072-133">1</span><span class="sxs-lookup"><span data-stu-id="7d072-133">1</span></span>     | <span data-ttu-id="7d072-134">/ifd/xmp/MicrosoftPhoto:CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="7d072-134">/ifd/xmp/MicrosoftPhoto:CameraSerialNumber</span></span> | <span data-ttu-id="7d072-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="7d072-135">Unicode</span></span>     | <span data-ttu-id="7d072-136">Yes</span><span class="sxs-lookup"><span data-stu-id="7d072-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="7d072-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d072-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d072-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d072-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d072-139">System. Photo. CameraSerialNumber</span><span class="sxs-lookup"><span data-stu-id="7d072-139">System.Photo.CameraSerialNumber</span></span>](../properties/props-system-photo-cameraserialnumber.md)
</dt> </dl>

 

 
