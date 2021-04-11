---
description: Define o gatilho de BLOB.
ms.assetid: 88bfd5cd-f563-4d0c-81a3-54a846805b87
title: Função SetNPPTriggerInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPTriggerInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 05b8bb3f7f95dc3246ef10f3945b9ab0868550cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164620"
---
# <a name="setnpptriggerinblob-function"></a><span data-ttu-id="104d6-103">Função SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="104d6-103">SetNPPTriggerInBlob function</span></span>

<span data-ttu-id="104d6-104">A função **SetNPPTriggerInBlob** define o gatilho de BLOB.</span><span class="sxs-lookup"><span data-stu-id="104d6-104">The **SetNPPTriggerInBlob** function sets the BLOB trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="104d6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="104d6-105">Syntax</span></span>


```C++
DWORD SetNPPTriggerInBlob(
  _In_  HBLOB     hBlob,
  _In_  LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="104d6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="104d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="104d6-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="104d6-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="104d6-108">O identificador para o BLOB.</span><span class="sxs-lookup"><span data-stu-id="104d6-108">The handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="104d6-109">*pTrigger* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="104d6-109">*pTrigger* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="104d6-110">Um ponteiro para o valor do gatilho.</span><span class="sxs-lookup"><span data-stu-id="104d6-110">A pointer to the trigger value.</span></span>

</dd> <dt>

<span data-ttu-id="104d6-111">*hErrorBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="104d6-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="104d6-112">O identificador para um BLOB de erro que especifica onde ocorreu o erro (se houver) no BLOB original.</span><span class="sxs-lookup"><span data-stu-id="104d6-112">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="104d6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="104d6-113">Return value</span></span>

<span data-ttu-id="104d6-114">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="104d6-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="104d6-115">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="104d6-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="104d6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="104d6-116">Remarks</span></span>

<span data-ttu-id="104d6-117">Esses dados de gatilho são armazenados na categoria de **gatilho** do blob.</span><span class="sxs-lookup"><span data-stu-id="104d6-117">This trigger data is stored in the **Trigger** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="104d6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="104d6-118">Requirements</span></span>



| <span data-ttu-id="104d6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="104d6-119">Requirement</span></span> | <span data-ttu-id="104d6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="104d6-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="104d6-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="104d6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="104d6-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="104d6-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="104d6-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="104d6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="104d6-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="104d6-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="104d6-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="104d6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="104d6-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="104d6-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="104d6-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="104d6-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="104d6-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="104d6-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="104d6-129">DLL</span><span class="sxs-lookup"><span data-stu-id="104d6-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="104d6-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="104d6-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="104d6-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="104d6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="104d6-132">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="104d6-132">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="104d6-133">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="104d6-133">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="104d6-134">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="104d6-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="104d6-135">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="104d6-135">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="104d6-136">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="104d6-136">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="104d6-137">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="104d6-137">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="104d6-138">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="104d6-138">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="104d6-139">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="104d6-139">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="104d6-140">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="104d6-140">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




