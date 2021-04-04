---
title: Determinando um tipo de atributo
description: O atributo systemFlags de um objeto attributeSchema contém um conjunto de sinalizadores que indicam várias qualidades do objeto de atributo, como, por exemplo, se o atributo é construído ou não replicado.
ms.assetid: 58f44ea4-ecbd-4650-b366-37b05a975c68
ms.tgt_platform: multiple
keywords:
- Determinando um tipo de atributo AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64b4d8b0ae5d6cbac38c9c44ed8e4a7aa5d5f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007326"
---
# <a name="determining-an-attribute-type"></a><span data-ttu-id="8e82e-104">Determinando um tipo de atributo</span><span class="sxs-lookup"><span data-stu-id="8e82e-104">Determining an Attribute Type</span></span>

<span data-ttu-id="8e82e-105">O atributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) de um objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) contém um conjunto de sinalizadores que indicam várias qualidades do objeto de atributo, como, por exemplo, se o atributo é construído ou não replicado.</span><span class="sxs-lookup"><span data-stu-id="8e82e-105">The [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute of an [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object contains a set of flags that indicate various qualities of the attribute object, such as whether the attribute is constructed or non-replicated.</span></span> <span data-ttu-id="8e82e-106">A tabela a seguir lista os sinalizadores do atributo **systemFlags** que afetam o tipo de armazenamento do atributo.</span><span class="sxs-lookup"><span data-stu-id="8e82e-106">The following table lists the flags of the **systemFlags** attribute that affect the storage type of the attribute.</span></span> 

| <span data-ttu-id="8e82e-107">Valor do sinalizador</span><span class="sxs-lookup"><span data-stu-id="8e82e-107">Flag value</span></span> | <span data-ttu-id="8e82e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e82e-108">Description</span></span>                                                                                                          |
|------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e82e-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8e82e-109">0x00000001</span></span> | <span data-ttu-id="8e82e-110">Se esse sinalizador estiver presente no atributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , o atributo não será replicado.</span><span class="sxs-lookup"><span data-stu-id="8e82e-110">If this flag is present in the [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute, the attribute is not replicated.</span></span> |
| <span data-ttu-id="8e82e-111">0x00000004</span><span class="sxs-lookup"><span data-stu-id="8e82e-111">0x00000004</span></span> | <span data-ttu-id="8e82e-112">Se esse sinalizador estiver presente no atributo [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) , o atributo será construído.</span><span class="sxs-lookup"><span data-stu-id="8e82e-112">If this flag is present in the [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute, the attribute is constructed.</span></span>    |



 

<span data-ttu-id="8e82e-113">É possível construir uma cadeia de caracteres de consulta que possa ser usada para consultar atributos construídos ou não replicados.</span><span class="sxs-lookup"><span data-stu-id="8e82e-113">It is possible to construct a query string that can be used to query for constructed or non-replicated attributes.</span></span> <span data-ttu-id="8e82e-114">Por exemplo, a cadeia de caracteres de consulta a seguir localiza todos os objetos [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) não replicados.</span><span class="sxs-lookup"><span data-stu-id="8e82e-114">For example, the following query string finds all non-replicated [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) objects.</span></span> <span data-ttu-id="8e82e-115">Lembre-se de que a cadeia de caracteres de consulta requer o equivalente Decimal do valor, não o equivalente hexadecimal do valor.</span><span class="sxs-lookup"><span data-stu-id="8e82e-115">Be aware that the query string requires the decimal equivalent of the value, not the hexadecimal equivalent of the value.</span></span> <span data-ttu-id="8e82e-116">Para obter mais informações sobre o OID de regra de correspondência usado por essa cadeia de caracteres de consulta, consulte [como especificar valores de comparação](how-to-specify-comparison-values.md).</span><span class="sxs-lookup"><span data-stu-id="8e82e-116">For more information about the matching rule OID used by this query string, see [How to Specify Comparison Values](how-to-specify-comparison-values.md).</span></span>


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.804:=1))
```



<span data-ttu-id="8e82e-117">O atributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) do objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de cada atributo define se um atributo é indexado; um atributo indexado tem um valor de 1, um atributo não indexado tem um valor de 0.</span><span class="sxs-lookup"><span data-stu-id="8e82e-117">The [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute of each attribute's [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object defines whether an attribute is indexed; an indexed attribute has a value of 1, a non-indexed attribute has a value of 0.</span></span> <span data-ttu-id="8e82e-118">Por exemplo, a cadeia de caracteres de consulta a seguir localiza os objetos **attributeSchema** que representam os atributos indexados.</span><span class="sxs-lookup"><span data-stu-id="8e82e-118">For example, the following query string finds the **attributeSchema** objects representing indexed attributes.</span></span>


```C++
(&(objectCategory=attributeSchema)(searchFlags=1))
```



<span data-ttu-id="8e82e-119">O atributo [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) do objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) de cada atributo define se um atributo é replicado para o catálogo global.</span><span class="sxs-lookup"><span data-stu-id="8e82e-119">The [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) attribute of each attribute's [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object defines whether an attribute is replicated to the global catalog.</span></span> <span data-ttu-id="8e82e-120">Esse atributo tem um valor de **true** se o atributo for um membro do catálogo global ou **false** se os atributos não estiverem no catálogo global.</span><span class="sxs-lookup"><span data-stu-id="8e82e-120">This attribute has a value of **TRUE** if the attribute is a member of the global catalog or **FALSE** if the attributes is not in the global catalog.</span></span> <span data-ttu-id="8e82e-121">Por exemplo, a cadeia de caracteres de consulta a seguir pesquisa os objetos **attributeSchema** que são replicados para o catálogo global.</span><span class="sxs-lookup"><span data-stu-id="8e82e-121">For example, the following query string searches the **attributeSchema** objects that are replicated to the global catalog.</span></span>


```C++
(&(objectCategory=attributeSchema)(isMemberOfPartialAttributeSet=TRUE))
```



 

 