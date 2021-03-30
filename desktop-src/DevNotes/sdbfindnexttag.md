---
description: Pesquisa a próxima marca correspondente no pai especificado e retorna o TAGID da correspondência.
ms.assetid: c96aa1c1-b0e6-49f5-9f74-7d0e050bee3b
title: Função SdbFindNextTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindNextTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a5baf728a75e4c02c20ed4207b7d6b9a968af1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826276"
---
# <a name="sdbfindnexttag-function"></a><span data-ttu-id="b2054-103">Função SdbFindNextTag</span><span class="sxs-lookup"><span data-stu-id="b2054-103">SdbFindNextTag function</span></span>

<span data-ttu-id="b2054-104">Pesquisa a próxima marca correspondente no pai especificado e retorna o **TagId** da correspondência.</span><span class="sxs-lookup"><span data-stu-id="b2054-104">Searches for the next TAG match within the specified parent and returns the **TAGID** of the match.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2054-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2054-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindNextTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a><span data-ttu-id="b2054-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2054-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2054-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b2054-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2054-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="b2054-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="b2054-109">*tiParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b2054-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2054-110">O **TagId** do início da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="b2054-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="b2054-111">Esse parâmetro pode ser **TagId \_ raiz** ou **\_ \_ lista de tipos de marca**.</span><span class="sxs-lookup"><span data-stu-id="b2054-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="b2054-112">*tiPrev* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b2054-112">*tiPrev* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2054-113">O **TagId** da correspondência anterior.</span><span class="sxs-lookup"><span data-stu-id="b2054-113">The **TAGID** of the previous match.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2054-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2054-114">Return value</span></span>

<span data-ttu-id="b2054-115">O **TagId** da correspondência.</span><span class="sxs-lookup"><span data-stu-id="b2054-115">The **TAGID** of the match.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2054-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2054-116">Remarks</span></span>

<span data-ttu-id="b2054-117">Antes de chamar essa função, chame a função [**SdbFindFirstTag**](sdbfindfirsttag.md) .</span><span class="sxs-lookup"><span data-stu-id="b2054-117">Before calling this function, call the [**SdbFindFirstTag**](sdbfindfirsttag.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2054-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2054-118">Requirements</span></span>



| <span data-ttu-id="b2054-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2054-119">Requirement</span></span> | <span data-ttu-id="b2054-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b2054-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2054-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2054-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b2054-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b2054-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b2054-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2054-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b2054-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b2054-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b2054-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b2054-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2054-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2054-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2054-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b2054-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2054-128">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="b2054-128">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="b2054-129">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="b2054-129">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




