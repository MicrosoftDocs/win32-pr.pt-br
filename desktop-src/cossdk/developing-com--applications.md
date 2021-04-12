---
description: Ao desenvolver aplicativos COM+, as principais tarefas incluem a criação de componentes COM para encapsular a lógica do aplicativo e integrar esses componentes em um aplicativo COM+, criar o aplicativo COM+ e administrar o aplicativo por meio de implantação e manutenção.
ms.assetid: 8c6ec901-1eeb-46b0-8a3a-26d8eff99f6d
title: Desenvolvendo aplicativos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee6495b7d8f7b2cc059b113f4250042cfd59b99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500848"
---
# <a name="developing-com-applications"></a><span data-ttu-id="a9053-103">Desenvolvendo aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="a9053-103">Developing COM+ Applications</span></span>

<span data-ttu-id="a9053-104">Ao desenvolver aplicativos COM+, as principais tarefas incluem a criação de componentes COM para encapsular a lógica do aplicativo e integrar esses componentes em um aplicativo COM+, criar o aplicativo COM+ e administrar o aplicativo por meio de implantação e manutenção.</span><span class="sxs-lookup"><span data-stu-id="a9053-104">When developing COM+ applications, the principal tasks include designing COM components to encapsulate application logic and integrating these components into a COM+ application, creating the COM+ application, and administering the application through deployment and maintenance.</span></span>

## <a name="designing-com-components"></a><span data-ttu-id="a9053-105">Criando componentes COM</span><span class="sxs-lookup"><span data-stu-id="a9053-105">Designing COM Components</span></span>

<span data-ttu-id="a9053-106">As etapas a seguir descrevem um procedimento geral para um bom design de componente:</span><span class="sxs-lookup"><span data-stu-id="a9053-106">The following steps describe a general procedure for good component design:</span></span>

1.  <span data-ttu-id="a9053-107">Defina as classes COM e as classes de implementação.</span><span class="sxs-lookup"><span data-stu-id="a9053-107">Define the COM classes and implementation classes.</span></span>
2.  <span data-ttu-id="a9053-108">Agrupe as classes em componentes.</span><span class="sxs-lookup"><span data-stu-id="a9053-108">Group the classes into components.</span></span>
3.  <span data-ttu-id="a9053-109">Selecione o conjunto de serviços COM+ para seu componente, mesmo se você não especificar todos eles ao desenvolver o componente.</span><span class="sxs-lookup"><span data-stu-id="a9053-109">Select the set of COM+ services for your component, even if you do not specify all of them when developing the component.</span></span> <span data-ttu-id="a9053-110">Esses serviços podem ser mais tarde especificados usando a ferramenta administrativa serviços de componentes ou o modelo de objeto de administração COM+ (consulte [automatizando a administração do com+](automating-com--administration.md) para obter mais informações sobre o modelo de objeto de administração com+).</span><span class="sxs-lookup"><span data-stu-id="a9053-110">These services can later be specified using the Component Services administrative tool or the COM+ administration object model (See [Automating COM+ Administration](automating-com--administration.md) for more information about the COM+ administration object model.)</span></span>

## <a name="creating-the-com-application"></a><span data-ttu-id="a9053-111">Criando o aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="a9053-111">Creating the COM+ Application</span></span>

<span data-ttu-id="a9053-112">Depois de criar os componentes COM, o desenvolvedor integra os componentes em um aplicativo COM+ e configura o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a9053-112">After designing the COM components, the developer integrates the components into a COM+ application and configures the application.</span></span> <span data-ttu-id="a9053-113">As etapas a seguir descrevem o processo:</span><span class="sxs-lookup"><span data-stu-id="a9053-113">The following steps describe the process:</span></span>

1.  <span data-ttu-id="a9053-114">Integre os componentes em um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="a9053-114">Integrate the components into a COM+ application.</span></span> <span data-ttu-id="a9053-115">Você pode integrar os componentes em um aplicativo existente do COM+ ou criar um novo aplicativo (vazio) para os componentes.</span><span class="sxs-lookup"><span data-stu-id="a9053-115">You can integrate the components into an existing COM+ application or create a new (empty) application for the components.</span></span> <span data-ttu-id="a9053-116">(Consulte [criando aplicativos com+](creating-com--applications.md).)</span><span class="sxs-lookup"><span data-stu-id="a9053-116">(See [Creating COM+ Applications](creating-com--applications.md).)</span></span>
2.  <span data-ttu-id="a9053-117">Especifique o conjunto correto de atributos para cada uma das classes (se houver, e se não for especificado na ferramenta de desenvolvimento).</span><span class="sxs-lookup"><span data-stu-id="a9053-117">Specify the correct set of attributes for each of the classes (if any, and if not specified in the development tool).</span></span> <span data-ttu-id="a9053-118">Esses atributos expressam as dependências dos componentes em qualquer serviço COM+ em que sua implementação possa depender (por exemplo, transações, componentes enfileirados, segurança, pool de objetos e ativação Just-in-time).</span><span class="sxs-lookup"><span data-stu-id="a9053-118">These attributes express the components dependencies on any COM+ services its implementation might rely on (for example, transactions, Queued Components, Security, Object Pooling, and Just-in-Time Activation).</span></span>
3.  <span data-ttu-id="a9053-119">Configure a estrutura de segurança (funções e atribuição de funções para classes, interfaces e métodos).</span><span class="sxs-lookup"><span data-stu-id="a9053-119">Set up the security framework (roles and assignment of roles to classes, interfaces, and methods).</span></span>
4.  <span data-ttu-id="a9053-120">Configure atributos específicos do ambiente em classes e aplicativos (o tamanho padrão do pool de objetos, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="a9053-120">Configure environment-specific attributes on classes and applications (the default object pool size, for example).</span></span> <span data-ttu-id="a9053-121">Esses atributos específicos do ambiente podem ser posteriormente definidos (ou modificados) pelo administrador do sistema.</span><span class="sxs-lookup"><span data-stu-id="a9053-121">These environment-specific attributes can later be set (or modified) by the system administrator.</span></span>
5.  <span data-ttu-id="a9053-122">Exporte o aplicativo para redistribuição e implantação.</span><span class="sxs-lookup"><span data-stu-id="a9053-122">Export the application for redistribution and deployment.</span></span>

<span data-ttu-id="a9053-123">Para obter informações mais detalhadas sobre as etapas de criação de aplicativos distribuídos, consulte [projetando aplicativos com+](designing-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="a9053-123">For more detailed information on the steps in designing distributed applications, see [Designing COM+ Applications](designing-com--applications.md).</span></span>

## <a name="administering-com-applications"></a><span data-ttu-id="a9053-124">Administrando aplicativos COM+</span><span class="sxs-lookup"><span data-stu-id="a9053-124">Administering COM+ Applications</span></span>

<span data-ttu-id="a9053-125">Normalmente, um desenvolvedor fornece um aplicativo COM+ parcialmente configurado para o administrador do sistema.</span><span class="sxs-lookup"><span data-stu-id="a9053-125">Typically, a developer delivers a partially configured COM+ application to the system administrator.</span></span> <span data-ttu-id="a9053-126">O administrador pode personalizar o aplicativo para um ou mais ambientes específicos (por exemplo, adicionando contas de usuário em funções e nomes de servidor em um cluster de aplicativo).</span><span class="sxs-lookup"><span data-stu-id="a9053-126">The administrator can then customize the application for one or more specific environments (for example, by adding user accounts in roles and server names in an application cluster).</span></span> <span data-ttu-id="a9053-127">As tarefas do administrador incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a9053-127">The administrator's tasks include the following:</span></span>

-   <span data-ttu-id="a9053-128">Instalar o aplicativo COM+ parcialmente configurado em um computador administrativo.</span><span class="sxs-lookup"><span data-stu-id="a9053-128">Installing the partially configured COM+ application on an administrative computer.</span></span>
-   <span data-ttu-id="a9053-129">Fornecendo atributos específicos do ambiente, como membros da função e o tamanho do pool de objetos.</span><span class="sxs-lookup"><span data-stu-id="a9053-129">Providing environment-specific attributes, such as role members and object pool size.</span></span>
-   <span data-ttu-id="a9053-130">Exportando novamente o aplicativo COM+ totalmente configurado.</span><span class="sxs-lookup"><span data-stu-id="a9053-130">Re-exporting the fully configured COM+ application.</span></span>
-   <span data-ttu-id="a9053-131">Criar um proxy de aplicativo (se o aplicativo for ser acessado remotamente).</span><span class="sxs-lookup"><span data-stu-id="a9053-131">Creating an application proxy (if the application is to be accessed remotely).</span></span>

<span data-ttu-id="a9053-132">Depois que um aplicativo é totalmente configurado para um ambiente específico, o administrador pode implantá-lo em computadores de teste ou produção.</span><span class="sxs-lookup"><span data-stu-id="a9053-132">After an application is fully configured for a specific environment, the administrator can then deploy it on test or production machines.</span></span> <span data-ttu-id="a9053-133">Isso envolve a instalação do aplicativo COM+ totalmente configurado em um ou mais computadores.</span><span class="sxs-lookup"><span data-stu-id="a9053-133">This involves installing the fully configured COM+ application on one or more computers.</span></span>

<span data-ttu-id="a9053-134">Para obter informações detalhadas sobre os procedimentos de administração do COM+, consulte a ferramenta administrativa serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="a9053-134">For detailed information on COM+ administration procedures, see the Component Services administrative tool.</span></span>

 

 



