---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Consulta o Orchestrator universal para determinar se o período pós-OOBE foi superado.
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 2ed354d365b795a0c959396e6b26d6bc73baad97
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/21/2021
ms.locfileid: "105780763"
---
# <a name="iuniversalorchestratorhasmoratoriumpassed-method"></a><span data-ttu-id="4409c-103">Método IUniversalOrchestrator:: HasMoratoriumPassed</span><span class="sxs-lookup"><span data-stu-id="4409c-103">IUniversalOrchestrator::HasMoratoriumPassed method</span></span>

> [!NOTE] 
> <span data-ttu-id="4409c-104">Essa API pertence à API do Orchestrator universal.</span><span class="sxs-lookup"><span data-stu-id="4409c-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="4409c-105">Permite que os clientes determinem se o universal Orchestrator está operando imediatamente após o novo dispositivo de experiência inicial, o que limita as tentativas de trabalho de minimizar a interrupção do usuário.</span><span class="sxs-lookup"><span data-stu-id="4409c-105">Allows clients to determine if Universal Orchestrator is operating immediately after the new device Out of Box Experience, which limits work attempts to minimize user interruption.</span></span> 

## <a name="syntax"></a><span data-ttu-id="4409c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4409c-106">Syntax</span></span>

```C++
HRESULT HasMoratoriumPassed(
  LPCWSTR callerIdentifier,
  BOOL*   moratoriumPassed);
```

## <a name="parameters"></a><span data-ttu-id="4409c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4409c-107">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="4409c-108">Uma cadeia de caracteres exclusiva que identifica todas as chamadas desse cliente específico.</span><span class="sxs-lookup"><span data-stu-id="4409c-108">A unique string that identifies all calls from this specific client.</span></span>

`hasMoratoriumPassed`

<span data-ttu-id="4409c-109">Parâmetro de saída que armazena o resultado da consulta.</span><span class="sxs-lookup"><span data-stu-id="4409c-109">Output parameter that stores the result of the query.</span></span>

## <a name="return-value"></a><span data-ttu-id="4409c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4409c-110">Return value</span></span>
<span data-ttu-id="4409c-111">Se esse método tiver sucesso, ele retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="4409c-111">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="4409c-112">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4409c-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4409c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4409c-113">Requirements</span></span>

| <span data-ttu-id="4409c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4409c-114">Requirement</span></span> | <span data-ttu-id="4409c-115">Versão</span><span class="sxs-lookup"><span data-stu-id="4409c-115">Version</span></span> |
|---|---|
| <span data-ttu-id="4409c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4409c-116">Minimum supported client</span></span> | <span data-ttu-id="4409c-117">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="4409c-117">Windows 10 1903</span></span> |
|   |   |



 

 



