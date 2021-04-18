---
description: Especifica e configura os serviços que devem estar ativos no domínio de serviço inserido ao chamar CoCreateActivity ou CoEnterServiceDomain.
ms.assetid: f546ded4-255e-4565-b588-f36175902778
title: Classe CServiceConfig (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CServiceConfig
api_type:
- COM
ms.openlocfilehash: e0b48b05be4afa1d42dbc8a16c4b596a08aba859
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782453"
---
# <a name="cserviceconfig-class"></a><span data-ttu-id="f3dc4-103">Classe CServiceConfig</span><span class="sxs-lookup"><span data-stu-id="f3dc4-103">CServiceConfig class</span></span>

<span data-ttu-id="f3dc4-104">Especifica e configura os serviços que devem estar ativos no domínio de serviço inserido ao chamar [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) ou [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).</span><span class="sxs-lookup"><span data-stu-id="f3dc4-104">Specifies and configures the services that are to be active in the service domain entered when calling either [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) or [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="f3dc4-105">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="f3dc4-105">When to implement</span></span>

<span data-ttu-id="f3dc4-106">Essa classe é implementada pelo COM+.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="f3dc4-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3dc4-107">Requirement</span></span> | <span data-ttu-id="f3dc4-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f3dc4-108">Value</span></span> |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3dc4-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="f3dc4-109">CLSID</span></span>      | <span data-ttu-id="f3dc4-110">\_CSERVICECONFIG CLSID</span><span class="sxs-lookup"><span data-stu-id="f3dc4-110">CLSID\_CServiceConfig</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="f3dc4-111">ProgID</span><span class="sxs-lookup"><span data-stu-id="f3dc4-111">ProgID</span></span>     | <span data-ttu-id="f3dc4-112">L "COMSVCS. CServiceConfig"</span><span class="sxs-lookup"><span data-stu-id="f3dc4-112">L"COMSVCS.CServiceConfig"</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="f3dc4-113">Interfaces</span><span class="sxs-lookup"><span data-stu-id="f3dc4-113">Interfaces</span></span> | [<span data-ttu-id="f3dc4-114">**IServiceComTIIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="f3dc4-114">**IServiceComTIIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> [<span data-ttu-id="f3dc4-115">**IServiceIISIntrinsicsConfig**</span><span class="sxs-lookup"><span data-stu-id="f3dc4-115">**IServiceIISIntrinsicsConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/> [<span data-ttu-id="f3dc4-116">**IServiceInheritanceConfig**</span><span class="sxs-lookup"><span data-stu-id="f3dc4-116">**IServiceInheritanceConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/> [<span data-ttu-id="f3dc4-117">**IServicePartitionConfig**</span><span class="sxs-lookup"><span data-stu-id="f3dc4-117">**IServicePartitionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/> [<span data-ttu-id="f3dc4-118">**IServiceSxSConfig**</span><span class="sxs-lookup"><span data-stu-id="f3dc4-118">**IServiceSxSConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/> [<span data-ttu-id="f3dc4-119">**IServiceSynchronizationConfig**</span><span class="sxs-lookup"><span data-stu-id="f3dc4-119">**IServiceSynchronizationConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> [<span data-ttu-id="f3dc4-120">**IServiceThreadPoolConfig**</span><span class="sxs-lookup"><span data-stu-id="f3dc4-120">**IServiceThreadPoolConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/> [<span data-ttu-id="f3dc4-121">**IServiceTrackerConfig**</span><span class="sxs-lookup"><span data-stu-id="f3dc4-121">**IServiceTrackerConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/> [<span data-ttu-id="f3dc4-122">**IServiceTransactionConfig**</span><span class="sxs-lookup"><span data-stu-id="f3dc4-122">**IServiceTransactionConfig**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/> |



 

## <a name="when-to-use"></a><span data-ttu-id="f3dc4-123">Quando usar</span><span class="sxs-lookup"><span data-stu-id="f3dc4-123">When to use</span></span>

<span data-ttu-id="f3dc4-124">Use essa classe para configurar os serviços que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-124">Use this class to configure the services that you want to use.</span></span> <span data-ttu-id="f3dc4-125">[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) e [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) permitem que você use os serviços configurados por essa classe sem a necessidade de vincular esses serviços a um componente antes de usá-los.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-125">[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) and [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) enable you to use the services configured by this class without needing to tie those services to a component before using them.</span></span>

<span data-ttu-id="f3dc4-126">Esta classe não foi projetada para ser usada em Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-126">This class was not designed to be used in Visual Basic.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3dc4-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3dc4-127">Remarks</span></span>

<span data-ttu-id="f3dc4-128">Para criar esse objeto, chame [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="f3dc4-128">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="f3dc4-129">Os objetos instanciados da classe **CServiceConfig** agregam o marshaler de thread livre para que possam ser armazenados por tempos de execução do sistema e reutilizados em diferentes Apartments.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-129">Objects instantiated from the **CServiceConfig** class aggregate the free-threaded marshaler so that they can be stored by system runtimes and reused in different apartments.</span></span>

<span data-ttu-id="f3dc4-130">Para configurar um serviço individual, chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para a interface associada ao serviço e, em seguida, chame os métodos nessa interface para estabelecer a configuração apropriada.</span><span class="sxs-lookup"><span data-stu-id="f3dc4-130">To configure an individual service, call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the interface associated with the service and then call methods on that interface to establish the appropriate configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3dc4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3dc4-131">Requirements</span></span>



| <span data-ttu-id="f3dc4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3dc4-132">Requirement</span></span> | <span data-ttu-id="f3dc4-133">Valor</span><span class="sxs-lookup"><span data-stu-id="f3dc4-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f3dc4-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3dc4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f3dc4-135">\[Somente aplicativos da área de trabalho do Windows XP com SP1\]</span><span class="sxs-lookup"><span data-stu-id="f3dc4-135">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f3dc4-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3dc4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f3dc4-137">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f3dc4-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f3dc4-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f3dc4-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3dc4-139"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3dc4-139"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3dc4-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3dc4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3dc4-141">**CoCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="f3dc4-141">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[<span data-ttu-id="f3dc4-142">**CoCreateFreeThreadedMarshaler**</span><span class="sxs-lookup"><span data-stu-id="f3dc4-142">**CoCreateFreeThreadedMarshaler**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler)
</dt> <dt>

[<span data-ttu-id="f3dc4-143">**CoEnterServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="f3dc4-143">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[<span data-ttu-id="f3dc4-144">**CoLeaveServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="f3dc4-144">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[<span data-ttu-id="f3dc4-145">Serviços COM+ sem componentes</span><span class="sxs-lookup"><span data-stu-id="f3dc4-145">COM+ Services Without Components</span></span>](com--services-without-components.md)
</dt> </dl>

 

