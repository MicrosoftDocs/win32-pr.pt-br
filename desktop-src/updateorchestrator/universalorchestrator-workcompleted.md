---
title: IUniversalOrchestrator::WorkCompleted
description: Chama o orquestrador universal para indicar que o trabalho foi concluído
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 5094ae864b4df9a3dd53b90c3b7d099a206a0ad8db1d1176b603b5ba45ca8194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966066"
---
# <a name="iuniversalorchestratorworkcompleted-method"></a>Método IUniversalOrchestrator:: WorkCompleted

> [!NOTE] 
> Essa API pertence à API do Orchestrator universal.

Permite que os clientes informem ao orquestrador universal que o trabalho agendado anteriormente foi concluído e pare os retornos de chamada para executar o trabalho até a próxima chamada bem-sucedida do cronograma.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT WorkCompleted(
  LPCWSTR callerIdentifier,
  BOOL    workCompleted);
```

## <a name="parameters"></a>Parâmetros

`callerIdentifier`

Uma cadeia de caracteres exclusiva que identifica todas as chamadas desse cliente específico.

`workCompleted`

**True** se o trabalho for concluído com êxito. Caso contrário, **false** se a tentativa de trabalho falhou e deve ser repetida no futuro. 

## <a name="return-value"></a>Valor retornado
Se esse método tiver sucesso, ele retornará **S_OK**.  Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

| Requisito | Versão |
|---|---|
| Cliente mínimo com suporte | Windows 10 1903 |
|   |   |



 

 



