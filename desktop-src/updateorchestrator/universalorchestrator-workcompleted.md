---
title: IUniversalOrchestrator::WorkCompleted
description: Chama o orquestrador universal para indicar que o trabalho foi concluído
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 8d4a08e7f021811e59a182a8b726397476b78433
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/21/2021
ms.locfileid: "105794647"
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

## <a name="return-value"></a>Retornar valor
Se esse método tiver sucesso, ele retornará **S_OK**.  Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

| Requisito | Versão |
|---|---|
| Cliente mínimo com suporte | Windows 10 1903 |
|   |   |



 

 



