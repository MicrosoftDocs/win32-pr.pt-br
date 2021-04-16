---
description: Um valor que define o sistema de medidas para um valor de profundidade em um quadro de vídeo.
ms.assetid: 7BFA846B-E614-4117-A196-298E065CB7F8
title: Atributo MF_MT_DEPTH_MEASUREMENT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8be6c06ea09f4017ae65935081eaa81d1ad00cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558015"
---
# <a name="mf_mt_depth_measurement-attribute"></a><span data-ttu-id="022ff-103">\_Atributo de \_ medida de profundidade do MF MT \_</span><span class="sxs-lookup"><span data-stu-id="022ff-103">MF\_MT\_DEPTH\_MEASUREMENT attribute</span></span>

<span data-ttu-id="022ff-104">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="022ff-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="022ff-105">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="022ff-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="022ff-106">Um valor que define o sistema de medidas para um valor de profundidade em um quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="022ff-106">A value that defines the measurement system for a depth value in a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="022ff-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="022ff-107">Data type</span></span>

<span data-ttu-id="022ff-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="022ff-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="022ff-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="022ff-109">Remarks</span></span>

<span data-ttu-id="022ff-110">Esse valor é um membro da enumeração [**\_ MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement)</span><span class="sxs-lookup"><span data-stu-id="022ff-110">This value is a member of the [**\_MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement) enumeration</span></span>

<span data-ttu-id="022ff-111">Se esse atributo não estiver presente, supõe-se que seja **DistanceToFocalPlane**.</span><span class="sxs-lookup"><span data-stu-id="022ff-111">If this attribute is not present it is assumed to be **DistanceToFocalPlane**.</span></span> <span data-ttu-id="022ff-112">Normalmente, a distância para o plano focal é mais fácil de consumir em um sistema de coordenadas euclidiana 3D.</span><span class="sxs-lookup"><span data-stu-id="022ff-112">The distance to focal plane is typically easier to consume in a 3D Euclidian coordinate system.</span></span>

![ilustração de distancetofocalplane](images/distance-to-focal-plane.png)

<span data-ttu-id="022ff-114">A distância para o formato do centro focal é normalmente dados brutos do sensor, como o tempo de câmeras de voo.</span><span class="sxs-lookup"><span data-stu-id="022ff-114">The distance to focal center format is typically raw data from sensor such as time of flight cameras.</span></span>

![ilustração de distancetoopticalcenter](images/distance-to-optical-center.png)

<span data-ttu-id="022ff-116">As câmeras de profundidade não podem detectar a profundidade de todos os pixels.</span><span class="sxs-lookup"><span data-stu-id="022ff-116">Depth cameras cannot sense the depth of all pixels.</span></span> <span data-ttu-id="022ff-117">Quando a confiança de um pixel é baixa, devido ao material, oclusão ou fora do intervalo, etc, o valor de profundidade nesse pixel pode ser inválido.</span><span class="sxs-lookup"><span data-stu-id="022ff-117">When the confidence of a pixel is low, because of material, occlusion, or out of range etc, the depth value on that pixel can be invalid.</span></span>

<span data-ttu-id="022ff-118">Quando um valor de pixel de profundidade é 0, o pixel é inválido.</span><span class="sxs-lookup"><span data-stu-id="022ff-118">When a depth pixel value is 0, the pixel is invalid.</span></span>

<span data-ttu-id="022ff-119">Algumas câmeras de profundidade anexam metadados de bitmask para cada pixel, além do valor de profundidade para representar o motivo pelo qual a profundidade de pixel é inválida, devido ao material, oclusão ou fora do intervalo, etc. Recomendamos que você evite anexar esses metadados como bits em valor de profundidade, porque normalmente isso levará a dificuldade ao usar esses valores no sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="022ff-119">Some depth cameras attach bitmask metadata for each pixel in addition to the depth value to represent the reason why the depth of pixel is invalid, due to material, occlusion or out of range etc. We recommend that you avoid attaching such metadata as bits in depth value, because it will typically lead to difficulty when using such values in pixel shader.</span></span> <span data-ttu-id="022ff-120">Stead.</span><span class="sxs-lookup"><span data-stu-id="022ff-120">Instead.</span></span> <span data-ttu-id="022ff-121">Recomendamos que você use um buffer de imagem 8 bits separado com a mesma resolução e anexe-o como atributo de [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span><span class="sxs-lookup"><span data-stu-id="022ff-121">we recommend that you use a separate 8bit image buffer with same resolution and attach it as attribute of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span> <span data-ttu-id="022ff-122">Esses metadados variam de acordo com cada fornecedor da câmera e não são padronizados pela plataforma.</span><span class="sxs-lookup"><span data-stu-id="022ff-122">Such metadata varies for each camera vendor and is not standardized by the platform.</span></span> <span data-ttu-id="022ff-123">É recomendável usar 16 bits completos para o valor de profundidade para facilitar o processamento downstream e usar um valor fixo como 0 para invalidação.</span><span class="sxs-lookup"><span data-stu-id="022ff-123">We recommend using full 16 bits for the depth value for easier processing downstream and using a fixed value such as 0 for invalidation.</span></span>

## <a name="requirements"></a><span data-ttu-id="022ff-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="022ff-124">Requirements</span></span>



| <span data-ttu-id="022ff-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="022ff-125">Requirement</span></span> | <span data-ttu-id="022ff-126">Valor</span><span class="sxs-lookup"><span data-stu-id="022ff-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="022ff-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="022ff-127">Minimum supported client</span></span><br/> | <span data-ttu-id="022ff-128">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="022ff-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="022ff-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="022ff-129">Minimum supported server</span></span><br/> | <span data-ttu-id="022ff-130">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="022ff-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="022ff-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="022ff-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="022ff-132"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="022ff-132"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




