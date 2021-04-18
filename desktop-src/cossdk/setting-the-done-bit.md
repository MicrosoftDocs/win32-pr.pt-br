---
description: Definindo o bit concluído
ms.assetid: badd3b5a-ce6f-4be7-9dd8-a3b17344b185
title: Definindo o bit concluído
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a53368377016c88633d91d942cde1970d979563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797624"
---
# <a name="setting-the-done-bit"></a><span data-ttu-id="2e133-103">Definindo o bit concluído</span><span class="sxs-lookup"><span data-stu-id="2e133-103">Setting the Done Bit</span></span>

<span data-ttu-id="2e133-104">O COM+ desativará um objeto ativado por JIT com base no status de uma propriedade de contexto, o bit feito, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2e133-104">COM+ will deactivate a JIT-activated object based on the status of a context property, the done bit, as follows:</span></span>

-   <span data-ttu-id="2e133-105">Quando o bit Done é definido como true, o COM+ desativa o objeto quando a chamada do método atual retorna.</span><span class="sxs-lookup"><span data-stu-id="2e133-105">When the done bit is set to True, COM+ deactivates the object when the current method call returns.</span></span>
-   <span data-ttu-id="2e133-106">Quando o bit Done é definido como false, o objeto permanece ativo quando a chamada do método atual retorna.</span><span class="sxs-lookup"><span data-stu-id="2e133-106">When the done bit is set to False, the object remains active when the current method call returns.</span></span>

<span data-ttu-id="2e133-107">Por padrão, o bit Done é definido como false quando um objeto é criado e seu contexto é inicializado.</span><span class="sxs-lookup"><span data-stu-id="2e133-107">By default, the done bit is set to False when an object is created and its context initialized.</span></span> <span data-ttu-id="2e133-108">(Qualquer objeto ativado por JIT é criado em seu próprio contexto para que ele tenha seu próprio bit feito para ser definido.) No entanto, você pode alterar essa configuração padrão de acordo com cada método usando a propriedade auto-done.</span><span class="sxs-lookup"><span data-stu-id="2e133-108">(Any JIT-activated object is created in its own context so that it has its own done bit to set.) However, you can change this default setting on a per-method basis by using the auto-done property.</span></span> <span data-ttu-id="2e133-109">Você pode definir o bit concluído das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="2e133-109">You can set the done bit in the following ways:</span></span>

-   <span data-ttu-id="2e133-110">Usando [ **IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span><span class="sxs-lookup"><span data-stu-id="2e133-110">Using [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)</span></span>
-   <span data-ttu-id="2e133-111">Usando [ **IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span><span class="sxs-lookup"><span data-stu-id="2e133-111">Using [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)</span></span>
-   <span data-ttu-id="2e133-112">Usando a propriedade auto-Done</span><span class="sxs-lookup"><span data-stu-id="2e133-112">Using the auto-done property</span></span>

## <a name="using-icontextstate"></a><span data-ttu-id="2e133-113">Usando IContextState</span><span class="sxs-lookup"><span data-stu-id="2e133-113">Using IContextState</span></span>

<span data-ttu-id="2e133-114">Você pode usar [**IContextState:: SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) para definir o bit Done como true ou false.</span><span class="sxs-lookup"><span data-stu-id="2e133-114">You can use [**IContextState::SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) to set the done bit to True or False.</span></span>

<span data-ttu-id="2e133-115">Você pode usar [**IContextState:: GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) para obter o status atual do bit realizado do contexto do objeto.</span><span class="sxs-lookup"><span data-stu-id="2e133-115">You can use [**IContextState::GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) to get the current status of the done bit from the object context.</span></span>

## <a name="using-iobjectcontext"></a><span data-ttu-id="2e133-116">Usando IObjectContext</span><span class="sxs-lookup"><span data-stu-id="2e133-116">Using IObjectContext</span></span>

<span data-ttu-id="2e133-117">Você pode usar os seguintes métodos em [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) para definir o bit realizado enquanto define simultaneamente o bit consistente usado para votação em transações:</span><span class="sxs-lookup"><span data-stu-id="2e133-117">You can use the following methods on [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) to set the done bit while simultaneously setting the consistent bit used for voting in transactions:</span></span>

-   <span data-ttu-id="2e133-118">[**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) sinaliza que você concluiu e que votará para confirmar a transação atual.</span><span class="sxs-lookup"><span data-stu-id="2e133-118">[**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) signals both that you are done and that you vote to commit the current transaction.</span></span> <span data-ttu-id="2e133-119">Ele define o bit Done e o bit consistente como true.</span><span class="sxs-lookup"><span data-stu-id="2e133-119">It sets both the done bit and the consistent bit to True.</span></span>
-   <span data-ttu-id="2e133-120">Os sinais [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) que você concluiu e Dooms a transação atual.</span><span class="sxs-lookup"><span data-stu-id="2e133-120">[**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) signals that you are done and dooms the current transaction.</span></span> <span data-ttu-id="2e133-121">Ele define o bit Done como true e o bit consistente como false.</span><span class="sxs-lookup"><span data-stu-id="2e133-121">It sets the done bit to True and the consistent bit to False.</span></span>
-   <span data-ttu-id="2e133-122">[**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) sinaliza que você não está pronto, mas que você votará para confirmar a transação.</span><span class="sxs-lookup"><span data-stu-id="2e133-122">[**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) signals that you are not done but that you vote to commit the transaction.</span></span> <span data-ttu-id="2e133-123">Ele define o bit Done como false e o bit consistente como true.</span><span class="sxs-lookup"><span data-stu-id="2e133-123">It sets the done bit to False and the consistent bit to True.</span></span>
-   <span data-ttu-id="2e133-124">[**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) sinaliza que você não está pronto e que vote em não confirmar a transação no momento, geralmente porque o estado é inconsistente.</span><span class="sxs-lookup"><span data-stu-id="2e133-124">[**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) signals that you are not done and that you vote not to commit the transaction at this time, usually because the state is inconsistent.</span></span> <span data-ttu-id="2e133-125">Ele define o bit Done e o bit consistente como false.</span><span class="sxs-lookup"><span data-stu-id="2e133-125">It sets both the done bit and the consistent bit to False.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e133-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e133-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e133-127">Conceitos de ativação Just-in-time COM+</span><span class="sxs-lookup"><span data-stu-id="2e133-127">COM+ Just-in-Time Activation Concepts</span></span>](com--just-in-time-activation-concepts.md)
</dt> <dt>

[<span data-ttu-id="2e133-128">Habilitando a ativação JIT para um componente</span><span class="sxs-lookup"><span data-stu-id="2e133-128">Enabling JIT Activation for a Component</span></span>](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="2e133-129">Pooling de objetos e ativação JIT do COM+</span><span class="sxs-lookup"><span data-stu-id="2e133-129">Object Pooling and COM+ JIT Activation</span></span>](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[<span data-ttu-id="2e133-130">Transações e ativação JIT do COM+</span><span class="sxs-lookup"><span data-stu-id="2e133-130">Transactions and COM+ JIT Activation</span></span>](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



