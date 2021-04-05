---
description: A função GetDwordFromBlob recupera o valor de DWORD nomeado de um BLOB.
ms.assetid: edad74a7-b726-46d9-b49f-9984272d0a29
title: Função GetDwordFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDwordFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 064985f0f3b9a235dc1c00d683fe4b11371df87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089966"
---
# <a name="getdwordfromblob-function"></a><span data-ttu-id="87de9-103">Função GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="87de9-103">GetDwordFromBlob function</span></span>

<span data-ttu-id="87de9-104">A função **GetDwordFromBlob** recupera o valor de **DWORD** nomeado de um blob.</span><span class="sxs-lookup"><span data-stu-id="87de9-104">The **GetDwordFromBlob** function retrieves the named **DWORD** value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="87de9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87de9-105">Syntax</span></span>


```C++
DWORD GetDwordFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       DWORD *pDword
);
```



## <a name="parameters"></a><span data-ttu-id="87de9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87de9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87de9-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87de9-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87de9-108">Identificador para um BLOB.</span><span class="sxs-lookup"><span data-stu-id="87de9-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="87de9-109">*pOwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87de9-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87de9-110">Ponteiro para o nome do proprietário do BLOB.</span><span class="sxs-lookup"><span data-stu-id="87de9-110">Pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="87de9-111">*pCategoryName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87de9-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87de9-112">Ponteiro para o nome da categoria de BLOB.</span><span class="sxs-lookup"><span data-stu-id="87de9-112">Pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="87de9-113">*pTagName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87de9-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87de9-114">Ponteiro para o nome da marca de BLOB.</span><span class="sxs-lookup"><span data-stu-id="87de9-114">Pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="87de9-115">*pDword* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="87de9-115">*pDword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87de9-116">Ponteiro para o valor **DWORD** do blob.</span><span class="sxs-lookup"><span data-stu-id="87de9-116">Pointer to the **DWORD** value of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87de9-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87de9-117">Return value</span></span>

<span data-ttu-id="87de9-118">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="87de9-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="87de9-119">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que descreve o erro.</span><span class="sxs-lookup"><span data-stu-id="87de9-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="87de9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87de9-120">Requirements</span></span>



| <span data-ttu-id="87de9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="87de9-121">Requirement</span></span> | <span data-ttu-id="87de9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="87de9-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87de9-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87de9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="87de9-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="87de9-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="87de9-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87de9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="87de9-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="87de9-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="87de9-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="87de9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="87de9-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="87de9-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="87de9-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87de9-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="87de9-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87de9-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="87de9-131">DLL</span><span class="sxs-lookup"><span data-stu-id="87de9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87de9-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87de9-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87de9-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="87de9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87de9-134">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="87de9-134">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="87de9-135">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="87de9-135">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="87de9-136">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="87de9-136">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="87de9-137">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="87de9-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="87de9-138">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="87de9-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="87de9-139">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="87de9-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="87de9-140">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="87de9-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="87de9-141">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="87de9-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="87de9-142">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="87de9-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="87de9-143">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="87de9-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




