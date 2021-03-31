---
title: Localizando objetos por nome
description: A maioria dos objetos no Active Directory Domain Services usar a propriedade CN como seu atributo de nomenclatura.
ms.assetid: c5df7403-23bc-440e-8cd6-215ab8037aed
ms.tgt_platform: multiple
keywords:
- Active Directory, usando, pesquisando, por nome
- ANÚNCIO de objeto, pesquisando por nome
- Localizando objetos por nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914faa443402a1d20698aabaf0bf4a112279a322
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634941"
---
# <a name="finding-objects-by-name"></a><span data-ttu-id="6c85a-106">Localizando objetos por nome</span><span class="sxs-lookup"><span data-stu-id="6c85a-106">Finding Objects by Name</span></span>

<span data-ttu-id="6c85a-107">A maioria dos objetos no Active Directory Domain Services usar a propriedade **CN** como seu atributo de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="6c85a-107">Most objects in Active Directory Domain Services use the **cn** property as their naming attribute.</span></span> <span data-ttu-id="6c85a-108">Alguns objetos, no entanto, usam um atributo de nomenclatura diferente de **CN**.</span><span class="sxs-lookup"><span data-stu-id="6c85a-108">Some objects, however, use a naming attribute other than **cn**.</span></span> <span data-ttu-id="6c85a-109">Por exemplo, um controlador de domínio usa a propriedade **domainDns** para o atributo de nomenclatura e uma unidade organizacional usa a propriedade **OrganizationalUnit** para o atributo de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="6c85a-109">For example, a domain controller uses the **domainDNS** property for the naming attribute and an organizational unit uses the **organizationalUnit** property for the naming attribute.</span></span> <span data-ttu-id="6c85a-110">Para evitar a utilização de um atributo de nomenclatura diferente para diferentes tipos de objeto, a propriedade **Name** , que contém o nome distinto relativo do objeto, deve ser usada para pesquisar objetos pelo nome.</span><span class="sxs-lookup"><span data-stu-id="6c85a-110">To avoid having to use a different naming attribute for different object types, the **name** property, which contains the relative distinguished name of the object, should be used to search for objects by name.</span></span>

## <a name="examples"></a><span data-ttu-id="6c85a-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6c85a-111">Examples</span></span>

<span data-ttu-id="6c85a-112">Os exemplos de código a seguir mostram diferentes cadeias de caracteres de consulta que podem ser usadas para localizar objetos por nome.</span><span class="sxs-lookup"><span data-stu-id="6c85a-112">The following code examples show different query strings that can be used to find objects by name.</span></span>

<span data-ttu-id="6c85a-113">A cadeia de caracteres de consulta a seguir localiza todos os objetos com um nome que começa com "Jeff".</span><span class="sxs-lookup"><span data-stu-id="6c85a-113">The following query string finds all objects with a name that begins with "Jeff".</span></span>


```C++
(name=Jeff*)
```



<span data-ttu-id="6c85a-114">A cadeia de caracteres de consulta a seguir localiza todos os objetos de computador com um nome que começa com "concedido" ou "Corp".</span><span class="sxs-lookup"><span data-stu-id="6c85a-114">The following query string finds all computer objects with a name that begins with "leased" or "corp".</span></span>


```C++
(&(objectCategory=computer)(|(name=leased*)(name=corp*)))
```



<span data-ttu-id="6c85a-115">A cadeia de caracteres de consulta a seguir localiza todos os usuários e com um nome que começa com "Karen" ou "Jeff".</span><span class="sxs-lookup"><span data-stu-id="6c85a-115">The following query string finds all users and with a name that begins with "Karen" or "Jeff".</span></span>


```C++
(&(&(objectClass=user)(objectCategory=person))(|(name=Karen*)(name=Jeff*)))
```



 

 




