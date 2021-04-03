---
description: Fornece acesso a uma coleção de informações de segurança que representa a identidade de um chamador. Usando essa classe, você pode descobrir sobre um determinado chamador em uma cadeia de chamadores que faz parte do contexto de chamada de segurança.
ms.assetid: c6b28695-1b08-490a-8d56-eb55d82f3e7a
title: Classe SecurityIdentity (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityIdentity
api_type:
- COM
ms.openlocfilehash: 6775c06bc25bfb32a1c2c247868fd2a9fbc9aade
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103663841"
---
# <a name="securityidentity-class"></a><span data-ttu-id="1bdf5-104">Classe SecurityIdentity</span><span class="sxs-lookup"><span data-stu-id="1bdf5-104">SecurityIdentity class</span></span>

<span data-ttu-id="1bdf5-105">Fornece acesso a uma coleção de informações de segurança que representa a identidade de um chamador.</span><span class="sxs-lookup"><span data-stu-id="1bdf5-105">Provides access to a collection of security information representing a caller's identity.</span></span> <span data-ttu-id="1bdf5-106">Usando essa classe, você pode descobrir sobre um determinado chamador em uma cadeia de chamadores que faz parte do contexto de chamada de segurança.</span><span class="sxs-lookup"><span data-stu-id="1bdf5-106">Using this class, you can find out about a particular caller in a chain of callers that is part of the security call context.</span></span> <span data-ttu-id="1bdf5-107">Para obter mais informações sobre como as informações de contexto de chamada de segurança são acessadas, consulte segurança de componente programático.</span><span class="sxs-lookup"><span data-stu-id="1bdf5-107">For more information about how security call context information is accessed, see Programmatic Component Security.</span></span>

<span data-ttu-id="1bdf5-108">Somente aplicativos COM+ que usam segurança baseada em função podem acessar a classe **SecurityIdentity** .</span><span class="sxs-lookup"><span data-stu-id="1bdf5-108">Only COM+ applications that use role-based security can access the **SecurityIdentity** class.</span></span> <span data-ttu-id="1bdf5-109">Para obter mais informações sobre funções, consulte [Administração de segurança baseada em funções](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="1bdf5-109">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="1bdf5-110">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="1bdf5-110">When to implement</span></span>

<span data-ttu-id="1bdf5-111">Essa classe é implementada pelo COM+.</span><span class="sxs-lookup"><span data-stu-id="1bdf5-111">This class is implemented by COM+.</span></span>



| <span data-ttu-id="1bdf5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bdf5-112">Requirement</span></span> | <span data-ttu-id="1bdf5-113">Valor</span><span class="sxs-lookup"><span data-stu-id="1bdf5-113">Value</span></span> |
|------------|--------------------------------------------------------|
| <span data-ttu-id="1bdf5-114">Interfaces</span><span class="sxs-lookup"><span data-stu-id="1bdf5-114">Interfaces</span></span> | [<span data-ttu-id="1bdf5-115">**ISecurityIdentityColl**</span><span class="sxs-lookup"><span data-stu-id="1bdf5-115">**ISecurityIdentityColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="1bdf5-116">Quando usar</span><span class="sxs-lookup"><span data-stu-id="1bdf5-116">When to use</span></span>

<span data-ttu-id="1bdf5-117">Use essa classe para acessar os métodos de [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span><span class="sxs-lookup"><span data-stu-id="1bdf5-117">Use this class to access the methods of [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span></span>

## <a name="remarks"></a><span data-ttu-id="1bdf5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bdf5-118">Remarks</span></span>

<span data-ttu-id="1bdf5-119">Você não pode criar diretamente um objeto **SecurityIdentity** .</span><span class="sxs-lookup"><span data-stu-id="1bdf5-119">You cannot directly create a **SecurityIdentity** object.</span></span> <span data-ttu-id="1bdf5-120">Para usar os métodos de [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll), você deve obter uma referência à sua implementação chamando [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), fornecendo \_ ISecurityCallContext de IID para o parâmetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="1bdf5-120">To use the methods of [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span> <span data-ttu-id="1bdf5-121">Em seguida, chame [**ISecurityCallContext:: get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) solicitando um item de contexto de chamada de segurança que é uma coleção de identidade de segurança (como "DirectCaller" ou "OriginalCaller").</span><span class="sxs-lookup"><span data-stu-id="1bdf5-121">Next, call [**ISecurityCallContext::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span> <span data-ttu-id="1bdf5-122">Em seguida, chame [**ISecurityIdentityColl:: get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) para recuperar um item de identidade de segurança (como "Name" ou "AuthenticationService").</span><span class="sxs-lookup"><span data-stu-id="1bdf5-122">Then call [**ISecurityIdentityColl::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) to retrieve a security identity item (such as "Name" or "AuthenticationService").</span></span>

<span data-ttu-id="1bdf5-123">Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="1bdf5-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="1bdf5-124">Você não pode criar diretamente um objeto SecurityIdentity.</span><span class="sxs-lookup"><span data-stu-id="1bdf5-124">You cannot directly create a SecurityIdentity object.</span></span> <span data-ttu-id="1bdf5-125">Para usar suas propriedades, você deve obter um refernece para sua implementação usando o [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="1bdf5-125">To use its properties, you must obtain a refernece to its implementation using [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span> <span data-ttu-id="1bdf5-126">Em seguida, obtenha a propriedade item do objeto, solicitando um item de contexto de chamada de segurança que seja uma coleção de identidades de segurança (como "DirectCaller" ou "OriginalCaller").</span><span class="sxs-lookup"><span data-stu-id="1bdf5-126">Next, get the Item property of the object, requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span> <span data-ttu-id="1bdf5-127">Em seguida, use a propriedade item do objeto SecurityIdentity para recuperar um item de identidade de segurança (como "nome" ou "AuthenticationService").</span><span class="sxs-lookup"><span data-stu-id="1bdf5-127">Then, use the Item property of the SecurityIdentity object to retrieve a security identity item (such as "Name" or "AuthenticationService").</span></span>

## <a name="requirements"></a><span data-ttu-id="1bdf5-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bdf5-128">Requirements</span></span>



| <span data-ttu-id="1bdf5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bdf5-129">Requirement</span></span> | <span data-ttu-id="1bdf5-130">Valor</span><span class="sxs-lookup"><span data-stu-id="1bdf5-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1bdf5-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bdf5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1bdf5-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1bdf5-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1bdf5-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1bdf5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1bdf5-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1bdf5-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1bdf5-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1bdf5-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bdf5-136"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bdf5-136"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bdf5-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bdf5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bdf5-138">**GetSecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="1bdf5-138">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="1bdf5-139">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="1bdf5-139">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[<span data-ttu-id="1bdf5-140">Segurança de componente programática</span><span class="sxs-lookup"><span data-stu-id="1bdf5-140">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="1bdf5-141">Administração de segurança baseada em funções</span><span class="sxs-lookup"><span data-stu-id="1bdf5-141">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="1bdf5-142">**SecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="1bdf5-142">**SecurityCallContext**</span></span>](securitycallcontext.md)
</dt> <dt>

[<span data-ttu-id="1bdf5-143">**SecurityCallers**</span><span class="sxs-lookup"><span data-stu-id="1bdf5-143">**SecurityCallers**</span></span>](securitycallers.md)
</dt> </dl>

 

