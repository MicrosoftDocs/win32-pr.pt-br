---
description: Implementando um dispensador de recursos COM+
ms.assetid: 083c5962-f55a-435a-964e-fdc868f9bd3d
title: Implementando um dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81e189f3bfc5025bc949ef6e5bc82bf9408c339
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089571"
---
# <a name="implementing-a-com-resource-dispenser"></a><span data-ttu-id="dd9f0-103">Implementando um dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="dd9f0-103">Implementing a COM+ Resource Dispenser</span></span>

<span data-ttu-id="dd9f0-104">As etapas a seguir descrevem um procedimento geral para implementar um dispensador de recursos COM+:</span><span class="sxs-lookup"><span data-stu-id="dd9f0-104">The following steps outline a general procedure for implementing a COM+ resource dispenser:</span></span>

1.  <span data-ttu-id="dd9f0-105">Decida sobre o formato **RESTYPID** que categoriza como seus recursos diferem uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="dd9f0-105">Decide on **RESTYPID** format that categorizes how your resources differ from each other.</span></span>

2.  <span data-ttu-id="dd9f0-106">Use a biblioteca e o arquivo de cabeçalho Mtxdm. h e Mtxdm. lib, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="dd9f0-106">Use the Mtxdm.h and Mtxdm.lib header file and library, respectively.</span></span>

3.  <span data-ttu-id="dd9f0-107">Crie uma DLL que implemente a interface [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) e a API que você deseja expor aos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="dd9f0-107">Build a DLL that implements the [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) interface and the API you want to expose to applications.</span></span>

4.  <span data-ttu-id="dd9f0-108">Na inicialização ([*DllMain*](/windows/desktop/Dlls/dllmain) ou primeiro chamada para a API do dispensador), chame a função [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) .</span><span class="sxs-lookup"><span data-stu-id="dd9f0-108">In the startup ([*DllMain*](/windows/desktop/Dlls/dllmain) or first call to the dispenser API), call the [**GetDispenserManager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) function.</span></span> <span data-ttu-id="dd9f0-109">Isso retorna um ponteiro para a interface [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) do Gerenciador do dispensador.</span><span class="sxs-lookup"><span data-stu-id="dd9f0-109">This returns a pointer to the dispenser manager's [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) interface.</span></span>

5.  <span data-ttu-id="dd9f0-110">Chame [**IDispenserManager:: RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), passando um ponteiro para a implementação de [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver).</span><span class="sxs-lookup"><span data-stu-id="dd9f0-110">Call [**IDispenserManager::RegisterDispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser), passing a pointer to your implementation of [**IDispenserDriver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver).</span></span> <span data-ttu-id="dd9f0-111">Isso faz com que o Gerenciador do dispensador crie um detentor (Gerenciador de pooling) para o dispensador de recursos e, em seguida, retorne o ponteiro para a interface [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) .</span><span class="sxs-lookup"><span data-stu-id="dd9f0-111">This causes the dispenser manager to create a holder (pooling manager) for your resource dispenser and then return the pointer to your [**IHolder**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder) interface.</span></span>

6.  <span data-ttu-id="dd9f0-112">Armazene esse ponteiro para que você possa chamar [**IHolder:: AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) e [**IHolder:: FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span><span class="sxs-lookup"><span data-stu-id="dd9f0-112">Store this pointer so that you can call [**IHolder::AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) and [**IHolder::FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span></span>

7.  <span data-ttu-id="dd9f0-113">Agora você pode (em resposta a chamadas para sua API) fazer chamadas para [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) e [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span><span class="sxs-lookup"><span data-stu-id="dd9f0-113">You can now (in response to calls to your API) make calls to [**AllocResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-allocresource) and [**FreeResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-freeresource).</span></span> <span data-ttu-id="dd9f0-114">Inicialmente, o **AllocResource** responde chamando de volta para o método [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) , mas as chamadas de **AllocResource** posteriores são atendidas a partir do pool crescente de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd9f0-114">**AllocResource** initially responds by calling back to your [**CreateResource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-createresource) method, but later **AllocResource** calls are serviced from the growing pool of resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd9f0-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd9f0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd9f0-116">Conceitos do dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="dd9f0-116">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="dd9f0-117">Interfaces do dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="dd9f0-117">COM+ Resource Dispenser Interfaces</span></span>](com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 
