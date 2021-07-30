---
title: IUniversalOrchestrator::WorkCompleted
description: Chama o orquestrador universal para indicar que o trabalho foi concluído
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: e36a3ba744df807abbebc6332ac8433010afd667
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991823"
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



 

 



