---
title: IAgentCharacterEx getidentificaçãodocontextodaajuda
description: IAgentCharacterEx getidentificaçãodocontextodaajuda
ms.assetid: 9dec5b0c-4758-4859-9aa6-6db3ef0d6b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfec03a217745838b88a592433defae01529ed50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636795"
---
# <a name="iagentcharacterexgethelpcontextid"></a>IAgentCharacterEx:: getidentificaçãodocontextodaajuda

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of character's help topic ID
);
```

Recupera o [**HelpContextId**](helpcontextid-property.md) para o caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*
</dt> <dd>

Endereço de uma variável que recebe o número de contexto do tópico da ajuda para o caractere.

</dd> </dl>

Se você tiver criado um arquivo de ajuda do Windows para seu aplicativo e definir a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Microsoft Agent chamará automaticamente a ajuda quando [**HelpModeOn**](helpmodeon-property.md) estiver definido como **true** e o usuário selecionar o caractere. Se houver um número de contexto em [**HelpContextId**](helpcontextid-property.md), o Agent chamará ajuda e procurará o tópico identificado pelo número de contexto atual. O número de contexto atual é o valor de **HelpContextId** para o caractere.

**IAgentCharacterEx:: getidentificaçãodocontextodaajuda** retorna o [**HelpContextId**](helpcontextid-property.md) definido para o caractere. Ele não retorna o **HelpContextId** definido por outros clientes.

> [!Note]  
> A criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx:: setidentificaçãodocontextodaajuda**](iagentcharacterex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: setarquivodeajudaname**](iagentcharacterex--sethelpfilename.md)


 

 




