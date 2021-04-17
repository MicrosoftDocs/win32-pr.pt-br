---
description: A função GetMacAddressFromBlob recupera o endereço MAC nomeado de um BLOB.
ms.assetid: 1769c92c-0946-447c-885a-fcf175fa1bf3
title: Função GetMacAddressFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetMacAddressFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 022d4f618c09652c368f6664b194b4ebafc81717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760226"
---
# <a name="getmacaddressfromblob-function"></a><span data-ttu-id="aa1ee-103">Função GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="aa1ee-103">GetMacAddressFromBlob function</span></span>

<span data-ttu-id="aa1ee-104">A função **GetMacAddressFromBlob** recupera o endereço MAC nomeado de um blob.</span><span class="sxs-lookup"><span data-stu-id="aa1ee-104">The **GetMacAddressFromBlob** function retrieves the named MAC address from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa1ee-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa1ee-105">Syntax</span></span>


```C++
DWORD GetMacAddressFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       BYTE  *pMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="aa1ee-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa1ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa1ee-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa1ee-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa1ee-108">Identificador para um BLOB.</span><span class="sxs-lookup"><span data-stu-id="aa1ee-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="aa1ee-109">*pOwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa1ee-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa1ee-110">Ponteiro para o nome do proprietário do BLOB.</span><span class="sxs-lookup"><span data-stu-id="aa1ee-110">Pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="aa1ee-111">*pCategoryName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa1ee-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa1ee-112">Ponteiro para o nome da categoria de BLOB.</span><span class="sxs-lookup"><span data-stu-id="aa1ee-112">Pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="aa1ee-113">*pTagName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa1ee-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa1ee-114">Ponteiro para o nome da marca de BLOB.</span><span class="sxs-lookup"><span data-stu-id="aa1ee-114">Pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="aa1ee-115">*pMacAddress* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="aa1ee-115">*pMacAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa1ee-116">Ponteiro para o endereço MAC do BLOB.</span><span class="sxs-lookup"><span data-stu-id="aa1ee-116">Pointer to the MAC address of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa1ee-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa1ee-117">Return value</span></span>

<span data-ttu-id="aa1ee-118">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="aa1ee-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="aa1ee-119">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que descreve o erro.</span><span class="sxs-lookup"><span data-stu-id="aa1ee-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa1ee-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa1ee-120">Requirements</span></span>



| <span data-ttu-id="aa1ee-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa1ee-121">Requirement</span></span> | <span data-ttu-id="aa1ee-122">Valor</span><span class="sxs-lookup"><span data-stu-id="aa1ee-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa1ee-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa1ee-123">Minimum supported client</span></span><br/> | <span data-ttu-id="aa1ee-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="aa1ee-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="aa1ee-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa1ee-125">Minimum supported server</span></span><br/> | <span data-ttu-id="aa1ee-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="aa1ee-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="aa1ee-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="aa1ee-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa1ee-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa1ee-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="aa1ee-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aa1ee-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="aa1ee-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa1ee-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="aa1ee-131">DLL</span><span class="sxs-lookup"><span data-stu-id="aa1ee-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa1ee-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa1ee-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa1ee-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa1ee-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa1ee-134">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="aa1ee-134">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="aa1ee-135">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="aa1ee-135">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="aa1ee-136">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="aa1ee-136">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="aa1ee-137">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="aa1ee-137">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="aa1ee-138">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="aa1ee-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="aa1ee-139">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="aa1ee-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="aa1ee-140">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="aa1ee-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="aa1ee-141">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="aa1ee-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="aa1ee-142">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="aa1ee-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="aa1ee-143">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="aa1ee-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




