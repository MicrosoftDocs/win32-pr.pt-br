---
Description: Recupera a cadeia de caracteres para o TAGID especificado.
ms.assetid: d67d386d-a2c5-46e2-8887-9ee20ea427f9
title: Função SdbReadStringTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3f368d66e0fbc144a46683a04655cd7f650c3bce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919070"
---
# <a name="sdbreadstringtag-function"></a><span data-ttu-id="c0043-103">Função SdbReadStringTag</span><span class="sxs-lookup"><span data-stu-id="c0043-103">SdbReadStringTag function</span></span>

<span data-ttu-id="c0043-104">Recupera a cadeia de caracteres para o **TagId** especificado.</span><span class="sxs-lookup"><span data-stu-id="c0043-104">Retrieves the string for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0043-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0043-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadStringTag(
  _In_  PDB    pdb,
  _In_  TAGID  tiWhich,
  _Out_ LPTSTR pwszBuffer,
  _In_  DWORD  cchBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="c0043-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0043-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0043-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0043-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0043-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="c0043-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="c0043-109">*tiWhich* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0043-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0043-110">O **TagId** que corresponde aos dados a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="c0043-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="c0043-111">*pwszBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c0043-111">*pwszBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0043-112">O buffer que recebe a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c0043-112">The buffer that receives the string.</span></span> <span data-ttu-id="c0043-113">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c0043-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c0043-114">*cchBufferSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0043-114">*cchBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0043-115">O tamanho do buffer *pwszBuffer* , em caracteres.</span><span class="sxs-lookup"><span data-stu-id="c0043-115">The size of the *pwszBuffer* buffer, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0043-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0043-116">Return value</span></span>

<span data-ttu-id="c0043-117">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="c0043-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0043-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0043-118">Requirements</span></span>



| <span data-ttu-id="c0043-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0043-119">Requirement</span></span> | <span data-ttu-id="c0043-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c0043-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0043-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0043-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c0043-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c0043-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c0043-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0043-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c0043-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c0043-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c0043-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c0043-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0043-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0043-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0043-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0043-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0043-128">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="c0043-128">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="c0043-129">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="c0043-129">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="c0043-130">**SdbReadBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="c0043-130">**SdbReadBinaryTag**</span></span>](sdbreadbinarytag.md)
</dt> <dt>

[<span data-ttu-id="c0043-131">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="c0043-131">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> </dl>

 

 




