---
title: Network. maxBandwidth
description: A propriedade maxBandwidth especifica ou recupera a largura de banda máxima permitida.
ms.assetid: 303acf51-8d3a-4e58-8aa8-c0b6db1e4fbb
keywords:
- Network. maxBandwidth Windows Media Player
topic_type:
- apiref
api_name:
- Network.maxBandwidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbe8283c4cc756a4f88fad1240df3a757b53a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752187"
---
# <a name="networkmaxbandwidth"></a><span data-ttu-id="793fc-104">Network. maxBandwidth</span><span class="sxs-lookup"><span data-stu-id="793fc-104">Network.maxBandwidth</span></span>

<span data-ttu-id="793fc-105">A propriedade **maxBandwidth** especifica ou recupera a largura de banda máxima permitida.</span><span class="sxs-lookup"><span data-stu-id="793fc-105">The **maxBandwidth** property specifies or retrieves the maximum allowed bandwidth.</span></span>

## <a name="syntax"></a><span data-ttu-id="793fc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="793fc-106">Syntax</span></span>

<span data-ttu-id="793fc-107">*Player*. *rede*. **maxBandwidth**</span><span class="sxs-lookup"><span data-stu-id="793fc-107">*player*.*network*.**maxBandwidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="793fc-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="793fc-108">Possible Values</span></span>

<span data-ttu-id="793fc-109">Essa propriedade é um **número** de leitura/gravação (**longo**).</span><span class="sxs-lookup"><span data-stu-id="793fc-109">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="793fc-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="793fc-110">Remarks</span></span>

<span data-ttu-id="793fc-111">Esta propriedade não tem valor padrão.</span><span class="sxs-lookup"><span data-stu-id="793fc-111">This property has no default value.</span></span> <span data-ttu-id="793fc-112">Seu valor pode ser especificado enquanto o Windows Media Player está em execução, mas a alteração não entrará em vigor até que o item de mídia atual seja liberado abrindo outro ou chamando o *Player*. **fechar**.</span><span class="sxs-lookup"><span data-stu-id="793fc-112">Its value can be specified while Windows Media Player is playing, but the change will not take effect until the current media item is released by opening another one or by calling *Player*.**close**.</span></span> <span data-ttu-id="793fc-113">O Windows Media Player tenta atingir a maior largura de banda possível.</span><span class="sxs-lookup"><span data-stu-id="793fc-113">Windows Media Player attempts to achieve the highest bandwidth possible.</span></span> <span data-ttu-id="793fc-114">Somente no caso do valor que está sendo definido, qualquer redução de largura de banda ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="793fc-114">Only in the case of the value being set will any bandwidth reduction occur.</span></span>

<span data-ttu-id="793fc-115">Essa configuração é útil para reduzir a quantidade de largura de banda usada, principalmente no caso de um fluxo de taxa de bits múltipla (MBR).</span><span class="sxs-lookup"><span data-stu-id="793fc-115">This setting is useful for reducing the amount of bandwidth used, particularly in the case of a multiple bit rate (MBR) stream.</span></span> <span data-ttu-id="793fc-116">Um fluxo MBR contém vários fluxos com taxas de bits diferentes.</span><span class="sxs-lookup"><span data-stu-id="793fc-116">An MBR stream contains multiple streams with different bit rates.</span></span> <span data-ttu-id="793fc-117">Em alguns casos, pode ser desejável usar um fluxo com uma taxa de bits inferior à necessária pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="793fc-117">In some cases, it may be desirable to use a stream with a lower bit rate than the client requires.</span></span> <span data-ttu-id="793fc-118">Nesse caso, a definição da propriedade **maxBandwidth** selecionará um fluxo de taxa de bits inferior.</span><span class="sxs-lookup"><span data-stu-id="793fc-118">In this case, setting the **maxBandwidth** property will select a lower bit-rate stream.</span></span>

<span data-ttu-id="793fc-119">Por exemplo, um fluxo MBR pode incluir fluxos codificados a 20 kilobits por segundo (Kbps), 37 kbps e 200 Kbps.</span><span class="sxs-lookup"><span data-stu-id="793fc-119">For example, an MBR stream could include streams encoded at 20 kilobits per second (Kbps), 37 Kbps, and 200 Kbps.</span></span> <span data-ttu-id="793fc-120">Definir a propriedade **maxBandwidth** como 50.000 (50 kbps) selecionará o fluxo de 37 Kbps em vez do fluxo de 200 Kbps.</span><span class="sxs-lookup"><span data-stu-id="793fc-120">Setting the **maxBandwidth** property to 50,000 (50 Kbps) will select the 37 Kbps stream instead of the 200 Kbps stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="793fc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="793fc-121">Requirements</span></span>



| <span data-ttu-id="793fc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="793fc-122">Requirement</span></span> | <span data-ttu-id="793fc-123">Valor</span><span class="sxs-lookup"><span data-stu-id="793fc-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="793fc-124">Versão</span><span class="sxs-lookup"><span data-stu-id="793fc-124">Version</span></span><br/> | <span data-ttu-id="793fc-125">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="793fc-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="793fc-126">DLL</span><span class="sxs-lookup"><span data-stu-id="793fc-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="793fc-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="793fc-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="793fc-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="793fc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="793fc-129">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="793fc-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="793fc-130">**Player. fechar**</span><span class="sxs-lookup"><span data-stu-id="793fc-130">**Player.close**</span></span>](player-close.md)
</dt> </dl>

 

 





