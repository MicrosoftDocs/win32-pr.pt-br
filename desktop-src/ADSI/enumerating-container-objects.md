---
title: Enumerando objetos de contêiner
description: Por convenção, todos os itens em uma enumeração em ADSI devem ser do mesmo tipo de dados de automação. Por exemplo, uma enumeração não deve retornar alguns itens como uma variante do tipo VT \_ i4 e outros como uma variante do tipo VT \_ BSTR.
ms.assetid: 155caa67-05db-432b-b813-0d891a502301
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5514596b02521fa869ffd7c712dcac2cacb40192
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754418"
---
# <a name="enumerating-container-objects"></a><span data-ttu-id="c8015-104">Enumerando objetos de contêiner</span><span class="sxs-lookup"><span data-stu-id="c8015-104">Enumerating Container Objects</span></span>

<span data-ttu-id="c8015-105">Por convenção, todos os itens em uma enumeração em ADSI devem ser do mesmo tipo de dados de automação.</span><span class="sxs-lookup"><span data-stu-id="c8015-105">By convention, all items in an enumeration in ADSI must be of the same Automation data type.</span></span> <span data-ttu-id="c8015-106">Por exemplo, uma enumeração não deve retornar alguns itens como uma **variante** do tipo **VT \_ i4** e outros como uma **variante** do tipo **VT \_ BSTR**.</span><span class="sxs-lookup"><span data-stu-id="c8015-106">For example, an enumeration should not return some items as a **VARIANT** of type **VT\_I4** and others as a **VARIANT** of type **VT\_BSTR**.</span></span>

<span data-ttu-id="c8015-107">Para enumerar uma lista de itens que um objeto mantém, um cliente solicita a criação de um objeto de enumeração para o tipo específico de informações que estão sendo listadas.</span><span class="sxs-lookup"><span data-stu-id="c8015-107">To enumerate a list of items that an object maintains, a client requests the creation of an enumeration object for the specific type of information being listed.</span></span> <span data-ttu-id="c8015-108">No ADSI, o cliente pode listar os objetos em objetos de namespace, objetos de contêiner genéricos, objetos de coleção, objetos de membro ou objetos de esquema.</span><span class="sxs-lookup"><span data-stu-id="c8015-108">In ADSI, the client may list the objects in namespace objects, generic container objects, collection objects, member objects, or schema objects.</span></span> <span data-ttu-id="c8015-109">A ADSI fornece um filtro que pode ser definido e modificado para limitar as correspondências em qualquer enumeração, por meio da propriedade [**IADsContainer. Filter**](iadscontainer-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="c8015-109">ADSI provides a filter that can be set and modified to limit the matches in any enumeration though the [**IADsContainer.Filter**](iadscontainer-property-methods.md) property.</span></span> <span data-ttu-id="c8015-110">Exemplos de implementações de objetos enumeradores podem ser encontrados no código do componente do provedor de exemplo para os seguintes objetos de contêiner do ADs.</span><span class="sxs-lookup"><span data-stu-id="c8015-110">Examples of implementations of enumerator objects can be found in the example provider component code for the following ADs container objects.</span></span>



| <span data-ttu-id="c8015-111">Tipo de objeto</span><span class="sxs-lookup"><span data-stu-id="c8015-111">Object type</span></span>         | <span data-ttu-id="c8015-112">code</span><span class="sxs-lookup"><span data-stu-id="c8015-112">code</span></span>         |
|---------------------|--------------|
| <span data-ttu-id="c8015-113">Contêiner genérico</span><span class="sxs-lookup"><span data-stu-id="c8015-113">Generic Container</span></span>   | <span data-ttu-id="c8015-114">cenumobj. cpp</span><span class="sxs-lookup"><span data-stu-id="c8015-114">cenumobj.cpp</span></span> |
| <span data-ttu-id="c8015-115">Contêiner de namespace</span><span class="sxs-lookup"><span data-stu-id="c8015-115">Namespace Container</span></span> | <span data-ttu-id="c8015-116">cenumns. cpp</span><span class="sxs-lookup"><span data-stu-id="c8015-116">cenumns.cpp</span></span>  |
| <span data-ttu-id="c8015-117">Contêiner de esquema</span><span class="sxs-lookup"><span data-stu-id="c8015-117">Schema Container</span></span>    | <span data-ttu-id="c8015-118">cenumsch. cpp</span><span class="sxs-lookup"><span data-stu-id="c8015-118">cenumsch.cpp</span></span> |



 

<span data-ttu-id="c8015-119">Para obter informações do lado do cliente, consulte [coleções e grupos](collections-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="c8015-119">For client-side information, see [Collections and Groups](collections-and-groups.md).</span></span>

 

 




