---
description: Grava uma entrada nula no banco de dados especificado.
ms.assetid: 2a29389b-d4f6-4527-a429-c9459b095f2f
title: Função SdbWriteNULLTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteNULLTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 662d5c4db31f199df8b3b9f7368aba118ea6e8fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163972"
---
# <a name="sdbwritenulltag-function"></a><span data-ttu-id="83638-103">Função SdbWriteNULLTag</span><span class="sxs-lookup"><span data-stu-id="83638-103">SdbWriteNULLTag function</span></span>

<span data-ttu-id="83638-104">Grava uma entrada **nula** no banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="83638-104">Writes a **NULL** entry to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="83638-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83638-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteNULLTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a><span data-ttu-id="83638-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83638-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83638-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83638-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83638-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="83638-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="83638-109">*tTag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83638-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83638-110">A marca para a entrada.</span><span class="sxs-lookup"><span data-stu-id="83638-110">The TAG for the entry.</span></span> <span data-ttu-id="83638-111">Essa marca deve ser do tipo **marca \_ tipo \_ NULL**.</span><span class="sxs-lookup"><span data-stu-id="83638-111">This TAG must be of type **TAG\_TYPE\_NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83638-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83638-112">Return value</span></span>

<span data-ttu-id="83638-113">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="83638-113">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="83638-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83638-114">Requirements</span></span>



| <span data-ttu-id="83638-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="83638-115">Requirement</span></span> | <span data-ttu-id="83638-116">Valor</span><span class="sxs-lookup"><span data-stu-id="83638-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83638-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83638-117">Minimum supported client</span></span><br/> | <span data-ttu-id="83638-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83638-118">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="83638-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83638-119">Minimum supported server</span></span><br/> | <span data-ttu-id="83638-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="83638-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="83638-121">DLL</span><span class="sxs-lookup"><span data-stu-id="83638-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83638-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83638-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83638-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="83638-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83638-124">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="83638-124">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="83638-125">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="83638-125">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="83638-126">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="83638-126">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="83638-127">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="83638-127">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




