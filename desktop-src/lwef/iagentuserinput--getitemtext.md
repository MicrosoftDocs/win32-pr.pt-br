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
# <a name="iagentuserinputgetitemtext"></a>IAgentUserInput::GetItemText

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetItemText(
   Long dwItemIndex,  // index of Command alternative
   BSTR * pbszText    // address of voice text for Command 
);
```

Recupera o texto de voz para uma alternativa de [**comando**](command-event.md) passada para o retorno de chamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

O índice de uma alternativa de [**comando**](command-event.md) passada para o retorno de chamada de [**comando IAgentNotifySink::**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*
</dt> <dd>

Endereço de um BSTR que recebe o valor do texto de voz para o [**comando**](command-event.md).

</dd> </dl>

Se a entrada de voz não foi a origem do comando, por exemplo, se o usuário selecionou o comando no menu pop-up do caractere, o servidor retornará **nulo** para o texto de voz do [**comando**](command-event.md).

## <a name="see-also"></a>Consulte Também

[**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput:: getitemid**](iagentuserinput--getitemid.md), [**IAgentUserInput:: GetAllItemData**](iagentuserinput--getallitemdata.md)


 

 




