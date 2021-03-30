---
title: Interface IReconcileInitiator
description: Expõe métodos que fornecem ao porta-arquivos reconciliador o meio para notificar o iniciador sobre seu progresso, definir um objeto de encerramento e solicitar uma determinada versão de um documento. O iniciador é responsável por implementar essa interface.
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
keywords:
- Recursos do ambiente Windows herdado da interface IReconcileInitiator
- Recursos do ambiente Windows herdado da interface IReconcileInitiator, descritos
topic_type:
- apiref
api_name:
- IReconcileInitiator
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759ad26fd87db7076811b9b31d6ef39df1479e3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644674"
---
# <a name="ireconcileinitiator-interface"></a><span data-ttu-id="3f678-106">Interface IReconcileInitiator</span><span class="sxs-lookup"><span data-stu-id="3f678-106">IReconcileInitiator interface</span></span>

<span data-ttu-id="3f678-107">Expõe métodos que fornecem ao porta-arquivos reconciliador o meio para notificar o iniciador sobre seu progresso, definir um objeto de encerramento e solicitar uma determinada versão de um documento.</span><span class="sxs-lookup"><span data-stu-id="3f678-107">Exposes methods that provide the briefcase reconciler with the means to notify the initiator of its progress, to set a termination object, and to request a given version of a document.</span></span> <span data-ttu-id="3f678-108">O iniciador é responsável por implementar essa interface.</span><span class="sxs-lookup"><span data-stu-id="3f678-108">The initiator is responsible for implementing this interface.</span></span>

## <a name="members"></a><span data-ttu-id="3f678-109">Membros</span><span class="sxs-lookup"><span data-stu-id="3f678-109">Members</span></span>

<span data-ttu-id="3f678-110">A interface **IReconcileInitiator** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3f678-110">The **IReconcileInitiator** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3f678-111">**IReconcileInitiator** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3f678-111">**IReconcileInitiator** also has these types of members:</span></span>

-   [<span data-ttu-id="3f678-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3f678-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3f678-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="3f678-113">Methods</span></span>

<span data-ttu-id="3f678-114">A interface **IReconcileInitiator** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3f678-114">The **IReconcileInitiator** interface has these methods.</span></span>



| <span data-ttu-id="3f678-115">Método</span><span class="sxs-lookup"><span data-stu-id="3f678-115">Method</span></span>                                                                 | <span data-ttu-id="3f678-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f678-116">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f678-117">**SetAbortCallback**</span><span class="sxs-lookup"><span data-stu-id="3f678-117">**SetAbortCallback**</span></span>](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)       | <span data-ttu-id="3f678-118">Define o objeto por meio do qual o iniciador pode finalizar uma reconciliação de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="3f678-118">Sets the object through which the initiator can asynchronously terminate a reconciliation.</span></span> <span data-ttu-id="3f678-119">Um porta-arquivos reconciliador normalmente define esse objeto para reconciliações que são demoradas ou envolvem a interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3f678-119">A briefcase reconciler typically sets this object for reconciliations that are lengthy or involve user interaction.</span></span> <br/>                                                                                              |
| [<span data-ttu-id="3f678-120">**SetProgressFeedback**</span><span class="sxs-lookup"><span data-stu-id="3f678-120">**SetProgressFeedback**</span></span>](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback) | <span data-ttu-id="3f678-121">Indica a quantidade de progresso que o porta-arquivos Reconciler fez para concluir a reconciliação.</span><span class="sxs-lookup"><span data-stu-id="3f678-121">Indicates the amount of progress the briefcase reconciler has made toward completing the reconciliation.</span></span> <span data-ttu-id="3f678-122">O valor é uma fração e é calculado como o quociente dos parâmetros *ulProgress* e *ulProgressMax* .</span><span class="sxs-lookup"><span data-stu-id="3f678-122">The amount is a fraction and is computed as the quotient of the *ulProgress* and *ulProgressMax* parameters.</span></span> <span data-ttu-id="3f678-123">Os reconciliadores devem chamar esse método periodicamente durante o processo de reconciliação.</span><span class="sxs-lookup"><span data-stu-id="3f678-123">Reconcilers should call this method periodically during their reconciliation process.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="3f678-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f678-124">Requirements</span></span>



| <span data-ttu-id="3f678-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f678-125">Requirement</span></span> | <span data-ttu-id="3f678-126">Valor</span><span class="sxs-lookup"><span data-stu-id="3f678-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f678-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f678-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3f678-128">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3f678-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="3f678-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f678-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3f678-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3f678-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3f678-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3f678-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f678-132"><dt>Shell32.dll (versão 4,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="3f678-132"><dt>Shell32.dll (version 4.0 or later)</dt></span></span> </dl> |



 

