---
title: EQUALIZERSETTINGS. fading cruzado
description: O atributo fading cruzado especifica ou recupera um valor que indica se o esmaecimento cruzado está habilitado.
ms.assetid: 6c5a31f3-982e-4660-80ff-30b7a4290a15
keywords:
- EQUALIZERSETTINGS. fading cruzado Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.crossFade
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0472f90f94b5c4ba56948848476b6585502427c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760448"
---
# <a name="equalizersettingscrossfade"></a><span data-ttu-id="17b8b-104">EQUALIZERSETTINGS. fading cruzado</span><span class="sxs-lookup"><span data-stu-id="17b8b-104">EQUALIZERSETTINGS.crossFade</span></span>

<span data-ttu-id="17b8b-105">O atributo **fading cruzado** especifica ou recupera um valor que indica se o esmaecimento cruzado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="17b8b-105">The **crossFade** attribute specifies or retrieves a value indicating whether cross-fade is enabled.</span></span>

``` syntax
        elementID.crossFade
```

## <a name="possible-values"></a><span data-ttu-id="17b8b-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="17b8b-106">Possible Values</span></span>

<span data-ttu-id="17b8b-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="17b8b-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="17b8b-108">Valor</span><span class="sxs-lookup"><span data-stu-id="17b8b-108">Value</span></span> | <span data-ttu-id="17b8b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="17b8b-109">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="17b8b-110">true</span><span class="sxs-lookup"><span data-stu-id="17b8b-110">true</span></span>  | <span data-ttu-id="17b8b-111">O esmaecimento cruzado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="17b8b-111">Cross-fade is enabled.</span></span>           |
| <span data-ttu-id="17b8b-112">false</span><span class="sxs-lookup"><span data-stu-id="17b8b-112">false</span></span> | <span data-ttu-id="17b8b-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="17b8b-113">Default.</span></span> <span data-ttu-id="17b8b-114">O esmaecimento cruzado está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="17b8b-114">Cross-fade is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="17b8b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="17b8b-115">Remarks</span></span>

<span data-ttu-id="17b8b-116">Cross-esmaecimento é um recurso de processamento de áudio que diminui gradualmente o volume de um item de mídia próximo ao final de sua reprodução enquanto inicia simultaneamente a reprodução do próximo item de mídia no volume mínimo e o aumenta gradualmente para o volume normal.</span><span class="sxs-lookup"><span data-stu-id="17b8b-116">Cross-fade is an audio processing feature that gradually decreases the volume of one media item near the end of its playback while simultaneously starting playback of the next media item at minimum volume and gradually increasing it to normal volume.</span></span> <span data-ttu-id="17b8b-117">A sobreposição entre o início do segundo item de mídia e o final do primeiro item de mídia é especificado pelo atributo **crossFadeWindow** .</span><span class="sxs-lookup"><span data-stu-id="17b8b-117">The overlap between the start of the second media item and the end of the first media item is specified by the **crossFadeWindow** attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="17b8b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17b8b-118">Requirements</span></span>



| <span data-ttu-id="17b8b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="17b8b-119">Requirement</span></span> | <span data-ttu-id="17b8b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="17b8b-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="17b8b-121">Versão</span><span class="sxs-lookup"><span data-stu-id="17b8b-121">Version</span></span><br/> | <span data-ttu-id="17b8b-122">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="17b8b-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="17b8b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="17b8b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b8b-124">**Elemento EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="17b8b-124">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="17b8b-125">**EQUALIZERSETTINGS.crossFadeWindow**</span><span class="sxs-lookup"><span data-stu-id="17b8b-125">**EQUALIZERSETTINGS.crossFadeWindow**</span></span>](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 





