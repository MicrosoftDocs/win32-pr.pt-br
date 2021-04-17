---
description: Controlando recursos não alocados
ms.assetid: ebaca876-5249-4b6b-b0d5-08f098e3f5f5
title: Controlando recursos não alocados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c9f814e08798b4fbb0f160e0d0e0f8aabebba7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765752"
---
# <a name="tracking-non-allocated-resources"></a><span data-ttu-id="8176d-103">Controlando recursos não alocados</span><span class="sxs-lookup"><span data-stu-id="8176d-103">Tracking Non-Allocated Resources</span></span>

<span data-ttu-id="8176d-104">O Gerenciador do dispensador pode rastrear um recurso que não está inventariado, com base no conhecimento do tempo de vida do objeto.</span><span class="sxs-lookup"><span data-stu-id="8176d-104">The dispenser manager can track a resource that is not inventoried, based on knowledge of the object's lifetime.</span></span> <span data-ttu-id="8176d-105">Quando um recurso rastreado não alocado é liberado, ele é destruído e, portanto, não é retornado para o inventário.</span><span class="sxs-lookup"><span data-stu-id="8176d-105">When a tracked, non-allocated resource is freed, it is destroyed and therefore not returned to inventory.</span></span> <span data-ttu-id="8176d-106">Esse modo somente acompanhamento para recursos que são baratos para criar e destruir é mais útil do que armazená-los no inventário.</span><span class="sxs-lookup"><span data-stu-id="8176d-106">This track-only mode for resources that are inexpensive to create and destroy is more useful than storing them in inventory.</span></span> <span data-ttu-id="8176d-107">Esse modo também é útil para gerenciar um dispensador de memória ou para um recurso que é difícil de inventariar porque há muitos tipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="8176d-107">This mode is also useful for managing a memory dispenser or for a resource that is difficult to inventory because there are too many different types.</span></span>

<span data-ttu-id="8176d-108">No modo somente rastreamento, um dispensador de recurso cria diretamente um recurso solicitado em vez de pedir ao Gerenciador de dispensadores para alocar um do inventário.</span><span class="sxs-lookup"><span data-stu-id="8176d-108">In track-only mode, a resource dispenser directly creates a requested resource instead of asking the dispenser manager to allocate one from inventory.</span></span> <span data-ttu-id="8176d-109">Antes de retornar esse recurso para o componente de aplicativo solicitante, o dispensador de recursos informa o gerente do dispensador para controlar o recurso, o que garante que, mesmo que o componente fique inativo para liberar o recurso, o Gerenciador do dispensador fará isso quando o tempo de vida do componente terminar.</span><span class="sxs-lookup"><span data-stu-id="8176d-109">Before returning this resource to the requesting application component, the resource dispenser tells the dispenser manager to track the resource, which ensures that even if the component neglects to free the resource, the dispenser manager will do so when the component's lifetime is over.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8176d-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8176d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8176d-111">Conceitos do dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="8176d-111">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



