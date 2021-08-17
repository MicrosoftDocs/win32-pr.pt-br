---
title: IAgentUserInput GetAllItemData
description: IAgentUserInput GetAllItemData
ms.assetid: d1857b28-c745-4ed2-b49e-774f247e7348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d74c59e05e021fdff05ee8991c4563a7a4be918f6ecb244c26402b5234b240b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105142"
---
# <a name="iagentuserinputgetallitemdata"></a>IAgentUserInput::GetAllItemData

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetAllItemData(
   VARIANT * pdwItemIndices,  // address of variable for alternative IDs
   VARIANT * plConfidences,   // address of variable for confidence scores
   VARIANT * pbszText         // address of variable for voice text
);
```

Recupera os dados de todas as alternativas [**de comando**](command-event.md) passadas para um retorno de [**chamada IAgentNotifySink::Command.**](iagentnotifysink--command.md)

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*
</dt> <dd>

Endereço de uma variável que recebe as IDs de [**Comandos**](command-event.md) passadas para o retorno de chamada [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

</dd> <dt>

<span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*
</dt> <dd>

Endereço de uma variável que recebe as pontuações de confiança para alternativas [**de**](command-event.md) comando passadas para o retorno de chamada [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*
</dt> <dd>

Endereço de uma variável que [](command-event.md) recebe o texto de voz para Alternativas de comando passadas para o retorno de chamada [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

</dd> </dl>

Se a entrada de fala disparar [**IAgentNotifySink::Command**](iagentnotifysink--command.md), o servidor retornará a melhor combinação, a segunda melhor e a terceira melhor, se elas são fornecidas pelo mecanismo de fala. Ele fornece as pontuações de confiança relativa, no intervalo de -100 a 100, e o texto real "ouvido" pelo mecanismo de fala. Se a melhor combinação for um comando fornecido pelo servidor, o servidor enviará uma ID NULL, mas ainda enviará uma pontuação de confiança e o [**texto voz.**](voice-property.md)

Se a entrada de fala não era a origem do evento; por exemplo, se o usuário selecionou o comando no menu pop-up do [](command-event.md) caractere, o servidor do Microsoft Agent retornará a ID do Comando selecionado, com uma pontuação de confiança de 100 e texto de voz como NULL. As outras alternativas retornam como NULL com pontuações de confiança de zero (0) e texto de voz como NULL.

> [!Note]  
> Nem todos os mecanismos de reconhecimento de fala podem retornar todos os valores para todos os parâmetros desse evento. Verifique com o fornecedor do mecanismo para determinar se o mecanismo dá suporte à interface do Microsoft Speech API para retornar alternativas e pontuações de confiança.

 

## <a name="see-also"></a>Consulte Também

[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md)


 

 




