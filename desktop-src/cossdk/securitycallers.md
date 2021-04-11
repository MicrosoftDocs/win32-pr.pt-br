---
description: Fornece acesso a informações sobre chamadores individuais em uma coleção de chamadores. A coleção representa a cadeia de chamadas terminando com a chamada atual, e cada chamador na coleção representa a identidade de um chamador.
ms.assetid: 164fe12d-eeb3-402f-8aa3-e3545904d9c4
title: Classe SecurityCallers (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallers
api_type:
- COM
ms.openlocfilehash: c757b11bba6a30e8951915e1eace0811b6b6f732
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296087"
---
# <a name="securitycallers-class"></a><span data-ttu-id="be80e-104">Classe SecurityCallers</span><span class="sxs-lookup"><span data-stu-id="be80e-104">SecurityCallers class</span></span>

<span data-ttu-id="be80e-105">Fornece acesso a informações sobre chamadores individuais em uma coleção de chamadores.</span><span class="sxs-lookup"><span data-stu-id="be80e-105">Provides access to information about individual callers in a collection of callers.</span></span> <span data-ttu-id="be80e-106">A coleção representa a cadeia de chamadas terminando com a chamada atual, e cada chamador na coleção representa a identidade de um chamador.</span><span class="sxs-lookup"><span data-stu-id="be80e-106">The collection represents the chain of calls ending with the current call, and each caller in the collection represents the identity of one caller.</span></span> <span data-ttu-id="be80e-107">Somente os chamadores que cruzam um limite onde a segurança está marcada são incluídos na cadeia de chamadores.</span><span class="sxs-lookup"><span data-stu-id="be80e-107">Only callers who cross a boundary where security is checked are included in the chain of callers.</span></span> <span data-ttu-id="be80e-108">(No ambiente COM+, a segurança é verificada em limites de aplicativo.) O acesso a informações sobre a identidade de um chamador específico é fornecido por meio da classe [**SecurityIdentity**](securityidentity.md) , uma coleção de identidades.</span><span class="sxs-lookup"><span data-stu-id="be80e-108">(In the COM+ environment, security is checked at application boundaries.) Access to information about a particular caller's identity is provided through the [**SecurityIdentity**](securityidentity.md) class, an identity collection.</span></span>

<span data-ttu-id="be80e-109">Somente aplicativos COM+ que usam segurança baseada em função podem acessar a classe **SecurityCallers** .</span><span class="sxs-lookup"><span data-stu-id="be80e-109">Only COM+ applications that use role-based security can access the **SecurityCallers** class.</span></span> <span data-ttu-id="be80e-110">Para obter mais informações sobre funções, consulte [Administração de segurança baseada em funções](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="be80e-110">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="be80e-111">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="be80e-111">When to implement</span></span>

<span data-ttu-id="be80e-112">Essa classe é implementada pelo COM+.</span><span class="sxs-lookup"><span data-stu-id="be80e-112">This class is implemented by COM+.</span></span>



| <span data-ttu-id="be80e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="be80e-113">Requirement</span></span> | <span data-ttu-id="be80e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="be80e-114">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="be80e-115">Interfaces</span><span class="sxs-lookup"><span data-stu-id="be80e-115">Interfaces</span></span> | [<span data-ttu-id="be80e-116">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="be80e-116">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="be80e-117">Quando usar</span><span class="sxs-lookup"><span data-stu-id="be80e-117">When to use</span></span>

<span data-ttu-id="be80e-118">Use essa classe para acessar os métodos de [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span><span class="sxs-lookup"><span data-stu-id="be80e-118">Use this class to access the methods of [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span></span>

## <a name="remarks"></a><span data-ttu-id="be80e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="be80e-119">Remarks</span></span>

<span data-ttu-id="be80e-120">Você não pode criar diretamente um objeto **SecurityCallers** .</span><span class="sxs-lookup"><span data-stu-id="be80e-120">You cannot directly create a **SecurityCallers** object.</span></span> <span data-ttu-id="be80e-121">Para usar os métodos de [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll), você deve obter uma referência à sua implementação chamando [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), fornecendo \_ ISecurityCallContext de IID para o parâmetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="be80e-121">To use the methods of [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span> <span data-ttu-id="be80e-122">Em seguida, chame [**ISecurityCallContext:: get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) solicitando um item de contexto de chamada de segurança que é uma coleção de identidade de segurança (como "DirectCaller" ou "OriginalCaller").</span><span class="sxs-lookup"><span data-stu-id="be80e-122">Next, call [**ISecurityCallContext::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span>

<span data-ttu-id="be80e-123">Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="be80e-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="be80e-124">Você não pode criar diretamente um objeto SecurityCallers.</span><span class="sxs-lookup"><span data-stu-id="be80e-124">You cannot directly create a SecurityCallers object.</span></span> <span data-ttu-id="be80e-125">Para usar suas propriedades, você deve obter um refernece para sua implementação usando o [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="be80e-125">To use its properties, you must obtain a refernece to its implementation using [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span> <span data-ttu-id="be80e-126">Em seguida, obtenha a propriedade item do objeto, solicitando um item de contexto de chamada de segurança que seja uma coleção de identidades de segurança (como "DirectCaller" ou "OriginalCaller").</span><span class="sxs-lookup"><span data-stu-id="be80e-126">Next, get the Item property of the object, requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span>

## <a name="requirements"></a><span data-ttu-id="be80e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be80e-127">Requirements</span></span>



| <span data-ttu-id="be80e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="be80e-128">Requirement</span></span> | <span data-ttu-id="be80e-129">Valor</span><span class="sxs-lookup"><span data-stu-id="be80e-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="be80e-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be80e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="be80e-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="be80e-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="be80e-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be80e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="be80e-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="be80e-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="be80e-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="be80e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="be80e-135"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="be80e-135"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be80e-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="be80e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be80e-137">**GetSecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="be80e-137">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="be80e-138">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="be80e-138">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[<span data-ttu-id="be80e-139">Segurança de componente programática</span><span class="sxs-lookup"><span data-stu-id="be80e-139">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="be80e-140">Administração de segurança baseada em funções</span><span class="sxs-lookup"><span data-stu-id="be80e-140">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="be80e-141">**SecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="be80e-141">**SecurityCallContext**</span></span>](securitycallcontext.md)
</dt> <dt>

[<span data-ttu-id="be80e-142">**SecurityIdentity**</span><span class="sxs-lookup"><span data-stu-id="be80e-142">**SecurityIdentity**</span></span>](securityidentity.md)
</dt> </dl>

 

