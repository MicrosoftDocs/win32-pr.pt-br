---
description: Fornece acesso ao contexto de segurança da chamada atual, que contém informações sobre os chamadores de um objeto.
ms.assetid: e8ac05fb-6665-4e57-b64e-82d9799d29d4
title: Classe SecurityCallContext (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallContext
api_type:
- COM
ms.openlocfilehash: bd15b7e0317a507a2340cc148bb927bb5d94a37b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105793971"
---
# <a name="securitycallcontext-class"></a><span data-ttu-id="4c46c-103">Classe SecurityCallContext</span><span class="sxs-lookup"><span data-stu-id="4c46c-103">SecurityCallContext class</span></span>

<span data-ttu-id="4c46c-104">Fornece acesso ao contexto de segurança da chamada atual, que contém informações sobre os chamadores de um objeto.</span><span class="sxs-lookup"><span data-stu-id="4c46c-104">Provides access to the current call's security context, which contains information about an object's callers.</span></span> <span data-ttu-id="4c46c-105">Usando essa classe, você também pode descobrir se o chamador direto de um objeto é membro de uma função específica e se a segurança está habilitada para o objeto.</span><span class="sxs-lookup"><span data-stu-id="4c46c-105">Using this class, you can also find out whether an object's direct caller is a member of a particular role and whether security is enabled for the object.</span></span>

<span data-ttu-id="4c46c-106">Somente aplicativos COM+ que usam segurança baseada em função podem acessar a classe **SecurityCallContext** .</span><span class="sxs-lookup"><span data-stu-id="4c46c-106">Only COM+ applications that use role-based security can access the **SecurityCallContext** class.</span></span> <span data-ttu-id="4c46c-107">Para obter mais informações sobre funções, consulte [Administração de segurança baseada em funções](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="4c46c-107">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="4c46c-108">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="4c46c-108">When to implement</span></span>

<span data-ttu-id="4c46c-109">Essa classe é implementada pelo COM+.</span><span class="sxs-lookup"><span data-stu-id="4c46c-109">This class is implemented by COM+.</span></span>



| <span data-ttu-id="4c46c-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c46c-110">Requirement</span></span> | <span data-ttu-id="4c46c-111">Valor</span><span class="sxs-lookup"><span data-stu-id="4c46c-111">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="4c46c-112">Interfaces</span><span class="sxs-lookup"><span data-stu-id="4c46c-112">Interfaces</span></span> | [<span data-ttu-id="4c46c-113">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="4c46c-113">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="4c46c-114">Quando usar</span><span class="sxs-lookup"><span data-stu-id="4c46c-114">When to use</span></span>

<span data-ttu-id="4c46c-115">Use essa classe para acessar os métodos de [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="4c46c-115">Use this class to access the methods of [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span></span>

## <a name="remarks"></a><span data-ttu-id="4c46c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c46c-116">Remarks</span></span>

<span data-ttu-id="4c46c-117">Você não pode criar diretamente um objeto **SecurityCallContext** .</span><span class="sxs-lookup"><span data-stu-id="4c46c-117">You cannot directly create a **SecurityCallContext** object.</span></span> <span data-ttu-id="4c46c-118">Para usar os métodos de [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext), você deve obter uma referência à sua implementação chamando [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), fornecendo \_ ISecurityCallContext de IID para o parâmetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="4c46c-118">To use the methods of [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span>

<span data-ttu-id="4c46c-119">Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de serviços COM+.</span><span class="sxs-lookup"><span data-stu-id="4c46c-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="4c46c-120">Um objeto SecurityCallContext pode ser declarado usando "COMSVCSLib. SecurityCallContext" como o nome da classe; Ele é criado chamando [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="4c46c-120">A SecurityCallContext object can be declared using "COMSVCSLib.SecurityCallContext" as the class name; it is created by calling [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c46c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c46c-121">Requirements</span></span>



| <span data-ttu-id="4c46c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c46c-122">Requirement</span></span> | <span data-ttu-id="4c46c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="4c46c-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4c46c-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c46c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4c46c-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4c46c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="4c46c-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c46c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4c46c-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4c46c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4c46c-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4c46c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c46c-129"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c46c-129"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c46c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c46c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c46c-131">**GetSecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="4c46c-131">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="4c46c-132">**ISecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="4c46c-132">**ISecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="4c46c-133">Segurança de componente programática</span><span class="sxs-lookup"><span data-stu-id="4c46c-133">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="4c46c-134">Administração de segurança baseada em funções</span><span class="sxs-lookup"><span data-stu-id="4c46c-134">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="4c46c-135">**SecurityCallers**</span><span class="sxs-lookup"><span data-stu-id="4c46c-135">**SecurityCallers**</span></span>](securitycallers.md)
</dt> <dt>

[<span data-ttu-id="4c46c-136">**SecurityIdentity**</span><span class="sxs-lookup"><span data-stu-id="4c46c-136">**SecurityIdentity**</span></span>](securityidentity.md)
</dt> </dl>

 

