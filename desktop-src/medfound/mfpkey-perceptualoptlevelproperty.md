---
description: Especifica se o codec deve usar a otimização de perceptiva conservadora durante a codificação.
ms.assetid: f44fd932-d8f8-46c7-b17c-27e6141408ab
title: Propriedade MFPKEY_PERCEPTUALOPTLEVEL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d86857ca9d7e4205afc0baf9c212e92606511ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165381"
---
# <a name="mfpkey_perceptualoptlevel-property"></a><span data-ttu-id="6e1fd-103">\_Propriedade MFPKEY PERCEPTUALOPTLEVEL</span><span class="sxs-lookup"><span data-stu-id="6e1fd-103">MFPKEY\_PERCEPTUALOPTLEVEL Property</span></span>

<span data-ttu-id="6e1fd-104">Especifica se o codec deve usar a otimização de perceptiva conservadora durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="6e1fd-104">Specifies whether the codec should use conservative perceptual optimization when encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="6e1fd-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="6e1fd-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="6e1fd-106">g \_ wszWMVCPerceptualOptLevel</span><span class="sxs-lookup"><span data-stu-id="6e1fd-106">g\_wszWMVCPerceptualOptLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="6e1fd-107">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="6e1fd-107">Data Type</span></span>

<span data-ttu-id="6e1fd-108">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="6e1fd-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="6e1fd-109">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="6e1fd-109">Default Value</span></span>

<span data-ttu-id="6e1fd-110">0</span><span class="sxs-lookup"><span data-stu-id="6e1fd-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="6e1fd-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e1fd-111">Remarks</span></span>

<span data-ttu-id="6e1fd-112">A otimização de perceptiva conservadora é um processo pelo qual o codec tenta identificar regiões "importantes" e "não importantes" no quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6e1fd-112">Conservative perceptual optimization is a process by which the codec attempts to identify "important" and "unimportant" regions in the video frame.</span></span> <span data-ttu-id="6e1fd-113">Depois de identificar essas regiões do quadro, o codec dará uma prioridade mais alta à qualidade das regiões importantes, às custas da qualidade de regiões não importantes.</span><span class="sxs-lookup"><span data-stu-id="6e1fd-113">After identifying these regions of the frame, the codec will give a higher priority to the quality of important regions, at the expense of the quality of unimportant regions.</span></span>

<span data-ttu-id="6e1fd-114">A otimização de perceptiva enfatiza a aparência da imagem correta para o olho humano, em vez de insistir na precisão matemática estrita.</span><span class="sxs-lookup"><span data-stu-id="6e1fd-114">Perceptual optimization emphasizes making the image appear correct to the human eye instead of insisting on strict mathematical accuracy.</span></span>

<span data-ttu-id="6e1fd-115">Os resultados da otimização irão variar consideravelmente dependendo do tipo de vídeo que está sendo codificado.</span><span class="sxs-lookup"><span data-stu-id="6e1fd-115">The results of the optimization will vary considerably depending on the type of video being encoded.</span></span> <span data-ttu-id="6e1fd-116">Esse recurso pode ser adequado para a baixa taxa de bits e a codificação de baixa resolução (por exemplo, web streaming), mas provavelmente deve ser evitado ao mirar a qualidade do vídeo de arquivamento.</span><span class="sxs-lookup"><span data-stu-id="6e1fd-116">This feature could be well suited for low bit-rate and low resolution encoding (for example, web streaming), but should probably be avoided when aiming for archival video quality.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e1fd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e1fd-117">Requirements</span></span>



| <span data-ttu-id="6e1fd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e1fd-118">Requirement</span></span> | <span data-ttu-id="6e1fd-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6e1fd-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e1fd-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e1fd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6e1fd-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6e1fd-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6e1fd-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e1fd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6e1fd-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6e1fd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6e1fd-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e1fd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e1fd-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e1fd-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e1fd-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e1fd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e1fd-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6e1fd-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




