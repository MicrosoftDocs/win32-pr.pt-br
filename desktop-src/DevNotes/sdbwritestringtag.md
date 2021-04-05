---
description: Grava uma cadeia de caracteres no banco de dados especificado.
ms.assetid: 72c62d91-0c1c-4ff8-8829-1c3ec1fa8648
title: Função SdbWriteStringTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4ac588d99408d0d7f13bc0fd13d8abe8a6580e69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826273"
---
# <a name="sdbwritestringtag-function"></a><span data-ttu-id="398b7-103">Função SdbWriteStringTag</span><span class="sxs-lookup"><span data-stu-id="398b7-103">SdbWriteStringTag function</span></span>

<span data-ttu-id="398b7-104">Grava uma cadeia de caracteres no banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="398b7-104">Writes a string to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="398b7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="398b7-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteStringTag(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszData
);
```



## <a name="parameters"></a><span data-ttu-id="398b7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="398b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="398b7-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="398b7-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="398b7-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="398b7-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="398b7-109">*tTag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="398b7-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="398b7-110">A marca para a entrada.</span><span class="sxs-lookup"><span data-stu-id="398b7-110">The TAG for the entry.</span></span> <span data-ttu-id="398b7-111">Essa marca deve ser do tipo **marca \_ tipo \_ STRINGREF**.</span><span class="sxs-lookup"><span data-stu-id="398b7-111">This TAG must be of type **TAG\_TYPE\_STRINGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="398b7-112">*pwszData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="398b7-112">*pwszData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="398b7-113">A cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="398b7-113">The null-terminated string.</span></span> <span data-ttu-id="398b7-114">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="398b7-114">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="398b7-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="398b7-115">Return value</span></span>

<span data-ttu-id="398b7-116">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="398b7-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="398b7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="398b7-117">Requirements</span></span>



| <span data-ttu-id="398b7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="398b7-118">Requirement</span></span> | <span data-ttu-id="398b7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="398b7-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="398b7-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="398b7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="398b7-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="398b7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="398b7-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="398b7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="398b7-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="398b7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="398b7-124">DLL</span><span class="sxs-lookup"><span data-stu-id="398b7-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="398b7-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="398b7-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="398b7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="398b7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="398b7-127">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="398b7-127">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="398b7-128">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="398b7-128">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="398b7-129">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="398b7-129">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="398b7-130">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="398b7-130">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




