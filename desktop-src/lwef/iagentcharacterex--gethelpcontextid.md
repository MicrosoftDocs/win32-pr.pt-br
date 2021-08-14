---
title: IAgentCharacterEx getidentificaçãodocontextodaajuda
description: IAgentCharacterEx getidentificaçãodocontextodaajuda
ms.assetid: 9dec5b0c-4758-4859-9aa6-6db3ef0d6b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3a64de0f4373bcaa890156ec88595d066aae9ae84b5b242fe62ffae10479d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750790"
---
# <a name="iagentcharacterexgethelpcontextid"></a>IAgentCharacterEx:: getidentificaçãodocontextodaajuda

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

se você tiver criado um arquivo de ajuda Windows para seu aplicativo e definir a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Microsoft Agent chamará automaticamente a ajuda quando [**HelpModeOn**](helpmodeon-property.md) estiver definido como **True** e o usuário selecionará o caractere. Se houver um número de contexto em [**HelpContextId**](helpcontextid-property.md), o Agent chamará ajuda e procurará o tópico identificado pelo número de contexto atual. O número de contexto atual é o valor de **HelpContextId** para o caractere.

**IAgentCharacterEx:: getidentificaçãodocontextodaajuda** retorna o [**HelpContextId**](helpcontextid-property.md) definido para o caractere. Ele não retorna o **HelpContextId** definido por outros clientes.

> [!Note]  
> a criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx:: setidentificaçãodocontextodaajuda**](iagentcharacterex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: setarquivodeajudaname**](iagentcharacterex--sethelpfilename.md)


 

 




