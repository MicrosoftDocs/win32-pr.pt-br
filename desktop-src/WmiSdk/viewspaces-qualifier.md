---
description: O qualificador ViewSpaces define os nomes e o local dos namespaces onde as instâncias de origem estão localizadas. Você pode especificar qualquer combinação de namespaces em computadores locais ou remotos.
ms.assetid: 15d71bb6-842d-4f5a-b2e3-e9f60f0aea3b
ms.tgt_platform: multiple
title: Qualificador ViewSpaces
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSpaces
api_type:
- NA
api_location: ''
ms.openlocfilehash: 683f5596497f3c1e1ad0f2b85eaaa1460177a0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171778"
---
# <a name="viewspaces-qualifier"></a><span data-ttu-id="db675-104">Qualificador ViewSpaces</span><span class="sxs-lookup"><span data-stu-id="db675-104">ViewSpaces Qualifier</span></span>

<span data-ttu-id="db675-105">O **qualificador ViewSpaces** define os nomes e o local dos namespaces onde as instâncias de origem estão localizadas.</span><span class="sxs-lookup"><span data-stu-id="db675-105">The **ViewSpaces qualifier** defines the names and location of the namespaces where the source instances are located.</span></span> <span data-ttu-id="db675-106">Você pode especificar qualquer combinação de namespaces em computadores locais ou remotos.</span><span class="sxs-lookup"><span data-stu-id="db675-106">You can specify any combination of namespaces on local or remote computers.</span></span>

<span data-ttu-id="db675-107">O exemplo a seguir lista dois namespaces no computador local.</span><span class="sxs-lookup"><span data-stu-id="db675-107">The following example lists two namespaces on the local computer.</span></span>


```mof
ViewSpaces{"\\\\.\\root\\LocalNamespace",
     "\\\\.\\root\\RemoteNamespace"}
```



<span data-ttu-id="db675-108">O [provedor de exibição](view-provider.md) corresponde às consultas de origem no [qualificador ViewSources](viewsources-qualifier.md) para os namespaces listados no qualificador **ViewSpaces** na ordem em que as consultas e os namespaces são listados.</span><span class="sxs-lookup"><span data-stu-id="db675-108">The [View provider](view-provider.md) matches the source queries in the [ViewSources qualifier](viewsources-qualifier.md) to the namespaces listed in the **ViewSpaces** qualifier in the order the queries and namespaces are listed.</span></span> <span data-ttu-id="db675-109">Normalmente, há uma relação um-para-um entre o número de namespaces listados no qualificador **ViewSpaces** e as consultas listadas no qualificador **ViewSources** .</span><span class="sxs-lookup"><span data-stu-id="db675-109">Normally, there is a one-to-one relationship between the number of namespaces listed in the **ViewSpaces** qualifier and the queries listed in the **ViewSources** qualifier.</span></span> <span data-ttu-id="db675-110">Em alguns casos, talvez você queira que as consultas listadas no qualificador ViewSources sejam executadas em dois ou mais namespaces.</span><span class="sxs-lookup"><span data-stu-id="db675-110">In some cases, you may want the queries listed in the ViewSources qualifier to execute against two or more namespaces.</span></span> <span data-ttu-id="db675-111">Você pode usar dois pontos duplos "::" para separar vários namespaces que serão avaliados por uma das consultas na matriz **ViewSources** .</span><span class="sxs-lookup"><span data-stu-id="db675-111">You can use a double colon "::" to separate multiple namespaces that will be evaluated by one of the queries in the **ViewSources** array.</span></span>

<span data-ttu-id="db675-112">No exemplo a seguir, a primeira consulta na matriz [**ViewSources**](viewsources-qualifier.md) será executada no namespace no primeiro par de aspas, a segunda consulta em relação aos três namespaces no segundo par de aspas e a terceira consulta em relação aos dois namespaces no terceiro par de aspas.</span><span class="sxs-lookup"><span data-stu-id="db675-112">In the following example, the first query in the [**ViewSources**](viewsources-qualifier.md) array will be run against the namespace in the first pair of quotes, the second query against the three namespaces in the second pair of quotes, and the third query against the two namespaces in the third pair of quotes.</span></span>


```mof
ViewSpaces
    {
    "\\\\.\\root\\LocalNamespace",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace2::
        \\\\.\\root\\RemoteNamespace3",

    "\\\\.\\root\\RemoteNamespace1::
        \\\\.\\root\\RemoteNamespace3"
    }
```



## <a name="requirements"></a><span data-ttu-id="db675-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db675-113">Requirements</span></span>



| <span data-ttu-id="db675-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="db675-114">Requirement</span></span> | <span data-ttu-id="db675-115">Valor</span><span class="sxs-lookup"><span data-stu-id="db675-115">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="db675-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db675-116">Minimum supported client</span></span><br/> | <span data-ttu-id="db675-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db675-117">Windows Vista</span></span><br/>       |
| <span data-ttu-id="db675-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db675-118">Minimum supported server</span></span><br/> | <span data-ttu-id="db675-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db675-119">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="db675-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="db675-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db675-121">**Qualificadores específicos para o provedor de exibição**</span><span class="sxs-lookup"><span data-stu-id="db675-121">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




