---
description: A função CoCreateActivity é usada para enviar o trabalho em lotes para o sistema COM+. Ele permite que aplicativos baseados em script ofereçam suporte a uma configuração de serviço COM+ em todo o aplicativo.
ms.assetid: af734507-516c-43f1-9c5e-c77cde1b8008
title: Usando os serviços COM+ por meio do CoCreateActivity
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b3296756b91d0f8ea29b1d67c11c78c431cfcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764430"
---
# <a name="using-com-services-through-cocreateactivity"></a><span data-ttu-id="6917e-104">Usando os serviços COM+ por meio do CoCreateActivity</span><span class="sxs-lookup"><span data-stu-id="6917e-104">Using COM+ Services Through CoCreateActivity</span></span>

<span data-ttu-id="6917e-105">A função [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) é usada para enviar o trabalho em lotes para o sistema com+.</span><span class="sxs-lookup"><span data-stu-id="6917e-105">The [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) function is used to submit batch work to the COM+ system.</span></span> <span data-ttu-id="6917e-106">Ele permite que aplicativos baseados em script ofereçam suporte a uma configuração de serviço COM+ em todo o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6917e-106">It allows script-based applications to support an application-wide COM+ service configuration.</span></span>

<span data-ttu-id="6917e-107">Os serviços COM+ desejados são configurados por meio de um objeto [**CServiceConfig**](cserviceconfig.md) que é passado para a função.</span><span class="sxs-lookup"><span data-stu-id="6917e-107">The desired COM+ services are configured through a [**CServiceConfig**](cserviceconfig.md) object that is passed in to the function.</span></span> <span data-ttu-id="6917e-108">A função cria um objeto de atividade e retorna a interface [**IServiceActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) desse objeto.</span><span class="sxs-lookup"><span data-stu-id="6917e-108">The function creates an activity object and returns the [**IServiceActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) interface of that object.</span></span> <span data-ttu-id="6917e-109">O trabalho em lotes pode ser enviado de forma síncrona ou assíncrona, usando os métodos [**SynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) ou [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) de **IServiceActivity**, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6917e-109">The batch work can be submitted either synchronously or asynchronously, by using the [**SynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) or [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) methods of **IServiceActivity**, respectively.</span></span> <span data-ttu-id="6917e-110">Um ponteiro para uma interface [**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) é passado para cada um desses métodos, e o trabalho em lotes é implementado pelo desenvolvedor no método [**oncall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) da interface **IServiceCall** .</span><span class="sxs-lookup"><span data-stu-id="6917e-110">A pointer to an [**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) interface is passed in to each of these methods, and the batch work is implemented by the developer in the [**OnCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) method of the **IServiceCall** interface.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="6917e-111">Ferramenta administrativa serviços de componentes</span><span class="sxs-lookup"><span data-stu-id="6917e-111">Component Services Administrative Tool</span></span>

<span data-ttu-id="6917e-112">Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="6917e-112">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="6917e-113">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6917e-113">Visual Basic</span></span>

<span data-ttu-id="6917e-114">Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="6917e-114">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="6917e-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="6917e-115">C/C++</span></span>

<span data-ttu-id="6917e-116">O fragmento de código a seguir ilustra como usar os serviços COM+ por meio do [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity).</span><span class="sxs-lookup"><span data-stu-id="6917e-116">The following code fragment illustrates how to use COM+ services through [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity).</span></span> <span data-ttu-id="6917e-117">O tratamento de erros foi omitido para fins de brevidade.</span><span class="sxs-lookup"><span data-stu-id="6917e-117">Error handling is omitted for brevity.</span></span> <span data-ttu-id="6917e-118">Este fragmento de código usa o objeto [**CServiceConfig**](cserviceconfig.md) que foi criado e configurado na [configuração de serviços com+ com CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span><span class="sxs-lookup"><span data-stu-id="6917e-118">This code fragment uses the [**CServiceConfig**](cserviceconfig.md) object that was created and configured in [Configuring COM+ Services with CServiceConfig](configuring-com--services-with-cserviceconfig.md).</span></span>


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER,
//   IID_IUnknown, (void**)&pUnknownCSC);

// Create the activity for our services.
HRESULT hr = CoCreateActivity(pUnknownCSC, IID_IServiceActivity, (void**)&pActivity);
if (FAILED(hr)) throw(hr);

// Do the batch work synchronously.
// The batch work is implemented in pServiceCall->OnCall().
hr = pActivity->SynchronousCall(pServiceCall);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a><span data-ttu-id="6917e-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6917e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6917e-120">**CoCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="6917e-120">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[<span data-ttu-id="6917e-121">Configurando serviços COM+ com CServiceConfig</span><span class="sxs-lookup"><span data-stu-id="6917e-121">Configuring COM+ Services with CServiceConfig</span></span>](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="6917e-122">**CServiceConfig**</span><span class="sxs-lookup"><span data-stu-id="6917e-122">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="6917e-123">Usando os serviços COM+ por meio de CoEnterServiceDomain e CoLeaveServiceDomain</span><span class="sxs-lookup"><span data-stu-id="6917e-123">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

 



