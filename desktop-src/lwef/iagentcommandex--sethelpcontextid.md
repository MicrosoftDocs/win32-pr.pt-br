---
title: IAgentCommandEx setidentificaçãodocontextodaajuda
description: IAgentCommandEx setidentificaçãodocontextodaajuda
ms.assetid: 861d55dc-f584-495c-a148-016af8f7a3e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7539cef8e986db40ef94a8fd3d47073fbe489d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105781194"
---
# <a name="iagentcommandexsethelpcontextid"></a>IAgentCommandEx:: setidentificaçãodocontextodaajuda

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetHelpContextID(
   long ulID  //  ID for help topic
);
```

Define o [**HelpContextId**](helpcontextid-property-com.md) para um objeto de [**comando**](/windows/desktop/lwef/the-command-object) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*
</dt> <dd>

O número de contexto do tópico da ajuda associado ao objeto de [**comando**](/windows/desktop/lwef/the-command-object) ; usado para fornecer ajuda contextual para o comando.

</dd> </dl>

Se você criou um arquivo de ajuda do Windows para seu aplicativo e o definiu na propriedade [**HelpFile**](helpfile-property.md) do caractere. O Microsoft Agent chama automaticamente a ajuda quando [**HelpModeOn**](helpmodeon-property.md) é definido como **true** e o usuário seleciona o comando. Se houver um número de contexto em [**HelpContextId**](helpcontextid-property-com.md), o Agent chamará ajuda e procurará o tópico identificado pelo número de contexto atual. O número de contexto atual é o valor de **HelpContextId** para o comando.

> [!Note]  
> A criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCommandEx:: getidentificaçãodocontextodaajuda**](iagentcommandex--gethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: setarquivodeajudaname**](iagentcharacterex--sethelpfilename.md)


 

 