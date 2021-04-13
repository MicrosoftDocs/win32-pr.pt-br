---
title: IAgentUserInput GetItemConfidence
description: IAgentUserInput GetItemConfidence
ms.assetid: 7d1ca2f0-416c-43c3-99a8-9f287cb88de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846e1fca9ea1245a62fc68330d68263b63fb7cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291739"
---
# <a name="iagentuserinputgetitemconfidence"></a><span data-ttu-id="14cb2-103">IAgentUserInput::GetItemConfidence</span><span class="sxs-lookup"><span data-stu-id="14cb2-103">IAgentUserInput::GetItemConfidence</span></span>

<span data-ttu-id="14cb2-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="14cb2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetItemConfidence(
   long dwItemIndex,    // index of Command alternative
   long * plConfidence  // address of confidence value for Command 
);
```

<span data-ttu-id="14cb2-105">Recupera o valor de confiança de um [**comando**](command-event.md) passado para um retorno de chamada de [**comando IAgentNotifySink::**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="14cb2-105">Retrieves the confidence value for a [**Command**](command-event.md) passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="14cb2-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="14cb2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="14cb2-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span><span class="sxs-lookup"><span data-stu-id="14cb2-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span></span>
</dt> <dd>

<span data-ttu-id="14cb2-108">O índice de uma alternativa de [**comando**](command-event.md) passada para o retorno de chamada de [**comando IAgentNotifySink::**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="14cb2-108">The index of a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="14cb2-109"><span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*plConfidence*</span><span class="sxs-lookup"><span data-stu-id="14cb2-109"><span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*plConfidence*</span></span>
</dt> <dd>

<span data-ttu-id="14cb2-110">Endereço de uma variável que recebe a pontuação de confiança para uma alternativa de [**comando**](command-event.md) passada para o retorno de chamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="14cb2-110">Address of a variable that receives the confidence score for a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> </dl>

<span data-ttu-id="14cb2-111">Se a entrada de voz não foi a origem do comando, por exemplo, se o usuário selecionou o comando no menu pop-up do caractere, o servidor do Microsoft Agent retornará o valor de confiança da melhor correspondência como 100 e os valores de confiança para todas as outras alternativas como zero (0).</span><span class="sxs-lookup"><span data-stu-id="14cb2-111">If voice input was not the source for the command, for example, if the user selected the command from the character's pop-up menu, the Microsoft Agent server returns the confidence value of the best match as 100 and the confidence values for all other alternatives as zero (0).</span></span>

## <a name="see-also"></a><span data-ttu-id="14cb2-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="14cb2-112">See Also</span></span>

<span data-ttu-id="14cb2-113">[**IAgentUserInput:: Getitemid**](iagentuserinput--getitemid.md), [**IAgentUserInput:: GetAllItemData**](iagentuserinput--getallitemdata.md), [**IAgentUserInput:: GetItemText**](iagentuserinput--getitemtext.md)</span><span class="sxs-lookup"><span data-stu-id="14cb2-113">[**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md)</span></span>


 

 




