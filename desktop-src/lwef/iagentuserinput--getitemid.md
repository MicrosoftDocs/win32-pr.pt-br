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
# <a name="iagentuserinputgetitemid"></a>IAgentUserInput:: getitemid

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetItemID(
   long dwItemIndex,    // index of Command alternative
   long * pdwCommandID  // address of a variable for number of alternatives 
);
```

Recupera o identificador de uma alternativa de [**comando**](command-event.md) passada para um retorno de chamada de [**comando IAgentNotifySink::**](iagentnotifysink--command.md) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

O índice da alternativa de [**comando**](command-event.md) passado para o retorno de chamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*pdwCommandID*
</dt> <dd>

Endereço de uma variável que recebe a ID de um [**comando**](command-event.md).

</dd> </dl>

Se a entrada de voz disparar o retorno de chamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) , o servidor retornará as IDs para quaisquer [**comandos**](command-event.md) correspondentes definidos pelo seu aplicativo.

## <a name="see-also"></a>Consulte Também

[**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput:: GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput:: GetAllItemData**](iagentuserinput--getallitemdata.md)


 

 




