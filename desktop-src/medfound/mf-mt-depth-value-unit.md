---
description: Um valor que define as unidades para um valor de profundidade em um quadro de vídeo.
ms.assetid: 0D7238F3-C224-48BD-8654-B3182DFB244C
title: Atributo MF_MT_DEPTH_VALUE_UNIT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f6086a34f62c26b3fe1fa611318792c9056a50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780370"
---
# <a name="mf_mt_depth_value_unit-attribute"></a><span data-ttu-id="0fe60-103">\_Atributo de \_ unidade de valor de profundidade \_ \_ do MF MT</span><span class="sxs-lookup"><span data-stu-id="0fe60-103">MF\_MT\_DEPTH\_VALUE\_UNIT attribute</span></span>

<span data-ttu-id="0fe60-104">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="0fe60-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0fe60-105">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="0fe60-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0fe60-106">Um valor que define as unidades para um valor de profundidade em um quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0fe60-106">A value that defines the units for a depth value in a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="0fe60-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0fe60-107">Data type</span></span>

<span data-ttu-id="0fe60-108">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="0fe60-108">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="0fe60-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fe60-109">Remarks</span></span>

<span data-ttu-id="0fe60-110">O valor de unidade é um valor de UINT64 em comedidores, no intervalo de 1e a 9 metros.</span><span class="sxs-lookup"><span data-stu-id="0fe60-110">The unit value is a UINT64 value in nanometers, in the range 1e - 9 meters.</span></span> <span data-ttu-id="0fe60-111">Se esse valor não estiver presente, o valor padrão da unidade será 1e-3, o que indica que cada nível de pixel é medido em 1 milímetro no espaço físico.</span><span class="sxs-lookup"><span data-stu-id="0fe60-111">If this value is not present, the default value of the unit is 1e-3, which indicates each pixel level is measured in 1 millimeter in physical space.</span></span>

<span data-ttu-id="0fe60-112">As câmeras de profundidade não podem detectar a profundidade de todos os pixels.</span><span class="sxs-lookup"><span data-stu-id="0fe60-112">Depth cameras cannot sense the depth of all pixels.</span></span> <span data-ttu-id="0fe60-113">Quando a confiança de um pixel é baixa, devido ao material, oclusão ou fora do intervalo, etc, o valor de profundidade nesse pixel pode ser inválido.</span><span class="sxs-lookup"><span data-stu-id="0fe60-113">When the confidence of a pixel is low, because of material, occlusion, or out of range etc, the depth value on that pixel can be invalid.</span></span>

<span data-ttu-id="0fe60-114">Quando um valor de pixel de profundidade é 0, o pixel é inválido.</span><span class="sxs-lookup"><span data-stu-id="0fe60-114">When a depth pixel value is 0, the pixel is invalid.</span></span>

<span data-ttu-id="0fe60-115">Algumas câmeras de profundidade anexam metadados de bitmask para cada pixel, além do valor de profundidade para representar o motivo pelo qual a profundidade de pixel é inválida, devido ao material, oclusão ou fora do intervalo, etc. Recomendamos que você evite anexar esses metadados como bits em valor de profundidade, porque normalmente isso levará a dificuldade ao usar esses valores no sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="0fe60-115">Some depth cameras attach bitmask metadata for each pixel in addition to the depth value to represent the reason why the depth of pixel is invalid, due to material, occlusion or out of range etc. We recommend that you avoid attaching such metadata as bits in depth value, because it will typically lead to difficulty when using such values in pixel shader.</span></span> <span data-ttu-id="0fe60-116">Stead.</span><span class="sxs-lookup"><span data-stu-id="0fe60-116">Instead.</span></span> <span data-ttu-id="0fe60-117">Recomendamos que você use um buffer de imagem 8 bits separado com a mesma resolução e anexe-o como atributo de [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span><span class="sxs-lookup"><span data-stu-id="0fe60-117">we recommend that you use a separate 8bit image buffer with same resolution and attach it as attribute of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span> <span data-ttu-id="0fe60-118">Esses metadados variam de acordo com cada fornecedor da câmera e não são padronizados pela plataforma.</span><span class="sxs-lookup"><span data-stu-id="0fe60-118">Such metadata varies for each camera vendor and is not standardized by the platform.</span></span> <span data-ttu-id="0fe60-119">É recomendável usar 16 bits completos para o valor de profundidade para facilitar o processamento downstream e usar um valor fixo como 0 para invalidação.</span><span class="sxs-lookup"><span data-stu-id="0fe60-119">We recommend using full 16 bits for the depth value for easier processing downstream and using a fixed value such as 0 for invalidation.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fe60-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fe60-120">Requirements</span></span>



| <span data-ttu-id="0fe60-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fe60-121">Requirement</span></span> | <span data-ttu-id="0fe60-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0fe60-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0fe60-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fe60-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0fe60-124">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="0fe60-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0fe60-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fe60-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0fe60-126">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="0fe60-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="0fe60-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0fe60-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fe60-128"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fe60-128"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




