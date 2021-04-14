---
title: IAgentUserInput GetAllItemData
description: IAgentUserInput GetAllItemData
ms.assetid: d1857b28-c745-4ed2-b49e-774f247e7348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced6a618d4fbbc093bf54c19fc393b7e195f2069
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453471"
---
# <a name="iagentuserinputgetallitemdata"></a><span data-ttu-id="fc6db-103">IAgentUserInput::GetAllItemData</span><span class="sxs-lookup"><span data-stu-id="fc6db-103">IAgentUserInput::GetAllItemData</span></span>

<span data-ttu-id="fc6db-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fc6db-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAllItemData(
   VARIANT * pdwItemIndices,  // address of variable for alternative IDs
   VARIANT * plConfidences,   // address of variable for confidence scores
   VARIANT * pbszText         // address of variable for voice text
);
```

<span data-ttu-id="fc6db-105">Recupera os dados para todas as alternativas de [**comando**](command-event.md) passadas para um retorno de chamada de [**comando IAgentNotifySink::**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="fc6db-105">Retrieves the data for all [**Command**](command-event.md) alternatives passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="fc6db-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fc6db-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="fc6db-107"><span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*</span><span class="sxs-lookup"><span data-stu-id="fc6db-107"><span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*</span></span>
</dt> <dd>

<span data-ttu-id="fc6db-108">Endereço de uma variável que recebe as IDs dos [**comandos**](command-event.md) passados para o retorno de chamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="fc6db-108">Address of a variable that receives the IDs of [**Commands**](command-event.md) passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="fc6db-109"><span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*</span><span class="sxs-lookup"><span data-stu-id="fc6db-109"><span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*</span></span>
</dt> <dd>

<span data-ttu-id="fc6db-110">Endereço de uma variável que recebe as pontuações de confiança para alternativas de [**comando**](command-event.md) passadas para o retorno de chamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="fc6db-110">Address of a variable that receives the confidence scores for [**Command**](command-event.md) alternatives passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="fc6db-111"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span><span class="sxs-lookup"><span data-stu-id="fc6db-111"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span></span>
</dt> <dd>

<span data-ttu-id="fc6db-112">Endereço de uma variável que recebe o texto de voz para alternativas de [**comando**](command-event.md) passadas para o retorno de chamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="fc6db-112">Address of a variable that receives the voice text for [**Command**](command-event.md) alternatives passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> </dl>

<span data-ttu-id="fc6db-113">Se a entrada de fala disparar [**IAgentNotifySink:: Command**](iagentnotifysink--command.md), o servidor retornará a melhor correspondência, a segunda correspondência mais adequada e a terceira melhor correspondência, se elas forem fornecidas pelo mecanismo de fala.</span><span class="sxs-lookup"><span data-stu-id="fc6db-113">If speech input triggers [**IAgentNotifySink::Command**](iagentnotifysink--command.md), the server returns the best match, the second-best match, and the third-best match, if these are provided by the speech engine.</span></span> <span data-ttu-id="fc6db-114">Ele fornece as pontuações de confiança relativas, no intervalo de-100 a 100, e o texto real "ouvido" pelo mecanismo de fala.</span><span class="sxs-lookup"><span data-stu-id="fc6db-114">It provides the relative confidence scores, in the range of -100 to 100, and actual text "heard" by the speech engine.</span></span> <span data-ttu-id="fc6db-115">Se a melhor correspondência era um comando fornecido pelo servidor, o servidor envia uma ID nula, mas ainda envia uma pontuação de confiança e o texto [**da voz**](voice-property.md) .</span><span class="sxs-lookup"><span data-stu-id="fc6db-115">If the best match was a server-supplied command, the server sends a NULL ID, but still sends a confidence score and the [**Voice**](voice-property.md) text.</span></span>

<span data-ttu-id="fc6db-116">Se a entrada de fala não foi a origem do evento; por exemplo, se o usuário selecionou o comando no menu pop-up do caractere, o servidor do Microsoft Agent retorna a ID do [**comando**](command-event.md) selecionado, com uma pontuação de confiança de 100 e texto de voz como nulo.</span><span class="sxs-lookup"><span data-stu-id="fc6db-116">If speech input was not the source for the event; for example, if the user selected the command from the character's pop-up menu, the Microsoft Agent server returns the ID of the [**Command**](command-event.md) selected, with a confidence score of 100 and voice text as NULL.</span></span> <span data-ttu-id="fc6db-117">As outras alternativas retornam como NULL com pontuações de confiança de zero (0) e texto de voz como NULL.</span><span class="sxs-lookup"><span data-stu-id="fc6db-117">The other alternatives return as NULL with confidence scores of zero (0) and voice text as NULL.</span></span>

> [!Note]  
> <span data-ttu-id="fc6db-118">Nem todos os mecanismos de reconhecimento de fala podem retornar todos os valores para todos os parâmetros desse evento.</span><span class="sxs-lookup"><span data-stu-id="fc6db-118">Not all speech recognition engines may return all the values for all the parameters of this event.</span></span> <span data-ttu-id="fc6db-119">Verifique com o fornecedor do mecanismo para determinar se o mecanismo oferece suporte à interface do Microsoft Speech API para retornar alternativas e pontuações de confiança.</span><span class="sxs-lookup"><span data-stu-id="fc6db-119">Check with your engine vendor to determine whether the engine supports the Microsoft Speech API interface for returning alternatives and confidence scores.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="fc6db-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="fc6db-120">See Also</span></span>

<span data-ttu-id="fc6db-121">[**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput:: GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput:: getitemid**](iagentuserinput--getitemid.md)</span><span class="sxs-lookup"><span data-stu-id="fc6db-121">[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md)</span></span>


 

 




