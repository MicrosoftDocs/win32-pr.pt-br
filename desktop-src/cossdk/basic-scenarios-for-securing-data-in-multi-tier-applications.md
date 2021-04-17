---
description: Este tópico apresenta alguns cenários de bloco de construção, ilustrando os critérios discutidos em decidindo onde impor a segurança.
ms.assetid: e9820e53-8891-4bff-a333-00ad2dbb03a4
title: Cenários básicos para proteger dados em aplicativos de várias camadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7929bcfeba96b43b7ec91513b42ffb7f46266613
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782696"
---
# <a name="basic-scenarios-for-securing-data-in-multi-tier-applications"></a><span data-ttu-id="3109f-103">Cenários básicos para proteger dados em aplicativos de várias camadas</span><span class="sxs-lookup"><span data-stu-id="3109f-103">Basic Scenarios for Securing Data in Multi-Tier Applications</span></span>

<span data-ttu-id="3109f-104">Este tópico apresenta alguns cenários de bloco de construção, ilustrando os critérios discutidos em [decidindo onde impor a segurança](deciding-where-to-enforce-security.md).</span><span class="sxs-lookup"><span data-stu-id="3109f-104">This topic presents a few building-block scenarios, illustrating the criteria discussed in [Deciding Where to Enforce Security](deciding-where-to-enforce-security.md).</span></span>

## <a name="trusted-server-scenario"></a><span data-ttu-id="3109f-105">Cenário de servidor confiável</span><span class="sxs-lookup"><span data-stu-id="3109f-105">Trusted Server Scenario</span></span>

-   <span data-ttu-id="3109f-106">O banco de dados confia totalmente no aplicativo COM+ para autenticar e autorizar os usuários finais a acessar os dados no banco de dado.</span><span class="sxs-lookup"><span data-stu-id="3109f-106">The database fully trusts the COM+ application to authenticate and authorize end users to access data in the database.</span></span>
-   <span data-ttu-id="3109f-107">Preferivelmente, o banco de dados é protegido contra qualquer acesso, exceto pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3109f-107">Preferably, the database is secured against any access except through the application.</span></span>
-   <span data-ttu-id="3109f-108">O aplicativo COM+ usa a segurança baseada em função para autorizar usuários.</span><span class="sxs-lookup"><span data-stu-id="3109f-108">The COM+ application uses role-based security to authorize users.</span></span>
-   <span data-ttu-id="3109f-109">As conexões são abertas sob a identidade do aplicativo COM+ e são totalmente pooling.</span><span class="sxs-lookup"><span data-stu-id="3109f-109">Connections are opened under the COM+ application's identity and are fully poolable.</span></span>
-   <span data-ttu-id="3109f-110">A auditoria e o registro em log podem ser feitos pelo aplicativo COM+, ou essas informações podem ser passadas para o banco de dados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3109f-110">Auditing and logging can be done by the COM+ application, or this information can be passed into the database by the application.</span></span>

<span data-ttu-id="3109f-111">Esse cenário funciona melhor para dados que podem ser acessados por categorias previsíveis de usuários que podem ser encapsuladas em funções.</span><span class="sxs-lookup"><span data-stu-id="3109f-111">This scenario works best for data that can be accessed by predictable categories of users that can be encapsulated in roles.</span></span> <span data-ttu-id="3109f-112">Por exemplo, somente "gerentes", "informadores" e "contadores" têm permissão para acessar contas.</span><span class="sxs-lookup"><span data-stu-id="3109f-112">For example, only "Managers," "Tellers," and "Accountants" have permission to access accounts.</span></span> <span data-ttu-id="3109f-113">A lógica de negócios do que precisamente cada um está habilitado é imposta na camada intermediária.</span><span class="sxs-lookup"><span data-stu-id="3109f-113">The business logic of what precisely each is enabled to do is enforced in the middle tier.</span></span>

## <a name="impersonation-scenario"></a><span data-ttu-id="3109f-114">Cenário de representação</span><span class="sxs-lookup"><span data-stu-id="3109f-114">Impersonation Scenario</span></span>

-   <span data-ttu-id="3109f-115">O banco de dados faz sua própria autenticação e autorização de usuários finais para ajudar a limitar o acesso a dados no banco de dado.</span><span class="sxs-lookup"><span data-stu-id="3109f-115">The database does its own authentication and authorization of end users to help limit access to data in the database.</span></span>
-   <span data-ttu-id="3109f-116">O aplicativo COM+ representa clientes sempre que ele está acessando o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3109f-116">The COM+ application impersonates clients whenever it is accessing the database.</span></span>
-   <span data-ttu-id="3109f-117">As conexões são feitas em uma base por chamada e não podem ser reutilizadas.</span><span class="sxs-lookup"><span data-stu-id="3109f-117">Connections are made on a per-call basis and can't be reused.</span></span>

<span data-ttu-id="3109f-118">Esse cenário funciona melhor para dados que estão fortemente ligados a classes muito pequenas de usuários.</span><span class="sxs-lookup"><span data-stu-id="3109f-118">This scenario works best for data that is closely bound to very small classes of users.</span></span> <span data-ttu-id="3109f-119">Por exemplo, cada funcionário pode acessar apenas seu próprio arquivo de equipe, e cada gerente pode acessar somente os arquivos de equipe de seus relatórios.</span><span class="sxs-lookup"><span data-stu-id="3109f-119">For example, each employee can access only his own personnel file, and each manager can access only the personnel files of her reports.</span></span>

## <a name="hybrid-scenario"></a><span data-ttu-id="3109f-120"> Cenário Híbrido</span><span class="sxs-lookup"><span data-stu-id="3109f-120">Hybrid Scenario</span></span>

<span data-ttu-id="3109f-121">Uma combinação dos dois cenários anteriores, em que a representação é usada somente quando necessário.</span><span class="sxs-lookup"><span data-stu-id="3109f-121">A combination of the preceding two scenarios, where impersonation is used only when it is needed.</span></span>

<span data-ttu-id="3109f-122">Esse cenário funciona melhor em situações em que você tem relações de dados de usuário híbridos.</span><span class="sxs-lookup"><span data-stu-id="3109f-122">This scenario works best in situations where you have hybrid user-data relationships.</span></span> <span data-ttu-id="3109f-123">Por exemplo, você tem "gerentes", "Digars", "contadores" e milhares de clientes Web individuais que podem acessar apenas suas próprias contas.</span><span class="sxs-lookup"><span data-stu-id="3109f-123">For example, you have "Managers," "Tellers," "Accountants," and thousands of individual Web clients who can access just their own accounts.</span></span> <span data-ttu-id="3109f-124">Você pode separar caminhos lógicos por meio do aplicativo, potencialmente com componentes separados, para lidar com a última classe de usuários, principalmente onde as suposições de desempenho para esses usuários são diferentes.</span><span class="sxs-lookup"><span data-stu-id="3109f-124">You can separate logic paths through the application, potentially with separate components, to handle the latter class of users, particularly where performance assumptions for those users are different.</span></span>

## <a name="trusted-scenario-using-microsoft-sql-server-roles"></a><span data-ttu-id="3109f-125">Cenário confiável usando funções de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="3109f-125">Trusted Scenario Using Microsoft SQL Server Roles</span></span>

-   <span data-ttu-id="3109f-126">Microsoft SQL Server 7,0 e posterior podem autorizar o acesso a linhas específicas usando funções, mas confia no aplicativo COM+ para autenticar e autorizar usuários e mapeá-los para as funções corretas no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3109f-126">Microsoft SQL Server 7.0 and later can authorize access to specific rows using roles but trusts the COM+ application to authenticate and authorize users and to map them to the correct roles in the database.</span></span>
-   <span data-ttu-id="3109f-127">O aplicativo COM+ autoriza os usuários usando a segurança baseada em função e as funções de aplicativo correspondem bem às funções de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3109f-127">The COM+ application authorizes users using role-based security, and the application roles correspond well to database roles.</span></span>
-   <span data-ttu-id="3109f-128">As conexões podem ser abertas que são específicas para uma função de banco de dados específica.</span><span class="sxs-lookup"><span data-stu-id="3109f-128">Connections can be opened that are specific to a particular database role.</span></span> <span data-ttu-id="3109f-129">Essas conexões podem ser reutilizadas se forem mantidas por objetos em pool nos aplicativos COM+.</span><span class="sxs-lookup"><span data-stu-id="3109f-129">These connections can be reused if they are held by pooled objects in the COM+ applications.</span></span> <span data-ttu-id="3109f-130">Para obter detalhes sobre como fazer isso, consulte [pooling de objetos com+](com--object-pooling.md).</span><span class="sxs-lookup"><span data-stu-id="3109f-130">For details on how to do this, see [COM+ Object Pooling](com--object-pooling.md).</span></span>
-   <span data-ttu-id="3109f-131">A auditoria e o registro em log podem ser feitos pelo aplicativo COM+, ou essas informações podem ser passadas para o banco de dados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3109f-131">Auditing and logging can be done by the COM+ application, or this information can be passed in to the database by the application.</span></span>

<span data-ttu-id="3109f-132">Esse cenário funciona melhor para geralmente os mesmos tipos de usuários e dados que no primeiro cenário de servidor confiável, pois o aplicativo COM+ ainda é amplamente confiável para lidar com a autorização corretamente.</span><span class="sxs-lookup"><span data-stu-id="3109f-132">This scenario works best for generally the same kinds of users and data as in the first trusted server scenario because the COM+ application is still being largely trusted to handle authorization correctly.</span></span> <span data-ttu-id="3109f-133">No entanto, ele ajuda a proteger o banco de dados contra acesso não autorizado e, ao mesmo tempo, permite o acesso potencialmente de várias fontes fora do aplicativo COM+, sem incorrer no dimensionamento e nas penalidades de desempenho presentes com o cenário de representação.</span><span class="sxs-lookup"><span data-stu-id="3109f-133">However, it does help protect the database against unauthorized access while allowing access potentially from multiple sources outside the COM+ application, without incurring the scaling and performance penalties present with the impersonation scenario.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3109f-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3109f-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3109f-135">Decidindo onde impor a segurança</span><span class="sxs-lookup"><span data-stu-id="3109f-135">Deciding Where to Enforce Security</span></span>](deciding-where-to-enforce-security.md)
</dt> <dt>

[<span data-ttu-id="3109f-136">Segurança de aplicativos de várias camadas</span><span class="sxs-lookup"><span data-stu-id="3109f-136">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> </dl>

 

 



