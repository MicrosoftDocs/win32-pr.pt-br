---
title: IUniversalOrchestrator::ScheduleWork
description: Chama o Orchestrator universal para agendar trabalho
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: bb2ecc67167e0651663856354a07ec86f985c664f1d2bccff98917adf72f054d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966065"
---
# <a name="iuniversalorchestratorschedulework-method"></a>Método IUniversalOrchestrator:: Scheduley

> [!NOTE] 
> Essa API pertence à API do Orchestrator universal.

Permite que os clientes informem ao orquestrador universal que o trabalho está pendente e forneça um binário que será chamado pelo orquestrador universal para executar o trabalho de atualização em um momento posterior.

O binário de retorno de chamada deve ser assinado com um certificado da Microsoft válido e o chamador deve chamar a chamada de agenda do contexto do sistema.

## <a name="syntax"></a>Sintaxe

```C++
HRESULT ScheduleWork(
  LPCWSTR callerIdentifier,
  LPCWSTR cmdLine
  LPCWSTR startArg,
  LPCWSTR pauseArg);
```

## <a name="parameters"></a>Parâmetros

`callerIdentifier`

Uma cadeia de caracteres exclusiva que identifica todas as chamadas desse cliente específico.

`cmdLine`

O caminho completo para o binário de retorno de chamada que será invocado pelo Universal Orchestrator para executar o trabalho.

`startArg`

Parâmetros a serem passados para o binário de retorno de chamada para indicar que Start é solicitado.

`pauseArg`

*(opcional)* Parâmetros a serem passados para o binário de retorno de chamada para indicar que Pause é solicitado.

## <a name="return-value"></a>Valor retornado
Se esse método tiver sucesso, ele retornará **S_OK**.  Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

| Requisito | Versão |
|---|---|
| Cliente mínimo com suporte | Windows 10 1903 |
|   |   |



 

 



