---
title: Provedores de serviços ADSI
description: Este tópico fornece uma visão geral dos provedores de serviços ADSI fornecidos no servidor.
ms.assetid: 419d7953-a879-4d6c-be74-173d76c3f932
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, provedores de serviços
- ADSI de provedores de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44ba4ebc63338bfb38d2b9d5da1f46e51b31aa8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105756283"
---
# <a name="adsi-service-providers"></a><span data-ttu-id="b7d8d-105">Provedores de serviços ADSI</span><span class="sxs-lookup"><span data-stu-id="b7d8d-105">ADSI Service Providers</span></span>

<span data-ttu-id="b7d8d-106">A ADSI inclui os provedores de serviços listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b7d8d-106">ADSI includes the service providers listed in the following table.</span></span>



| <span data-ttu-id="b7d8d-107">Provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="b7d8d-107">Service provider</span></span> | <span data-ttu-id="b7d8d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7d8d-108">Description</span></span>                                                                                | <span data-ttu-id="b7d8d-109">Para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="b7d8d-109">For more information</span></span>                                      |
|------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="b7d8d-110">LDAP</span><span class="sxs-lookup"><span data-stu-id="b7d8d-110">LDAP</span></span><br/>  | <span data-ttu-id="b7d8d-111">Implementação de namespace compatível com o Lightweight Directory Access Protocol.</span><span class="sxs-lookup"><span data-stu-id="b7d8d-111">Namespace implementation compatible with Lightweight Directory Access Protocol.</span></span><br/> | [<span data-ttu-id="b7d8d-112">Provedor LDAP ADSI</span><span class="sxs-lookup"><span data-stu-id="b7d8d-112">ADSI LDAP Provider</span></span>](adsi-ldap-provider.md)<br/>   |
| <span data-ttu-id="b7d8d-113">WinNT</span><span class="sxs-lookup"><span data-stu-id="b7d8d-113">WinNT</span></span><br/> | <span data-ttu-id="b7d8d-114">Implementação de namespace compatível com o Windows.</span><span class="sxs-lookup"><span data-stu-id="b7d8d-114">Namespace implementation compatible with Windows.</span></span><br/>                               | [<span data-ttu-id="b7d8d-115">Provedor ADSI de WinNT</span><span class="sxs-lookup"><span data-stu-id="b7d8d-115">ADSI WinNT Provider</span></span>](adsi-winnt-provider.md)<br/> |



 

<span data-ttu-id="b7d8d-116">Outros provedores de serviços são incluídos como parte de produtos diferentes da ADSI.</span><span class="sxs-lookup"><span data-stu-id="b7d8d-116">Other service providers are included as part of products other than ADSI.</span></span> <span data-ttu-id="b7d8d-117">A seguir estão os provedores de serviços ADSI implementados pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b7d8d-117">The following are the ADSI service providers implemented by Microsoft.</span></span>



| <span data-ttu-id="b7d8d-118">Provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="b7d8d-118">Service provider</span></span> | <span data-ttu-id="b7d8d-119">Para obter mais informações</span><span class="sxs-lookup"><span data-stu-id="b7d8d-119">For more information</span></span>                                                                        |
|------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d8d-120">IIS</span><span class="sxs-lookup"><span data-stu-id="b7d8d-120">IIS</span></span><br/>   | <span data-ttu-id="b7d8d-121">[Arquitetura do provedor ADSI do IIS](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="b7d8d-121">[IIS ADSI Provider Architecture](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))</span></span><br/> |



 

<span data-ttu-id="b7d8d-122">Os métodos e métodos de propriedade expostos por interfaces ADSI não têm suporte de todos os provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="b7d8d-122">The methods and property methods exposed by ADSI interfaces are not supported by every service provider.</span></span> <span data-ttu-id="b7d8d-123">Como os diferentes serviços de diretório variam de acordo com os tipos de objetos e propriedades armazenados, use protocolos diferentes e a autenticação, a ADSI foi projetada para funcionar diretamente com os provedores de serviços com suporte.</span><span class="sxs-lookup"><span data-stu-id="b7d8d-123">Because different directory services vary in the types of objects and properties stored, use different protocols, and authentication, ADSI is designed to work seamlessly with supported service providers.</span></span> <span data-ttu-id="b7d8d-124">Portanto, há interfaces, métodos e métodos de propriedade que funcionam com um provedor de serviços, como o LDAP, que podem não funcionar em outro, como o WinNT.</span><span class="sxs-lookup"><span data-stu-id="b7d8d-124">Thus, there are interfaces, methods, and property methods that work with one service provider, such as LDAP, that may not work on another, such as WinNT.</span></span>

<span data-ttu-id="b7d8d-125">Esta seção contém informações específicas do provedor, como o formato ADsPath, uma lista de objetos ADSI usados para esse provedor de serviços e informações de tipo e sintaxe de dados para os provedores de serviços incluídos na ADSI.</span><span class="sxs-lookup"><span data-stu-id="b7d8d-125">This section contains provider-specific information, such as the ADsPath format, a listing of ADSI objects used for that service provider, and data type and syntax information for the service providers included with ADSI.</span></span> <span data-ttu-id="b7d8d-126">Também há uma descrição resumida das interfaces ADSI com suporte de cada provedor incluído na ADSI.</span><span class="sxs-lookup"><span data-stu-id="b7d8d-126">There is also a summary description of ADSI interfaces supported by each provider included with ADSI.</span></span>

<span data-ttu-id="b7d8d-127">Na ADSI, provedores diferentes são associados a DLLs diferentes.</span><span class="sxs-lookup"><span data-stu-id="b7d8d-127">In ADSI, different providers are associated with different DLLs.</span></span> <span data-ttu-id="b7d8d-128">O provedor LDAP está associado a Adsldp.dll, Adsldpc.dll e Adsmsext.dll.</span><span class="sxs-lookup"><span data-stu-id="b7d8d-128">The LDAP provider is associated with Adsldp.dll, Adsldpc.dll, and Adsmsext.dll.</span></span> <span data-ttu-id="b7d8d-129">O provedor WinNT está associado a Adsnt.dll.</span><span class="sxs-lookup"><span data-stu-id="b7d8d-129">The WinNT provider is associated with Adsnt.dll.</span></span> <span data-ttu-id="b7d8d-130">O provedor do roteador está associado a Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="b7d8d-130">The ROUTER provider is associated with Activeds.dll.</span></span>

> [!Note]  
> <span data-ttu-id="b7d8d-131">Não presuma que os provedores ADSI padrão sejam thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b7d8d-131">Do not assume that default ADSI providers are thread-safe.</span></span> <span data-ttu-id="b7d8d-132">Os desenvolvedores de aplicativos multithread devem coordenar o acesso entre threads por meio do uso adequado de objetos de sincronização, como semáforos, exclusões mútuas, seções críticas e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b7d8d-132">Multithreaded application developers should coordinate access between threads through the proper use of synchronization objects such as semaphores, mutexes, critical sections, and so on.</span></span>

 

<span data-ttu-id="b7d8d-133">Para obter mais informações sobre provedores de serviços ADSI, consulte suporte de [roteador](adsi-router.md) e [provedor ADSI de interfaces ADSI](provider-support-of-adsi-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="b7d8d-133">For more information about ADSI service providers, see [ADSI Router](adsi-router.md) and [Provider Support of ADSI interfaces](provider-support-of-adsi-interfaces.md).</span></span>

 

