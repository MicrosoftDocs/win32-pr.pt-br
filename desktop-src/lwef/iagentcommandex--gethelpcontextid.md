---
title: IAgentCommandEx getidentificaçãodocontextodaajuda
description: IAgentCommandEx getidentificaçãodocontextodaajuda
ms.assetid: 97b390f3-ab24-4c09-aa87-d76076eba995
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f330e8ae8cd8bdaff5e27ccd00352b41b07be2b6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365991"
---
# <a name="iagentcommandexgethelpcontextid"></a>IAgentCommandEx:: getidentificaçãodocontextodaajuda

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulID  //  address of command's help topic ID
);
```

Recupera o [**HelpContextId**](helpcontextid-property-com.md) para um objeto de [**comando**](/windows/desktop/lwef/the-command-object) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pulID"></span><span id="pulid"></span><span id="PULID"></span>*pulID*
</dt> <dd>

Endereço de uma variável que recebe o número de contexto do tópico da ajuda associado ao objeto de [**comando**](/windows/desktop/lwef/the-command-object) .

</dd> </dl>

Se você tiver criado um arquivo de ajuda do Windows para seu aplicativo e definir a propriedade [**HelpFile**](helpfile-property.md) de seu caractere para esse arquivo, o Microsoft Agent chamará automaticamente a ajuda quando [**HelpModeOn**](helpmodeon-property.md) estiver definido como **true** e o usuário selecionará o comando. Se houver um número de contexto em [**HelpContextId**](helpcontextid-property-com.md), o Agent chamará ajuda e procurará o tópico identificado pelo número de contexto atual. O número de contexto atual é o valor de **HelpContextId** para o comando.

> [!Note]  
> A criação de um arquivo de ajuda requer o compilador de ajuda do Microsoft Windows.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCommandEx:: setidentificaçãodocontextodaajuda**](iagentcommandex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: setarquivodeajudaname**](iagentcharacterex--sethelpfilename.md)


 

 