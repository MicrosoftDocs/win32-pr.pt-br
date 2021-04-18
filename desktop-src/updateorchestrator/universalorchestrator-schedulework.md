---
title: IUniversalOrchestrator::ScheduleWork
description: Chama o Orchestrator universal para agendar trabalho
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 456df8f975114f7bdf750a0449f3bd98efcc3b2e
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/21/2021
ms.locfileid: "105764340"
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

## <a name="return-value"></a>Retornar valor
Se esse método tiver sucesso, ele retornará **S_OK**.  Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos

| Requisito | Versão |
|---|---|
| Cliente mínimo com suporte | Windows 10 1903 |
|   |   |



 

 



