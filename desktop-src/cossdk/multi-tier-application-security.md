---
description: Segurança de aplicativos de várias camadas
ms.assetid: ff84eeed-ddfd-40e8-8f42-625b4d49ecd5
title: Segurança de aplicativos de várias camadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150f7894c7d11e832786e31ab028f9dbac35f6e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760731"
---
# <a name="multi-tier-application-security"></a><span data-ttu-id="11cf6-103">Segurança de aplicativos de várias camadas</span><span class="sxs-lookup"><span data-stu-id="11cf6-103">Multi-Tier Application Security</span></span>

<span data-ttu-id="11cf6-104">Você pode enfrentar opções difíceis de decidir precisamente onde impor a segurança em um aplicativo baseado em componentes de várias camadas: no banco de dados?</span><span class="sxs-lookup"><span data-stu-id="11cf6-104">You can face difficult choices in deciding precisely where to enforce security in a multi-tier, component-based application: At the database?</span></span> <span data-ttu-id="11cf6-105">Na camada intermediária?</span><span class="sxs-lookup"><span data-stu-id="11cf6-105">At the middle tier?</span></span> <span data-ttu-id="11cf6-106">Nos componentes?</span><span class="sxs-lookup"><span data-stu-id="11cf6-106">In the components?</span></span> <span data-ttu-id="11cf6-107">Outro lugar?</span><span class="sxs-lookup"><span data-stu-id="11cf6-107">Somewhere else?</span></span> <span data-ttu-id="11cf6-108">Parte?</span><span class="sxs-lookup"><span data-stu-id="11cf6-108">Everywhere?</span></span> <span data-ttu-id="11cf6-109">À medida que os mecanismos de segurança aumentam em número e complexidade, os declínios de desempenho e o comportamento do aplicativo se tornam menos previsíveis.</span><span class="sxs-lookup"><span data-stu-id="11cf6-109">As security mechanisms increase in number and complexity, performance declines and application behavior becomes less predictable.</span></span> <span data-ttu-id="11cf6-110">No entanto, você deve garantir que os dados estejam protegidos, que as regras de negócio sejam seguidas e que a atividade significativa seja registrada e ainda ter seu aplicativo funcionando para clientes como pretendido.</span><span class="sxs-lookup"><span data-stu-id="11cf6-110">Nevertheless, you must ensure that data is protected, business rules are followed, and significant activity is logged, and still have your application work for clients as intended.</span></span> <span data-ttu-id="11cf6-111">Você deve ter certeza de que cada caminho de cliente por meio de seu aplicativo está correto e que os pontos de verificação de segurança que você tem em vigor serão suficientes.</span><span class="sxs-lookup"><span data-stu-id="11cf6-111">You must be certain that every client path through your application is correct and that the security checkpoints you have in place will suffice.</span></span>

<span data-ttu-id="11cf6-112">A decisão mais difícil é geralmente se a segurança deve ser imposta no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="11cf6-112">The hardest decision is often whether to enforce security at the database.</span></span> <span data-ttu-id="11cf6-113">Historicamente, é aí que a segurança é mais rígida, pois é percebida como um reino que precisa ser verdadeiramente seguro, e os administradores de banco de dados são muito relutantes em confiar em outra pessoa para impor a segurança para eles.</span><span class="sxs-lookup"><span data-stu-id="11cf6-113">Historically, this is where security is tightest because it is perceived as the one kingdom that needs to be truly secure, and database administrators are very reluctant to trust someone else to enforce security for them.</span></span> <span data-ttu-id="11cf6-114">Mas a imposição da segurança no banco de dados pode ser bastante cara e difícil de dimensionar, o que é precisamente o ponto de escrever aplicativos de várias camadas em primeiro lugar.</span><span class="sxs-lookup"><span data-stu-id="11cf6-114">But enforcing security at the database can be quite expensive and difficult to scale, which is precisely the point of writing multi-tier applications in the first place.</span></span>

<span data-ttu-id="11cf6-115">A regra geral a seguir com aplicativos de várias camadas escalonáveis usando COM+ é que, sempre que possível, você deve impor segurança detalhada no aplicativo COM+ na camada intermediária.</span><span class="sxs-lookup"><span data-stu-id="11cf6-115">The general rule to follow with scalable multi-tier applications using COM+ is that, whenever possible, you should enforce detailed security in the COM+ application at the middle tier.</span></span> <span data-ttu-id="11cf6-116">Isso permite que você aproveite totalmente os serviços escalonáveis fornecidos pelo COM+.</span><span class="sxs-lookup"><span data-stu-id="11cf6-116">Doing so enables you to fully leverage the scalable services provided by COM+.</span></span> <span data-ttu-id="11cf6-117">Autentique no banco de dados somente quando for absolutamente necessário, e avalie totalmente as implicações de desempenho de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="11cf6-117">Authenticate at the database only when you absolutely need to, and fully weigh the performance implications of doing so.</span></span>

<span data-ttu-id="11cf6-118">Para obter uma discussão sobre problemas a serem considerados ao decidir onde executar verificações de segurança, consulte [decidindo onde impor a segurança](deciding-where-to-enforce-security.md).</span><span class="sxs-lookup"><span data-stu-id="11cf6-118">For a discussion of issues to consider in deciding where to perform security checks, see [Deciding Where to Enforce Security](deciding-where-to-enforce-security.md).</span></span>

<span data-ttu-id="11cf6-119">Para obter uma discussão sobre alguns cenários básicos de proteção de aplicativos de várias camadas, consulte [cenários básicos para proteger dados em aplicativos de várias camadas](basic-scenarios-for-securing-data-in-multi-tier-applications.md).</span><span class="sxs-lookup"><span data-stu-id="11cf6-119">For a discussion of some basic scenarios in securing multi-tier applications, see [Basic Scenarios for Securing Data in Multi-Tier Applications](basic-scenarios-for-securing-data-in-multi-tier-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="11cf6-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11cf6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11cf6-121">Autenticação de cliente</span><span class="sxs-lookup"><span data-stu-id="11cf6-121">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="11cf6-122">Representação e delegação de cliente</span><span class="sxs-lookup"><span data-stu-id="11cf6-122">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="11cf6-123">Segurança de aplicativos de biblioteca</span><span class="sxs-lookup"><span data-stu-id="11cf6-123">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="11cf6-124">Segurança de componente programática</span><span class="sxs-lookup"><span data-stu-id="11cf6-124">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="11cf6-125">Administração de segurança baseada em funções</span><span class="sxs-lookup"><span data-stu-id="11cf6-125">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="11cf6-126">Usando a política de restrição de software no COM+</span><span class="sxs-lookup"><span data-stu-id="11cf6-126">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



