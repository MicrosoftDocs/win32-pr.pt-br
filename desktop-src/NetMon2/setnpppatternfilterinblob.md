---
description: Define o filtro de correspondência de padrões de BLOB.
ms.assetid: 44e7c67a-f430-4d68-bc7f-f6bbd5b9e5a9
title: Função SetNPPPatternFilterInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPPatternFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: b2e8989264a042368b37926bbb502f48ab2fb04b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501888"
---
# <a name="setnpppatternfilterinblob-function"></a><span data-ttu-id="73c33-103">Função SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="73c33-103">SetNPPPatternFilterInBlob function</span></span>

<span data-ttu-id="73c33-104">A função **SetNPPPatternFilterInBlob** define o filtro de correspondência de padrões de BLOB.</span><span class="sxs-lookup"><span data-stu-id="73c33-104">The **SetNPPPatternFilterInBlob** function sets the BLOB pattern match filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="73c33-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73c33-105">Syntax</span></span>


```C++
DWORD SetNPPPatternFilterInBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="73c33-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73c33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73c33-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73c33-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73c33-108">O identificador para o BLOB.</span><span class="sxs-lookup"><span data-stu-id="73c33-108">The handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="73c33-109">*pExpression* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73c33-109">*pExpression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73c33-110">Um ponteiro para uma estrutura de [expressão](expression.md) que define a expressão de filtro que está sendo definida.</span><span class="sxs-lookup"><span data-stu-id="73c33-110">A pointer to an [EXPRESSION](expression.md) structure that defines the filter expression being set.</span></span>

</dd> <dt>

<span data-ttu-id="73c33-111">*hErrorBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="73c33-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73c33-112">O identificador para um BLOB de erro que especifica onde ocorreu o erro (se houver) no BLOB original.</span><span class="sxs-lookup"><span data-stu-id="73c33-112">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73c33-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73c33-113">Return value</span></span>

<span data-ttu-id="73c33-114">Se a função **SetNPPPatternFilterInBlob** for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="73c33-114">If the **SetNPPPatternFilterInBlob** function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="73c33-115">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="73c33-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="73c33-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="73c33-116">Remarks</span></span>

<span data-ttu-id="73c33-117">O padrão corresponde os dados de filtro armazenados na categoria de **configuração** do blob.</span><span class="sxs-lookup"><span data-stu-id="73c33-117">The pattern match filter data stored in the **Config** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="73c33-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73c33-118">Requirements</span></span>



| <span data-ttu-id="73c33-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="73c33-119">Requirement</span></span> | <span data-ttu-id="73c33-120">Valor</span><span class="sxs-lookup"><span data-stu-id="73c33-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73c33-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73c33-121">Minimum supported client</span></span><br/> | <span data-ttu-id="73c33-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="73c33-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="73c33-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73c33-123">Minimum supported server</span></span><br/> | <span data-ttu-id="73c33-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="73c33-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="73c33-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="73c33-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="73c33-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="73c33-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="73c33-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73c33-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="73c33-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73c33-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="73c33-129">DLL</span><span class="sxs-lookup"><span data-stu-id="73c33-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73c33-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73c33-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73c33-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="73c33-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73c33-132">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="73c33-132">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="73c33-133">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="73c33-133">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="73c33-134">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="73c33-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="73c33-135">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="73c33-135">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="73c33-136">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="73c33-136">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="73c33-137">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="73c33-137">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="73c33-138">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="73c33-138">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="73c33-139">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="73c33-139">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="73c33-140">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="73c33-140">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




