---
description: A função SetBoolInBlob define um valor booliano em um determinado local dentro de um BLOB.
ms.assetid: 354d22be-b8c4-4068-8356-19b30ac188d0
title: Função SetBoolInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetBoolInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5cfbb9a3410d511ab143f1d77584a0144435c230
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505723"
---
# <a name="setboolinblob-function"></a><span data-ttu-id="81d4b-103">Função SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="81d4b-103">SetBoolInBlob function</span></span>

<span data-ttu-id="81d4b-104">A função **SetBoolInBlob** define um valor booliano em um determinado local dentro de um blob.</span><span class="sxs-lookup"><span data-stu-id="81d4b-104">The **SetBoolInBlob** function sets a Boolean value at a given location within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="81d4b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81d4b-105">Syntax</span></span>


```C++
DWORD SetBoolInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       BOOL  Bool
);
```



## <a name="parameters"></a><span data-ttu-id="81d4b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81d4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81d4b-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="81d4b-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d4b-108">Identificador para um BLOB.</span><span class="sxs-lookup"><span data-stu-id="81d4b-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="81d4b-109">*pOwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="81d4b-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d4b-110">Ponteiro para o nome do **proprietário** do blob.</span><span class="sxs-lookup"><span data-stu-id="81d4b-110">Pointer to the BLOB **Owner** name.</span></span>

</dd> <dt>

<span data-ttu-id="81d4b-111">*pCategoryName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="81d4b-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d4b-112">Ponteiro para o nome da **categoria** de BLOB.</span><span class="sxs-lookup"><span data-stu-id="81d4b-112">Pointer to the BLOB **Category** name.</span></span>

</dd> <dt>

<span data-ttu-id="81d4b-113">*pTagName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="81d4b-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d4b-114">Ponteiro para o nome da **marca** de BLOB.</span><span class="sxs-lookup"><span data-stu-id="81d4b-114">Pointer to the BLOB **Tag** name.</span></span>

</dd> <dt>

<span data-ttu-id="81d4b-115">*Bool* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="81d4b-115">*Bool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d4b-116">Valor booliano definido no local especificado.</span><span class="sxs-lookup"><span data-stu-id="81d4b-116">Boolean value that is set at the given location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81d4b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="81d4b-117">Return value</span></span>

<span data-ttu-id="81d4b-118">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="81d4b-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="81d4b-119">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="81d4b-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="81d4b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81d4b-120">Requirements</span></span>



| <span data-ttu-id="81d4b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="81d4b-121">Requirement</span></span> | <span data-ttu-id="81d4b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="81d4b-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81d4b-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81d4b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="81d4b-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="81d4b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="81d4b-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81d4b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="81d4b-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="81d4b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="81d4b-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="81d4b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="81d4b-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="81d4b-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="81d4b-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81d4b-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="81d4b-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81d4b-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="81d4b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="81d4b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81d4b-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81d4b-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81d4b-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="81d4b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81d4b-134">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="81d4b-134">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="81d4b-135">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="81d4b-135">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="81d4b-136">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="81d4b-136">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="81d4b-137">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="81d4b-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="81d4b-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="81d4b-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="81d4b-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="81d4b-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="81d4b-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="81d4b-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="81d4b-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="81d4b-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="81d4b-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="81d4b-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




