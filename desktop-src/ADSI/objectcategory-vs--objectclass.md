---
title: objectCategory versus objectClass
description: Os atributos objectCategory e objectClass podem se referir a uma determinada classe de esquema de um objeto de diretório.
ms.assetid: 66dadedb-61e4-4184-9b87-0fff036a94d9
ms.tgt_platform: multiple
keywords:
- ADSI de objectCategory versus objectClass
- atributos ASI, pesquisando atributos objectCategory e objectClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbbb8c5fe737b7c81193a75cdae6b772db64e69c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004865"
---
# <a name="objectcategory-vs-objectclass"></a><span data-ttu-id="69525-105">objectCategory versus objectClass</span><span class="sxs-lookup"><span data-stu-id="69525-105">objectCategory vs. objectClass</span></span>

<span data-ttu-id="69525-106">Os atributos **objectCategory** e **objectClass** podem se referir a uma determinada classe de esquema de um objeto de diretório.</span><span class="sxs-lookup"><span data-stu-id="69525-106">Both the **objectCategory** and **objectClass** attributes can refer to a given schema class of a directory object.</span></span> <span data-ttu-id="69525-107">No entanto, há uma distinção importante na semântica entre os dois.</span><span class="sxs-lookup"><span data-stu-id="69525-107">However, there is an important distinction in semantics between the two.</span></span> <span data-ttu-id="69525-108">"objectClass = Joy" refere-se a esses objetos de diretório nos quais "Joy" representa qualquer classe na hierarquia de classes de objeto.</span><span class="sxs-lookup"><span data-stu-id="69525-108">"objectClass=joy" refers to such directory objects in which "joy" represents any class in the object class hierarchy.</span></span> <span data-ttu-id="69525-109">"objectCategory = Joy", por outro lado, refere-se aos objetos de diretório nos quais "Joy" identifica uma classe específica na hierarquia de classes de objeto.</span><span class="sxs-lookup"><span data-stu-id="69525-109">"objectCategory=joy", on the other hand, refers to those directory objects in which "joy" identifies a specific class in the object class hierarchy.</span></span>

<span data-ttu-id="69525-110">o **objectClass** pode assumir vários valores, enquanto **objectCategory** usa um único valor.</span><span class="sxs-lookup"><span data-stu-id="69525-110">**objectClass** can take multiple values whereas **objectCategory** takes a single value.</span></span> <span data-ttu-id="69525-111">Por isso, **objectCategory** é mais adequado para a correspondência de tipos de objetos em uma pesquisa de diretório.</span><span class="sxs-lookup"><span data-stu-id="69525-111">Because of this, **objectCategory** is better suited for type matching of objects in a directory search.</span></span> <span data-ttu-id="69525-112">A ADSI usa isso como o critério de correspondência padrão.</span><span class="sxs-lookup"><span data-stu-id="69525-112">ADSI uses this as the default matching criterion.</span></span> <span data-ttu-id="69525-113">Pesquisas usando um **objectClass** não são escalonáveis para bancos de dados grandes.</span><span class="sxs-lookup"><span data-stu-id="69525-113">Searches using one **objectClass** are not scalable to large databases.</span></span> <span data-ttu-id="69525-114">A ADSI dá suporte a sintaxes "(objectCategory = SomeDN)" e "(objectCategory = \_ \_ nome de exibição LDAP \_ de \_ classe)".</span><span class="sxs-lookup"><span data-stu-id="69525-114">ADSI supports "(objectCategory=SomeDN)" and "(objectCategory=Ldap\_Display\_Name\_of\_Class)" syntaxes.</span></span>

<span data-ttu-id="69525-115">A exceção a tudo isso é que o filtro de pesquisa LDAP "(objectClass = \* )" não especifica uma pesquisa na classe de objeto, mas meramente testa a presença dos objetos.</span><span class="sxs-lookup"><span data-stu-id="69525-115">The exception to all of this is that the LDAP search filter "(objectClass=\*)" does not specify a search on object class, but merely tests for the presence of the objects.</span></span>

 

 




