---
title: IAgentUserInput getitemid
description: IAgentUserInput getitemid
ms.assetid: 3afd4d9d-51bb-4086-bf7b-7c9a2ddcd807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde65fc10a4cb467bd69f200e3244f1a2a73c0424d64f6a4babbd2cefd18e0be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609256"
---
# <a name="iagentuserinputgetitemid"></a>IAgentUserInput:: getitemid

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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


 

 




