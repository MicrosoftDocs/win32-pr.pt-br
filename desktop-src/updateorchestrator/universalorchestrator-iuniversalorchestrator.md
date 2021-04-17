---
title: Interface IUniversalOrchestrator
description: Uma interface COM que fornece métodos para permitir que um cliente se comunique com o Orchestrator universal.
ms.date: 01/14/2021
ms.topic: interface
ms.openlocfilehash: 6fa5dfd9f7853159645fbe3b543c228450f4e1c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/21/2021
ms.locfileid: "105790668"
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