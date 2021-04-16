---
description: Grava dados binários no banco de dado especificado.
ms.assetid: 935321b8-904e-46be-ad11-77d89670a072
title: Função SdbWriteBinaryTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e79de8549eb4c0a0f1b8a914c59d21ccfb3bcf7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500868"
---
# <a name="sdbwritebinarytag-function"></a><span data-ttu-id="e4e2a-103">Função SdbWriteBinaryTag</span><span class="sxs-lookup"><span data-stu-id="e4e2a-103">SdbWriteBinaryTag function</span></span>

<span data-ttu-id="e4e2a-104">Grava dados binários no banco de dado especificado.</span><span class="sxs-lookup"><span data-stu-id="e4e2a-104">Writes binary data to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4e2a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4e2a-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteBinaryTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ PBYTE pBuffer,
  _In_ DWORD dwSize
);
```



## <a name="parameters"></a><span data-ttu-id="e4e2a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4e2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4e2a-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4e2a-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e2a-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="e4e2a-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="e4e2a-109">*tTag* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4e2a-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e2a-110">A marca para a entrada.</span><span class="sxs-lookup"><span data-stu-id="e4e2a-110">The TAG for the entry.</span></span> <span data-ttu-id="e4e2a-111">Essa marca deve ser do tipo **tipo de marca \_ \_ Binary**.</span><span class="sxs-lookup"><span data-stu-id="e4e2a-111">This TAG must be of type **TAG\_TYPE\_BINARY**.</span></span>

</dd> <dt>

<span data-ttu-id="e4e2a-112">*pBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4e2a-112">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e2a-113">O buffer que contém os dados.</span><span class="sxs-lookup"><span data-stu-id="e4e2a-113">The buffer that contains the data.</span></span> <span data-ttu-id="e4e2a-114">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e4e2a-114">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e4e2a-115">*dwSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4e2a-115">*dwSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e2a-116">O tamanho do buffer *pBuffer* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="e4e2a-116">The size of the *pBuffer* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4e2a-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4e2a-117">Return value</span></span>

<span data-ttu-id="e4e2a-118">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="e4e2a-118">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4e2a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4e2a-119">Requirements</span></span>



| <span data-ttu-id="e4e2a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4e2a-120">Requirement</span></span> | <span data-ttu-id="e4e2a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e4e2a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4e2a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4e2a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e4e2a-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4e2a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e4e2a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4e2a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e4e2a-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e4e2a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e4e2a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e4e2a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4e2a-127"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4e2a-127"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4e2a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4e2a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4e2a-129">**SdbWriteBinaryTagFromFile**</span><span class="sxs-lookup"><span data-stu-id="e4e2a-129">**SdbWriteBinaryTagFromFile**</span></span>](sdbwritebinarytagfromfile.md)
</dt> <dt>

[<span data-ttu-id="e4e2a-130">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="e4e2a-130">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="e4e2a-131">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="e4e2a-131">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="e4e2a-132">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="e4e2a-132">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="e4e2a-133">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="e4e2a-133">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




