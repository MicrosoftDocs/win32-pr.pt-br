---
Description: Recupera os dados binários para o TAGID especificado.
ms.assetid: b349f2af-2505-4efc-bd59-203f7666ce61
title: Função SdbReadBinaryTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 024b432c3210b98721a0cf3058bad0f765287fde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753677"
---
# <a name="sdbreadbinarytag-function"></a><span data-ttu-id="0b089-103">Função SdbReadBinaryTag</span><span class="sxs-lookup"><span data-stu-id="0b089-103">SdbReadBinaryTag function</span></span>

<span data-ttu-id="0b089-104">Recupera os dados binários para o **TagId** especificado.</span><span class="sxs-lookup"><span data-stu-id="0b089-104">Retrieves the binary data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b089-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b089-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadBinaryTag(
  _In_  PDB   pdb,
  _In_  TAGID tiWhich,
  _Out_ PBYTE pBuffer,
  _In_  DWORD dwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="0b089-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b089-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b089-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b089-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b089-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="0b089-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="0b089-109">*tiWhich* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b089-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b089-110">O **TagId** que corresponde aos dados a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="0b089-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="0b089-111">*pBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0b089-111">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b089-112">O buffer que recebe os dados binários.</span><span class="sxs-lookup"><span data-stu-id="0b089-112">The buffer that receives the binary data.</span></span> <span data-ttu-id="0b089-113">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0b089-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0b089-114">*dwBufferSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b089-114">*dwBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b089-115">O tamanho do buffer *pBuffer* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="0b089-115">The size of the *pBuffer* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b089-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0b089-116">Return value</span></span>

<span data-ttu-id="0b089-117">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="0b089-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b089-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b089-118">Requirements</span></span>



| <span data-ttu-id="0b089-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b089-119">Requirement</span></span> | <span data-ttu-id="0b089-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0b089-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b089-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b089-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0b089-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0b089-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0b089-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b089-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0b089-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0b089-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0b089-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0b089-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b089-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b089-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b089-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b089-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b089-128">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="0b089-128">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="0b089-129">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="0b089-129">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="0b089-130">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="0b089-130">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="0b089-131">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="0b089-131">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




