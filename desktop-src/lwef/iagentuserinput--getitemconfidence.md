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
# <a name="iagentuserinputgetitemconfidence"></a>IAgentUserInput::GetItemConfidence

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetItemConfidence(
   long dwItemIndex,    // index of Command alternative
   long * plConfidence  // address of confidence value for Command 
);
```

Recupera o valor de confiança de um [**comando**](command-event.md) passado para um retorno de chamada de [**comando IAgentNotifySink::**](iagentnotifysink--command.md) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

O índice de uma alternativa de [**comando**](command-event.md) passada para o retorno de chamada de [**comando IAgentNotifySink::**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*plConfidence*
</dt> <dd>

Endereço de uma variável que recebe a pontuação de confiança para uma alternativa de [**comando**](command-event.md) passada para o retorno de chamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

</dd> </dl>

Se a entrada de voz não foi a origem do comando, por exemplo, se o usuário selecionou o comando no menu pop-up do caractere, o servidor do Microsoft Agent retornará o valor de confiança da melhor correspondência como 100 e os valores de confiança para todas as outras alternativas como zero (0).

## <a name="see-also"></a>Consulte Também

[**IAgentUserInput:: Getitemid**](iagentuserinput--getitemid.md), [**IAgentUserInput:: GetAllItemData**](iagentuserinput--getallitemdata.md), [**IAgentUserInput:: GetItemText**](iagentuserinput--getitemtext.md)


 

 




