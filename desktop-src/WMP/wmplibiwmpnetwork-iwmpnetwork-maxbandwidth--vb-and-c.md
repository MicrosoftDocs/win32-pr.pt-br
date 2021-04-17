---
title: Propriedade IWMPNetwork maxBandwidth
description: A propriedade maxBandwidth Obtém ou define a largura de banda máxima permitida.
ms.assetid: ff7548d8-b80f-4cb4-bdd6-86d585fef329
keywords:
- Propriedade maxBandwidth Windows Media Player
- Propriedade maxBandwidth Windows Media Player, interface IWMPNetwork
- Interface IWMPNetwork Windows Media Player, Propriedade maxBandwidth
topic_type:
- apiref
api_name:
- IWMPNetwork.maxBandwidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3620d609db0f1786da673923f54d726b3c99994a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747283"
---
# <a name="iwmpnetworkmaxbandwidth-property"></a><span data-ttu-id="f6324-106">Propriedade IWMPNetwork:: maxBandwidth</span><span class="sxs-lookup"><span data-stu-id="f6324-106">IWMPNetwork::maxBandwidth property</span></span>

<span data-ttu-id="f6324-107">A propriedade **maxBandwidth** Obtém ou define a largura de banda máxima permitida.</span><span class="sxs-lookup"><span data-stu-id="f6324-107">The **maxBandwidth** property gets or sets the maximum allowed bandwidth.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6324-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6324-108">Syntax</span></span>


```CSharp
public System.Int32 maxBandwidth {get; set;}
```


```VB

Public Property maxBandwidth As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="f6324-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f6324-109">Property value</span></span>

<span data-ttu-id="f6324-110">Um **System. Int32** que é a largura de banda máxima.</span><span class="sxs-lookup"><span data-stu-id="f6324-110">A **System.Int32** that is the maximum bandwidth.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6324-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6324-111">Remarks</span></span>

<span data-ttu-id="f6324-112">Esta propriedade não tem um valor padrão.</span><span class="sxs-lookup"><span data-stu-id="f6324-112">This property does not have a default value.</span></span> <span data-ttu-id="f6324-113">O valor pode ser especificado enquanto o Windows Media Player está em execução, mas a alteração não entrará em vigor até que o item de mídia atual seja liberado abrindo outro ou chamando **AxWindowsMediaPlayer. Close**.</span><span class="sxs-lookup"><span data-stu-id="f6324-113">The value can be specified while Windows Media Player is playing, but the change will not take effect until the current media item is released by opening another one or by calling **AxWindowsMediaPlayer.close**.</span></span> <span data-ttu-id="f6324-114">O Windows Media Player tenta atingir a maior largura de banda possível.</span><span class="sxs-lookup"><span data-stu-id="f6324-114">Windows Media Player attempts to achieve the highest bandwidth possible.</span></span> <span data-ttu-id="f6324-115">Nenhuma redução intencional da largura de banda ocorrerá a menos que esse valor seja definido.</span><span class="sxs-lookup"><span data-stu-id="f6324-115">No intentional reduction of bandwidth will occur unless this value is set.</span></span>

<span data-ttu-id="f6324-116">Essa configuração é útil para reduzir a quantidade de largura de banda usada, principalmente no caso de um fluxo de taxa de bits múltipla (MBR).</span><span class="sxs-lookup"><span data-stu-id="f6324-116">This setting is useful for reducing the amount of bandwidth used, particularly in the case of a multiple bit rate (MBR) stream.</span></span> <span data-ttu-id="f6324-117">Um fluxo MBR contém vários fluxos com taxas de bits diferentes.</span><span class="sxs-lookup"><span data-stu-id="f6324-117">An MBR stream contains multiple streams with different bit rates.</span></span> <span data-ttu-id="f6324-118">Em alguns casos, pode ser desejável usar um fluxo com uma taxa de bits inferior à necessária pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="f6324-118">In some cases, it may be desirable to use a stream with a lower bit rate than the client requires.</span></span> <span data-ttu-id="f6324-119">Nesse caso, a especificação de uma taxa de bits inferior com a propriedade **IWMPNetwork. maxBandwidth** selecionará um fluxo de taxa de bits inferior.</span><span class="sxs-lookup"><span data-stu-id="f6324-119">In this case, specifying a lower bit rate with the **IWMPNetwork.maxBandwidth** property will select a lower bit-rate stream.</span></span> <span data-ttu-id="f6324-120">Por exemplo, um fluxo MBR pode incluir fluxos codificados a 20 kilobits por segundo (Kbps), 37 kbps e 200 Kbps.</span><span class="sxs-lookup"><span data-stu-id="f6324-120">For example, an MBR stream might include streams encoded at 20 kilobits per second (Kbps), 37 Kbps, and 200 Kbps.</span></span> <span data-ttu-id="f6324-121">Usar **IWMPNetwork. maxBandwidth** para especificar uma taxa de bits de 50.000 (50 kbps) selecionará o fluxo de 37 Kbps em vez do fluxo de 200 Kbps.</span><span class="sxs-lookup"><span data-stu-id="f6324-121">Using **IWMPNetwork.maxBandwidth** to specify a bit rate of 50,000 (50 Kbps) will select the 37 Kbps stream instead of the 200 Kbps stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6324-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6324-122">Requirements</span></span>



| <span data-ttu-id="f6324-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6324-123">Requirement</span></span> | <span data-ttu-id="f6324-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f6324-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6324-125">Versão</span><span class="sxs-lookup"><span data-stu-id="f6324-125">Version</span></span><br/>   | <span data-ttu-id="f6324-126">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="f6324-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f6324-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="f6324-127">Namespace</span></span><br/> | <span data-ttu-id="f6324-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f6324-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f6324-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="f6324-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f6324-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f6324-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6324-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6324-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6324-132">**AxWindowsMediaPlayer. Close (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f6324-132">**AxWindowsMediaPlayer.close (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[<span data-ttu-id="f6324-133">**Interface IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f6324-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





