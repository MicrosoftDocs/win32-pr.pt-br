---
description: Usando os serviços COM+ por meio de CoEnterServiceDomain e CoLeaveServiceDomain
ms.assetid: 763fb01e-5daf-4e9b-8ef1-9ae79c0a84cc
title: Usando os serviços COM+ por meio de CoEnterServiceDomain e CoLeaveServiceDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d87931628e177374dd07b40e9917a56c168a81
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089363"
---
# <a name="using-com-services-through-coenterservicedomain-and-coleaveservicedomain"></a><span data-ttu-id="7488a-103">Usando os serviços COM+ por meio de CoEnterServiceDomain e CoLeaveServiceDomain</span><span class="sxs-lookup"><span data-stu-id="7488a-103">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>

<span data-ttu-id="7488a-104">[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) e [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) são usados juntos para envolver uma área de código que é executada em seu próprio contexto e pode usar serviços com+ sem a necessidade de componentes com+.</span><span class="sxs-lookup"><span data-stu-id="7488a-104">[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) and [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) are used together to surround an area of code that runs in its own context and can use COM+ services without the need for COM+ components.</span></span> <span data-ttu-id="7488a-105">Os serviços COM+ que são usados neste contexto são configurados por meio do objeto [**CServiceConfig**](cserviceconfig.md) que é passado para **CoEnterServiceDomain**.</span><span class="sxs-lookup"><span data-stu-id="7488a-105">The COM+ services that are used in this context are configured through the [**CServiceConfig**](cserviceconfig.md) object that is passed in to **CoEnterServiceDomain**.</span></span> <span data-ttu-id="7488a-106">O código que está circundado por **CoEnterServiceDomain** e **CoLeaveServiceDomain** se comporta como se fosse um método chamado em um objeto criado dentro desse contexto.</span><span class="sxs-lookup"><span data-stu-id="7488a-106">The code that is surrounded by **CoEnterServiceDomain** and **CoLeaveServiceDomain** behaves as though it were a method that is called on an object created within this context.</span></span>

<span data-ttu-id="7488a-107">Um aplicativo de script pode usar esse par de funções para fornecer suporte em tempo de execução de serviços COM+ sem componentes.</span><span class="sxs-lookup"><span data-stu-id="7488a-107">A scripting application can use this pair of functions to provide run-time support of COM+ services without components.</span></span> <span data-ttu-id="7488a-108">Por exemplo, um aplicativo de script pode ser desenvolvido para fornecer marcas que permitem que os gravadores de script insiram e deixem um domínio de serviço dentro do script.</span><span class="sxs-lookup"><span data-stu-id="7488a-108">For example, a scripting application can be developed to provide tags that allow the script writers to enter and leave a service domain within the script.</span></span> <span data-ttu-id="7488a-109">Quando o mecanismo de script processa o script e encontra as marcas, ele pode chamar [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) com um objeto [**CServiceConfig**](cserviceconfig.md) pré-configurado, executar o código necessário e, em seguida, chamar [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span><span class="sxs-lookup"><span data-stu-id="7488a-109">When the scripting engine processes the script and encounters the tags, it can call [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) with a preconfigured [**CServiceConfig**](cserviceconfig.md) object, run the necessary code, and then call [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="7488a-110">Ferramenta administrativa serviços de componentes</span><span class="sxs-lookup"><span data-stu-id="7488a-110">Component Services Administrative Tool</span></span>

<span data-ttu-id="7488a-111">Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="7488a-111">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="7488a-112">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7488a-112">Visual Basic</span></span>

<span data-ttu-id="7488a-113">Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="7488a-113">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="7488a-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="7488a-114">C/C++</span></span>

<span data-ttu-id="7488a-115">O fragmento de código a seguir ilustra como usar os serviços COM+ entre chamadas para [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) e [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span><span class="sxs-lookup"><span data-stu-id="7488a-115">The following code fragment illustrates how to use COM+ services between calls to [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) and [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).</span></span> <span data-ttu-id="7488a-116">O tratamento de erros foi omitido para fins de brevidade.</span><span class="sxs-lookup"><span data-stu-id="7488a-116">Error handling is omitted for brevity.</span></span> <span data-ttu-id="7488a-117">Este fragmento de código usa o objeto [**CServiceConfig**](cserviceconfig.md) que foi criado e configurado na [configuração de serviços com+ com CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span><span class="sxs-lookup"><span data-stu-id="7488a-117">This code fragment uses the [**CServiceConfig**](cserviceconfig.md) object that was created and configured in [Configuring COM+ Services with CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span></span>


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
//   IID_IUnknown, (void**)&pUnknownCSC);

// Enter the Service Domain.
HRESULT hr = CoEnterServiceDomain(pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Do the work that uses COM+ services here.
//DoMyWork();

// Leave the Service Domain.
CoLeaveServiceDomain(NULL);
```



## <a name="related-topics"></a><span data-ttu-id="7488a-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7488a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7488a-119">**CoEnterServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="7488a-119">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[<span data-ttu-id="7488a-120">**CoLeaveServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="7488a-120">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[<span data-ttu-id="7488a-121">Configurando serviços COM+ com CServiceConfig</span><span class="sxs-lookup"><span data-stu-id="7488a-121">Configuring COM+ Services with CServiceConfig</span></span>](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="7488a-122">**CServiceConfig**</span><span class="sxs-lookup"><span data-stu-id="7488a-122">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="7488a-123">Usando os serviços COM+ por meio do CoCreateActivity</span><span class="sxs-lookup"><span data-stu-id="7488a-123">Using COM+ Services Through CoCreateActivity</span></span>](using-com--services-through-cocreateactivity.md)
</dt> </dl>

 

 



