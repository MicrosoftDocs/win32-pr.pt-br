---
title: IAgentCommandEx SetHelpContextID
description: IAgentCommandEx SetHelpContextID
ms.assetid: 861d55dc-f584-495c-a148-016af8f7a3e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6b876276d42ff07081b60194e90beff3ad9ef19fec383c50d70a551e1c9a5e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750180"
---
# <a name="iagentcommandexsethelpcontextid"></a>IAgentCommandEx::SetHelpContextID

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetHelpContextID(
   long ulID  //  ID for help topic
);
```

Define [**HelpContextID para**](helpcontextid-property-com.md) um [**objeto Command.**](/windows/desktop/lwef/the-command-object)

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*
</dt> <dd>

O número de contexto do tópico de ajuda associado ao [**objeto Command;**](/windows/desktop/lwef/the-command-object) usado para fornecer Ajuda contextul para o comando.

</dd> </dl>

Se você tiver criado um arquivo Windows Ajuda para seu aplicativo e defini-lo na propriedade [**HelpFile do**](helpfile-property.md) caractere. O Microsoft Agent chama automaticamente a [**Ajuda quando HelpModeOn**](helpmodeon-property.md) está definido como **True** e o usuário seleciona o comando. Se houver um número de contexto no [**HelpContextID,**](helpcontextid-property-com.md)o Agent chamará a Ajuda e procurará o tópico identificado pelo número de contexto atual. O número de contexto atual é o valor **de HelpContextID** para o comando.

> [!Note]  
> A criação de um arquivo de Ajuda requer o Microsoft Windows Help Compiler.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCommandEx::GetHelpContextID**](iagentcommandex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 