---
description: TAGREF-contém o índice de uma entrada e suas informações de marca em um banco de dados de Shim.
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34e27a60847630e7bbd8e07ccf005dfd7b474d7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096624"
---
# <a name="tagref"></a><span data-ttu-id="79ea1-103">TAGREF</span><span class="sxs-lookup"><span data-stu-id="79ea1-103">TAGREF</span></span>

<span data-ttu-id="79ea1-104">Contém o índice de uma entrada e suas informações de marca em um banco de dados Shim.</span><span class="sxs-lookup"><span data-stu-id="79ea1-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a><span data-ttu-id="79ea1-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="79ea1-105">Remarks</span></span>

<span data-ttu-id="79ea1-106">Um **TAGREF** é específico para um banco de dados de Shim e é válido em vários bancos.</span><span class="sxs-lookup"><span data-stu-id="79ea1-106">A **TAGREF** is specific to a shim database and valid across multiple databases.</span></span> <span data-ttu-id="79ea1-107">Pode ser um valor inteiro que representa o índice ou um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="79ea1-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="79ea1-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ nulo (0)</span><span class="sxs-lookup"><span data-stu-id="79ea1-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="79ea1-109">O **TAGREF** não existe.</span><span class="sxs-lookup"><span data-stu-id="79ea1-109">The **TAGREF** does not exist.</span></span> <span data-ttu-id="79ea1-110">Esse valor é retornado de uma função quando não pode retornar um **TAGREF** válido.</span><span class="sxs-lookup"><span data-stu-id="79ea1-110">This value is returned from a function when it cannot return a valid **TAGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="79ea1-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>\_Raiz TAGREF (0)</span><span class="sxs-lookup"><span data-stu-id="79ea1-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="79ea1-112">Indica uma marca de lista raiz que pode ser usada como um pai para obter um **TAGREF** filho.</span><span class="sxs-lookup"><span data-stu-id="79ea1-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGREF**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79ea1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79ea1-113">Requirements</span></span>



| <span data-ttu-id="79ea1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="79ea1-114">Requirement</span></span> | <span data-ttu-id="79ea1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="79ea1-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="79ea1-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79ea1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="79ea1-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="79ea1-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="79ea1-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79ea1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="79ea1-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="79ea1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="79ea1-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="79ea1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79ea1-121">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="79ea1-121">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> <dt>

[<span data-ttu-id="79ea1-122">**Tags**</span><span class="sxs-lookup"><span data-stu-id="79ea1-122">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="79ea1-123">Tipos de marca</span><span class="sxs-lookup"><span data-stu-id="79ea1-123">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="79ea1-124">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="79ea1-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




