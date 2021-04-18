---
title: IAgentUserInput getitemid
description: IAgentUserInput getitemid
ms.assetid: 3afd4d9d-51bb-4086-bf7b-7c9a2ddcd807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ae1386d87fa6051111801c5603837519eeb4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105810874"
---
# <a name="iagentuserinputgetitemid"></a><span data-ttu-id="df70d-103">IAgentUserInput:: getitemid</span><span class="sxs-lookup"><span data-stu-id="df70d-103">IAgentUserInput::GetItemID</span></span>

<span data-ttu-id="df70d-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="df70d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetItemID(
   long dwItemIndex,    // index of Command alternative
   long * pdwCommandID  // address of a variable for number of alternatives 
);
```

<span data-ttu-id="df70d-105">Recupera o identificador de uma alternativa de [**comando**](command-event.md) passada para um retorno de chamada de [**comando IAgentNotifySink::**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="df70d-105">Retrieves the identifier of a [**Command**](command-event.md) alternative passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="df70d-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="df70d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="df70d-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span><span class="sxs-lookup"><span data-stu-id="df70d-107"><span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*</span></span>
</dt> <dd>

<span data-ttu-id="df70d-108">O índice da alternativa de [**comando**](command-event.md) passado para o retorno de chamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="df70d-108">The index of the [**Command**](command-event.md) alternative passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="df70d-109"><span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*pdwCommandID*</span><span class="sxs-lookup"><span data-stu-id="df70d-109"><span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*pdwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="df70d-110">Endereço de uma variável que recebe a ID de um [**comando**](command-event.md).</span><span class="sxs-lookup"><span data-stu-id="df70d-110">Address of a variable that receives the ID of a [**Command**](command-event.md).</span></span>

</dd> </dl>

<span data-ttu-id="df70d-111">Se a entrada de voz disparar o retorno de chamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) , o servidor retornará as IDs para quaisquer [**comandos**](command-event.md) correspondentes definidos pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="df70d-111">If voice input triggers the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback, the server returns the IDs for any matching [**Commands**](command-event.md) defined by your application.</span></span>

## <a name="see-also"></a><span data-ttu-id="df70d-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="df70d-112">See Also</span></span>

<span data-ttu-id="df70d-113">[**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput:: GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput:: GetAllItemData**](iagentuserinput--getallitemdata.md)</span><span class="sxs-lookup"><span data-stu-id="df70d-113">[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md)</span></span>


 

 




