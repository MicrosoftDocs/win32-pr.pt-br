---
description: Especifica a direção de um objeto IContextLink.
ms.assetid: 4ba7dca7-6801-45bf-bbf1-1dd3172fbfa2
title: Enumeração ContextLinkDirection (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContextLinkDirection
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 82e10c7e908b4cc4035d8bfdde55d863f7b6ecf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828744"
---
# <a name="contextlinkdirection-enumeration"></a><span data-ttu-id="dc89c-103">Enumeração ContextLinkDirection</span><span class="sxs-lookup"><span data-stu-id="dc89c-103">ContextLinkDirection enumeration</span></span>

<span data-ttu-id="dc89c-104">Especifica a direção de um objeto [**IContextLink**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="dc89c-104">Specifies the direction of an [**IContextLink**](icontextlink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc89c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc89c-105">Syntax</span></span>


```C++
typedef enum ContextLinkDirection { 
  ContextLinkDirection_LinksWith  = 0,
  ContextLinkDirection_LinksFrom  = 1,
  ContextLinkDirection_LinksTo    = 2
} ContextLinkDirection;
```



## <a name="constants"></a><span data-ttu-id="dc89c-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="dc89c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dc89c-107"><span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**ContextLinkDirection \_ LinksWith**</span><span class="sxs-lookup"><span data-stu-id="dc89c-107"><span id="ContextLinkDirection_LinksWith"></span><span id="contextlinkdirection_linkswith"></span><span id="CONTEXTLINKDIRECTION_LINKSWITH"></span>**ContextLinkDirection\_LinksWith**</span></span>
</dt> <dd>

<span data-ttu-id="dc89c-108">O [**IContextNode**](icontextnode.md) é um desenho direcional que aponta para fora do [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="dc89c-108">The [**IContextNode**](icontextnode.md) is a directional drawing that points away from the [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc89c-109"><span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**ContextLinkDirection \_ LinksFrom**</span><span class="sxs-lookup"><span data-stu-id="dc89c-109"><span id="ContextLinkDirection_LinksFrom"></span><span id="contextlinkdirection_linksfrom"></span><span id="CONTEXTLINKDIRECTION_LINKSFROM"></span>**ContextLinkDirection\_LinksFrom**</span></span>
</dt> <dd>

<span data-ttu-id="dc89c-110">O [**IContextNode**](icontextnode.md) é um desenho direcional que aponta para o [**IContextLink**](icontextlink.md).</span><span class="sxs-lookup"><span data-stu-id="dc89c-110">The [**IContextNode**](icontextnode.md) is a directional drawing that points to the [**IContextLink**](icontextlink.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc89c-111"><span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**Links do ContextLinkDirectionto \_**</span><span class="sxs-lookup"><span data-stu-id="dc89c-111"><span id="ContextLinkDirection_LinksTo"></span><span id="contextlinkdirection_linksto"></span><span id="CONTEXTLINKDIRECTION_LINKSTO"></span>**ContextLinkDirection\_LinksTo**</span></span>
</dt> <dd>

<span data-ttu-id="dc89c-112">Não há desenhos direcionais no link.</span><span class="sxs-lookup"><span data-stu-id="dc89c-112">There are no directional drawings in the link.</span></span> <span data-ttu-id="dc89c-113">Por exemplo, um desenho de tinta pode sublinhar uma palavra à tinta.</span><span class="sxs-lookup"><span data-stu-id="dc89c-113">For example, an ink drawing can underline an ink word.</span></span> <span data-ttu-id="dc89c-114">Não há nenhuma direção inferida do sublinhado.</span><span class="sxs-lookup"><span data-stu-id="dc89c-114">There is no direction inferred from the underline.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="dc89c-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dc89c-115">Examples</span></span>

<span data-ttu-id="dc89c-116">O exemplo a seguir usa um objeto [**IContextNode**](icontextnode.md) , `m_pSelectedNode` e salva todos os objetos **IContextNode** aos quais ele se vincula, orientando a árvore ancestral e adicionando os objetos a um `CArray` objeto, `linkedToNodes` .</span><span class="sxs-lookup"><span data-stu-id="dc89c-116">The following example takes an [**IContextNode**](icontextnode.md) object, `m_pSelectedNode`, and saves all the **IContextNode** objects that it links to by walking up the ancestor tree and adding the objects into a `CArray` object, `linkedToNodes`.</span></span> <span data-ttu-id="dc89c-117">`CheckHResult` é uma função que usa um `HRESULT` e uma cadeia de caracteres e gera uma exceção criada com a cadeia de caracteres se o `HRESULT` não for **êxito**.</span><span class="sxs-lookup"><span data-stu-id="dc89c-117">`CheckHResult` is a function that takes an `HRESULT` and a string, and throws an exception created with the string if the `HRESULT` is not **SUCCESS**.</span></span>


```C++
// Find all first ancestor that contains links of type Enclose
CArray<IContextNode*,IContextNode*> linkedToNodes = CArray<IContextNode*,IContextNode*>();
IContextNode* pAncestor;
CheckHResult(m_pSelectedNode->GetParentNode(&pAncestor),
    "IContextNode::GetParentNode failed");
while (pAncestor != NULL)
{
    // Get the links
    IContextLinks* pLinks;
    CheckHResult(pAncestor->GetContextLinks(&pLinks),
        "IContextNode::GetContextLinks failed");
    ULONG nLinks;
    CheckHResult(pLinks->GetCount(&nLinks), "IContextLinks::GetCount failed");
    for (ULONG i = 0; i < nLinks; i++)
    {
        IContextLink* pLink;
        CheckHResult(pLinks->GetContextLink(i, &pLink),
            "IContextLinks::GetContextLink failed");
        // Check link direction
        ContextLinkDirection linkDirection;
        CheckHResult(pLink->GetContextLinkDirection(&linkDirection),
            "IContextLink:GetContextLinkDirection failed");
        if (linkDirection == ContextLinkDirection_LinksTo)
        {
            // Get source node and add the array
            IContextNode* pSourceNode;
            CheckHResult(pLink->GetSourceNode(&pSourceNode),
                "IContextLink::GetSourceNode failed");
            linkedToNodes.Add(pSourceNode);
        }
    }
            
    // Go up another level
    IContextNode* pNewAncestor;
    CheckHResult(pAncestor->GetParentNode(&pNewAncestor),
        "IContextNode::GetParentNode failed");
    pAncestor = pNewAncestor;
}
```



## <a name="requirements"></a><span data-ttu-id="dc89c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc89c-118">Requirements</span></span>



| <span data-ttu-id="dc89c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc89c-119">Requirement</span></span> | <span data-ttu-id="dc89c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="dc89c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc89c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc89c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dc89c-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="dc89c-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dc89c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc89c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dc89c-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dc89c-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="dc89c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dc89c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc89c-126"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="dc89c-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc89c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc89c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc89c-128">**IContextLink**</span><span class="sxs-lookup"><span data-stu-id="dc89c-128">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="dc89c-129">**IContextNode::AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="dc89c-129">**IContextNode::AddContextLink**</span></span>](icontextnode-addcontextlink.md)
</dt> </dl>

 

 




