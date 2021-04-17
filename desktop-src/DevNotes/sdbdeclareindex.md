---
description: Declara um novo índice no banco de dados especificado.
ms.assetid: 21a09201-8f84-4263-b258-77716826a3cd
title: Função SdbDeclareIndex
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbDeclareIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 68004a29d01288a2e1d177b8a33df32b919e73ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754901"
---
# <a name="sdbdeclareindex-function"></a><span data-ttu-id="99edc-103">Função SdbDeclareIndex</span><span class="sxs-lookup"><span data-stu-id="99edc-103">SdbDeclareIndex function</span></span>

<span data-ttu-id="99edc-104">Declara um novo índice no banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="99edc-104">Declares a new index in the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="99edc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99edc-105">Syntax</span></span>


```C++
BOOL WINAPI SdbDeclareIndex(
  _In_  PDB     pdb,
  _In_  TAG     tWhich,
  _In_  TAG     tKey,
  _In_  DWORD   dwEntries,
  _In_  BOOL    bUniqueKey,
  _Out_ INDEXID *piiIndex
);
```



## <a name="parameters"></a><span data-ttu-id="99edc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99edc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99edc-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99edc-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99edc-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="99edc-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="99edc-109">*tWhich* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99edc-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99edc-110">Esse parâmetro deve ser **uma \_ \_ lista de tipos de marca**.</span><span class="sxs-lookup"><span data-stu-id="99edc-110">This parameter must be **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="99edc-111">*tKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99edc-111">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99edc-112">A marca que especifica o tipo a ser usado como chave.</span><span class="sxs-lookup"><span data-stu-id="99edc-112">The TAG that specifies the type to be used as the key.</span></span> <span data-ttu-id="99edc-113">Esse parâmetro não pode ser uma **\_ \_ lista de tipos de marca**.</span><span class="sxs-lookup"><span data-stu-id="99edc-113">This parameter cannot be **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="99edc-114">*dwEntries* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99edc-114">*dwEntries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99edc-115">O número de entradas a serem alocadas no índice.</span><span class="sxs-lookup"><span data-stu-id="99edc-115">The number of entries to allocate in the index.</span></span>

</dd> <dt>

<span data-ttu-id="99edc-116">*bUniqueKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99edc-116">*bUniqueKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99edc-117">Se esse parâmetro for **true**, o índice será um índice de chave exclusiva.</span><span class="sxs-lookup"><span data-stu-id="99edc-117">If this parameter is **TRUE**, the index is a unique-key index.</span></span>

</dd> <dt>

<span data-ttu-id="99edc-118">*piiIndex* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="99edc-118">*piiIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99edc-119">A **IndexID** resultante do índice recentemente declarado.</span><span class="sxs-lookup"><span data-stu-id="99edc-119">The resulting **INDEXID** of the newly declared index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99edc-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99edc-120">Return value</span></span>

<span data-ttu-id="99edc-121">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="99edc-121">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="99edc-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="99edc-122">Remarks</span></span>

<span data-ttu-id="99edc-123">Chame essa função antes de gravar marcas no novo índice.</span><span class="sxs-lookup"><span data-stu-id="99edc-123">Call this function before writing tags to the new index.</span></span>

## <a name="requirements"></a><span data-ttu-id="99edc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99edc-124">Requirements</span></span>



| <span data-ttu-id="99edc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="99edc-125">Requirement</span></span> | <span data-ttu-id="99edc-126">Valor</span><span class="sxs-lookup"><span data-stu-id="99edc-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99edc-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99edc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="99edc-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99edc-128">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="99edc-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99edc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="99edc-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="99edc-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="99edc-131">DLL</span><span class="sxs-lookup"><span data-stu-id="99edc-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99edc-132"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99edc-132"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99edc-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="99edc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99edc-134">**INDEXid**</span><span class="sxs-lookup"><span data-stu-id="99edc-134">**INDEXID**</span></span>](indexid.md)
</dt> <dt>

[<span data-ttu-id="99edc-135">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="99edc-135">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="99edc-136">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="99edc-136">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="99edc-137">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="99edc-137">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




