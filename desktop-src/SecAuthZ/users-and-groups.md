---
description: Explica a definição de usuários e grupos na API do Gerenciador de autorização.
ms.assetid: 783be0b2-7894-4780-900d-98918f824a04
title: Usuários e Grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c40ee9234fa8d6259282855011cfc3fc008d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749962"
---
# <a name="users-and-groups"></a><span data-ttu-id="13028-103">Usuários e Grupos</span><span class="sxs-lookup"><span data-stu-id="13028-103">Users and Groups</span></span>

<span data-ttu-id="13028-104">No Gerenciador de autorização, os destinatários da política de autorização são representados pelos seguintes grupos:</span><span class="sxs-lookup"><span data-stu-id="13028-104">In Authorization Manager, recipients of authorization policy are represented by the following groups:</span></span>

-   <span data-ttu-id="13028-105">Usuários e grupos do Windows</span><span class="sxs-lookup"><span data-stu-id="13028-105">Windows Users and Groups</span></span>

    <span data-ttu-id="13028-106">Esses grupos incluem usuários, computadores e grupos internos para entidades de segurança.</span><span class="sxs-lookup"><span data-stu-id="13028-106">These groups include users, computers, and built-in groups for security principals.</span></span>

-   <span data-ttu-id="13028-107">Grupos de consulta LDAP</span><span class="sxs-lookup"><span data-stu-id="13028-107">LDAP Query Groups</span></span>

    <span data-ttu-id="13028-108">A associação nesses grupos é calculada dinamicamente conforme necessário nas consultas do protocolo LDAP.</span><span class="sxs-lookup"><span data-stu-id="13028-108">Membership in these groups is dynamically calculated as needed from Lightweight Directory Access Protocol (LDAP) queries.</span></span> <span data-ttu-id="13028-109">Um grupo de consulta LDAP é um tipo de grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="13028-109">An LDAP query group is a type of application group.</span></span>

-   <span data-ttu-id="13028-110">Grupos de aplicativos básicos</span><span class="sxs-lookup"><span data-stu-id="13028-110">Basic Application Groups</span></span>

    <span data-ttu-id="13028-111">Esses grupos consistem em grupos de consulta LDAP, usuários e grupos do Windows e outros grupos de aplicativos básicos.</span><span class="sxs-lookup"><span data-stu-id="13028-111">These groups consist of LDAP query groups, Windows users and groups, and other basic application groups.</span></span>

## <a name="windows-users-and-groups"></a><span data-ttu-id="13028-112">Usuários e grupos do Windows</span><span class="sxs-lookup"><span data-stu-id="13028-112">Windows Users and Groups</span></span>

<span data-ttu-id="13028-113">Esses são os mesmos usuários e grupos usados em todo o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="13028-113">These are the same as the users and groups used throughout the Windows operating system.</span></span>

## <a name="ldap-query-groups"></a><span data-ttu-id="13028-114">Grupos de consulta LDAP</span><span class="sxs-lookup"><span data-stu-id="13028-114">LDAP Query Groups</span></span>

<span data-ttu-id="13028-115">No Gerenciador de autorização, você pode usar consultas LDAP para corresponder os atributos do usuário com aqueles do objeto do usuário em Active Directory.</span><span class="sxs-lookup"><span data-stu-id="13028-115">In Authorization Manager, you can use LDAP queries to match the user's attributes with those of the user's object in Active Directory.</span></span>

<span data-ttu-id="13028-116">Por exemplo, a consulta a seguir localiza todos, exceto Andy.</span><span class="sxs-lookup"><span data-stu-id="13028-116">For example, the following query finds everyone except Andy.</span></span>


```C++
(&(objectCategory=person)(objectClass=user)(!cn=andy))
```



<span data-ttu-id="13028-117">A consulta a seguir localiza todos os membros do alias de alguém em www.fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="13028-117">The following query finds all members of the someone alias at www.fabrikam.com.</span></span>


```C++
(memberOf=CN=someone,OU=litwareinc,DC=Fabrikam,DC=com)
```



## <a name="basic-application-groups"></a><span data-ttu-id="13028-118">Grupos de aplicativos básicos</span><span class="sxs-lookup"><span data-stu-id="13028-118">Basic Application Groups</span></span>

<span data-ttu-id="13028-119">Na API do Gerenciador de autorização, um grupo de aplicativos é representado por um objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .</span><span class="sxs-lookup"><span data-stu-id="13028-119">In the Authorization Manager API, an application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span> <span data-ttu-id="13028-120">Um grupo de aplicativos básico é um tipo de grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="13028-120">A basic application group is a type of application group.</span></span>

<span data-ttu-id="13028-121">Para definir a associação básica do grupo de aplicativos, defina quem é um membro e defina quem não é um membro.</span><span class="sxs-lookup"><span data-stu-id="13028-121">To define basic application group membership, define who is a member and define who is not a member.</span></span> <span data-ttu-id="13028-122">Essas duas etapas são executadas da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="13028-122">Both of these steps are carried out in the same way.</span></span> <span data-ttu-id="13028-123">Especifique zero ou mais usuários e grupos do Windows, grupos de aplicativos básicos definidos anteriormente ou grupos de consulta LDAP.</span><span class="sxs-lookup"><span data-stu-id="13028-123">Specify zero or more Windows users and groups, previously defined basic application groups, or LDAP query groups.</span></span> <span data-ttu-id="13028-124">A associação do grupo de aplicativos básico é calculada removendo quaisquer não membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="13028-124">The membership of the basic application group is calculated by removing any nonmembers from the group.</span></span> <span data-ttu-id="13028-125">O Gerenciador de autorização faz isso automaticamente em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="13028-125">Authorization Manager does this automatically at run time.</span></span>

<span data-ttu-id="13028-126">A não-membro em um grupo de aplicativos básico tem precedência sobre a associação.</span><span class="sxs-lookup"><span data-stu-id="13028-126">Nonmembership in a basic application group takes precedence over membership.</span></span>

<span data-ttu-id="13028-127">Definições de associação circular não são permitidas; Eles resultam na seguinte mensagem de erro: "não é possível adicionar GroupName.</span><span class="sxs-lookup"><span data-stu-id="13028-127">Circular membership definitions are not allowed; they result in the following error message: "Cannot add GroupName.</span></span> <span data-ttu-id="13028-128">Ocorreu o seguinte problema: um loop foi detectado. "</span><span class="sxs-lookup"><span data-stu-id="13028-128">The following problem occurred: A loop has been detected."</span></span>

## <a name="related-topics"></a><span data-ttu-id="13028-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="13028-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13028-130">Definindo grupos de usuários em C++</span><span class="sxs-lookup"><span data-stu-id="13028-130">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)
</dt> </dl>

 

 



