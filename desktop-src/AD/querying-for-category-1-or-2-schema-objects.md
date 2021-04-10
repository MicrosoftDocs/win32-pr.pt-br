---
title: Consultando objetos de esquema de categoria 1 ou 2
description: O atributo systemFlags dos objetos attributeSchema e classSchema é um bitmask inteiro que contém sinalizadores que indicam qualidades de sistema adicionais do atributo ou da classe.
ms.assetid: 5cc8f296-df3e-4643-9694-543f069a2cc7
ms.tgt_platform: multiple
keywords:
- Consultando o AD de objetos de esquema de categoria 1 ou 2
- ANÚNCIO de objeto, consultando objetos de esquema de categoria 1 ou 2
- AD do esquema, consultando objetos de esquema de categoria 1 ou 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c67b57821cbebc80b3b6e93d158bbb8af8f7103
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104293888"
---
# <a name="querying-for-category-1-or-2-schema-objects"></a><span data-ttu-id="c2630-106">Consultando objetos de esquema de categoria 1 ou 2</span><span class="sxs-lookup"><span data-stu-id="c2630-106">Querying for Category 1 or 2 Schema Objects</span></span>

<span data-ttu-id="c2630-107">O atributo **systemFlags** dos objetos **attributeSchema** e **classSchema** é um bitmask inteiro que contém sinalizadores que indicam qualidades de sistema adicionais do atributo ou da classe.</span><span class="sxs-lookup"><span data-stu-id="c2630-107">The **systemFlags** attribute of **attributeSchema** and **classSchema** objects is an integer bitmask that contains flags that indicate additional system qualities of the attribute or class.</span></span> <span data-ttu-id="c2630-108">A [**enumeração \_ \_ enum do ADS SYSTEMFLAG**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) contém valores que correspondem aos bits que você pode definir no atributo **systemFlags** .</span><span class="sxs-lookup"><span data-stu-id="c2630-108">The [**ADS\_SYSTEMFLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) enumeration contains values that correspond to the bits you can set in the **systemFlags** attribute.</span></span> <span data-ttu-id="c2630-109">Há bits **systemFlags** adicionais que você não pode definir, como o bit 0x10, que indica se o atributo ou a classe é a categoria 1 ou a categoria 2.</span><span class="sxs-lookup"><span data-stu-id="c2630-109">There are additional **systemFlags** bits that you cannot set, such as the 0x10 bit which indicates whether the attribute or class is category 1 or category 2.</span></span> <span data-ttu-id="c2630-110">O bit 0x10 é definido para objetos Category 1, que são as classes e os atributos incluídos no esquema base incluído no sistema.</span><span class="sxs-lookup"><span data-stu-id="c2630-110">The 0x10 bit is set for category 1 objects, which are the classes and attributes included in the base schema included with the system.</span></span> <span data-ttu-id="c2630-111">O bit não está definido para atributos e classes da categoria 2, que são extensões para o esquema.</span><span class="sxs-lookup"><span data-stu-id="c2630-111">The bit is not set for category 2 attributes and classes, which are extensions to the schema.</span></span> <span data-ttu-id="c2630-112">Se não existir nenhuma propriedade **systemFlags** em um objeto **attributeSchema** ou **classSchema** , ela será a categoria 2.</span><span class="sxs-lookup"><span data-stu-id="c2630-112">If no **systemFlags** property exists on an **attributeSchema** or **classSchema** object, it is category 2.</span></span>

<span data-ttu-id="c2630-113">O **\_ bit de regra de correspondência LDAP \_ \_ \_ e** a regra de correspondência podem ser usados para pesquisar objetos que tenham o sinalizador 0x10 definido no atributo **systemFlags** .</span><span class="sxs-lookup"><span data-stu-id="c2630-113">The **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule can be used to search for objects that have the 0x10 flag set in the **systemFlags** attribute.</span></span> <span data-ttu-id="c2630-114">Para obter mais informações, consulte [sintaxe do filtro de pesquisa](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="c2630-114">For more information, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

## <a name="querying-for-category-1"></a><span data-ttu-id="c2630-115">Consultando a categoria 1</span><span class="sxs-lookup"><span data-stu-id="c2630-115">Querying for Category 1</span></span>

<span data-ttu-id="c2630-116">A cadeia de consulta a seguir procura atributos da categoria 1 (objetos **attributeSchema** com o bit 0x10 definido na propriedade **systemFlags** ).</span><span class="sxs-lookup"><span data-stu-id="c2630-116">The following query string searches for category 1 attributes (**attributeSchema** objects with the 0x10 bit set in the **systemFlags** property).</span></span>


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.803:=16) )
```



<span data-ttu-id="c2630-117">Lembre-se de que, no exemplo acima, a sintaxe de consulta LDAP requer valores decimais; Portanto, o valor hexadecimal do sinalizador deve ser convertido em decimal.</span><span class="sxs-lookup"><span data-stu-id="c2630-117">Be aware that, in the example above, the LDAP query syntax requires decimal values; therefore, the hex value of the flag must be converted to decimal.</span></span> <span data-ttu-id="c2630-118">Nesse caso, a categoria de 1 bit é 0x10, portanto, o valor do filtro deve ser especificado como 16.</span><span class="sxs-lookup"><span data-stu-id="c2630-118">In this case, category 1 bit is 0x10 so the filter value must be specified as 16.</span></span>

## <a name="querying-for-category-2"></a><span data-ttu-id="c2630-119">Consultando a categoria 2</span><span class="sxs-lookup"><span data-stu-id="c2630-119">Querying for Category 2</span></span>

<span data-ttu-id="c2630-120">A cadeia de consulta a seguir procura atributos da categoria 2 (objetos **attributeSchema** que não têm o bit 0x10 definido na propriedade **systemFlags** ).</span><span class="sxs-lookup"><span data-stu-id="c2630-120">The following query string searches for category 2 attributes (**attributeSchema** objects that do not have the 0x10 bit set in the **systemFlags** property).</span></span>


```C++
(&(objectCategory=attributeSchema)(!(systemFlags:1.2.840.113556.1.4.803:=16)))
```



<span data-ttu-id="c2630-121">Lembre-se de que essa consulta também retorna objetos **attributeSchema** que não têm uma propriedade **systemFlags** e, portanto, implicitamente não têm o sinalizador especificado definido.</span><span class="sxs-lookup"><span data-stu-id="c2630-121">Be aware that this query also returns **attributeSchema** objects that do not have a **systemFlags** property, and, therefore, implicitly do not have the specified flag set.</span></span>

 

 