---
description: Grava um valor de palavra no banco de dados especificado.
ms.assetid: 8f921e14-4a82-4d8e-83fa-beb78118ecb8
title: Função SdbWriteWORDTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75a5b3eb430901de36d5aca325f928aae266bc39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500866"
---
# <a name="sdbwritewordtag-function"></a><span data-ttu-id="65eac-103">Função SdbWriteWORDTag</span><span class="sxs-lookup"><span data-stu-id="65eac-103">SdbWriteWORDTag function</span></span>

<span data-ttu-id="65eac-104">Grava um valor de **palavra** no banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="65eac-104">Writes a **WORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="65eac-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65eac-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteWORDTag(
  _In_ PDB  pdb,
  _In_ TAG  tTag,
  _In_ WORD wData
);
```



## <a name="parameters"></a><span data-ttu-id="65eac-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65eac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65eac-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65eac-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65eac-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="65eac-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="65eac-109">*tTag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65eac-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65eac-110">A marca para a entrada.</span><span class="sxs-lookup"><span data-stu-id="65eac-110">The TAG for the entry.</span></span> <span data-ttu-id="65eac-111">Essa marca deve ser do tipo **tipo de marca \_ \_ Word**.</span><span class="sxs-lookup"><span data-stu-id="65eac-111">This TAG must be of type **TAG\_TYPE\_WORD**.</span></span>

</dd> <dt>

<span data-ttu-id="65eac-112">*wData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65eac-112">*wData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65eac-113">O valor.</span><span class="sxs-lookup"><span data-stu-id="65eac-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65eac-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="65eac-114">Return value</span></span>

<span data-ttu-id="65eac-115">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="65eac-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="65eac-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65eac-116">Requirements</span></span>



| <span data-ttu-id="65eac-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="65eac-117">Requirement</span></span> | <span data-ttu-id="65eac-118">Valor</span><span class="sxs-lookup"><span data-stu-id="65eac-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65eac-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65eac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="65eac-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65eac-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="65eac-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65eac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="65eac-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="65eac-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="65eac-123">DLL</span><span class="sxs-lookup"><span data-stu-id="65eac-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65eac-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65eac-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65eac-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="65eac-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65eac-126">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="65eac-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="65eac-127">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="65eac-127">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="65eac-128">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="65eac-128">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="65eac-129">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="65eac-129">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> </dl>

 

 




