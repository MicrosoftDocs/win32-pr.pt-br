---
title: WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR (Wmsdkidl. h)
description: A transição de fade-to-Color elimina da imagem até um quadro de cor sólida.
ms.assetid: 4ec52682-1ca2-436d-b7ce-2a9d407ff50e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3873a24cee74e8cad3f6cd91d39f20a72ffa8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761140"
---
# <a name="wmt_videoimage_transition_fade_to_color"></a><span data-ttu-id="6c23d-104">WMT \_ \_ transição \_ de VIDEOIMAGE esmaecer \_ para \_ cor</span><span class="sxs-lookup"><span data-stu-id="6c23d-104">WMT\_VIDEOIMAGE\_TRANSITION\_FADE\_TO\_COLOR</span></span>

<span data-ttu-id="6c23d-105">A transição de fade-to-Color elimina da imagem até um quadro de cor sólida.</span><span class="sxs-lookup"><span data-stu-id="6c23d-105">The fade-to-color transition dissolves from the image to a frame of solid color.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c23d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c23d-106">Parameters</span></span>

<span data-ttu-id="6c23d-107">A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.</span><span class="sxs-lookup"><span data-stu-id="6c23d-107">The following table describes the parameters used by this transition and lists the members of the [**WMT\_VIDEOIMAGE\_SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) structure to which they are assigned.</span></span>



| <span data-ttu-id="6c23d-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c23d-108">Parameter</span></span>         | <span data-ttu-id="6c23d-109">Membro da estrutura</span><span class="sxs-lookup"><span data-stu-id="6c23d-109">Structure member</span></span> | <span data-ttu-id="6c23d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6c23d-110">Description</span></span>                                                                                                                                                                                                               |
|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c23d-111">Vermelho</span><span class="sxs-lookup"><span data-stu-id="6c23d-111">Red</span></span>               | <span data-ttu-id="6c23d-112">**fEffectPara0**</span><span class="sxs-lookup"><span data-stu-id="6c23d-112">**fEffectPara0**</span></span> | <span data-ttu-id="6c23d-113">Valor vermelho da cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="6c23d-113">Red value of the background color.</span></span> <span data-ttu-id="6c23d-114">Defina como um número entre 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="6c23d-114">Set to a number between 0 and 255.</span></span>                                                                                                                                                     |
| <span data-ttu-id="6c23d-115">Verde</span><span class="sxs-lookup"><span data-stu-id="6c23d-115">Green</span></span>             | <span data-ttu-id="6c23d-116">**fEffectPara1**</span><span class="sxs-lookup"><span data-stu-id="6c23d-116">**fEffectPara1**</span></span> | <span data-ttu-id="6c23d-117">Valor verde da cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="6c23d-117">Green value of the background color.</span></span> <span data-ttu-id="6c23d-118">Defina como um número entre 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="6c23d-118">Set to a number between 0 and 255.</span></span>                                                                                                                                                   |
| <span data-ttu-id="6c23d-119">Azul</span><span class="sxs-lookup"><span data-stu-id="6c23d-119">Blue</span></span>              | <span data-ttu-id="6c23d-120">**fEffectPara2**</span><span class="sxs-lookup"><span data-stu-id="6c23d-120">**fEffectPara2**</span></span> | <span data-ttu-id="6c23d-121">Valor azul da cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="6c23d-121">Blue value of the background color.</span></span> <span data-ttu-id="6c23d-122">Defina como um número entre 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="6c23d-122">Set to a number between 0 and 255.</span></span>                                                                                                                                                    |
| <span data-ttu-id="6c23d-123">Peso do plano de fundo</span><span class="sxs-lookup"><span data-stu-id="6c23d-123">Background weight</span></span> | <span data-ttu-id="6c23d-124">**fEffectPara3**</span><span class="sxs-lookup"><span data-stu-id="6c23d-124">**fEffectPara3**</span></span> | <span data-ttu-id="6c23d-125">Peso da cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="6c23d-125">Weight of the background color.</span></span> <span data-ttu-id="6c23d-126">Esse parâmetro expressa a porcentagem da cor do plano de fundo na combinação como um decimal.</span><span class="sxs-lookup"><span data-stu-id="6c23d-126">This parameter expresses the percentage of the background color in the mix as a decimal.</span></span> <span data-ttu-id="6c23d-127">Por exemplo, para misturar a cor do plano de fundo em 30%, tornando a imagem 70% da combinação, defina como 0,30.</span><span class="sxs-lookup"><span data-stu-id="6c23d-127">For example, to blend the background color at 30%, making the image 70% of the mix, set to 0.30.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="6c23d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c23d-128">Requirements</span></span>



| <span data-ttu-id="6c23d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c23d-129">Requirement</span></span> | <span data-ttu-id="6c23d-130">Valor</span><span class="sxs-lookup"><span data-stu-id="6c23d-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c23d-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c23d-131">Header</span></span><br/> | <dl> <span data-ttu-id="6c23d-132"><dt>Wmsdkidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c23d-132"><dt>Wmsdkidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c23d-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c23d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c23d-134">**Transições de imagem de vídeo**</span><span class="sxs-lookup"><span data-stu-id="6c23d-134">**Video Image Transitions**</span></span>](video-image-transitions.md)
</dt> </dl>

 

 





