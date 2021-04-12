---
description: Localiza o primeiro registro DWORD no índice especificado que atende aos critérios especificados.
ms.assetid: 81302f84-497d-4fef-b348-eee2a53284c7
title: Função SdbFindFirstDWORDIndexedTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstDWORDIndexedTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f3c9290f98fb24d856561114bc654da0315c5a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500741"
---
# <a name="sdbfindfirstdwordindexedtag-function"></a><span data-ttu-id="e27be-103">Função SdbFindFirstDWORDIndexedTag</span><span class="sxs-lookup"><span data-stu-id="e27be-103">SdbFindFirstDWORDIndexedTag function</span></span>

<span data-ttu-id="e27be-104">Localiza o primeiro registro **DWORD** no índice especificado que atende aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="e27be-104">Finds the first **DWORD** record in the specified index that meets the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="e27be-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e27be-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindFirstDWORDIndexedTag(
  _In_  PDB       pdb,
  _In_  TAG       tWhich,
  _In_  TAG       tKey,
  _In_  DWORD     dwName,
  _Out_ FIND_INFO *pFindInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e27be-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e27be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e27be-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e27be-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e27be-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="e27be-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="e27be-109">*tWhich* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e27be-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e27be-110">O tipo do índice.</span><span class="sxs-lookup"><span data-stu-id="e27be-110">The index type.</span></span> <span data-ttu-id="e27be-111">Consulte a [**marca**](tag.md) para obter uma lista de valores.</span><span class="sxs-lookup"><span data-stu-id="e27be-111">See [**TAG**](tag.md) for a list of values.</span></span>

</dd> <dt>

<span data-ttu-id="e27be-112">*tKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e27be-112">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e27be-113">O tipo principal.</span><span class="sxs-lookup"><span data-stu-id="e27be-113">The key type.</span></span>

</dd> <dt>

<span data-ttu-id="e27be-114">*dwName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e27be-114">*dwName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e27be-115">O nome dos dados a serem encontrados.</span><span class="sxs-lookup"><span data-stu-id="e27be-115">The name of the data to be found.</span></span> <span data-ttu-id="e27be-116">Esse valor será convertido em uma chave.</span><span class="sxs-lookup"><span data-stu-id="e27be-116">This value will be converted into a key.</span></span>

</dd> <dt>

<span data-ttu-id="e27be-117">*pFindInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e27be-117">*pFindInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e27be-118">Uma estrutura de [**\_ informações de localização**](find-info.md) que recebe o registro.</span><span class="sxs-lookup"><span data-stu-id="e27be-118">A [**FIND\_INFO**](find-info.md) structure that receives the record.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e27be-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e27be-119">Return value</span></span>

<span data-ttu-id="e27be-120">O **TagId** da primeira correspondência ou **marca \_ NULL** se nenhuma correspondência for encontrada.</span><span class="sxs-lookup"><span data-stu-id="e27be-120">The **TAGID** of the first match or **TAG\_NULL** if no match is found.</span></span>

## <a name="requirements"></a><span data-ttu-id="e27be-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e27be-121">Requirements</span></span>



| <span data-ttu-id="e27be-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e27be-122">Requirement</span></span> | <span data-ttu-id="e27be-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e27be-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e27be-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e27be-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e27be-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e27be-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e27be-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e27be-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e27be-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e27be-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e27be-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e27be-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e27be-129"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e27be-129"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e27be-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e27be-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e27be-131">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="e27be-131">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> </dl>

 

 




