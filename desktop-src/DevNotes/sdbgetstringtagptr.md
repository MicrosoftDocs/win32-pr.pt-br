---
description: Recupera os dados de cadeia de caracteres para o TAGID especificado.
ms.assetid: c558e0bb-7e35-4298-93fb-400db00a2972
title: Função SdbGetStringTagPtr
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetStringTagPtr
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 56c80c4000df95fe13486d95bb872bfc39274389
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920344"
---
# <a name="sdbgetstringtagptr-function"></a><span data-ttu-id="94e77-103">Função SdbGetStringTagPtr</span><span class="sxs-lookup"><span data-stu-id="94e77-103">SdbGetStringTagPtr function</span></span>

<span data-ttu-id="94e77-104">Recupera os dados de cadeia de caracteres para o **TagId** especificado.</span><span class="sxs-lookup"><span data-stu-id="94e77-104">Retrieves the string data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="94e77-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94e77-105">Syntax</span></span>


```C++
LPTSTR WINAPI SdbGetStringTagPtr(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="94e77-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94e77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94e77-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="94e77-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94e77-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="94e77-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="94e77-109">*tiWhich* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="94e77-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94e77-110">O **TagId** que corresponde aos dados de cadeia de caracteres a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="94e77-110">The **TAGID** that corresponds to the string data to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94e77-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="94e77-111">Return value</span></span>

<span data-ttu-id="94e77-112">A função retornará um ponteiro para os dados da cadeia de caracteres ou **NULL** se **TagId** for inválido ou não for do tipo marca de tipo **\_ cadeia de \_ caracteres** ou **tipo de marca \_ \_ STRINGREF**.</span><span class="sxs-lookup"><span data-stu-id="94e77-112">The function returns a pointer to the string data or **NULL** if the **TAGID** is invalid or not of type **TAG\_TYPE\_STRING** or **TAG\_TYPE\_STRINGREF**.</span></span>

## <a name="requirements"></a><span data-ttu-id="94e77-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94e77-113">Requirements</span></span>



| <span data-ttu-id="94e77-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="94e77-114">Requirement</span></span> | <span data-ttu-id="94e77-115">Valor</span><span class="sxs-lookup"><span data-stu-id="94e77-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94e77-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94e77-116">Minimum supported client</span></span><br/> | <span data-ttu-id="94e77-117">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="94e77-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="94e77-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94e77-118">Minimum supported server</span></span><br/> | <span data-ttu-id="94e77-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="94e77-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="94e77-120">DLL</span><span class="sxs-lookup"><span data-stu-id="94e77-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94e77-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94e77-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94e77-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="94e77-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94e77-123">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="94e77-123">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="94e77-124">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="94e77-124">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="94e77-125">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="94e77-125">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="94e77-126">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="94e77-126">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




