---
description: Contém o índice de uma entrada e suas informações de marca em um banco de dados Shim.
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TAGID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7d8b8a25633d3505936d105b0eef7ed38746ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920234"
---
# <a name="tagid"></a><span data-ttu-id="23b68-103">TAGID</span><span class="sxs-lookup"><span data-stu-id="23b68-103">TAGID</span></span>

<span data-ttu-id="23b68-104">Contém o índice de uma entrada e suas informações de marca em um banco de dados Shim.</span><span class="sxs-lookup"><span data-stu-id="23b68-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a><span data-ttu-id="23b68-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="23b68-105">Remarks</span></span>

<span data-ttu-id="23b68-106">Um **TagId** é específico para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="23b68-106">A **TAGID** is specific to a database.</span></span> <span data-ttu-id="23b68-107">Pode ser um valor inteiro que representa o índice ou um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="23b68-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="23b68-108"><span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID \_ nulo (0)</span><span class="sxs-lookup"><span data-stu-id="23b68-108"><span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="23b68-109">O **TagId** não existe.</span><span class="sxs-lookup"><span data-stu-id="23b68-109">The **TAGID** does not exist.</span></span> <span data-ttu-id="23b68-110">Esse valor é retornado de uma função quando não pode retornar um **TagId** válido.</span><span class="sxs-lookup"><span data-stu-id="23b68-110">This value is returned from a function when it cannot return a valid **TAGID**.</span></span>

</dd> <dt>

<span data-ttu-id="23b68-111"><span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>\_Raiz TagId (0)</span><span class="sxs-lookup"><span data-stu-id="23b68-111"><span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>TAGID\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="23b68-112">Indica uma marca de lista raiz que pode ser usada como um pai para obter um **TagId** filho.</span><span class="sxs-lookup"><span data-stu-id="23b68-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGID**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23b68-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23b68-113">Requirements</span></span>



| <span data-ttu-id="23b68-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="23b68-114">Requirement</span></span> | <span data-ttu-id="23b68-115">Valor</span><span class="sxs-lookup"><span data-stu-id="23b68-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="23b68-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23b68-116">Minimum supported client</span></span><br/> | <span data-ttu-id="23b68-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23b68-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="23b68-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23b68-118">Minimum supported server</span></span><br/> | <span data-ttu-id="23b68-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="23b68-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="23b68-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="23b68-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23b68-121">**Tags**</span><span class="sxs-lookup"><span data-stu-id="23b68-121">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="23b68-122">Tipos de marca</span><span class="sxs-lookup"><span data-stu-id="23b68-122">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="23b68-123">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="23b68-123">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




