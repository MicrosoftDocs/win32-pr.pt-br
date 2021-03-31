---
description: A função GetNPPPatternFilterFromBlob recupera o filtro de correspondência de padrão de um BLOB específico.
ms.assetid: b17cde55-8abb-4699-960f-676cbbb24326
title: Função GetNPPPatternFilterFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPPatternFilterFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5758c53fe21231d300058a9168e556e9f9ceaa43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646795"
---
# <a name="getnpppatternfilterfromblob-function"></a><span data-ttu-id="5257f-103">Função GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="5257f-103">GetNPPPatternFilterFromBlob function</span></span>

<span data-ttu-id="5257f-104">A função **GetNPPPatternFilterFromBlob** recupera o filtro de correspondência de padrão de um blob específico.</span><span class="sxs-lookup"><span data-stu-id="5257f-104">The **GetNPPPatternFilterFromBlob** function retrieves the pattern match filter from a specific BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="5257f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5257f-105">Syntax</span></span>


```C++
DWORD GetNPPPatternFilterFromBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="5257f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5257f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5257f-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5257f-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5257f-108">Identificador para o BLOB.</span><span class="sxs-lookup"><span data-stu-id="5257f-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="5257f-109">*pExpression* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5257f-109">*pExpression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5257f-110">Ponteiro para a expressão de filtro.</span><span class="sxs-lookup"><span data-stu-id="5257f-110">Pointer to the filter expression.</span></span>

</dd> <dt>

<span data-ttu-id="5257f-111">*hErrorBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5257f-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5257f-112">Identificador para um BLOB de erro que especifica onde ocorreu o erro (se houver) no BLOB original.</span><span class="sxs-lookup"><span data-stu-id="5257f-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5257f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5257f-113">Return value</span></span>

<span data-ttu-id="5257f-114">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="5257f-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5257f-115">Se a função não for bem-sucedida, o valor de retorno será um NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="5257f-115">If the function is unsuccessful, the return value is a NMERR that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="5257f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="5257f-116">Remarks</span></span>

<span data-ttu-id="5257f-117">As informações de filtro de correspondência de padrão são armazenadas na categoria de **configuração** do blob.</span><span class="sxs-lookup"><span data-stu-id="5257f-117">The pattern match filter information is stored in the **Config** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="5257f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5257f-118">Requirements</span></span>



| <span data-ttu-id="5257f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5257f-119">Requirement</span></span> | <span data-ttu-id="5257f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5257f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5257f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5257f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5257f-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5257f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5257f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5257f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5257f-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5257f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5257f-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5257f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5257f-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5257f-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="5257f-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5257f-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="5257f-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5257f-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="5257f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5257f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5257f-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5257f-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5257f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="5257f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5257f-132">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="5257f-132">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="5257f-133">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="5257f-133">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="5257f-134">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="5257f-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="5257f-135">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="5257f-135">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="5257f-136">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="5257f-136">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="5257f-137">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="5257f-137">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="5257f-138">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="5257f-138">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="5257f-139">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="5257f-139">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="5257f-140">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="5257f-140">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="5257f-141">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="5257f-141">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




