---
title: IAgentUserInput GetAllItemData
description: IAgentUserInput GetAllItemData
ms.assetid: d1857b28-c745-4ed2-b49e-774f247e7348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced6a618d4fbbc093bf54c19fc393b7e195f2069
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453471"
---
# <a name="iagentuserinputgetallitemdata"></a>IAgentUserInput::GetAllItemData

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetAllItemData(
   VARIANT * pdwItemIndices,  // address of variable for alternative IDs
   VARIANT * plConfidences,   // address of variable for confidence scores
   VARIANT * pbszText         // address of variable for voice text
);
```

Recupera os dados para todas as alternativas de [**comando**](command-event.md) passadas para um retorno de chamada de [**comando IAgentNotifySink::**](iagentnotifysink--command.md) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*
</dt> <dd>

Endereço de uma variável que recebe as IDs dos [**comandos**](command-event.md) passados para o retorno de chamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*
</dt> <dd>

Endereço de uma variável que recebe as pontuações de confiança para alternativas de [**comando**](command-event.md) passadas para o retorno de chamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*
</dt> <dd>

Endereço de uma variável que recebe o texto de voz para alternativas de [**comando**](command-event.md) passadas para o retorno de chamada [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

</dd> </dl>

Se a entrada de fala disparar [**IAgentNotifySink:: Command**](iagentnotifysink--command.md), o servidor retornará a melhor correspondência, a segunda correspondência mais adequada e a terceira melhor correspondência, se elas forem fornecidas pelo mecanismo de fala. Ele fornece as pontuações de confiança relativas, no intervalo de-100 a 100, e o texto real "ouvido" pelo mecanismo de fala. Se a melhor correspondência era um comando fornecido pelo servidor, o servidor envia uma ID nula, mas ainda envia uma pontuação de confiança e o texto [**da voz**](voice-property.md) .

Se a entrada de fala não foi a origem do evento; por exemplo, se o usuário selecionou o comando no menu pop-up do caractere, o servidor do Microsoft Agent retorna a ID do [**comando**](command-event.md) selecionado, com uma pontuação de confiança de 100 e texto de voz como nulo. As outras alternativas retornam como NULL com pontuações de confiança de zero (0) e texto de voz como NULL.

> [!Note]  
> Nem todos os mecanismos de reconhecimento de fala podem retornar todos os valores para todos os parâmetros desse evento. Verifique com o fornecedor do mecanismo para determinar se o mecanismo oferece suporte à interface do Microsoft Speech API para retornar alternativas e pontuações de confiança.

 

## <a name="see-also"></a>Consulte Também

[**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput:: GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput:: getitemid**](iagentuserinput--getitemid.md)


 

 




