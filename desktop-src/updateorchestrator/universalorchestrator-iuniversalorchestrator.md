---
title: Interface IUniversalOrchestrator
description: Uma interface COM que fornece métodos para permitir que um cliente se comunique com o Universal Orchestrator.
ms.date: 01/14/2021
ms.topic: reference
ms.openlocfilehash: 5dbbaafb38ab9d790d32beca9b014f933d5d53d5
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991843"
---
# <a name="iuniversalorchestrator-interface"></a>Interface IUniversalOrchestrator

> [!NOTE] 
> Essa API pertence à API universal do Orchestrator.

**IUniversalOrchestrator** é uma interface COM que fornece os métodos a seguir para permitir que um cliente se comunique com o Universal Orchestrator.

## <a name="methods"></a>Métodos

|Método | Descrição |
|---|---|
|[::ScheduleWork](universalorchestrator-schedulework.md) | Registra o trabalho pendente com o Orquestrador Universal. |
|[::WorkCompleted](universalorchestrator-workcompleted.md) | Informa ao Orquestrador Universal que todo o trabalho foi concluído. |
|[::HasMor ltdapassed](universalorchestrator-hasmoratoriumpassed.md) | Consulta o Universal Orchestrator para determinar se ele está operando imediatamente após a nova experiência pronta para uso do dispositivo. |


## <a name="requirements"></a>Requisitos

| Requisito | Versão |
|---|---|
| Cliente mínimo com suporte | Windows 10 1903 |
|   |   |