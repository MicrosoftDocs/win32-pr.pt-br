---
description: Como um aplicativo de biblioteca COM+ é hospedado por outro processo, que pode ter suas próprias configurações de segurança, a segurança para aplicativos de biblioteca requer uma consideração especial.
ms.assetid: a966020c-a0bd-467c-b6d3-e09267cf5574
title: Segurança de aplicativos de biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2885173f3798d33ed26a5b447fde4429b9bf96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500892"
---
# <a name="library-application-security"></a><span data-ttu-id="fa58b-103">Segurança de aplicativos de biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa58b-103">Library Application Security</span></span>

<span data-ttu-id="fa58b-104">Como um aplicativo de biblioteca COM+ é hospedado por outro processo, que pode ter suas próprias configurações de segurança, a segurança para aplicativos de biblioteca requer uma consideração especial.</span><span class="sxs-lookup"><span data-stu-id="fa58b-104">Because a COM+ library application is hosted by another process, which may have its own security settings, security for library applications requires special consideration.</span></span>

<span data-ttu-id="fa58b-105">As seguintes restrições se aplicam à segurança do aplicativo de biblioteca:</span><span class="sxs-lookup"><span data-stu-id="fa58b-105">The following constraints apply to library application security:</span></span>

-   <span data-ttu-id="fa58b-106">Os aplicativos de biblioteca são executados no token de segurança do processo do cliente em vez de em sua própria identidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="fa58b-106">Library applications run under the client process security token rather than under their own user identity.</span></span> <span data-ttu-id="fa58b-107">Eles têm apenas tantos privilégios quanto o cliente.</span><span class="sxs-lookup"><span data-stu-id="fa58b-107">They have only as much privilege as the client has.</span></span>
-   <span data-ttu-id="fa58b-108">Os aplicativos de biblioteca não controlam a segurança em nível de processo.</span><span class="sxs-lookup"><span data-stu-id="fa58b-108">Library applications do not control process-level security.</span></span> <span data-ttu-id="fa58b-109">Nenhum usuário em funções será adicionado ao descritor de segurança para o processo.</span><span class="sxs-lookup"><span data-stu-id="fa58b-109">No users in roles will be added to the security descriptor for the process.</span></span> <span data-ttu-id="fa58b-110">A única maneira de um aplicativo de biblioteca executar suas próprias verificações de acesso é usar a segurança em nível de componente.</span><span class="sxs-lookup"><span data-stu-id="fa58b-110">The only way for a library application to perform its own access checks is to use component-level security.</span></span> <span data-ttu-id="fa58b-111">(Consulte [limites de segurança](security-boundaries.md).)</span><span class="sxs-lookup"><span data-stu-id="fa58b-111">(See [Security Boundaries](security-boundaries.md).)</span></span>
-   <span data-ttu-id="fa58b-112">Os aplicativos de biblioteca podem ser configurados para participar ou não participar da autenticação de processo de host, habilitando ou desabilitando a autenticação.</span><span class="sxs-lookup"><span data-stu-id="fa58b-112">Library applications can be configured to either participate or not participate in host process authentication, by enabling or disabling authentication.</span></span> <span data-ttu-id="fa58b-113">(Consulte [habilitando a autenticação para um aplicativo de biblioteca](enabling-authentication-for-a-library-application.md).)</span><span class="sxs-lookup"><span data-stu-id="fa58b-113">(See [Enabling Authentication for a Library Application](enabling-authentication-for-a-library-application.md).)</span></span>
-   <span data-ttu-id="fa58b-114">Aplicativos de biblioteca não podem definir um nível de representação; Eles usam o do processo de host.</span><span class="sxs-lookup"><span data-stu-id="fa58b-114">Library applications cannot set an impersonation level; they use that of the host process.</span></span>

## <a name="using-library-applications-to-limit-application-privilege"></a><span data-ttu-id="fa58b-115">Usando aplicativos de biblioteca para limitar o privilégio do aplicativo</span><span class="sxs-lookup"><span data-stu-id="fa58b-115">Using Library Applications to Limit Application Privilege</span></span>

<span data-ttu-id="fa58b-116">Em alguns casos, talvez você queira configurar um aplicativo especificamente como um aplicativo de biblioteca para que ele seja executado sob a identidade do processo de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="fa58b-116">In some cases, you may want to configure an application specifically as a library application so that it runs under the identity of the hosting process.</span></span> <span data-ttu-id="fa58b-117">Isso limita o aplicativo de forma fundamental para que ele possa acessar somente os recursos que o cliente, o processo de host, pode acessar.</span><span class="sxs-lookup"><span data-stu-id="fa58b-117">Doing so fundamentally limits the application so that it can access only those resources that its client, the host process, can access.</span></span> <span data-ttu-id="fa58b-118">Os threads nos quais os componentes do aplicativo de biblioteca são executados usarão o token de processo por padrão e, portanto, quando eles fazem chamadas fora do aplicativo ou acessam recursos como arquivos protegidos com um descritor de segurança, parecerão ser o cliente.</span><span class="sxs-lookup"><span data-stu-id="fa58b-118">The threads that the library application components run on will use the process token by default, and therefore when they make calls outside of the application or access resources such as files guarded with a security descriptor, they will appear to be the client.</span></span> <span data-ttu-id="fa58b-119">Para aplicativos que executam trabalho confidencial, essa pode ser uma maneira fácil de controlar o escopo de suas ações.</span><span class="sxs-lookup"><span data-stu-id="fa58b-119">For applications that perform sensitive work, this may be an easy way to control the scope of their actions.</span></span>

## <a name="effectively-securing-library-applications"></a><span data-ttu-id="fa58b-120">Protegendo aplicativos de biblioteca com eficiência</span><span class="sxs-lookup"><span data-stu-id="fa58b-120">Effectively Securing Library Applications</span></span>

<span data-ttu-id="fa58b-121">Há considerações especiais na configuração da segurança baseada em função e da autenticação para aplicativos de biblioteca para que eles sejam executados conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="fa58b-121">There are special considerations in configuring role-based security and authentication for library applications so that they perform as expected.</span></span> <span data-ttu-id="fa58b-122">Para obter detalhes, consulte [Configurando a segurança para aplicativos de biblioteca](configuring-security-for-library-applications.md).</span><span class="sxs-lookup"><span data-stu-id="fa58b-122">For details, see [Configuring Security for Library Applications](configuring-security-for-library-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa58b-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa58b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa58b-124">Autenticação de cliente</span><span class="sxs-lookup"><span data-stu-id="fa58b-124">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="fa58b-125">Representação e delegação de cliente</span><span class="sxs-lookup"><span data-stu-id="fa58b-125">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="fa58b-126">Segurança de aplicativos de várias camadas</span><span class="sxs-lookup"><span data-stu-id="fa58b-126">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="fa58b-127">Segurança de componente programática</span><span class="sxs-lookup"><span data-stu-id="fa58b-127">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="fa58b-128">Administração de segurança baseada em funções</span><span class="sxs-lookup"><span data-stu-id="fa58b-128">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="fa58b-129">Usando a política de restrição de software no COM+</span><span class="sxs-lookup"><span data-stu-id="fa58b-129">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



