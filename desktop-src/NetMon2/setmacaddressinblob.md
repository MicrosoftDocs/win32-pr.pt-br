---
description: A função SetMacAddressInBlob define o endereço MAC solicitado de um BLOB.
ms.assetid: f44d0cec-ced7-4d2a-a58e-aeb476bfe800
title: Função SetMacAddressInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetMacAddressInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2183f5635dcdb15362a86a77ae2b3c109c71dbd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829179"
---
# <a name="setmacaddressinblob-function"></a><span data-ttu-id="c374a-103">Função SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="c374a-103">SetMacAddressInBlob function</span></span>

<span data-ttu-id="c374a-104">A função **SetMacAddressInBlob** define o endereço MAC solicitado de um blob.</span><span class="sxs-lookup"><span data-stu-id="c374a-104">The **SetMacAddressInBlob** function sets the requested MAC address of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="c374a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c374a-105">Syntax</span></span>


```C++
DWORD SetMacAddressInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const BYTE  *pMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="c374a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c374a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c374a-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c374a-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c374a-108">Identificador para o BLOB que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="c374a-108">Handle to the BLOB being set.</span></span>

</dd> <dt>

<span data-ttu-id="c374a-109">*pOwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c374a-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c374a-110">Ponteiro para o nome do **proprietário** do blob que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="c374a-110">Pointer to the BLOB **Owner** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="c374a-111">*pCategoryName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c374a-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c374a-112">Ponteiro para o nome da **categoria** de BLOB que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="c374a-112">Pointer to the BLOB **Category** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="c374a-113">*pTagName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c374a-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c374a-114">Ponteiro para o nome da **marca** de BLOB que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="c374a-114">Pointer to the BLOB **Tag** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="c374a-115">*pMacAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c374a-115">*pMacAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c374a-116">Ponteiro para o endereço MAC do BLOB que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="c374a-116">Pointer to the MAC address of the BLOB being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c374a-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c374a-117">Return value</span></span>

<span data-ttu-id="c374a-118">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="c374a-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c374a-119">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="c374a-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c374a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c374a-120">Requirements</span></span>



| <span data-ttu-id="c374a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c374a-121">Requirement</span></span> | <span data-ttu-id="c374a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c374a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c374a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c374a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c374a-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c374a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c374a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c374a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c374a-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c374a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c374a-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c374a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c374a-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c374a-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="c374a-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c374a-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="c374a-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c374a-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="c374a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c374a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c374a-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c374a-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c374a-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="c374a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c374a-134">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="c374a-134">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="c374a-135">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="c374a-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="c374a-136">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="c374a-136">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="c374a-137">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="c374a-137">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="c374a-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="c374a-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="c374a-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="c374a-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="c374a-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="c374a-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="c374a-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="c374a-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="c374a-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="c374a-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




