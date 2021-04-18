---
title: Player. PlayState
description: A propriedade PlayState recupera um valor que indica o estado da operação do Windows Media Player.
ms.assetid: 8ed1ee1f-8731-402a-aff5-5ae513a35eea
keywords:
- Player. PlayState Windows Media Player
topic_type:
- apiref
api_name:
- Player.playState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c442b1be9e1ea15b8a54c2dafc264edf8aeb479
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814021"
---
# <a name="playerplaystate"></a><span data-ttu-id="fd2e7-104">Player. PlayState</span><span class="sxs-lookup"><span data-stu-id="fd2e7-104">Player.playState</span></span>

<span data-ttu-id="fd2e7-105">A propriedade **PlayState** recupera um valor que indica o estado da operação do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-105">The **playState** property retrieves a value indicating the state of the Windows Media Player operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd2e7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd2e7-106">Syntax</span></span>

<span data-ttu-id="fd2e7-107">*Player* . **PlayState**</span><span class="sxs-lookup"><span data-stu-id="fd2e7-107">*player* .**playState**</span></span>

## <a name="possible-values"></a><span data-ttu-id="fd2e7-108">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="fd2e7-108">Possible Values</span></span>

<span data-ttu-id="fd2e7-109">Essa propriedade é um **número** somente leitura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="fd2e7-109">This property is a read-only **Number** (**long**).</span></span> <span data-ttu-id="fd2e7-110">A constante de enumeração de estilo C pode ser derivada pela prefixação do valor de estado com "wmpps".</span><span class="sxs-lookup"><span data-stu-id="fd2e7-110">The C-style enumeration constant can be derived by prefixing the state value with "wmpps".</span></span> <span data-ttu-id="fd2e7-111">Por exemplo, a constante para o estado de execução é **wmppsPlaying**.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-111">For example, the constant for the Playing state is **wmppsPlaying**.</span></span>



| <span data-ttu-id="fd2e7-112">Valor</span><span class="sxs-lookup"><span data-stu-id="fd2e7-112">Value</span></span> | <span data-ttu-id="fd2e7-113">Estado</span><span class="sxs-lookup"><span data-stu-id="fd2e7-113">State</span></span>         | <span data-ttu-id="fd2e7-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd2e7-114">Description</span></span>                                                                                                                 |
|-------|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd2e7-115">0</span><span class="sxs-lookup"><span data-stu-id="fd2e7-115">0</span></span>     | <span data-ttu-id="fd2e7-116">Indefinido</span><span class="sxs-lookup"><span data-stu-id="fd2e7-116">Undefined</span></span>     | <span data-ttu-id="fd2e7-117">O Windows Media Player está em um estado indefinido.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-117">Windows Media Player is in an undefined state.</span></span>                                                                              |
| <span data-ttu-id="fd2e7-118">1</span><span class="sxs-lookup"><span data-stu-id="fd2e7-118">1</span></span>     | <span data-ttu-id="fd2e7-119">Parado</span><span class="sxs-lookup"><span data-stu-id="fd2e7-119">Stopped</span></span>       | <span data-ttu-id="fd2e7-120">A reprodução do item de mídia atual foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-120">Playback of the current media item is stopped.</span></span>                                                                              |
| <span data-ttu-id="fd2e7-121">2</span><span class="sxs-lookup"><span data-stu-id="fd2e7-121">2</span></span>     | <span data-ttu-id="fd2e7-122">Em Pausa</span><span class="sxs-lookup"><span data-stu-id="fd2e7-122">Paused</span></span>        | <span data-ttu-id="fd2e7-123">A reprodução do item de mídia atual está em pausa.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-123">Playback of the current media item is paused.</span></span> <span data-ttu-id="fd2e7-124">Quando um item de mídia é pausado, retomar a reprodução começa no mesmo local.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-124">When a media item is paused, resuming playback begins from the same location.</span></span> |
| <span data-ttu-id="fd2e7-125">3</span><span class="sxs-lookup"><span data-stu-id="fd2e7-125">3</span></span>     | <span data-ttu-id="fd2e7-126">Reproduzindo</span><span class="sxs-lookup"><span data-stu-id="fd2e7-126">Playing</span></span>       | <span data-ttu-id="fd2e7-127">O item de mídia atual está sendo reproduzido.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-127">The current media item is playing.</span></span>                                                                                          |
| <span data-ttu-id="fd2e7-128">4</span><span class="sxs-lookup"><span data-stu-id="fd2e7-128">4</span></span>     | <span data-ttu-id="fd2e7-129">ScanForward</span><span class="sxs-lookup"><span data-stu-id="fd2e7-129">ScanForward</span></span>   | <span data-ttu-id="fd2e7-130">O item de mídia atual é encaminhamento rápido.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-130">The current media item is fast forwarding.</span></span>                                                                                  |
| <span data-ttu-id="fd2e7-131">5</span><span class="sxs-lookup"><span data-stu-id="fd2e7-131">5</span></span>     | <span data-ttu-id="fd2e7-132">ScanReverse</span><span class="sxs-lookup"><span data-stu-id="fd2e7-132">ScanReverse</span></span>   | <span data-ttu-id="fd2e7-133">O item de mídia atual é rebobinado rápido.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-133">The current media item is fast rewinding.</span></span>                                                                                   |
| <span data-ttu-id="fd2e7-134">6</span><span class="sxs-lookup"><span data-stu-id="fd2e7-134">6</span></span>     | <span data-ttu-id="fd2e7-135">de resposta</span><span class="sxs-lookup"><span data-stu-id="fd2e7-135">Buffering</span></span>     | <span data-ttu-id="fd2e7-136">O item de mídia atual está obtendo dados adicionais do servidor.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-136">The current media item is getting additional data from the server.</span></span>                                                          |
| <span data-ttu-id="fd2e7-137">7</span><span class="sxs-lookup"><span data-stu-id="fd2e7-137">7</span></span>     | <span data-ttu-id="fd2e7-138">Aguardando</span><span class="sxs-lookup"><span data-stu-id="fd2e7-138">Waiting</span></span>       | <span data-ttu-id="fd2e7-139">A conexão é estabelecida, mas o servidor não está enviando dados.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-139">Connection is established, but the server is not sending data.</span></span> <span data-ttu-id="fd2e7-140">Aguardando a sessão começar.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-140">Waiting for session to begin.</span></span>                                |
| <span data-ttu-id="fd2e7-141">8</span><span class="sxs-lookup"><span data-stu-id="fd2e7-141">8</span></span>     | <span data-ttu-id="fd2e7-142">MediaEnded</span><span class="sxs-lookup"><span data-stu-id="fd2e7-142">MediaEnded</span></span>    | <span data-ttu-id="fd2e7-143">O item de mídia concluiu a reprodução.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-143">Media item has completed playback.</span></span>                                                                                          |
| <span data-ttu-id="fd2e7-144">9</span><span class="sxs-lookup"><span data-stu-id="fd2e7-144">9</span></span>     | <span data-ttu-id="fd2e7-145">Transição</span><span class="sxs-lookup"><span data-stu-id="fd2e7-145">Transitioning</span></span> | <span data-ttu-id="fd2e7-146">Preparando novo item de mídia.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-146">Preparing new media item.</span></span>                                                                                                   |
| <span data-ttu-id="fd2e7-147">10</span><span class="sxs-lookup"><span data-stu-id="fd2e7-147">10</span></span>    | <span data-ttu-id="fd2e7-148">Ready</span><span class="sxs-lookup"><span data-stu-id="fd2e7-148">Ready</span></span>         | <span data-ttu-id="fd2e7-149">Pronto para começar a jogar.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-149">Ready to begin playing.</span></span>                                                                                                     |
| <span data-ttu-id="fd2e7-150">11</span><span class="sxs-lookup"><span data-stu-id="fd2e7-150">11</span></span>    | <span data-ttu-id="fd2e7-151">Reconexão</span><span class="sxs-lookup"><span data-stu-id="fd2e7-151">Reconnecting</span></span>  | <span data-ttu-id="fd2e7-152">Reconectando ao fluxo.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-152">Reconnecting to stream.</span></span>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="fd2e7-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd2e7-153">Remarks</span></span>

<span data-ttu-id="fd2e7-154">Não há garantia de que os Estados do Windows Media Player ocorram em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-154">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="fd2e7-155">Além disso, nem todo estado ocorre necessariamente durante uma sequência de eventos.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-155">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="fd2e7-156">Você não deve escrever código que dependa da ordem de estado.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-156">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="fd2e7-157">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fd2e7-157">Examples</span></span>

<span data-ttu-id="fd2e7-158">O código JScript a seguir mostra o uso do *Player*. Propriedade **PlayState** .</span><span class="sxs-lookup"><span data-stu-id="fd2e7-158">The following JScript code shows the use of the *player*.**playState** property.</span></span> <span data-ttu-id="fd2e7-159">Um elemento de texto HTML, chamado "MyText", exibe o status atual.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-159">An HTML text element, named "myText", displays the current status.</span></span> <span data-ttu-id="fd2e7-160">O objeto de **jogador** foi criado com ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="fd2e7-160">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether Windows Media Player is in the playing state.
if (3 == Player.playState)
    myText.value = "Windows Media Player is playing!";
else
    myText.value = "Windows Media Player is NOT playing!";
```



## <a name="requirements"></a><span data-ttu-id="fd2e7-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd2e7-161">Requirements</span></span>



| <span data-ttu-id="fd2e7-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd2e7-162">Requirement</span></span> | <span data-ttu-id="fd2e7-163">Valor</span><span class="sxs-lookup"><span data-stu-id="fd2e7-163">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fd2e7-164">Versão</span><span class="sxs-lookup"><span data-stu-id="fd2e7-164">Version</span></span><br/> | <span data-ttu-id="fd2e7-165">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="fd2e7-165">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fd2e7-166">DLL</span><span class="sxs-lookup"><span data-stu-id="fd2e7-166">DLL</span></span><br/>     | <dl> <span data-ttu-id="fd2e7-167"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd2e7-167"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd2e7-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd2e7-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd2e7-169">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="fd2e7-169">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="fd2e7-170">**Evento Player. PlayStateChange**</span><span class="sxs-lookup"><span data-stu-id="fd2e7-170">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> </dl>

 

 





