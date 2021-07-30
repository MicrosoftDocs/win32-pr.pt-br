---
title: IUniversalOrchestrator::ScheduleWork
description: Chama o Orchestrator universal para agendar trabalho
ms.topic: reference
ms.date: 01/14/2021
ms.openlocfilehash: 4c49d06a28497c33e86cc1e919fdb59f2363d1f5
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991813"
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



 

 



