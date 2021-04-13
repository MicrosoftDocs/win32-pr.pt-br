---
description: Contém o índice de uma entrada e suas informações de marca em um banco de dados Shim.
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8631811f101850b68bdbad1097c19b9a41737bd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500825"
---
# <a name="tagref"></a><span data-ttu-id="5ddda-103">TAGREF</span><span class="sxs-lookup"><span data-stu-id="5ddda-103">TAGREF</span></span>

<span data-ttu-id="5ddda-104">Contém o índice de uma entrada e suas informações de marca em um banco de dados Shim.</span><span class="sxs-lookup"><span data-stu-id="5ddda-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a><span data-ttu-id="5ddda-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ddda-105">Remarks</span></span>

<span data-ttu-id="5ddda-106">Um **TAGREF** é específico para um banco de dados de Shim e é válido em vários bancos.</span><span class="sxs-lookup"><span data-stu-id="5ddda-106">A **TAGREF** is specific to a shim database and valid across multiple databases.</span></span> <span data-ttu-id="5ddda-107">Pode ser um valor inteiro que representa o índice ou um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="5ddda-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="5ddda-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ nulo (0)</span><span class="sxs-lookup"><span data-stu-id="5ddda-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="5ddda-109">O **TAGREF** não existe.</span><span class="sxs-lookup"><span data-stu-id="5ddda-109">The **TAGREF** does not exist.</span></span> <span data-ttu-id="5ddda-110">Esse valor é retornado de uma função quando não pode retornar um **TAGREF** válido.</span><span class="sxs-lookup"><span data-stu-id="5ddda-110">This value is returned from a function when it cannot return a valid **TAGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="5ddda-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>\_Raiz TAGREF (0)</span><span class="sxs-lookup"><span data-stu-id="5ddda-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="5ddda-112">Indica uma marca de lista raiz que pode ser usada como um pai para obter um **TAGREF** filho.</span><span class="sxs-lookup"><span data-stu-id="5ddda-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGREF**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ddda-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ddda-113">Requirements</span></span>



| <span data-ttu-id="5ddda-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ddda-114">Requirement</span></span> | <span data-ttu-id="5ddda-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5ddda-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5ddda-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ddda-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5ddda-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ddda-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5ddda-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ddda-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5ddda-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5ddda-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5ddda-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ddda-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ddda-121">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="5ddda-121">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> <dt>

[<span data-ttu-id="5ddda-122">**Tags**</span><span class="sxs-lookup"><span data-stu-id="5ddda-122">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="5ddda-123">Tipos de marca</span><span class="sxs-lookup"><span data-stu-id="5ddda-123">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="5ddda-124">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="5ddda-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




