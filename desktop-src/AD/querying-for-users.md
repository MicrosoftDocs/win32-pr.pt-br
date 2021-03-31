---
title: Consultando usuários
description: Para consultar um usuário, a consulta deve conter a expressão de pesquisa \ 0034;( (usuário objectClass) (pessoa da objectCategory)) \ 0034;.
ms.assetid: a9f12de4-e1e2-41bb-b2cc-ff9c9fa1c39a
ms.tgt_platform: multiple
keywords:
- AD de usuários, consultando usuários
- Active Directory, usando, usuários, consultando usuários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39037ff805dab753aae066d1f6611432b28ea73c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640389"
---
# <a name="querying-for-users"></a><span data-ttu-id="76ed1-105">Consultando usuários</span><span class="sxs-lookup"><span data-stu-id="76ed1-105">Querying for Users</span></span>

<span data-ttu-id="76ed1-106">Para consultar um usuário, a consulta deve conter a expressão de pesquisa "(& (objectClass = user) (objectCategory = Person))".</span><span class="sxs-lookup"><span data-stu-id="76ed1-106">To query for a user, the query must contain the search expression "(&(objectClass=user)(objectCategory=person))".</span></span>

<span data-ttu-id="76ed1-107">Como a classe Computer é uma subclasse de User, uma consulta contendo somente (objectClass = user) retornará objetos User e Computer.</span><span class="sxs-lookup"><span data-stu-id="76ed1-107">Because the computer class is a subclass of user, a query containing only (objectClass=user) would return user objects and computer objects.</span></span> <span data-ttu-id="76ed1-108">Além disso, a categoria de objeto do objeto de usuário é Person (não User); Portanto, a expressão (objectCategory = user) não retorna nenhum usuário.</span><span class="sxs-lookup"><span data-stu-id="76ed1-108">Also, the object category of the user object is person (not user); therefore, the expression (objectCategory=user) does not return any users.</span></span> <span data-ttu-id="76ed1-109">Se você usar a expressão (objectCategory = Person), a consulta retornará objetos de usuário e objetos de contato.</span><span class="sxs-lookup"><span data-stu-id="76ed1-109">If you use the expression (objectCategory=person), the query returns user objects and contact objects.</span></span>

<span data-ttu-id="76ed1-110">Os usuários podem ser colocados em qualquer contêiner ou unidade organizacional em um domínio, bem como a raiz do domínio.</span><span class="sxs-lookup"><span data-stu-id="76ed1-110">Users can be placed in any container or organizational unit in a domain as well as the root of the domain.</span></span> <span data-ttu-id="76ed1-111">Isso significa que os usuários podem estar em vários locais na hierarquia de diretórios.</span><span class="sxs-lookup"><span data-stu-id="76ed1-111">This means that users can be in numerous locations in the directory hierarchy.</span></span> <span data-ttu-id="76ed1-112">Você pode executar uma pesquisa profunda para "(objectCategory = user)" para localizar todos os usuários em um contêiner, unidade organizacional, domínio, árvore de domínio ou floresta — dependendo do objeto que o ponteiro do [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) que você está usando está vinculado.</span><span class="sxs-lookup"><span data-stu-id="76ed1-112">You can perform a deep search for "(objectCategory=user)" to find all users in a container, organizational unit, domain, domain tree, or forest—depending on the object that the [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer you are using is bound to.</span></span>

 

 