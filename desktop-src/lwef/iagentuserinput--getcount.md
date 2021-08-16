---
title: IAgentUserInput GetCount
description: IAgentUserInput GetCount
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f52c296dd152fd1e31a87e21d80f8b25d52ae880b300487cdcba746e81dfa0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749513"
---
# <a name="iagentuserinputgetcount"></a>IAgentUserInput::GetCount

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of a variable for number of alternatives 
);
```

Recupera o número de alternativas [**de comando**](command-event.md) passadas para um retorno de [**chamada IAgentNotifySink::Command.**](iagentnotifysink--command.md)

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

Endereço de uma variável que recebe a contagem de alternativas [**de Comandos**](command-event.md) identificadas pelo servidor.

</dd> </dl>

Se a entrada de voz não for a origem do comando, por exemplo, se o usuário selecionou o comando no menu pop-up do caractere, **GetCount** retornará 1. Se **GetCount** retornar zero (0), o mecanismo de reconhecimento de fala detectou a entrada falada, mas determinou que não havia nenhum comando correspondente.

 

 




