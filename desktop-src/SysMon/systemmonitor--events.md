---
title: Eventos de SystemMonitor
description: A classe SystemMonitor tem os seguintes eventos
ms.assetid: 64d9befd-5ea0-4888-b0fb-cff889f1d188
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3584eed86abcaef019f0fc8f8bd794a80abca1143286317189889231bbc2cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882942"
---
# <a name="systemmonitor-events"></a>Eventos de SystemMonitor

A classe [**SystemMonitor**](systemmonitor.md) tem os seguintes eventos:

-   [**OnCounterAdded**](systemmonitor-oncounteradded.md)
-   [**OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)
-   [**OnCounterSelected**](-systemmonitor-oncounterselected.md)
-   [**AoClicarDuasVezes**](-systemmonitor-ondblclick.md)
-   [**OnSampleCollected**](-systemmonitor-onsamplecollected.md)

> [!Note]  
> Você deve retornar do manipulador de eventos antes que o [**intervalo de atualização**](systemmonitor-updateinterval.md) expire; caso contrário, o SYSMON exibirá uma caixa de mensagem indicando ao usuário que ele não pôde obter amostras de valores de contadores para o intervalo de atualização anterior.

 

 

 




