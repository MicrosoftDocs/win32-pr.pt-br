---
description: Recupera um valor booliano nomeado de um BLOB.
ms.assetid: 26acfd2a-5b17-47ad-8f7b-7793174a13c3
title: Função GetBoolFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBoolFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e09a35f71181343cd401b3288c2b2c74a46f677b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759622"
---
# <a name="getboolfromblob-function"></a><span data-ttu-id="5ebbb-103">Função GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="5ebbb-103">GetBoolFromBlob function</span></span>

<span data-ttu-id="5ebbb-104">A função **GetBoolFromBlob** recupera um valor booliano nomeado de um blob.</span><span class="sxs-lookup"><span data-stu-id="5ebbb-104">The **GetBoolFromBlob** function retrieves a named Boolean value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ebbb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ebbb-105">Syntax</span></span>


```C++
DWORD GetBoolFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       BOOL  *pBool
);
```



## <a name="parameters"></a><span data-ttu-id="5ebbb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ebbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ebbb-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ebbb-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ebbb-108">Um identificador para um BLOB.</span><span class="sxs-lookup"><span data-stu-id="5ebbb-108">A handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="5ebbb-109">*pOwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ebbb-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ebbb-110">Um ponteiro para o nome do proprietário do BLOB.</span><span class="sxs-lookup"><span data-stu-id="5ebbb-110">A pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="5ebbb-111">*pCategoryName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ebbb-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ebbb-112">Um ponteiro para o nome da categoria de BLOB.</span><span class="sxs-lookup"><span data-stu-id="5ebbb-112">A pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="5ebbb-113">*pTagName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5ebbb-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ebbb-114">Um ponteiro para o nome da marca de BLOB.</span><span class="sxs-lookup"><span data-stu-id="5ebbb-114">A pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="5ebbb-115">*pBool* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5ebbb-115">*pBool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ebbb-116">Ponteiro para o valor booliano do BLOB.</span><span class="sxs-lookup"><span data-stu-id="5ebbb-116">Pointer to the Boolean value of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ebbb-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5ebbb-117">Return value</span></span>

<span data-ttu-id="5ebbb-118">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="5ebbb-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5ebbb-119">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que descreve o erro.</span><span class="sxs-lookup"><span data-stu-id="5ebbb-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ebbb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ebbb-120">Requirements</span></span>



| <span data-ttu-id="5ebbb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ebbb-121">Requirement</span></span> | <span data-ttu-id="5ebbb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5ebbb-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ebbb-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ebbb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5ebbb-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5ebbb-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5ebbb-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ebbb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5ebbb-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5ebbb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5ebbb-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5ebbb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ebbb-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ebbb-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="5ebbb-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5ebbb-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="5ebbb-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ebbb-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="5ebbb-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5ebbb-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ebbb-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ebbb-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ebbb-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ebbb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ebbb-134">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="5ebbb-134">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="5ebbb-135">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="5ebbb-135">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="5ebbb-136">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="5ebbb-136">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="5ebbb-137">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="5ebbb-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="5ebbb-138">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="5ebbb-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="5ebbb-139">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="5ebbb-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="5ebbb-140">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="5ebbb-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="5ebbb-141">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="5ebbb-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="5ebbb-142">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="5ebbb-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="5ebbb-143">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="5ebbb-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




