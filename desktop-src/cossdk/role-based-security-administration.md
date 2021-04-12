---
description: Administração de segurança do Role-Based
ms.assetid: 7247758e-f486-4ce2-afca-f0d10fffe626
title: Administração de segurança do Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714cede74e105a68b0a5fed2371858054add954e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501047"
---
# <a name="role-based-security-administration"></a><span data-ttu-id="71d41-103">Administração de segurança do Role-Based</span><span class="sxs-lookup"><span data-stu-id="71d41-103">Role-Based Security Administration</span></span>

<span data-ttu-id="71d41-104">A segurança baseada em função é um serviço automático fornecido pelo COM+ que permite que você construa administrativamente e aplique uma política de controle de acesso para seu aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="71d41-104">Role-based security is an automatic service provided by COM+ that enables you to administratively construct and enforce an access control policy for your COM+ application.</span></span> <span data-ttu-id="71d41-105">Com um modelo de configuração de segurança flexível e extensível, a segurança baseada em função oferece uma vantagem considerável sobre a imposição de toda a segurança em seus componentes e oferece os seguintes benefícios:</span><span class="sxs-lookup"><span data-stu-id="71d41-105">With a flexible and extensible security configuration model, role-based security offers a considerable advantage over enforcing all security within your components and provides the following benefits:</span></span>

-   <span data-ttu-id="71d41-106">Você pode configurar a segurança administrativamente, usando a ferramenta administrativa serviços de componentes ou as funções administrativas.</span><span class="sxs-lookup"><span data-stu-id="71d41-106">You can configure security administratively, using either the Component Services administrative tool or the Administrative functions.</span></span>
-   <span data-ttu-id="71d41-107">Você não precisa escrever lógica relacionada à segurança em seus componentes quando a proteção de função no nível do método fornece um controle de acesso suficiente.</span><span class="sxs-lookup"><span data-stu-id="71d41-107">You don't have to write security-related logic into your components when role protection at the method level provides you with fine enough access control.</span></span>
-   <span data-ttu-id="71d41-108">Você não precisa considerar a segurança na interface ou no design de componentes.</span><span class="sxs-lookup"><span data-stu-id="71d41-108">You don't have to factor security into interface or component design.</span></span> <span data-ttu-id="71d41-109">Em vez disso, você pode definir a segurança em uma base método por método.</span><span class="sxs-lookup"><span data-stu-id="71d41-109">Instead, you can set security on a method-by-method basis.</span></span>
-   <span data-ttu-id="71d41-110">Você pode se concentrar na estrutura da política de segurança que deseja impor e por meio de funções, essa política pode ser claramente expressa para os administradores que implantam seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="71d41-110">You can focus on the structure of the security policy you want to enforce, and through roles, that policy can be clearly expressed to the administrators deploying your application.</span></span>
-   <span data-ttu-id="71d41-111">Você pode facilmente modificar uma política de segurança para se adaptar aos requisitos de segurança em evolução de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="71d41-111">You can easily modify a security policy to adapt to evolving security requirements for an application.</span></span>
-   <span data-ttu-id="71d41-112">Você pode criar políticas de segurança mais granulares programaticamente se precisar, usando a segurança baseada em função como plataforma de suporte.</span><span class="sxs-lookup"><span data-stu-id="71d41-112">You can build more granular security policies programmatically if you need to, using role-based security as a supporting platform.</span></span>
-   <span data-ttu-id="71d41-113">Você pode aproveitar a segurança baseada em função para fazer auditoria detalhada, pois você pode obter informações de segurança do chamador para uma cadeia inteira de chamadas upstream.</span><span class="sxs-lookup"><span data-stu-id="71d41-113">You can leverage role-based security to do detailed auditing, because you can obtain caller security information for an entire chain of upstream calls.</span></span>

> [!Note]  
> <span data-ttu-id="71d41-114">Os usuários na função Administrador do aplicativo do sistema devem ser membros do grupo Administradores local.</span><span class="sxs-lookup"><span data-stu-id="71d41-114">Users in the Administrator role for the System Application must be members of the local administrators group.</span></span> <span data-ttu-id="71d41-115">Além disso, a partir do Windows Server 2003, o recurso de autenticação para o aplicativo de sistema COM+ inclui o valor EOAC \_ Disable \_ AAA.</span><span class="sxs-lookup"><span data-stu-id="71d41-115">Also, as of Windows Server 2003, the authentication capability for the COM+ System Application includes the value EOAC\_DISABLE\_AAA.</span></span> <span data-ttu-id="71d41-116">Esse valor, que desabilita as ativações de Activate-as-Activator (AAA), é usado na chamada [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ao iniciar o aplicativo do sistema.</span><span class="sxs-lookup"><span data-stu-id="71d41-116">This value, which disables activate-as-activator (AAA) activations, is used in the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) call when launching the System Application.</span></span> <span data-ttu-id="71d41-117">Definir o recurso de autenticação como EOAC \_ Disable \_ AAA permite que um aplicativo executado em uma conta com privilégios (como LocalSystem) ajude a impedir que sua identidade seja usada para iniciar componentes não confiáveis.</span><span class="sxs-lookup"><span data-stu-id="71d41-117">Setting the authentication capability to EOAC\_DISABLE\_AAA allows an application that runs under a privileged account (such as LocalSystem) to help prevent its identity from being used to launch untrusted components.</span></span>

 

<span data-ttu-id="71d41-118">Consulte os tópicos a seguir nesta seção para obter informações sobre como funciona a segurança baseada em função e problemas a serem considerados ao usá-lo para construir uma política de segurança para um aplicativo:</span><span class="sxs-lookup"><span data-stu-id="71d41-118">See the following topics in this section for information about how role-based security works and issues to consider when using it to construct a security policy for an application:</span></span>

-   [<span data-ttu-id="71d41-119">Usando funções para autorização de cliente</span><span class="sxs-lookup"><span data-stu-id="71d41-119">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
-   [<span data-ttu-id="71d41-120">Criando funções com eficiência</span><span class="sxs-lookup"><span data-stu-id="71d41-120">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
-   [<span data-ttu-id="71d41-121">Limites de segurança</span><span class="sxs-lookup"><span data-stu-id="71d41-121">Security Boundaries</span></span>](security-boundaries.md)
-   [<span data-ttu-id="71d41-122">Informações de contexto de chamada de segurança</span><span class="sxs-lookup"><span data-stu-id="71d41-122">Security Call Context Information</span></span>](security-call-context-information.md)
-   [<span data-ttu-id="71d41-123">Propriedade de contexto de segurança</span><span class="sxs-lookup"><span data-stu-id="71d41-123">Security Context Property</span></span>](security-context-property.md)

<span data-ttu-id="71d41-124">Para obter descrições detalhadas das etapas envolvidas na configuração da segurança baseada em função para um aplicativo, consulte [configuring Role-Based Security](configuring-role-based-security.md).</span><span class="sxs-lookup"><span data-stu-id="71d41-124">For detailed how-to descriptions of the steps involved in configuring role-based security for an application, see [Configuring Role-Based Security](configuring-role-based-security.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="71d41-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71d41-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71d41-126">Autenticação de cliente</span><span class="sxs-lookup"><span data-stu-id="71d41-126">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="71d41-127">Representação e delegação de cliente</span><span class="sxs-lookup"><span data-stu-id="71d41-127">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="71d41-128">Segurança de aplicativos de biblioteca</span><span class="sxs-lookup"><span data-stu-id="71d41-128">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="71d41-129">Segurança de aplicativos de várias camadas</span><span class="sxs-lookup"><span data-stu-id="71d41-129">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="71d41-130">Segurança de componente programática</span><span class="sxs-lookup"><span data-stu-id="71d41-130">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="71d41-131">Usando a política de restrição de software no COM+</span><span class="sxs-lookup"><span data-stu-id="71d41-131">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
