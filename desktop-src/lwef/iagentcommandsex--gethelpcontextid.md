---
title: IAgentCommandsEx getidentificaçãodocontextodaajuda
description: IAgentCommandsEx getidentificaçãodocontextodaajuda
ms.assetid: db5f93e9-8cd3-4147-94b4-50cfe12033c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a49a633a66622626973e450b9566033b1ad96e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007466"
---
# <a name="iagentcommandsexgethelpcontextid"></a>IAgentCommandsEx:: getidentificaçãodocontextodaajuda

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of Commands object help topic ID
);
```

Recupera o [**HelpContextId**](helpcontextid-property.md) para um objeto de [**comando**](/windows/desktop/lwef/the-command-object) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*
</dt> <dd>

Endereço de uma variável que recebe o número de contexto do tópico da ajuda para o objeto de [**comando**](/windows/desktop/lwef/the-command-object) .

</dd> </dl>

Se você criou um arquivo de ajuda do Windows para seu aplicativo e definiu a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Microsoft Agent chama automaticamente Help quando [**HelpModeOn**](helpmodeon-property.md) está definido como **true** e o usuário seleciona o objeto [**Command**](/windows/desktop/lwef/the-command-object) . Se houver um número de contexto em [**HelpContextId**](helpcontextid-property.md), o Agent chamará ajuda e procurará o tópico identificado pelo número de contexto atual. O número de contexto atual é o valor de **HelpContextId** para o objeto de **comando** .

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

> [!Note]  
> A criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx:: setidentificaçãodocontextodaajuda**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: setarquivodeajudaname**](iagentcharacterex--sethelpfilename.md)


 

 