---
title: IAgentCommandsEx SetHelpContextID
description: IAgentCommandsEx SetHelpContextID
ms.assetid: b49d8184-f8dd-4359-9d45-3f038af18da5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e4ff5941d9f120c42cb2fa17d93a4f2a0c23e89d61dbee078b3ab5c3ffe611
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888236"
---
# <a name="iagentcommandsexsethelpcontextid"></a>IAgentCommandsEx::SetHelpContextID

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

Define [**HelpContextID para**](helpcontextid-property.md) um [**objeto Command.**](/windows/desktop/lwef/the-command-object)

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

O número de contexto do tópico de ajuda associado ao [**objeto Command;**](/windows/desktop/lwef/the-command-object) usado para fornecer Ajuda contextul para o comando.

</dd> </dl>

Se você tiver criado um arquivo Windows Ajuda para seu aplicativo e defini-lo na propriedade [**HelpFile do**](helpfile-property.md) caractere. O Agent chama automaticamente a [**Ajuda quando HelpModeOn**](helpmodeon-property.md) é definido como **True** e o usuário seleciona o comando. Se houver um número de contexto no [**HelpContextID,**](helpcontextid-property.md)o Agent chamará a Ajuda e procurará o tópico identificado pelo número de contexto atual. O número de contexto atual é o valor **de HelpContextID** para o comando. Se houver um número de contexto na propriedade **HelpContextID** do comando selecionado, a Ajuda exibirá um tópico correspondente ao contexto da Ajuda atual; caso contrário, ele exibirá "Nenhum tópico de Ajuda associado a este item".

Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.

> [!Note]  
> A criação de um arquivo de Ajuda requer o Compilador Windows Ajuda da Microsoft.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx::GetHelpContextID**](iagentcommandsex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 