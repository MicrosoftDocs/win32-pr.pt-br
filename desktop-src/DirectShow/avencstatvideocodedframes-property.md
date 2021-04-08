---
description: Retorna o número de quadros de vídeo que foram codificados.
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: Propriedade AVEncStatVideoCodedFrames (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aed3ed0a06003807a6bd0db90b8978282042daf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087701"
---
# <a name="avencstatvideocodedframes-property"></a><span data-ttu-id="44331-103">Propriedade AVEncStatVideoCodedFrames</span><span class="sxs-lookup"><span data-stu-id="44331-103">AVEncStatVideoCodedFrames property</span></span>

<span data-ttu-id="44331-104">Retorna o número de quadros de vídeo que foram codificados.</span><span class="sxs-lookup"><span data-stu-id="44331-104">Returns the number of video frames that were encoded.</span></span>

<span data-ttu-id="44331-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="44331-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="44331-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="44331-106">Data type</span></span>

<span data-ttu-id="44331-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="44331-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="44331-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="44331-108">Property GUID</span></span>

<span data-ttu-id="44331-109">**CODECAPI \_ AVEncStatVideoCodedFrames**</span><span class="sxs-lookup"><span data-stu-id="44331-109">**CODECAPI\_AVEncStatVideoCodedFrames**</span></span>

## <a name="remarks"></a><span data-ttu-id="44331-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="44331-110">Remarks</span></span>

<span data-ttu-id="44331-111">Essa propriedade estará disponível após a conclusão da codificação.</span><span class="sxs-lookup"><span data-stu-id="44331-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="44331-112">O valor dessa propriedade é igual à propriedade [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) menos o número de quadros descartados.</span><span class="sxs-lookup"><span data-stu-id="44331-112">The value of this property is equal to the [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) property minus the number of dropped frames.</span></span> <span data-ttu-id="44331-113">O codificador pode descartar quadros para permanecer dentro das restrições de taxa de bits especificadas.</span><span class="sxs-lookup"><span data-stu-id="44331-113">The encoder might drop frames to stay within the specified bit rate constraints.</span></span> <span data-ttu-id="44331-114">Ele também pode descartar quadros no final do fluxo (consulte a propriedade [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="44331-114">It might also drop frames at the end of the stream (see [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md) property).</span></span>

## <a name="requirements"></a><span data-ttu-id="44331-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44331-115">Requirements</span></span>



| <span data-ttu-id="44331-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="44331-116">Requirement</span></span> | <span data-ttu-id="44331-117">Valor</span><span class="sxs-lookup"><span data-stu-id="44331-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44331-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44331-118">Minimum supported client</span></span><br/> | <span data-ttu-id="44331-119">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="44331-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="44331-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44331-120">Minimum supported server</span></span><br/> | <span data-ttu-id="44331-121">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="44331-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="44331-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44331-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="44331-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="44331-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44331-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="44331-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44331-125">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="44331-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="44331-126">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="44331-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




