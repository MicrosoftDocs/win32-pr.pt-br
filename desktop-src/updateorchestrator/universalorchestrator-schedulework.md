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
# <a name="iuniversalorchestratorschedulework-method"></a><span data-ttu-id="bb3f8-103">Método IUniversalOrchestrator:: Scheduley</span><span class="sxs-lookup"><span data-stu-id="bb3f8-103">IUniversalOrchestrator::ScheduleWork method</span></span>

> [!NOTE] 
> <span data-ttu-id="bb3f8-104">Essa API pertence à API do Orchestrator universal.</span><span class="sxs-lookup"><span data-stu-id="bb3f8-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="bb3f8-105">Permite que os clientes informem ao orquestrador universal que o trabalho está pendente e forneça um binário que será chamado pelo orquestrador universal para executar o trabalho de atualização em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="bb3f8-105">Allows clients to inform Universal Orchestrator that work is pending and provide a binary that will be called by Universal Orchestrator to perform the update work at a later time.</span></span>

<span data-ttu-id="bb3f8-106">O binário de retorno de chamada deve ser assinado com um certificado da Microsoft válido e o chamador deve chamar a chamada de agenda do contexto do sistema.</span><span class="sxs-lookup"><span data-stu-id="bb3f8-106">The callback binary must be signed with a valid Microsoft certificate, and the caller must be invoking the ScheduleWork call from SYSTEM context.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb3f8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb3f8-107">Syntax</span></span>

```C++
HRESULT ScheduleWork(
  LPCWSTR callerIdentifier,
  LPCWSTR cmdLine
  LPCWSTR startArg,
  LPCWSTR pauseArg);
```

## <a name="parameters"></a><span data-ttu-id="bb3f8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb3f8-108">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="bb3f8-109">Uma cadeia de caracteres exclusiva que identifica todas as chamadas desse cliente específico.</span><span class="sxs-lookup"><span data-stu-id="bb3f8-109">A unique string that identifies all calls from this specific client.</span></span>

`cmdLine`

<span data-ttu-id="bb3f8-110">O caminho completo para o binário de retorno de chamada que será invocado pelo Universal Orchestrator para executar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="bb3f8-110">The full path to the callback binary that will be invoked by Universal Orchestrator to perform work.</span></span>

`startArg`

<span data-ttu-id="bb3f8-111">Parâmetros a serem passados para o binário de retorno de chamada para indicar que Start é solicitado.</span><span class="sxs-lookup"><span data-stu-id="bb3f8-111">Parameters to pass to the callback binary to indicate Start is requested.</span></span>

`pauseArg`

<span data-ttu-id="bb3f8-112">*(opcional)* Parâmetros a serem passados para o binário de retorno de chamada para indicar que Pause é solicitado.</span><span class="sxs-lookup"><span data-stu-id="bb3f8-112">*(optional)* Parameters to pass to the callback binary to indicate Pause is requested.</span></span>

## <a name="return-value"></a><span data-ttu-id="bb3f8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb3f8-113">Return value</span></span>
<span data-ttu-id="bb3f8-114">Se esse método tiver sucesso, ele retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="bb3f8-114">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="bb3f8-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bb3f8-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb3f8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb3f8-116">Requirements</span></span>

| <span data-ttu-id="bb3f8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb3f8-117">Requirement</span></span> | <span data-ttu-id="bb3f8-118">Versão</span><span class="sxs-lookup"><span data-stu-id="bb3f8-118">Version</span></span> |
|---|---|
| <span data-ttu-id="bb3f8-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb3f8-119">Minimum supported client</span></span> | <span data-ttu-id="bb3f8-120">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="bb3f8-120">Windows 10 1903</span></span> |
|   |   |



 

 



