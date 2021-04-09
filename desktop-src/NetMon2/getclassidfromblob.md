---
description: A função GetClassIDFromBlob recupera um valor de identificador de classe nomeado de um BLOB.
ms.assetid: fef29a42-ccd3-4655-958c-d150e5bcd0d7
title: Função GetClassIDFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetClassIDFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 70122422c47a986058322ca8d17082093e02a4b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089968"
---
# <a name="getclassidfromblob-function"></a><span data-ttu-id="c7ddd-103">Função GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="c7ddd-103">GetClassIDFromBlob function</span></span>

<span data-ttu-id="c7ddd-104">A função **GetClassIDFromBlob** recupera um valor de identificador de classe nomeado de um blob.</span><span class="sxs-lookup"><span data-stu-id="c7ddd-104">The **GetClassIDFromBlob** function retrieves a named class identifier value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7ddd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7ddd-105">Syntax</span></span>


```C++
DWORD GetClassIDFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="c7ddd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7ddd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7ddd-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c7ddd-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7ddd-108">Identificador para um BLOB.</span><span class="sxs-lookup"><span data-stu-id="c7ddd-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="c7ddd-109">*pOwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c7ddd-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7ddd-110">Ponteiro para o nome do proprietário do BLOB.</span><span class="sxs-lookup"><span data-stu-id="c7ddd-110">Pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="c7ddd-111">*pCategoryName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c7ddd-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7ddd-112">Ponteiro para o nome da categoria de BLOB.</span><span class="sxs-lookup"><span data-stu-id="c7ddd-112">Pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="c7ddd-113">*pTagName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c7ddd-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7ddd-114">Ponteiro para o nome da marca de BLOB.</span><span class="sxs-lookup"><span data-stu-id="c7ddd-114">Pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="c7ddd-115">*pCLSID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c7ddd-115">*pClsID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7ddd-116">Ponteiro para o identificador de classe de BLOB.</span><span class="sxs-lookup"><span data-stu-id="c7ddd-116">Pointer to the BLOB class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7ddd-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7ddd-117">Return value</span></span>

<span data-ttu-id="c7ddd-118">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="c7ddd-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c7ddd-119">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que descreve o erro.</span><span class="sxs-lookup"><span data-stu-id="c7ddd-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7ddd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7ddd-120">Requirements</span></span>



| <span data-ttu-id="c7ddd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7ddd-121">Requirement</span></span> | <span data-ttu-id="c7ddd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c7ddd-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7ddd-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7ddd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c7ddd-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c7ddd-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c7ddd-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7ddd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c7ddd-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c7ddd-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c7ddd-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c7ddd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7ddd-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7ddd-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="c7ddd-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7ddd-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7ddd-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7ddd-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="c7ddd-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c7ddd-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7ddd-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7ddd-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7ddd-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7ddd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7ddd-134">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="c7ddd-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="c7ddd-135">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="c7ddd-135">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="c7ddd-136">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="c7ddd-136">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="c7ddd-137">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="c7ddd-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="c7ddd-138">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="c7ddd-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="c7ddd-139">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="c7ddd-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="c7ddd-140">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="c7ddd-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="c7ddd-141">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="c7ddd-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="c7ddd-142">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="c7ddd-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="c7ddd-143">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="c7ddd-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




