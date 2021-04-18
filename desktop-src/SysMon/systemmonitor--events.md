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
ms.openlocfilehash: 94247cf81fcaf57f373c731cd4eaf06a3ca897ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105756122"
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

 

 

 




