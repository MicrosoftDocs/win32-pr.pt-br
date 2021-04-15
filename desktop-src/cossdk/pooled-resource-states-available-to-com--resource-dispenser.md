---
description: Estados de recursos em pool disponíveis para o dispensador de recursos COM+
ms.assetid: 5037f11c-d113-49b0-b26f-0e3bc59ae8b3
title: Estados de recursos em pool disponíveis para o dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0bc59dcc2b7e95e060c0d6e96a5880d09d26e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457052"
---
# <a name="pooled-resource-states-available-to-com-resource-dispenser"></a><span data-ttu-id="5fdac-103">Estados de recursos em pool disponíveis para o dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="5fdac-103">Pooled Resource States Available to COM+ Resource Dispenser</span></span>

<span data-ttu-id="5fdac-104">A qualquer momento, um recurso está em uso ou não está em uso e é inscrito ou não inscrito em uma transação.</span><span class="sxs-lookup"><span data-stu-id="5fdac-104">At any one time, a resource is either in use or not in use and is either enlisted or not enlisted in a transaction.</span></span> <span data-ttu-id="5fdac-105">Isso produz quatro Estados de recursos possíveis, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5fdac-105">This yields four possible resource states, as follows:</span></span>

-   <span data-ttu-id="5fdac-106">**Recursos no inventário não inscrito.**</span><span class="sxs-lookup"><span data-stu-id="5fdac-106">**Resources in unenlisted inventory.**</span></span> <span data-ttu-id="5fdac-107">Um recurso que não está sendo usado por um objeto e que não está inscrito em uma transação está no inventário não inscrito.</span><span class="sxs-lookup"><span data-stu-id="5fdac-107">A resource that is not in use by an object and not enlisted in a transaction is in unenlisted inventory.</span></span> <span data-ttu-id="5fdac-108">Um recurso no inventário geral está disponível para atribuição.</span><span class="sxs-lookup"><span data-stu-id="5fdac-108">A resource in general inventory is available for assignment.</span></span>

-   <span data-ttu-id="5fdac-109">**Recursos no inventário inscrito.**</span><span class="sxs-lookup"><span data-stu-id="5fdac-109">**Resources in enlisted inventory.**</span></span> <span data-ttu-id="5fdac-110">Um recurso que não está sendo usado por um objeto, mas que está inscrito em uma transação está no estoque inscrito.</span><span class="sxs-lookup"><span data-stu-id="5fdac-110">A resource that is not in use by an object but is enlisted in a transaction is in enlisted inventory.</span></span> <span data-ttu-id="5fdac-111">Esse recurso está disponível para atribuição somente a objetos em execução na mesma transação.</span><span class="sxs-lookup"><span data-stu-id="5fdac-111">Such a resource is available for assignment only to objects running in the same transaction.</span></span> <span data-ttu-id="5fdac-112">Um recurso passa do inventário inscrito para o inventário não inscrito quando o COM+ notifica o Gerenciador do dispensador de que a transação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="5fdac-112">A resource moves from enlisted inventory to unenlisted inventory when COM+ notifies the dispenser manager that the transaction is complete.</span></span>

-   <span data-ttu-id="5fdac-113">**Recursos no uso não inscrito.**</span><span class="sxs-lookup"><span data-stu-id="5fdac-113">**Resources in unenlisted use.**</span></span> <span data-ttu-id="5fdac-114">Se um recurso for atribuído a um objeto e a instância não estiver sendo executada em uma transação ou o dispensador de recurso tiver identificado o recurso como não transacional, esse recurso estará no uso não inscrito.</span><span class="sxs-lookup"><span data-stu-id="5fdac-114">If a resource is assigned to an object and the instance is not running in a transaction or the resource dispenser has identified the resource as non-transactional, this resource is in unenlisted use.</span></span>

-   <span data-ttu-id="5fdac-115">**Recursos no uso inscrito.**</span><span class="sxs-lookup"><span data-stu-id="5fdac-115">**Resources in enlisted use.**</span></span> <span data-ttu-id="5fdac-116">Se um recurso for atribuído a um objeto, a instância estiver sendo executada em uma transação e o dispensador de recursos tiver inscrito com êxito o recurso na transação, esse recurso estará no uso inscrito.</span><span class="sxs-lookup"><span data-stu-id="5fdac-116">If a resource is assigned to an object, the instance is running in a transaction, and the resource dispenser has successfully enlisted the resource in the transaction, this resource is in enlisted use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5fdac-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5fdac-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fdac-118">Conceitos do dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="5fdac-118">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="5fdac-119">Inlistando um recurso em uma transação</span><span class="sxs-lookup"><span data-stu-id="5fdac-119">Enlisting a Resource in a Transaction</span></span>](enlisting-a-resource-in-a-transaction.md)
</dt> </dl>

 

 



