---
Description: Recupera o valor QWORD para o TAGID especificado.
ms.assetid: 5fa94a95-c7f3-477b-ab7c-931e8d62d501
title: Função SdbReadQWORDTag
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 15227f3d7c3177a226f1b3cc77fc78efd34379d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369886"
---
# <a name="sdbreadqwordtag-function"></a><span data-ttu-id="2cfa7-103">Função SdbReadQWORDTag</span><span class="sxs-lookup"><span data-stu-id="2cfa7-103">SdbReadQWORDTag function</span></span>

<span data-ttu-id="2cfa7-104">Recupera o valor **QWORD** para o **TagId** especificado.</span><span class="sxs-lookup"><span data-stu-id="2cfa7-104">Retrieves the **QWORD** value for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cfa7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2cfa7-105">Syntax</span></span>


```C++
ULONGLONG WINAPI SdbReadQWORDTag(
  _In_ PDB       pdb,
  _In_ TAGID     tiWhich,
  _In_ ULONGLONG qwDefault
);
```



## <a name="parameters"></a><span data-ttu-id="2cfa7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2cfa7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cfa7-107">*PDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2cfa7-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cfa7-108">Um identificador para o banco de dados de Shim.</span><span class="sxs-lookup"><span data-stu-id="2cfa7-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="2cfa7-109">*tiWhich* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2cfa7-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cfa7-110">O **TagId** que corresponde aos dados a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="2cfa7-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="2cfa7-111">*qwDefault* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2cfa7-111">*qwDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cfa7-112">O valor padrão a ser retornado em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="2cfa7-112">The default value to be returned on failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cfa7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2cfa7-113">Return value</span></span>

<span data-ttu-id="2cfa7-114">A função retorna o valor em êxito ou *qwDefault* em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="2cfa7-114">The function returns the value on success or *qwDefault* on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cfa7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cfa7-115">Requirements</span></span>



| <span data-ttu-id="2cfa7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cfa7-116">Requirement</span></span> | <span data-ttu-id="2cfa7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2cfa7-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cfa7-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2cfa7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2cfa7-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2cfa7-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2cfa7-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2cfa7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2cfa7-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2cfa7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2cfa7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2cfa7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cfa7-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cfa7-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cfa7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="2cfa7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cfa7-125">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="2cfa7-125">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="2cfa7-126">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="2cfa7-126">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="2cfa7-127">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="2cfa7-127">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="2cfa7-128">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="2cfa7-128">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




