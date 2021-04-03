---
description: Cria uma nova marca de lista para operações de gravação.
ms.assetid: 3a52e2f2-9648-45fb-b487-ccfe5ed24f7f
title: Função SdbBeginWriteListTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbBeginWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a9dcf6bdd3798b18e08b796eb268f93dc4ec6bbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646461"
---
# <a name="sdbbeginwritelisttag-function"></a><span data-ttu-id="4a2b1-103">Função SdbBeginWriteListTag</span><span class="sxs-lookup"><span data-stu-id="4a2b1-103">SdbBeginWriteListTag function</span></span>

<span data-ttu-id="4a2b1-104">Cria uma nova marca de lista para operações de gravação.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-104">Creates a new list TAG for write operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a2b1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a2b1-105">Syntax</span></span>


```C++
TAGID WINAPI SdbBeginWriteListTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a><span data-ttu-id="4a2b1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a2b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a2b1-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4a2b1-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a2b1-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="4a2b1-109">*tTag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4a2b1-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a2b1-110">A marca para a nova entrada.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-110">The TAG for the new entry.</span></span> <span data-ttu-id="4a2b1-111">Esse valor deve ser do tipo **\_ \_ lista de tipos de marca**.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-111">This value must be of type **TAG\_TYPE\_LIST**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a2b1-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a2b1-112">Return value</span></span>

<span data-ttu-id="4a2b1-113">A função retorna o [**TagId**](tagid.md) da nova lista em êxito ou **TagId \_ nulo** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="4a2b1-113">The function returns the [**TAGID**](tagid.md) of the new list on success or **TAGID\_NULL** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a2b1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a2b1-114">Requirements</span></span>



| <span data-ttu-id="4a2b1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a2b1-115">Requirement</span></span> | <span data-ttu-id="4a2b1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4a2b1-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a2b1-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a2b1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4a2b1-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a2b1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4a2b1-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a2b1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4a2b1-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4a2b1-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4a2b1-121">DLL</span><span class="sxs-lookup"><span data-stu-id="4a2b1-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a2b1-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a2b1-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a2b1-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a2b1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a2b1-124">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="4a2b1-124">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="4a2b1-125">**SdbCloseDatabaseWrite**</span><span class="sxs-lookup"><span data-stu-id="4a2b1-125">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
</dt> <dt>

[<span data-ttu-id="4a2b1-126">**SdbEndWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="4a2b1-126">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="4a2b1-127">**Tags**</span><span class="sxs-lookup"><span data-stu-id="4a2b1-127">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="4a2b1-128">Tipos de marca</span><span class="sxs-lookup"><span data-stu-id="4a2b1-128">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="4a2b1-129">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="4a2b1-129">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




