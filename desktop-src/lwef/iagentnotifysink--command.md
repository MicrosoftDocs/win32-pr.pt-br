---
title: Comando IAgentNotifySink
description: Comando IAgentNotifySink
ms.assetid: d54fb2e8-27d6-47a4-8a1e-5419a94ea26d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690d2914db9d284cd4ba4b826905d3169b83f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917240"
---
# <a name="iagentnotifysinkcommand"></a>IAgentNotifySink:: comando

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Command(
   long dwCommandID,         // Command ID of the best match
   IUnknown * punkUserInput  // address of IAgentUserInput object 
);                          
```

Notifica um aplicativo cliente de que um [**comando**](/windows/desktop/lwef/the-command-object) foi selecionado pelo usuário.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

Identificador da melhor alternativa de comando de correspondência.

</dd> <dt>

<span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkUserInput*
</dt> <dd>

Endereço da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) para o objeto [**IAgentUserInput**](iagentuserinput.md) .

</dd> </dl>

Use [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para recuperar a interface [**IAgentUserInput**](iagentuserinput.md) .

O servidor notifica o cliente de entrada-ativo quando o usuário escolhe um comando por voz ou selecionando um comando no menu pop-up do caractere. O evento ocorre mesmo quando o usuário seleciona um dos comandos do servidor. Nesse caso, o servidor retorna uma ID de comando nula, a pontuação de confiança e o texto de voz retornado pelo mecanismo de fala para essa entrada.

## <a name="see-also"></a>Consulte Também

[**IAgentUserInput**](iagentuserinput.md)


 

 