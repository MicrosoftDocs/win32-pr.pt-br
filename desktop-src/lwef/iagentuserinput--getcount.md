---
title: GetCount IAgentUserInput
description: GetCount IAgentUserInput
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac4b597f7367eff10154bde256698ef371c3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159240"
---
# <a name="iagentuserinputgetcount"></a>IAgentUserInput:: GetCount

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of a variable for number of alternatives 
);
```

Recupera o número de alternativas de [**comando**](command-event.md) passadas para um retorno de chamada de [**comando IAgentNotifySink::**](iagentnotifysink--command.md) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

Endereço de uma variável que recebe a contagem de alternativas de [**comandos**](command-event.md) identificadas pelo servidor.

</dd> </dl>

Se a entrada de voz não foi a origem do comando, por exemplo, se o usuário selecionou o comando no menu pop-up do caractere, **GetCount** retornará 1. Se **GetCount** retornar zero (0), o mecanismo de reconhecimento de fala detectou uma entrada falada, mas determinou que não havia nenhum comando correspondente.

 

 




