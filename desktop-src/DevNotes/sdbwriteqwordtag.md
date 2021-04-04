---
description: Grava um valor QWORD no banco de dados especificado.
ms.assetid: 8ce566ea-a941-45fa-b031-26c3144ca02c
title: Função SdbWriteQWORDTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 58dcaad3487bb1f59a75dd6a671ecb43c9cf1751
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646297"
---
# <a name="sdbwriteqwordtag-function"></a><span data-ttu-id="96acf-103">Função SdbWriteQWORDTag</span><span class="sxs-lookup"><span data-stu-id="96acf-103">SdbWriteQWORDTag function</span></span>

<span data-ttu-id="96acf-104">Grava um valor **QWORD** no banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="96acf-104">Writes a **QWORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="96acf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96acf-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteQWORDTag(
  _In_ PDB       pdb,
  _In_ TAG       tTag,
  _In_ ULONGLONG qwData
);
```



## <a name="parameters"></a><span data-ttu-id="96acf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96acf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96acf-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="96acf-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96acf-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="96acf-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="96acf-109">*tTag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="96acf-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96acf-110">A marca para a entrada.</span><span class="sxs-lookup"><span data-stu-id="96acf-110">The TAG for the entry.</span></span> <span data-ttu-id="96acf-111">Essa marca deve ser do tipo **marca de tipo \_ \_ QWORD**.</span><span class="sxs-lookup"><span data-stu-id="96acf-111">This TAG must be of type **TAG\_TYPE\_QWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="96acf-112">*qwData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="96acf-112">*qwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96acf-113">O valor.</span><span class="sxs-lookup"><span data-stu-id="96acf-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96acf-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="96acf-114">Return value</span></span>

<span data-ttu-id="96acf-115">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="96acf-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="96acf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96acf-116">Requirements</span></span>



| <span data-ttu-id="96acf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="96acf-117">Requirement</span></span> | <span data-ttu-id="96acf-118">Valor</span><span class="sxs-lookup"><span data-stu-id="96acf-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96acf-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96acf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="96acf-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96acf-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="96acf-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96acf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="96acf-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="96acf-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="96acf-123">DLL</span><span class="sxs-lookup"><span data-stu-id="96acf-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96acf-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96acf-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96acf-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="96acf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96acf-126">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="96acf-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="96acf-127">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="96acf-127">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="96acf-128">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="96acf-128">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="96acf-129">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="96acf-129">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




