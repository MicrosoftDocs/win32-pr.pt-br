---
description: Recupera os dados binários para o TAGID especificado.
ms.assetid: 18992406-67b4-4c48-9629-04d6bf1c5824
title: Função SdbGetBinaryTagData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetBinaryTagData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 028b073b149482b79b848216e44b8a425d6ffb56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762860"
---
# <a name="sdbgetbinarytagdata-function"></a><span data-ttu-id="3b2e6-103">Função SdbGetBinaryTagData</span><span class="sxs-lookup"><span data-stu-id="3b2e6-103">SdbGetBinaryTagData function</span></span>

<span data-ttu-id="3b2e6-104">Recupera os dados binários para o **TagId** especificado.</span><span class="sxs-lookup"><span data-stu-id="3b2e6-104">Retrieves the binary data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b2e6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b2e6-105">Syntax</span></span>


```C++
PVOID WINAPI SdbGetBinaryTagData(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="3b2e6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b2e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b2e6-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b2e6-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b2e6-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="3b2e6-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="3b2e6-109">*tiWhich* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b2e6-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b2e6-110">O **TagId** que corresponde aos dados a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="3b2e6-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b2e6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b2e6-111">Return value</span></span>

<span data-ttu-id="3b2e6-112">A função retornará um ponteiro para os dados binários ou **nulo** se o **TagId** for inválido.</span><span class="sxs-lookup"><span data-stu-id="3b2e6-112">The function returns a pointer to the binary data or **NULL** if the **TAGID** is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b2e6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b2e6-113">Requirements</span></span>



| <span data-ttu-id="3b2e6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b2e6-114">Requirement</span></span> | <span data-ttu-id="3b2e6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3b2e6-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b2e6-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b2e6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3b2e6-117">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3b2e6-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3b2e6-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b2e6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3b2e6-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3b2e6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3b2e6-120">DLL</span><span class="sxs-lookup"><span data-stu-id="3b2e6-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b2e6-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b2e6-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b2e6-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b2e6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b2e6-123">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="3b2e6-123">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="3b2e6-124">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="3b2e6-124">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="3b2e6-125">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="3b2e6-125">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="3b2e6-126">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="3b2e6-126">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




