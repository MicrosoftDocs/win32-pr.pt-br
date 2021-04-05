---
description: Pesquisa a próxima marca filha dentro do pai especificado e retorna o TAGID do próximo filho.
ms.assetid: c7311f20-15ca-4b2d-a08d-8bb992a3a0cd
title: Função SdbGetNextChild
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetNextChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f2943eaf0baec84a9473b679743b9eafad3b7fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826354"
---
# <a name="sdbgetnextchild-function"></a><span data-ttu-id="aec62-103">Função SdbGetNextChild</span><span class="sxs-lookup"><span data-stu-id="aec62-103">SdbGetNextChild function</span></span>

<span data-ttu-id="aec62-104">Pesquisa a próxima marca filha dentro do pai especificado e retorna o **TagId** do próximo filho.</span><span class="sxs-lookup"><span data-stu-id="aec62-104">Searches for the next child TAG within the specified parent and returns the **TAGID** of the next child.</span></span>

## <a name="syntax"></a><span data-ttu-id="aec62-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aec62-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetNextChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a><span data-ttu-id="aec62-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aec62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aec62-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aec62-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aec62-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="aec62-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="aec62-109">*tiParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aec62-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aec62-110">O **TagId** do início da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="aec62-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="aec62-111">Esse parâmetro pode ser **TagId \_ raiz** ou **\_ \_ lista de tipos de marca**.</span><span class="sxs-lookup"><span data-stu-id="aec62-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="aec62-112">*tiPrev* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aec62-112">*tiPrev* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aec62-113">O **TagId** do filho anterior.</span><span class="sxs-lookup"><span data-stu-id="aec62-113">The **TAGID** of the previous child.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aec62-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aec62-114">Return value</span></span>

<span data-ttu-id="aec62-115">O **TagId** do filho ou **TagId \_ nulo** se nenhum filho for encontrado.</span><span class="sxs-lookup"><span data-stu-id="aec62-115">The **TAGID** of the child or **TAGID\_NULL** if no child is found.</span></span>

## <a name="remarks"></a><span data-ttu-id="aec62-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="aec62-116">Remarks</span></span>

<span data-ttu-id="aec62-117">Antes de chamar essa função, chame a função [**SdbGetFirstChild**](sdbgetfirstchild.md) .</span><span class="sxs-lookup"><span data-stu-id="aec62-117">Before calling this function, call the [**SdbGetFirstChild**](sdbgetfirstchild.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="aec62-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aec62-118">Requirements</span></span>



| <span data-ttu-id="aec62-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="aec62-119">Requirement</span></span> | <span data-ttu-id="aec62-120">Valor</span><span class="sxs-lookup"><span data-stu-id="aec62-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aec62-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aec62-121">Minimum supported client</span></span><br/> | <span data-ttu-id="aec62-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="aec62-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="aec62-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aec62-123">Minimum supported server</span></span><br/> | <span data-ttu-id="aec62-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aec62-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="aec62-125">DLL</span><span class="sxs-lookup"><span data-stu-id="aec62-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aec62-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aec62-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aec62-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="aec62-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aec62-128">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="aec62-128">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="aec62-129">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="aec62-129">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="aec62-130">**SdbGetFirstChild**</span><span class="sxs-lookup"><span data-stu-id="aec62-130">**SdbGetFirstChild**</span></span>](sdbgetfirstchild.md)
</dt> </dl>

 

 




