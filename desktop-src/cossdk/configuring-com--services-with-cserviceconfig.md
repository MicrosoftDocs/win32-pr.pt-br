---
description: Configurando serviços COM+ com CServiceConfig
ms.assetid: c44743a8-8b91-4e2a-9ba4-4cb6ae787999
title: Configurando serviços COM+ com CServiceConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8bbc6c3131347f450340863db70fd9b3999730
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646287"
---
# <a name="configuring-com-services-with-cserviceconfig"></a><span data-ttu-id="4b6b1-103">Configurando serviços COM+ com CServiceConfig</span><span class="sxs-lookup"><span data-stu-id="4b6b1-103">Configuring COM+ Services with CServiceConfig</span></span>

<span data-ttu-id="4b6b1-104">A classe [**CServiceConfig**](cserviceconfig.md) é usada para configurar os serviços com+ que podem ser usados sem componentes.</span><span class="sxs-lookup"><span data-stu-id="4b6b1-104">The [**CServiceConfig**](cserviceconfig.md) class is used to configure the COM+ services that can be used without components.</span></span> <span data-ttu-id="4b6b1-105">Ele agrega o marshaler de thread livre, portanto, ele pode ser usado em diferentes Apartments.</span><span class="sxs-lookup"><span data-stu-id="4b6b1-105">It aggregates the free-threaded marshaler, so it can be used in different apartments.</span></span> <span data-ttu-id="4b6b1-106">Para configurar um serviço individual, você deve chamar [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para a interface associada ao serviço e, em seguida, chamar métodos nessa interface para estabelecer a configuração apropriada.</span><span class="sxs-lookup"><span data-stu-id="4b6b1-106">To configure an individual service, you must call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the interface associated with the service and then call methods on that interface to establish the appropriate configuration.</span></span> <span data-ttu-id="4b6b1-107">A tabela a seguir descreve as interfaces que são implementadas por meio da classe **CServiceConfig** .</span><span class="sxs-lookup"><span data-stu-id="4b6b1-107">The following table describes the interfaces that are implemented through the **CServiceConfig** class.</span></span>



| <span data-ttu-id="4b6b1-108">Interface</span><span class="sxs-lookup"><span data-stu-id="4b6b1-108">Interface</span></span>                                                                         | <span data-ttu-id="4b6b1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b6b1-109">Description</span></span>                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b6b1-110">**IServiceInheritanceConfig**</span><span class="sxs-lookup"><span data-stu-id="4b6b1-110">**IServiceInheritanceConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/>         | <span data-ttu-id="4b6b1-111">A interface padrão para a classe.</span><span class="sxs-lookup"><span data-stu-id="4b6b1-111">The default interface for the class.</span></span> <span data-ttu-id="4b6b1-112">Ele é usado para inicializar rapidamente muitos dos serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="4b6b1-112">It is used to quickly initialize many of the COM+ services.</span></span><br/>                                                                                              |
| [<span data-ttu-id="4b6b1-113">**IServiceComTIIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="4b6b1-113">**IServiceComTIIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> | <span data-ttu-id="4b6b1-114">Usado para configurar as informações intrínsecas do integrador de transações COM (COMTI).</span><span class="sxs-lookup"><span data-stu-id="4b6b1-114">Used to configure the COM Transaction Integrator (COMTI) intrinsics information.</span></span> <span data-ttu-id="4b6b1-115">O COMTI permite que os desenvolvedores integrem programas de transação baseados em mainframe a aplicativos baseados em componentes.</span><span class="sxs-lookup"><span data-stu-id="4b6b1-115">COMTI allows developers to integrate mainframe-based transaction programs with component-based applications.</span></span><br/> |
| [<span data-ttu-id="4b6b1-116">**IServiceIISIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="4b6b1-116">**IServiceIISIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/>     | <span data-ttu-id="4b6b1-117">Usado para configurar as informações intrínsecas do Serviços de Informações da Internet (IIS).</span><span class="sxs-lookup"><span data-stu-id="4b6b1-117">Used to configure the Internet Information Services (IIS) intrinsics information.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="4b6b1-118">**IServicePartitionConfig**</span><span class="sxs-lookup"><span data-stu-id="4b6b1-118">**IServicePartitionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/>             | <span data-ttu-id="4b6b1-119">Usado para configurar como as partições COM+ são usadas com os serviços.</span><span class="sxs-lookup"><span data-stu-id="4b6b1-119">Used to configure how COM+ partitions are used with the services.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="4b6b1-120">**IServiceSxSConfig**</span><span class="sxs-lookup"><span data-stu-id="4b6b1-120">**IServiceSxSConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/>                         | <span data-ttu-id="4b6b1-121">Usado para configurar assemblies lado a lado.</span><span class="sxs-lookup"><span data-stu-id="4b6b1-121">Used to configure side-by-side assemblies.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="4b6b1-122">**IServiceSynchronizationConfig**</span><span class="sxs-lookup"><span data-stu-id="4b6b1-122">**IServiceSynchronizationConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> | <span data-ttu-id="4b6b1-123">Usado para configurar os serviços de sincronização COM+.</span><span class="sxs-lookup"><span data-stu-id="4b6b1-123">Used to configure COM+ synchronization services.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="4b6b1-124">**IServiceThreadPoolConfig**</span><span class="sxs-lookup"><span data-stu-id="4b6b1-124">**IServiceThreadPoolConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/>           | <span data-ttu-id="4b6b1-125">Usado para configurar o pool de threads para o serviço COM+.</span><span class="sxs-lookup"><span data-stu-id="4b6b1-125">Used to configure the thread pool for the COM+ service.</span></span> <span data-ttu-id="4b6b1-126">O pool de threads só pode ser configurado ao usar a função [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) .</span><span class="sxs-lookup"><span data-stu-id="4b6b1-126">The thread pool can be configured only when using the [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) function.</span></span><br/>                          |
| [<span data-ttu-id="4b6b1-127">**IServiceTrackerConfig**</span><span class="sxs-lookup"><span data-stu-id="4b6b1-127">**IServiceTrackerConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/>                 | <span data-ttu-id="4b6b1-128">Usado para configurar a propriedade do rastreador.</span><span class="sxs-lookup"><span data-stu-id="4b6b1-128">Used to configure the Tracker property.</span></span> <span data-ttu-id="4b6b1-129">Tracker é um mecanismo de relatório usado pelo código de monitoramento para observar qual código está sendo executado quando.</span><span class="sxs-lookup"><span data-stu-id="4b6b1-129">Tracker is a reporting mechanism used by monitoring code to watch which code is running when.</span></span><br/>                                                         |
| [<span data-ttu-id="4b6b1-130">**IServiceTransactionConfig**</span><span class="sxs-lookup"><span data-stu-id="4b6b1-130">**IServiceTransactionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/>         | <span data-ttu-id="4b6b1-131">Usado para configurar o serviço de transação COM+.</span><span class="sxs-lookup"><span data-stu-id="4b6b1-131">Used to configure the COM+ transaction service.</span></span><br/>                                                                                                                                               |



 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="4b6b1-132">Ferramenta administrativa serviços de componentes</span><span class="sxs-lookup"><span data-stu-id="4b6b1-132">Component Services Administrative Tool</span></span>

<span data-ttu-id="4b6b1-133">Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="4b6b1-133">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="4b6b1-134">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4b6b1-134">Visual Basic</span></span>

<span data-ttu-id="4b6b1-135">Não se aplica.</span><span class="sxs-lookup"><span data-stu-id="4b6b1-135">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="4b6b1-136">C/C++</span><span class="sxs-lookup"><span data-stu-id="4b6b1-136">C/C++</span></span>

<span data-ttu-id="4b6b1-137">O fragmento de código a seguir ilustra como criar e configurar um objeto [**CServiceConfig**](cserviceconfig.md) para usar transações com+.</span><span class="sxs-lookup"><span data-stu-id="4b6b1-137">The following code fragment illustrates how to create and configure a [**CServiceConfig**](cserviceconfig.md) object to use COM+ transactions.</span></span>


```C++
// Create a CServiceConfig object.
HRESULT hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
  IID_IUnknown, (void**)&pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Query for the IServiceInheritanceConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceInheritanceConfig, 
  (void**)&pInheritanceConfig);
if (FAILED(hr)) throw(hr);

// Inherit the current context before using transactions.
hr = pInheritanceConfig->ContainingContextTreatment(CSC_Inherit);
if (FAILED(hr)) throw(hr);

// Query for the IServiceTransactionConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceTransactionConfig, 
  (void**)&pTransactionConfig);
if (FAILED(hr)) throw(hr);

// Configure transactions to always create a new one.
hr = pTransactionConfig->ConfigureTransaction(CSC_NewTransaction);
if (FAILED(hr)) throw(hr);

// Set the isolation level of the transactions to ReadCommitted.
hr = pTransactionConfig->IsolationLevel( 
  COMAdminTxIsolationLevelReadCommitted);
if (FAILED(hr)) throw(hr);

// Set the transaction time-out to 1 minute.
hr = pTransactionConfig->TransactionTimeout(60);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a><span data-ttu-id="4b6b1-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4b6b1-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b6b1-139">**CServiceConfig**</span><span class="sxs-lookup"><span data-stu-id="4b6b1-139">**CServiceConfig**</span></span>](cserviceconfig.md)
</dt> <dt>

[<span data-ttu-id="4b6b1-140">Usando os serviços COM+ por meio do CoCreateActivity</span><span class="sxs-lookup"><span data-stu-id="4b6b1-140">Using COM+ Services Through CoCreateActivity</span></span>](using-com--services-through-cocreateactivity.md)
</dt> <dt>

[<span data-ttu-id="4b6b1-141">Usando os serviços COM+ por meio de CoEnterServiceDomain e CoLeaveServiceDomain</span><span class="sxs-lookup"><span data-stu-id="4b6b1-141">Using COM+ Services Through CoEnterServiceDomain and CoLeaveServiceDomain</span></span>](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

