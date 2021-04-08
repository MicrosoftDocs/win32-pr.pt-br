---
title: IAgentUserInput GetItemText
description: IAgentUserInput GetItemText
ms.assetid: 69653806-c001-4015-bd05-3c261a312ede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7010172147f86282903641c46aa5137ce69c80be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004780"
---
# <a name="iagentuserinputgetitemtext"></a><span data-ttu-id="28c13-103">IAgentUserInput::GetItemText</span><span class="sxs-lookup"><span data-stu-id="28c13-103">IAgentUserInput::GetItemText</span></span>

<span data-ttu-id="28c13-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="28c13-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetItemText(
   Long dwItemIndex,  // index of Command alternative
   BSTR * pbszText    // address of voice text for Command 
);
```

<span data-ttu-id="28c13-105">Recupera o texto de voz para uma alternativa de [**comando**](command-event.md) passada para o retorno de chamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="28c13-105">Retrieves the voice text for a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="28c13-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="28c13-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="28c13-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span><span class="sxs-lookup"><span data-stu-id="28c13-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span></span>
</dt> <dd>

<span data-ttu-id="28c13-108">O índice de uma alternativa de [**comando**](command-event.md) passada para o retorno de chamada de [**comando IAgentNotifySink::**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="28c13-108">The index of a [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="28c13-109"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span><span class="sxs-lookup"><span data-stu-id="28c13-109"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span></span>
</dt> <dd>

<span data-ttu-id="28c13-110">Endereço de um BSTR que recebe o valor do texto de voz para o [**comando**](command-event.md).</span><span class="sxs-lookup"><span data-stu-id="28c13-110">Address of a BSTR that receives the value of the voice text for the [**Command**](command-event.md).</span></span>

</dd> </dl>

<span data-ttu-id="28c13-111">Se a entrada de voz não foi a origem do comando, por exemplo, se o usuário selecionou o comando no menu pop-up do caractere, o servidor retornará **nulo** para o texto de voz do [**comando**](command-event.md).</span><span class="sxs-lookup"><span data-stu-id="28c13-111">If voice input was not the source for the command, for example, if the user selected the command from the character's pop-up menu, the server returns **NULL** for the [**Command**](command-event.md)'s voice text.</span></span>

## <a name="see-also"></a><span data-ttu-id="28c13-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="28c13-112">See Also</span></span>

<span data-ttu-id="28c13-113">[**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput:: getitemid**](iagentuserinput--getitemid.md), [**IAgentUserInput:: GetAllItemData**](iagentuserinput--getallitemdata.md)</span><span class="sxs-lookup"><span data-stu-id="28c13-113">[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md)</span></span>


 

 




