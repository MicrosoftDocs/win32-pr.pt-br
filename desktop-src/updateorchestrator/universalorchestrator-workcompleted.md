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
# <a name="iuniversalorchestratorworkcompleted-method"></a><span data-ttu-id="96321-103">Método IUniversalOrchestrator:: WorkCompleted</span><span class="sxs-lookup"><span data-stu-id="96321-103">IUniversalOrchestrator::WorkCompleted method</span></span>

> [!NOTE] 
> <span data-ttu-id="96321-104">Essa API pertence à API do Orchestrator universal.</span><span class="sxs-lookup"><span data-stu-id="96321-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="96321-105">Permite que os clientes informem ao orquestrador universal que o trabalho agendado anteriormente foi concluído e pare os retornos de chamada para executar o trabalho até a próxima chamada bem-sucedida do cronograma.</span><span class="sxs-lookup"><span data-stu-id="96321-105">Allows clients to inform Universal Orchestrator that the previously scheduled work has been completed and stop callbacks to perform work until the next successful ScheduleWork call.</span></span>

## <a name="syntax"></a><span data-ttu-id="96321-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96321-106">Syntax</span></span>

```C++
HRESULT WorkCompleted(
  LPCWSTR callerIdentifier,
  BOOL    workCompleted);
```

## <a name="parameters"></a><span data-ttu-id="96321-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96321-107">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="96321-108">Uma cadeia de caracteres exclusiva que identifica todas as chamadas desse cliente específico.</span><span class="sxs-lookup"><span data-stu-id="96321-108">A unique string that identifies all calls from this specific client.</span></span>

`workCompleted`

<span data-ttu-id="96321-109">**True** se o trabalho for concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="96321-109">**TRUE** if the work successfully completed.</span></span> <span data-ttu-id="96321-110">Caso contrário, **false** se a tentativa de trabalho falhou e deve ser repetida no futuro.</span><span class="sxs-lookup"><span data-stu-id="96321-110">Otherwise, **FALSE** if the work attempt failed and should be retried in the future.</span></span> 

## <a name="return-value"></a><span data-ttu-id="96321-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="96321-111">Return value</span></span>
<span data-ttu-id="96321-112">Se esse método tiver sucesso, ele retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="96321-112">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="96321-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="96321-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="96321-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96321-114">Requirements</span></span>

| <span data-ttu-id="96321-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="96321-115">Requirement</span></span> | <span data-ttu-id="96321-116">Versão</span><span class="sxs-lookup"><span data-stu-id="96321-116">Version</span></span> |
|---|---|
| <span data-ttu-id="96321-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96321-117">Minimum supported client</span></span> | <span data-ttu-id="96321-118">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="96321-118">Windows 10 1903</span></span> |
|   |   |



 

 



