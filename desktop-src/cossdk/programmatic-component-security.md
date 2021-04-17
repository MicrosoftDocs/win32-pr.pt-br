---
description: Quando você usa a segurança baseada em função no aplicativo COM+ que contém o componente, você tem acesso à funcionalidade de segurança programática de dentro do seu componente.
ms.assetid: 6117970c-5dbd-485e-978e-3aa96e42b359
title: Segurança de componente programática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31622608e4d4f54aeb53b403b5d8711ff9c6a9af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763087"
---
# <a name="programmatic-component-security"></a><span data-ttu-id="9decb-103">Segurança de componente programática</span><span class="sxs-lookup"><span data-stu-id="9decb-103">Programmatic Component Security</span></span>

<span data-ttu-id="9decb-104">Quando você usa a segurança baseada em função no aplicativo COM+ que contém o componente, você tem acesso à funcionalidade de segurança programática de dentro do seu componente.</span><span class="sxs-lookup"><span data-stu-id="9decb-104">When you use role-based security in the COM+ application that contains your component, you have access to programmatic security functionality from within your component.</span></span> <span data-ttu-id="9decb-105">Você pode verificar a associação de função para determinar se seções específicas de código são executadas. você pode acessar informações de segurança usando o objeto de contexto de chamada de segurança e pode determinar se a segurança está habilitada para a chamada atual.</span><span class="sxs-lookup"><span data-stu-id="9decb-105">You can check role membership to determine whether particular sections of code are executed, you can access security information using the security call context object, and you can determine whether security is enabled for the current call.</span></span> <span data-ttu-id="9decb-106">Você pode executar todas essas tarefas usando uma referência a um objeto [**SecurityCallContext**](securitycallcontext.md) (para aplicativos do Microsoft Visual Basic) ou um ponteiro para a interface [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) (para aplicativos C e Microsoft Visual C++).</span><span class="sxs-lookup"><span data-stu-id="9decb-106">You can perform all of these tasks by using a reference to a [**SecurityCallContext**](securitycallcontext.md) object (for Microsoft Visual Basic applications) or a pointer to the [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) interface (for C and Microsoft Visual C++ applications).</span></span>

<span data-ttu-id="9decb-107">Para obter mais informações sobre a segurança baseada em função programática, consulte os seguintes tópicos nesta seção:</span><span class="sxs-lookup"><span data-stu-id="9decb-107">For more information regarding programmatic role-based security, see the following topics in this section:</span></span>

-   [<span data-ttu-id="9decb-108">Verificando a associação de função</span><span class="sxs-lookup"><span data-stu-id="9decb-108">Checking Role Membership</span></span>](checking-role-membership.md)
-   [<span data-ttu-id="9decb-109">Determinando se a segurança do Role-Based está habilitada</span><span class="sxs-lookup"><span data-stu-id="9decb-109">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
-   [<span data-ttu-id="9decb-110">Acessando informações de contexto de chamada de segurança</span><span class="sxs-lookup"><span data-stu-id="9decb-110">Accessing Security Call Context Information</span></span>](accessing-security-call-context-information.md)

## <a name="impersonation-and-com-security-features"></a><span data-ttu-id="9decb-111">Representação e recursos de segurança COM</span><span class="sxs-lookup"><span data-stu-id="9decb-111">Impersonation and COM Security Features</span></span>

<span data-ttu-id="9decb-112">Se o componente for usado em um aplicativo COM+ que não usa segurança baseada em função, a verificação de função programática e as informações de contexto de chamada de segurança não estarão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9decb-112">If your component is used in a COM+ application that does not use role-based security, programmatic role checking and security call context information are not available.</span></span> <span data-ttu-id="9decb-113">No entanto, você pode usar a funcionalidade de segurança programática fornecida pelo COM.</span><span class="sxs-lookup"><span data-stu-id="9decb-113">However, you can use the programmatic security functionality provided by COM.</span></span> <span data-ttu-id="9decb-114">Para obter mais informações, consulte [segurança em com](/windows/desktop/com/security-in-com).</span><span class="sxs-lookup"><span data-stu-id="9decb-114">For more information, see [Security in COM](/windows/desktop/com/security-in-com).</span></span>

<span data-ttu-id="9decb-115">Embora você possa usar a maior parte da funcionalidade de segurança fornecida pelo COM, não é possível chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) de um componente que faz parte de um aplicativo com+, pois **CoInitializeSecurity** é chamado pelo substituto em que o aplicativo com+ é executado.</span><span class="sxs-lookup"><span data-stu-id="9decb-115">Although you can use most of the security functionality provided by COM, you cannot call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) from a component that is part of a COM+ application because **CoInitializeSecurity** is called by the surrogate that the COM+ application runs in.</span></span> <span data-ttu-id="9decb-116">No entanto, você pode chamar outras funções de segurança, como [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), que recupera informações sobre o cliente.</span><span class="sxs-lookup"><span data-stu-id="9decb-116">However, you can call other security functions, such as [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), which retrieves information about the client.</span></span>

<span data-ttu-id="9decb-117">Em particular, quando você precisa usar a identidade do cliente para acessar algum recurso — por exemplo, acessar um arquivo protegido por um descritor de segurança ou propagar a identidade do cliente por meio de um banco de dados — você pode executar a representação programaticamente.</span><span class="sxs-lookup"><span data-stu-id="9decb-117">In particular, when you need to use the client's identity to access some resource—for example, accessing a file protected by a security descriptor, or propagating the client's identity through to a database—you can perform impersonation programmatically.</span></span> <span data-ttu-id="9decb-118">Para obter mais detalhes sobre quando e como fazer isso, consulte [representação e delegação do cliente](client-impersonation-and-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="9decb-118">For more detail about when and how to do this, see [Client Impersonation and Delegation](client-impersonation-and-delegation.md).</span></span>

## <a name="testing-security-functionality"></a><span data-ttu-id="9decb-119">Testando a funcionalidade de segurança</span><span class="sxs-lookup"><span data-stu-id="9decb-119">Testing Security Functionality</span></span>

<span data-ttu-id="9decb-120">Se você usar a segurança programática do COM+ em seu componente, deverá integrar o componente a um aplicativo COM+ quando estiver pronto para testar a funcionalidade de segurança do componente.</span><span class="sxs-lookup"><span data-stu-id="9decb-120">If you use COM+ programmatic security in your component, you must integrate the component into a COM+ application when you are ready to test the component's security functionality.</span></span> <span data-ttu-id="9decb-121">Se um componente que usa a segurança programática do COM+ for executado sem ser integrado a um aplicativo COM+, exceções serão lançadas.</span><span class="sxs-lookup"><span data-stu-id="9decb-121">If a component using COM+ programmatic security is run without being integrated into a COM+ application, exceptions will be thrown.</span></span> <span data-ttu-id="9decb-122">Portanto, se você quiser garantir que esse componente também seja capaz de ser integrado com êxito a um aplicativo que não faz parte do ambiente COM+, deverá garantir que essas exceções sejam tratadas adequadamente.</span><span class="sxs-lookup"><span data-stu-id="9decb-122">Therefore, if you want to ensure that such a component is also capable of being successfully integrated into an application that is not part of the COM+ environment, you must ensure that these exceptions are handled appropriately.</span></span>

## <a name="documenting-security-requirements"></a><span data-ttu-id="9decb-123">Documentando os requisitos de segurança</span><span class="sxs-lookup"><span data-stu-id="9decb-123">Documenting Security Requirements</span></span>

<span data-ttu-id="9decb-124">Se você estiver escrevendo um componente autônomo para aplicativos COM+ que usam a segurança baseada em função, você precisará documentar o componente para que a segurança possa ser configurada adequadamente quando o componente for integrado a um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="9decb-124">If you are writing a stand-alone component for COM+ applications that use role-based security, you need to document the component so that security can be configured appropriately when the component is integrated into a COM+ application.</span></span> <span data-ttu-id="9decb-125">Por exemplo, você deve identificar as funções que devem ser adicionadas e explicar a quais métodos e interfaces cada função deve ser atribuída.</span><span class="sxs-lookup"><span data-stu-id="9decb-125">For example, you should identify the roles that must be added and explain which methods and interfaces each role should be assigned to.</span></span> <span data-ttu-id="9decb-126">Além disso, se um método como IsCallerInRole ("caixas") for chamado, você deverá descrever a funcionalidade que apenas os informadores têm acesso ao.</span><span class="sxs-lookup"><span data-stu-id="9decb-126">In addition, if a method such as IsCallerInRole("Teller") is called, you should describe the functionality that only Tellers have access to.</span></span> <span data-ttu-id="9decb-127">Você também deve especificar se uma função é necessária para ajudar a proteger o acesso a todo o componente.</span><span class="sxs-lookup"><span data-stu-id="9decb-127">You should also specify whether a role is required to help protect access to the entire component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9decb-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9decb-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9decb-129">Autenticação de cliente</span><span class="sxs-lookup"><span data-stu-id="9decb-129">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="9decb-130">Representação e delegação de cliente</span><span class="sxs-lookup"><span data-stu-id="9decb-130">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="9decb-131">Segurança de aplicativos de biblioteca</span><span class="sxs-lookup"><span data-stu-id="9decb-131">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="9decb-132">Segurança de aplicativos de várias camadas</span><span class="sxs-lookup"><span data-stu-id="9decb-132">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="9decb-133">Administração de segurança baseada em funções</span><span class="sxs-lookup"><span data-stu-id="9decb-133">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="9decb-134">Usando a política de restrição de software no COM+</span><span class="sxs-lookup"><span data-stu-id="9decb-134">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
