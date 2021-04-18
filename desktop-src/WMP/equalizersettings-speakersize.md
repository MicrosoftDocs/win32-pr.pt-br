---
title: EQUALIZERSETTINGS. Speakers
description: O atributo Speakize especifica ou recupera o número de índice do tamanho atual do alto-falante.
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- EQUALIZERSETTINGS. Speakers do Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26dc49af55e96d3ef8de4e8a4567b3a4296ca214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788169"
---
# <a name="equalizersettingsspeakersize"></a><span data-ttu-id="b9b1d-104">EQUALIZERSETTINGS. Speakers</span><span class="sxs-lookup"><span data-stu-id="b9b1d-104">EQUALIZERSETTINGS.speakerSize</span></span>

<span data-ttu-id="b9b1d-105">O atributo **speakize** especifica ou recupera o número de índice do tamanho atual do alto-falante.</span><span class="sxs-lookup"><span data-stu-id="b9b1d-105">The **speakerSize** attribute specifies or retrieves the index number of the current speaker size.</span></span>

``` syntax
        elementID.speakerSize
```

## <a name="possible-values"></a><span data-ttu-id="b9b1d-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="b9b1d-106">Possible Values</span></span>

<span data-ttu-id="b9b1d-107">Esse atributo é um **número** de leitura/gravação (Long) que contém um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b9b1d-107">This attribute is a read/write **Number** (long) containing one of the following values.</span></span>



| <span data-ttu-id="b9b1d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b9b1d-108">Value</span></span> | <span data-ttu-id="b9b1d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9b1d-109">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="b9b1d-110">0</span><span class="sxs-lookup"><span data-stu-id="b9b1d-110">0</span></span>     | <span data-ttu-id="b9b1d-111">Os alto-falantes atuais são fones de ouvido.</span><span class="sxs-lookup"><span data-stu-id="b9b1d-111">The current speakers are headphones.</span></span>     |
| <span data-ttu-id="b9b1d-112">1</span><span class="sxs-lookup"><span data-stu-id="b9b1d-112">1</span></span>     | <span data-ttu-id="b9b1d-113">Os alto-falantes atuais são do tamanho normal.</span><span class="sxs-lookup"><span data-stu-id="b9b1d-113">The current speakers are of normal size.</span></span> |
| <span data-ttu-id="b9b1d-114">2</span><span class="sxs-lookup"><span data-stu-id="b9b1d-114">2</span></span>     | <span data-ttu-id="b9b1d-115">Os alto-falantes atuais são grandes.</span><span class="sxs-lookup"><span data-stu-id="b9b1d-115">The current speakers are large.</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="b9b1d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9b1d-116">Remarks</span></span>

<span data-ttu-id="b9b1d-117">O nome amigável do tamanho do orador pode ser recuperado usando o atributo **currentSpeakerName** .</span><span class="sxs-lookup"><span data-stu-id="b9b1d-117">The friendly name of the speaker size can be retrieved using the **currentSpeakerName** attribute.</span></span>

<span data-ttu-id="b9b1d-118">Esse atributo será ignorado se **enhancedAudio** estiver definido como false.</span><span class="sxs-lookup"><span data-stu-id="b9b1d-118">This attribute is ignored if **enhancedAudio** is set to false.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9b1d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9b1d-119">Requirements</span></span>



| <span data-ttu-id="b9b1d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9b1d-120">Requirement</span></span> | <span data-ttu-id="b9b1d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b9b1d-121">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="b9b1d-122">Versão</span><span class="sxs-lookup"><span data-stu-id="b9b1d-122">Version</span></span><br/> | <span data-ttu-id="b9b1d-123">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="b9b1d-123">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b9b1d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9b1d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9b1d-125">**Elemento EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="b9b1d-125">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="b9b1d-126">**EQUALIZERSETTINGS.currentSpeakerName**</span><span class="sxs-lookup"><span data-stu-id="b9b1d-126">**EQUALIZERSETTINGS.currentSpeakerName**</span></span>](equalizersettings-currentspeakername.md)
</dt> <dt>

[<span data-ttu-id="b9b1d-127">**EQUALIZERSETTINGS.enhancedAudio**</span><span class="sxs-lookup"><span data-stu-id="b9b1d-127">**EQUALIZERSETTINGS.enhancedAudio**</span></span>](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 





