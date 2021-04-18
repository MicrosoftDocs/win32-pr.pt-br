---
description: A função SetDwordInBlob define o valor de DWORD nomeado de um BLOB.
ms.assetid: 9174cd5c-4442-4fbe-8dc7-f8a74e1cc85d
title: Função SetDwordInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDwordInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9bca0efe61824c6fb8dd41b0b241791b6303799d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757233"
---
# <a name="setdwordinblob-function"></a><span data-ttu-id="e6481-103">Função SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="e6481-103">SetDwordInBlob function</span></span>

<span data-ttu-id="e6481-104">A função **SetDwordInBlob** define o valor de **DWORD** nomeado de um blob.</span><span class="sxs-lookup"><span data-stu-id="e6481-104">The **SetDwordInBlob** function sets the named **DWORD** value of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6481-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6481-105">Syntax</span></span>


```C++
DWORD SetDwordInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       DWORD Dword
);
```



## <a name="parameters"></a><span data-ttu-id="e6481-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6481-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6481-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6481-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6481-108">Identificador para um BLOB que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="e6481-108">Handle to a BLOB being set.</span></span>

</dd> <dt>

<span data-ttu-id="e6481-109">*pOwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6481-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6481-110">Ponteiro para o nome do **proprietário** do blob que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="e6481-110">Pointer to the BLOB **Owner** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="e6481-111">*pCategoryName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6481-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6481-112">Ponteiro para o nome da **categoria** de BLOB que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="e6481-112">Pointer to the BLOB **Category** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="e6481-113">*pTagName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6481-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6481-114">Ponteiro para o nome da **marca** de BLOB que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="e6481-114">Pointer to the BLOB **Tag** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="e6481-115">*Valor DWORD* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6481-115">*Dword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6481-116">Valor **DWORD** do blob que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="e6481-116">**DWORD** value of the BLOB being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6481-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6481-117">Return value</span></span>

<span data-ttu-id="e6481-118">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="e6481-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e6481-119">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="e6481-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6481-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6481-120">Requirements</span></span>



| <span data-ttu-id="e6481-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6481-121">Requirement</span></span> | <span data-ttu-id="e6481-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e6481-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6481-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6481-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e6481-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e6481-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e6481-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6481-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e6481-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e6481-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e6481-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e6481-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6481-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6481-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="e6481-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6481-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="e6481-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6481-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="e6481-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e6481-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6481-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6481-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6481-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6481-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6481-134">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="e6481-134">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="e6481-135">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="e6481-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="e6481-136">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="e6481-136">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="e6481-137">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="e6481-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="e6481-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="e6481-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="e6481-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="e6481-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="e6481-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="e6481-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="e6481-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="e6481-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="e6481-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="e6481-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




