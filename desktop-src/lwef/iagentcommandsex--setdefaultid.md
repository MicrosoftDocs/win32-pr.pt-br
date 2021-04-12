---
title: IAgentCommandsEx setpadrão
description: IAgentCommandsEx setpadrão
ms.assetid: 056ec518-bf0b-403f-adc6-9b53b0c044a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37754eb61df7879511a03dde705936d36f905376
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365916"
---
# <a name="iagentcommandsexsetdefaultid"></a>IAgentCommandsEx:: setpadrão

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetDefaultID(
   long dwID,  // default command's ID
);
```

Define a ID do comando padrão em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*
</dt> <dd>

A ID do [**comando**](/windows/desktop/lwef/the-command-object) a ser definido como o padrão.

</dd> </dl>

Essa propriedade define o objeto de [**comando**](/windows/desktop/lwef/the-command-object) padrão definido em sua coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . O comando padrão é negrito no menu pop-up do caractere. No entanto, a definição do comando padrão não altera realmente o tratamento de comandos nem os eventos de clique duplo.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx:: getdefaultid**](iagentcommandsex--getdefaultid.md)


 

 