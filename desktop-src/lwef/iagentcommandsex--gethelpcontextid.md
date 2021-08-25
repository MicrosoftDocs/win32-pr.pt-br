---
title: IAgentCommandsEx GetHelpContextID
description: IAgentCommandsEx GetHelpContextID
ms.assetid: db5f93e9-8cd3-4147-94b4-50cfe12033c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e15088eae1025daf7c98695dcf7fd610a04c30089028af0887107228de84b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961826"
---
# <a name="iagentcommandsexgethelpcontextid"></a>IAgentCommandsEx::GetHelpContextID

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of Commands object help topic ID
);
```

Recupera o [**HelpContextID para**](helpcontextid-property.md) um [**objeto Command.**](/windows/desktop/lwef/the-command-object)

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*
</dt> <dd>

Endereço de uma variável que recebe o número de contexto do tópico de ajuda para o [**objeto Command.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

Se você tiver criado um arquivo de Ajuda Windows para seu aplicativo e definido a propriedade [**HelpFile**](helpfile-property.md) do caractere, o Microsoft Agent chamará automaticamente a Ajuda quando [**HelpModeOn**](helpmodeon-property.md) estiver definido como **True** e o usuário selecionar o objeto [**Command.**](/windows/desktop/lwef/the-command-object) Se houver um número de contexto no [**HelpContextID,**](helpcontextid-property.md)o Agent chamará a Ajuda e procurará o tópico identificado pelo número de contexto atual. O número de contexto atual é o valor **de HelpContextID** para o **objeto Command.**

Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.

> [!Note]  
> A criação de um arquivo de Ajuda requer o Compilador Windows Ajuda da Microsoft.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 