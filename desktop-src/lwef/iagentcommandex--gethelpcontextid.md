---
title: IAgentCommandEx GetHelpContextID
description: IAgentCommandEx GetHelpContextID
ms.assetid: 97b390f3-ab24-4c09-aa87-d76076eba995
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80f259b10adbdd1460f319b6fda4e5097c11136a5bf7ffde00a11d40a99656a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750179"
---
# <a name="iagentcommandexgethelpcontextid"></a>IAgentCommandEx::GetHelpContextID

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulID  //  address of command's help topic ID
);
```

Recupera o [**HelpContextID para**](helpcontextid-property-com.md) um [**objeto Command.**](/windows/desktop/lwef/the-command-object)

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pulID"></span><span id="pulid"></span><span id="PULID"></span>*pulID*
</dt> <dd>

Endereço de uma variável que recebe o número de contexto do tópico de ajuda associado ao [**objeto Command.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

Se você tiver criado um arquivo de Ajuda Windows para seu aplicativo e tiver definido a propriedade [**HelpFile**](helpfile-property.md) do caractere para esse arquivo, o Microsoft Agent chamará automaticamente a Ajuda quando [**HelpModeOn**](helpmodeon-property.md) estiver definido como **True** e o usuário selecionar o comando. Se houver um número de contexto no [**HelpContextID,**](helpcontextid-property-com.md)o Agent chamará a Ajuda e procurará o tópico identificado pelo número de contexto atual. O número de contexto atual é o valor **de HelpContextID** para o comando.

> [!Note]  
> A criação de um arquivo de Ajuda requer o Microsoft Windows Help Compiler.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCommandEx::SetHelpContextID**](iagentcommandex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 