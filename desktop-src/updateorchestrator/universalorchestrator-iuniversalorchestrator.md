---
title: Interface IUniversalOrchestrator
description: Uma interface COM que fornece métodos para permitir que um cliente se comunique com o Orchestrator universal.
ms.date: 01/14/2021
ms.topic: reference
ms.openlocfilehash: f3635f76236eb6c7a11bfa62311003b7d76357a9fbacc9fde85f0bdffed0c129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966112"
---
# <a name="iuniversalorchestrator-interface"></a>Interface IUniversalOrchestrator

> [!NOTE] 
> Essa API pertence à API do Orchestrator universal.

**IUniversalOrchestrator** é uma interface com que fornece os métodos a seguir para permitir que um cliente se comunique com o Orchestrator universal.

## <a name="methods"></a>Métodos

|Método | Descrição |
|---|---|
|[:: Agendar](universalorchestrator-schedulework.md) | Registra o trabalho pendente com o Orchestrator universal. |
|[::WorkCompleted](universalorchestrator-workcompleted.md) | Informa ao orquestrador universal que todo o trabalho foi concluído. |
|[::HasMoratoriumPassed](universalorchestrator-hasmoratoriumpassed.md) | Consulta o Orchestrator universal para determinar se ele está funcionando imediatamente após a nova experiência de dispositivo pronto para uso. |


## <a name="requirements"></a>Requisitos

| Requisito | Versão |
|---|---|
| Cliente mínimo com suporte | Windows 10 1903 |
|   |   |