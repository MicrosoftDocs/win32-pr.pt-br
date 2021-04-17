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
# <a name="iuniversalorchestrator-interface"></a><span data-ttu-id="9f10a-103">Interface IUniversalOrchestrator</span><span class="sxs-lookup"><span data-stu-id="9f10a-103">IUniversalOrchestrator interface</span></span>

> [!NOTE] 
> <span data-ttu-id="9f10a-104">Essa API pertence à API do Orchestrator universal.</span><span class="sxs-lookup"><span data-stu-id="9f10a-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="9f10a-105">**IUniversalOrchestrator** é uma interface com que fornece os métodos a seguir para permitir que um cliente se comunique com o Orchestrator universal.</span><span class="sxs-lookup"><span data-stu-id="9f10a-105">**IUniversalOrchestrator** is a COM interface that provides the following methods to allow a client to communicate with the Universal Orchestrator.</span></span>

## <a name="methods"></a><span data-ttu-id="9f10a-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="9f10a-106">Methods</span></span>

|<span data-ttu-id="9f10a-107">Método</span><span class="sxs-lookup"><span data-stu-id="9f10a-107">Method</span></span> | <span data-ttu-id="9f10a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f10a-108">Description</span></span> |
|---|---|
|[<span data-ttu-id="9f10a-109">:: Agendar</span><span class="sxs-lookup"><span data-stu-id="9f10a-109">::ScheduleWork</span></span>](universalorchestrator-schedulework.md) | <span data-ttu-id="9f10a-110">Registra o trabalho pendente com o Orchestrator universal.</span><span class="sxs-lookup"><span data-stu-id="9f10a-110">Registers pending work with the Universal Orchestrator.</span></span> |
|[<span data-ttu-id="9f10a-111">::WorkCompleted</span><span class="sxs-lookup"><span data-stu-id="9f10a-111">::WorkCompleted</span></span>](universalorchestrator-workcompleted.md) | <span data-ttu-id="9f10a-112">Informa ao orquestrador universal que todo o trabalho foi concluído.</span><span class="sxs-lookup"><span data-stu-id="9f10a-112">Informs the Universal Orchestrator that all work is complete.</span></span> |
|[<span data-ttu-id="9f10a-113">::HasMoratoriumPassed</span><span class="sxs-lookup"><span data-stu-id="9f10a-113">::HasMoratoriumPassed</span></span>](universalorchestrator-hasmoratoriumpassed.md) | <span data-ttu-id="9f10a-114">Consulta o Orchestrator universal para determinar se ele está funcionando imediatamente após a nova experiência de dispositivo pronto para uso.</span><span class="sxs-lookup"><span data-stu-id="9f10a-114">Queries Universal Orchestrator to determine if it is operating immediately after the new device Out of Box Experience.</span></span> |


## <a name="requirements"></a><span data-ttu-id="9f10a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f10a-115">Requirements</span></span>

| <span data-ttu-id="9f10a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f10a-116">Requirement</span></span> | <span data-ttu-id="9f10a-117">Versão</span><span class="sxs-lookup"><span data-stu-id="9f10a-117">Version</span></span> |
|---|---|
| <span data-ttu-id="9f10a-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f10a-118">Minimum supported client</span></span> | <span data-ttu-id="9f10a-119">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="9f10a-119">Windows 10 1903</span></span> |
|   |   |