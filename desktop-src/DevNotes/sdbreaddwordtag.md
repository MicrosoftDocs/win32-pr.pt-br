---
Description: Recupera o valor DWORD para o TAGID especificado.
ms.assetid: 6610e101-9068-4812-b0ca-528658b62535
title: Função SdbReadDWORDTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0f1f7acc113bc40388d62927b6d98f8ff7bdebf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086305"
---
# <a name="sdbreaddwordtag-function"></a><span data-ttu-id="0585c-103">Função SdbReadDWORDTag</span><span class="sxs-lookup"><span data-stu-id="0585c-103">SdbReadDWORDTag function</span></span>

<span data-ttu-id="0585c-104">Recupera o valor **DWORD** para o **TagId** especificado.</span><span class="sxs-lookup"><span data-stu-id="0585c-104">Retrieves the **DWORD** value for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0585c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0585c-105">Syntax</span></span>


```C++
DWORD WINAPI SdbReadDWORDTag(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich,
  _In_ DWORD dwDefault
);
```



## <a name="parameters"></a><span data-ttu-id="0585c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0585c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0585c-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0585c-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0585c-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="0585c-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="0585c-109">*tiWhich* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0585c-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0585c-110">O **TagId** que corresponde aos dados a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="0585c-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="0585c-111">*dwDefault* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0585c-111">*dwDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0585c-112">O valor padrão a ser retornado em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="0585c-112">The default value to be returned on failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0585c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0585c-113">Return value</span></span>

<span data-ttu-id="0585c-114">A função retorna o valor em êxito ou *dwDefault* em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="0585c-114">The function returns the value on success or *dwDefault* on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="0585c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0585c-115">Requirements</span></span>



| <span data-ttu-id="0585c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0585c-116">Requirement</span></span> | <span data-ttu-id="0585c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0585c-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0585c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0585c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0585c-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0585c-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0585c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0585c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0585c-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0585c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0585c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0585c-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0585c-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0585c-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0585c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0585c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0585c-125">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="0585c-125">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="0585c-126">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="0585c-126">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="0585c-127">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="0585c-127">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="0585c-128">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="0585c-128">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




