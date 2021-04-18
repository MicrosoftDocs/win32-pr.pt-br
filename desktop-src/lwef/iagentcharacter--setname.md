---
title: IAgentCharacter SetName
description: IAgentCharacter SetName
ms.assetid: 4944f910-60e9-446b-82e9-2794f445789a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec058e338adfa8c998bf26a1223ae71f0c7de3d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105815416"
---
# <a name="iagentcharactersetname"></a>IAgentCharacter:: SetName

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetName(
   BSTR bszName   // character name
);
```

Define o nome do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

Um BSTR que define o nome do caractere. O nome padrão de um caractere é definido quando ele é compilado com o editor de caracteres do Microsoft Agent. Você pode alterá-lo usando **IAgentCharacter:: SetName**; no entanto, isso altera o nome do caractere para todos os clientes atuais do caractere. Essa propriedade não é persistente (armazenada permanentemente). O nome do caractere é revertido para seu nome padrão sempre que o caractere é carregado pela primeira vez por um cliente.

O nome do caractere também pode depender de sua ID de idioma. Os caracteres podem ser compilados com nomes diferentes para idiomas diferentes.

O servidor usa a configuração de nome do caractere em partes da interface do Microsoft Agent, como o título da janela de comandos de voz quando o caractere é entrada-ativo e no menu pop-up da barra de tarefas do Microsoft Agent.

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter:: GetName**](iagentcharacter--getname.md)


 

 




