---
description: A função GetNPPTriggerFromBlob recupera o gatilho do BLOB fornecido.
ms.assetid: 48a27cf3-57b0-4241-a925-4209e0d384e2
title: Função GetNPPTriggerFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPTriggerFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 11622078354012de4796ddd43a698ac812951742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779600"
---
# <a name="getnpptriggerfromblob-function"></a><span data-ttu-id="40f74-103">Função GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="40f74-103">GetNPPTriggerFromBlob function</span></span>

<span data-ttu-id="40f74-104">A função **GetNPPTriggerFromBlob** recupera o gatilho do blob fornecido.</span><span class="sxs-lookup"><span data-stu-id="40f74-104">The **GetNPPTriggerFromBlob** function retrieves the trigger from the given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="40f74-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40f74-105">Syntax</span></span>


```C++
DWORD GetNPPTriggerFromBlob(
  _In_  HBLOB     hBlob,
  _Out_ LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="40f74-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40f74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40f74-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="40f74-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40f74-108">Identificador para o BLOB.</span><span class="sxs-lookup"><span data-stu-id="40f74-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="40f74-109">*pTrigger* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="40f74-109">*pTrigger* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40f74-110">Ponteiro para o valor do gatilho.</span><span class="sxs-lookup"><span data-stu-id="40f74-110">Pointer to the trigger value.</span></span>

</dd> <dt>

<span data-ttu-id="40f74-111">*hErrorBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="40f74-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40f74-112">Identificador para um BLOB de erro que especifica onde ocorreu o erro (se houver) no BLOB original.</span><span class="sxs-lookup"><span data-stu-id="40f74-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40f74-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40f74-113">Return value</span></span>

<span data-ttu-id="40f74-114">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="40f74-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="40f74-115">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="40f74-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="40f74-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="40f74-116">Remarks</span></span>

<span data-ttu-id="40f74-117">As informações do gatilho são armazenadas na categoria de **gatilho** do blob.</span><span class="sxs-lookup"><span data-stu-id="40f74-117">The trigger information is stored in the **Trigger** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="40f74-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40f74-118">Requirements</span></span>



| <span data-ttu-id="40f74-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="40f74-119">Requirement</span></span> | <span data-ttu-id="40f74-120">Valor</span><span class="sxs-lookup"><span data-stu-id="40f74-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40f74-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40f74-121">Minimum supported client</span></span><br/> | <span data-ttu-id="40f74-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="40f74-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="40f74-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40f74-123">Minimum supported server</span></span><br/> | <span data-ttu-id="40f74-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="40f74-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="40f74-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="40f74-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="40f74-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="40f74-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="40f74-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="40f74-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="40f74-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40f74-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="40f74-129">DLL</span><span class="sxs-lookup"><span data-stu-id="40f74-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40f74-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40f74-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40f74-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="40f74-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40f74-132">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="40f74-132">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="40f74-133">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="40f74-133">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="40f74-134">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="40f74-134">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="40f74-135">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="40f74-135">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="40f74-136">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="40f74-136">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="40f74-137">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="40f74-137">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="40f74-138">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="40f74-138">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="40f74-139">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="40f74-139">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="40f74-140">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="40f74-140">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




