---
description: Quando a segurança baseada em função está sendo usada, o objeto de contexto de chamada de segurança pode ser usado para acessar informações de segurança sobre a chamada atual.
ms.assetid: 9fc0a9e5-934c-4510-8fbb-1fb2817aa0ea
title: Acessando informações de contexto de chamada de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d7e5160c766783b6d43822571d624e0a595c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164099"
---
# <a name="accessing-security-call-context-information"></a><span data-ttu-id="71cb9-103">Acessando informações de contexto de chamada de segurança</span><span class="sxs-lookup"><span data-stu-id="71cb9-103">Accessing Security Call Context Information</span></span>

<span data-ttu-id="71cb9-104">Quando a segurança baseada em função está sendo usada, o objeto de contexto de chamada de segurança pode ser usado para acessar informações de segurança sobre a chamada atual.</span><span class="sxs-lookup"><span data-stu-id="71cb9-104">When role-based security is being used, the security call context object can be used to access security information about the current call.</span></span>

<span data-ttu-id="71cb9-105">As seguintes coleções de propriedades estão disponíveis no objeto de contexto de chamada de segurança:</span><span class="sxs-lookup"><span data-stu-id="71cb9-105">The following collections of properties are available from the security call context object:</span></span>

-   [<span data-ttu-id="71cb9-106">Coleção SecurityCallContext</span><span class="sxs-lookup"><span data-stu-id="71cb9-106">SecurityCallContext Collection</span></span>](#securitycallcontext-collection)
-   [<span data-ttu-id="71cb9-107">Coleção SecurityCallers</span><span class="sxs-lookup"><span data-stu-id="71cb9-107">SecurityCallers Collection</span></span>](#securitycallers-collection)
-   [<span data-ttu-id="71cb9-108">Coleção SecurityIdentity</span><span class="sxs-lookup"><span data-stu-id="71cb9-108">SecurityIdentity Collection</span></span>](#securityidentity-collection)
-   [<span data-ttu-id="71cb9-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71cb9-109">Related topics</span></span>](#related-topics)

## <a name="securitycallcontext-collection"></a><span data-ttu-id="71cb9-110">Coleção SecurityCallContext</span><span class="sxs-lookup"><span data-stu-id="71cb9-110">SecurityCallContext Collection</span></span>



| <span data-ttu-id="71cb9-111">Propriedade</span><span class="sxs-lookup"><span data-stu-id="71cb9-111">Property</span></span>                          | <span data-ttu-id="71cb9-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="71cb9-112">Description</span></span>                                                                                                                            |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71cb9-113">NumCallers</span><span class="sxs-lookup"><span data-stu-id="71cb9-113">NumCallers</span></span><br/>             | <span data-ttu-id="71cb9-114">O número de chamadores na cadeia de chamadas.</span><span class="sxs-lookup"><span data-stu-id="71cb9-114">The number of callers in the chain of calls.</span></span><br/>                                                                                |
| <span data-ttu-id="71cb9-115">MinAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="71cb9-115">MinAuthenticationLevel</span></span><br/> | <span data-ttu-id="71cb9-116">O nível de autenticação menos seguro de todos os chamadores na cadeia.</span><span class="sxs-lookup"><span data-stu-id="71cb9-116">The least secure authentication level of all callers in the chain.</span></span><br/>                                                          |
| <span data-ttu-id="71cb9-117">Chamadores</span><span class="sxs-lookup"><span data-stu-id="71cb9-117">Callers</span></span><br/>                | <span data-ttu-id="71cb9-118">Informações sobre a identidade dos chamadores upstream, na forma de uma coleção [**SecurityCallers**](securitycallers.md) .</span><span class="sxs-lookup"><span data-stu-id="71cb9-118">Information about the identity of upstream callers, in the form of a [**SecurityCallers**](securitycallers.md) collection.</span></span><br/> |
| <span data-ttu-id="71cb9-119">DirectCaller</span><span class="sxs-lookup"><span data-stu-id="71cb9-119">DirectCaller</span></span><br/>           | <span data-ttu-id="71cb9-120">O chamador que chamou o objeto diretamente (sem chamadores intermediários).</span><span class="sxs-lookup"><span data-stu-id="71cb9-120">The caller that called the object directly (with no intervening callers).</span></span> <br/>                                                  |
| <span data-ttu-id="71cb9-121">OriginalCaller</span><span class="sxs-lookup"><span data-stu-id="71cb9-121">OriginalCaller</span></span><br/>         | <span data-ttu-id="71cb9-122">O chamador que originou a cadeia de chamadas para o objeto.</span><span class="sxs-lookup"><span data-stu-id="71cb9-122">The caller that originated the chain of calls to the object.</span></span> <br/>                                                               |



 

<span data-ttu-id="71cb9-123">Para obter mais informações sobre como usar essa coleção, os desenvolvedores do Microsoft Visual Basic devem ver a classe [**SecurityCallContext**](securitycallcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="71cb9-123">For more information about how to use this collection, Microsoft Visual Basic developers should see the [**SecurityCallContext**](securitycallcontext.md) class.</span></span> <span data-ttu-id="71cb9-124">Os desenvolvedores de C e C++ devem se referir a [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="71cb9-124">C and C++ developers should refer to [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span></span>

## <a name="securitycallers-collection"></a><span data-ttu-id="71cb9-125">Coleção SecurityCallers</span><span class="sxs-lookup"><span data-stu-id="71cb9-125">SecurityCallers Collection</span></span>

<span data-ttu-id="71cb9-126">A coleção [**SecurityCallers**](securitycallers.md) representa chamadores que podem ser recuperados usando um índice entre 0 e 1 menor que NumCallers, inclusive.</span><span class="sxs-lookup"><span data-stu-id="71cb9-126">The [**SecurityCallers**](securitycallers.md) collection represents callers that can be retrieved by using an index between 0 and 1 less than NumCallers, inclusive.</span></span> <span data-ttu-id="71cb9-127">Cada chamador é representado por um objeto [**SecurityIdentity**](securityidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="71cb9-127">Each caller is represented by a [**SecurityIdentity**](securityidentity.md) object.</span></span>

<span data-ttu-id="71cb9-128">Para obter mais informações sobre essa coleção, Visual Basic os desenvolvedores devem ver a classe [**SecurityCallers**](securitycallers.md) .</span><span class="sxs-lookup"><span data-stu-id="71cb9-128">For more information about this collection, Visual Basic developers should see the [**SecurityCallers**](securitycallers.md) class.</span></span> <span data-ttu-id="71cb9-129">Os desenvolvedores de C e C++ devem se referir a [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span><span class="sxs-lookup"><span data-stu-id="71cb9-129">C and C++ developers should refer to [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span></span>

## <a name="securityidentity-collection"></a><span data-ttu-id="71cb9-130">Coleção SecurityIdentity</span><span class="sxs-lookup"><span data-stu-id="71cb9-130">SecurityIdentity Collection</span></span>



| <span data-ttu-id="71cb9-131">Propriedade</span><span class="sxs-lookup"><span data-stu-id="71cb9-131">Property</span></span>                         | <span data-ttu-id="71cb9-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="71cb9-132">Description</span></span>                                                                                                                                                          |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71cb9-133">SID</span><span class="sxs-lookup"><span data-stu-id="71cb9-133">SID</span></span><br/>                   | <span data-ttu-id="71cb9-134">O identificador de segurança do chamador.</span><span class="sxs-lookup"><span data-stu-id="71cb9-134">The security identifier for the caller.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="71cb9-135">AccountName</span><span class="sxs-lookup"><span data-stu-id="71cb9-135">AccountName</span></span><br/>           | <span data-ttu-id="71cb9-136">O nome da conta do chamador.</span><span class="sxs-lookup"><span data-stu-id="71cb9-136">The account name of the caller.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="71cb9-137">AuthenticationService</span><span class="sxs-lookup"><span data-stu-id="71cb9-137">AuthenticationService</span></span><br/> | <span data-ttu-id="71cb9-138">O serviço de autenticação usado, como NTLMSSP, Kerberos ou SSL.</span><span class="sxs-lookup"><span data-stu-id="71cb9-138">The authentication service used, such as NTLMSSP, Kerberos, or SSL.</span></span><br/>                                                                                       |
| <span data-ttu-id="71cb9-139">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="71cb9-139">AuthenticationLevel</span></span><br/>   | <span data-ttu-id="71cb9-140">O nível de autenticação usado, que representa a quantidade de proteção usada ao se comunicar com o objeto.</span><span class="sxs-lookup"><span data-stu-id="71cb9-140">The authentication level used, which represents the amount of protection used when communicating with the object.</span></span><br/>                                         |
| <span data-ttu-id="71cb9-141">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="71cb9-141">ImpersonationLevel</span></span><br/>    | <span data-ttu-id="71cb9-142">O nível de representação definido pelo cliente, se a representação tiver sido usada.</span><span class="sxs-lookup"><span data-stu-id="71cb9-142">The level of impersonation set by the client, if impersonation was used.</span></span> <span data-ttu-id="71cb9-143">Esse nível indica a quantidade de autoridade atribuída ao servidor pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="71cb9-143">This level indicates the amount of authority given to the server by the client.</span></span> <br/> |



 

<span data-ttu-id="71cb9-144">Para obter mais informações sobre essa coleção, Visual Basic os desenvolvedores devem ver a classe [**SecurityIdentity**](securityidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="71cb9-144">For more information on this collection, Visual Basic developers should see the [**SecurityIdentity**](securityidentity.md) class.</span></span> <span data-ttu-id="71cb9-145">Os desenvolvedores de C e C++ devem se referir a [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span><span class="sxs-lookup"><span data-stu-id="71cb9-145">C and C++ developers should refer to [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span></span>

## <a name="related-topics"></a><span data-ttu-id="71cb9-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71cb9-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71cb9-147">Verificando a associação de função</span><span class="sxs-lookup"><span data-stu-id="71cb9-147">Checking Role Membership</span></span>](checking-role-membership.md)
</dt> <dt>

[<span data-ttu-id="71cb9-148">Determinando se a segurança do Role-Based está habilitada</span><span class="sxs-lookup"><span data-stu-id="71cb9-148">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[<span data-ttu-id="71cb9-149">Segurança de componente programática</span><span class="sxs-lookup"><span data-stu-id="71cb9-149">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 




