---
description: Projetando para segurança
ms.assetid: 436f9d86-fbfa-4d5a-8580-fa1d4065c0aa
title: Projetando para segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69bc59b06cfcb7432806e548cc9808199b194e6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785176"
---
# <a name="designing-for-security"></a><span data-ttu-id="27f12-103">Projetando para segurança</span><span class="sxs-lookup"><span data-stu-id="27f12-103">Designing for Security</span></span>

<span data-ttu-id="27f12-104">A estratégia de ponta a ponta de segurança, obviamente, depende do tipo de aplicativo distribuído que você está desenvolvendo.</span><span class="sxs-lookup"><span data-stu-id="27f12-104">Your end-to-end strategy for security obviously depends on the type of distributed application you are developing.</span></span> <span data-ttu-id="27f12-105">A seguir, há várias sugestões para tratar da segurança em relação à lógica do aplicativo de camada intermediária:</span><span class="sxs-lookup"><span data-stu-id="27f12-105">Following are several suggestions for addressing security with respect to middle-tier application logic:</span></span>

-   <span data-ttu-id="27f12-106">Para obter eficiência e desempenho, autentique o mais próximo possível do usuário.</span><span class="sxs-lookup"><span data-stu-id="27f12-106">For efficiency and performance, authenticate as close to the user as you can.</span></span> <span data-ttu-id="27f12-107">Se seu aplicativo envolver uma arquitetura de lógica para banco de dados do navegador para o negócio, considere mapear os clientes do navegador para identidades de domínio, executar o aplicativo COM+ sob identidades específicas de cada aplicativo e configurar tabelas na camada de dados para que sejam acessíveis somente por uma identidade de aplicativo específica.</span><span class="sxs-lookup"><span data-stu-id="27f12-107">If your application involves a browser-to-business-logic-to-database architecture, consider mapping the browser clients to domain identities, run the COM+ application under identities specific to each application, and configure tables in the data tier to be accessible only by a particular application identity.</span></span> <span data-ttu-id="27f12-108">Esse cenário de servidor confiável é mais escalonável e menos problemático do que usar o DBMS para autenticação.</span><span class="sxs-lookup"><span data-stu-id="27f12-108">This trusted server scenario is more scalable and less problematic than using the DBMS for authenticating.</span></span>
-   <span data-ttu-id="27f12-109">Se estiver criando um componente que será usado em um aplicativo distribuído usando a segurança baseada em função, você poderá usar a funcionalidade de [segurança do com+](com--security.md) .</span><span class="sxs-lookup"><span data-stu-id="27f12-109">If you are designing a component that will be used in a distributed application using role-based security, you can use the [COM+ security](com--security.md) functionality.</span></span> <span data-ttu-id="27f12-110">Essa funcionalidade permite chamar métodos como [**IObjectContext:: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) e [**IObjectContext:: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) para ajudar a proteger blocos de código contra o acesso não autorizado.</span><span class="sxs-lookup"><span data-stu-id="27f12-110">This functionality allows you to call methods such as [**IObjectContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) and [**IObjectContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) to help protect blocks of code from unauthorized access.</span></span> <span data-ttu-id="27f12-111">Você também pode usar o contexto de chamada de segurança para obter informações sobre os chamadores de um objeto.</span><span class="sxs-lookup"><span data-stu-id="27f12-111">You can also use the security call context to get information about an object's callers.</span></span>
-   <span data-ttu-id="27f12-112">Se você estiver criando um componente que será usado em um aplicativo distribuído sem usar a segurança baseada em função, a segurança será automaticamente verificada somente no nível do processo.</span><span class="sxs-lookup"><span data-stu-id="27f12-112">If you are designing a component that will be used in a distributed application without using role-based security, security is automatically checked only at the process level.</span></span> <span data-ttu-id="27f12-113">Permissões de acesso de processo determinam quem recebe acesso ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="27f12-113">Process access permissions determine who is given access to the application.</span></span> <span data-ttu-id="27f12-114">Se você precisar de um controle mais detalhado sobre as configurações de segurança no processo ou no nível da interface, use a funcionalidade de segurança programática fornecida pelo COM.</span><span class="sxs-lookup"><span data-stu-id="27f12-114">If you need finer grain control over security settings at the process or at the interface level, use the programmatic security functionality provided by COM.</span></span>
-   <span data-ttu-id="27f12-115">Se um componente que usa a segurança programática do COM+ for executado sem ser integrado a um aplicativo COM+, exceções serão lançadas.</span><span class="sxs-lookup"><span data-stu-id="27f12-115">If a component using COM+ programmatic security is run without being integrated into a COM+ application, exceptions will be thrown.</span></span> <span data-ttu-id="27f12-116">Portanto, se você quiser que esse componente seja integrado com êxito a um aplicativo que não faz parte do ambiente COM+, você deve lidar com todas as exceções adequadamente.</span><span class="sxs-lookup"><span data-stu-id="27f12-116">Therefore, if you want such a component to be successfully integrated into an application that is not part of the COM+ environment, you must handle all exceptions appropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27f12-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="27f12-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27f12-118">Projetando para disponibilidade</span><span class="sxs-lookup"><span data-stu-id="27f12-118">Designing for Availability</span></span>](designing-for-availability.md)
</dt> <dt>

[<span data-ttu-id="27f12-119">Projetando para implantação</span><span class="sxs-lookup"><span data-stu-id="27f12-119">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> <dt>

[<span data-ttu-id="27f12-120">Projetando para escalabilidade</span><span class="sxs-lookup"><span data-stu-id="27f12-120">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="27f12-121">Segurança de componente programática</span><span class="sxs-lookup"><span data-stu-id="27f12-121">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 



