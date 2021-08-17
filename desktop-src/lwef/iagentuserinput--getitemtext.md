---
title: IAgentUserInput GetItemText
description: IAgentUserInput GetItemText
ms.assetid: 69653806-c001-4015-bd05-3c261a312ede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd9c1392bd56e3bb59212edeb79d862260786edb87583c0e8fdf049e8345b40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359036"
---
# <a name="iagentuserinputgetitemtext"></a>IAgentUserInput::GetItemText

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetItemText(
   Long dwItemIndex,  // index of Command alternative
   BSTR * pbszText    // address of voice text for Command 
);
```

Recupera o texto de voz de uma [**alternativa command**](command-event.md) passada para o retorno de [**chamada IAgentNotifySink::Command.**](iagentnotifysink--command.md)

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

O índice de uma [**alternativa de**](command-event.md) Comando passado para o retorno de [**chamada IAgentNotifySink::Command.**](iagentnotifysink--command.md)

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*
</dt> <dd>

Endereço de um BSTR que recebe o valor do texto de voz para o [**Comando**](command-event.md).

</dd> </dl>

Se a entrada de voz não for a origem do comando, por exemplo, se o usuário selecionou o comando no menu pop-up do caractere, o servidor retornará **NULL** para o texto de voz do comando. [](command-event.md)

## <a name="see-also"></a>Consulte Também

[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md)


 

 




