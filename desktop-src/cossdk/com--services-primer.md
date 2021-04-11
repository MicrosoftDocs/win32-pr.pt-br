---
description: O COM+ fornece um modelo de programação simples para usar seus serviços automáticos.
ms.assetid: 2d616b56-4b6a-4c3b-bbd8-d5ca03c4911f
title: Primer de serviços COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9fd9d256b0213d3b1c58cae7d9670f87e4f4423
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296117"
---
# <a name="com-services-primer"></a><span data-ttu-id="d7a13-103">Primer de serviços COM+</span><span class="sxs-lookup"><span data-stu-id="d7a13-103">COM+ Services Primer</span></span>

<span data-ttu-id="d7a13-104">O COM+ fornece um modelo de programação simples para usar seus serviços automáticos.</span><span class="sxs-lookup"><span data-stu-id="d7a13-104">COM+ provides a simple programming model for using its automatic services.</span></span> <span data-ttu-id="d7a13-105">Você pode simplesmente definir esses serviços como atributos declarativos em componentes e seus métodos.</span><span class="sxs-lookup"><span data-stu-id="d7a13-105">You can simply set these services as declarative attributes on components and their methods.</span></span> <span data-ttu-id="d7a13-106">Quando você define esses atributos, o COM+ entrega automaticamente os serviços solicitados ao objeto, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="d7a13-106">When you set these attributes, COM+ automatically delivers the requested services to the object as required.</span></span>

<span data-ttu-id="d7a13-107">Este primer mostra os serviços COM+ em ação percorrendo o código do componente de exemplo em três etapas definidas.</span><span class="sxs-lookup"><span data-stu-id="d7a13-107">This primer shows COM+ services in action by walking through sample component code in three defined steps.</span></span> <span data-ttu-id="d7a13-108">A complexidade das informações é compilada conforme as etapas estão em andamento.</span><span class="sxs-lookup"><span data-stu-id="d7a13-108">The complexity of the information builds as the steps progress.</span></span> <span data-ttu-id="d7a13-109">O código se concentra no modelo de programação simplificado, usando o processamento de transações para demonstrar princípios COM+ básicos.</span><span class="sxs-lookup"><span data-stu-id="d7a13-109">The code focuses on the simplified programming model, using transaction processing to demonstrate basic COM+ principles.</span></span>

<span data-ttu-id="d7a13-110">Cada uma das etapas a seguir ilustra um aspecto fundamental dos serviços COM+:</span><span class="sxs-lookup"><span data-stu-id="d7a13-110">Each of the following steps illustrates a fundamental aspect of COM+ services:</span></span>

-   [<span data-ttu-id="d7a13-111">Etapa 1: Criando um componente transacional</span><span class="sxs-lookup"><span data-stu-id="d7a13-111">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
-   [<span data-ttu-id="d7a13-112">Etapa 2: estendendo uma transação entre vários componentes</span><span class="sxs-lookup"><span data-stu-id="d7a13-112">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
-   [<span data-ttu-id="d7a13-113">Etapa 3: reutilizando os componentes</span><span class="sxs-lookup"><span data-stu-id="d7a13-113">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)

## <a name="related-topics"></a><span data-ttu-id="d7a13-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7a13-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7a13-115">Visão geral da programação COM+</span><span class="sxs-lookup"><span data-stu-id="d7a13-115">COM+ Programming Overview</span></span>](com--programming-overview.md)
</dt> <dt>

[<span data-ttu-id="d7a13-116">Visão geral do aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="d7a13-116">COM+ Application Overview</span></span>](com--application-overview.md)
</dt> <dt>

[<span data-ttu-id="d7a13-117">Configurando aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="d7a13-117">Configuring COM+ Applications</span></span>](configuring-com--applications.md)
</dt> <dt>

[<span data-ttu-id="d7a13-118">Contextos COM+ e modelos de Threading</span><span class="sxs-lookup"><span data-stu-id="d7a13-118">COM+ Contexts and Threading Models</span></span>](com--contexts-and-threading-models.md)
</dt> <dt>

[<span data-ttu-id="d7a13-119">Criando aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="d7a13-119">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="d7a13-120">Criando aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="d7a13-120">Designing COM+ Applications</span></span>](designing-com--applications.md)
</dt> </dl>

 

 



