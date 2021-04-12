---
title: IAgentCommandsEx getpadrão
description: IAgentCommandsEx getpadrão
ms.assetid: 14079ae0-ad2c-4f38-9371-9914f8402e49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4380eca62a65758979a94fb23511348b11acdf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104366013"
---
# <a name="iagentcommandsexgetdefaultid"></a>IAgentCommandsEx:: getdefaultid

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetDefaultID(
   long * pdwID  // address of default command's ID
);
```

Recupera a ID do comando padrão em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*
</dt> <dd>

Endereço de uma variável que recebe a ID do conjunto de [**comandos**](/windows/desktop/lwef/the-command-object) como padrão.

</dd> </dl>

Essa propriedade retorna o objeto de [**comando**](/windows/desktop/lwef/the-command-object) padrão atual em sua coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) . O comando padrão é negrito no menu pop-up do caractere. No entanto, a definição do comando padrão não altera o tratamento de comandos nem eventos de clique duplo.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx:: setpadrão**](iagentcommandsex--setdefaultid.md)


 

 