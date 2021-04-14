---
description: Retorna uma cadeia de caracteres localizada em uma determinada posição dentro de um BLOB.
ms.assetid: 5930a30b-f0ed-4d5b-a0ba-6cead55c2fcd
title: Função GetStringFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 475600fb6128b5dbbaf9333f8c550351831f0a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460960"
---
# <a name="getstringfromblob-function"></a><span data-ttu-id="c2bd5-103">Função GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="c2bd5-103">GetStringFromBlob function</span></span>

<span data-ttu-id="c2bd5-104">A função **GetStringFromBlob** retorna uma cadeia de caracteres localizada em uma determinada posição dentro de um blob.</span><span class="sxs-lookup"><span data-stu-id="c2bd5-104">The **GetStringFromBlob** function returns a string located at a given position within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2bd5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2bd5-105">Syntax</span></span>


```C++
DWORD GetStringFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_ const char  **ppString
);
```



## <a name="parameters"></a><span data-ttu-id="c2bd5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2bd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2bd5-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2bd5-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2bd5-108">Um identificador para o BLOB.</span><span class="sxs-lookup"><span data-stu-id="c2bd5-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="c2bd5-109">*pOwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2bd5-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2bd5-110">Uma seção de **proprietário** de BLOB em que a cadeia de caracteres está localizada.</span><span class="sxs-lookup"><span data-stu-id="c2bd5-110">A BLOB **Owner** section where the string is located.</span></span>

</dd> <dt>

<span data-ttu-id="c2bd5-111">*pCategoryName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2bd5-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2bd5-112">Uma seção de **categoria** de BLOB em que a cadeia de caracteres está localizada.</span><span class="sxs-lookup"><span data-stu-id="c2bd5-112">A BLOB **Category** section where the string is located.</span></span>

</dd> <dt>

<span data-ttu-id="c2bd5-113">*pTagName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2bd5-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2bd5-114">A **marca** da cadeia de caracteres solicitada.</span><span class="sxs-lookup"><span data-stu-id="c2bd5-114">The **Tag** of the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="c2bd5-115">*ppString* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c2bd5-115">*ppString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2bd5-116">Um ponteiro para uma variável que aponta para a cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="c2bd5-116">A pointer to a variable that points to the returned string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2bd5-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2bd5-117">Return value</span></span>

<span data-ttu-id="c2bd5-118">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="c2bd5-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c2bd5-119">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="c2bd5-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

<span data-ttu-id="c2bd5-120">Se os dados de **proprietário**, **categoria** ou **marca** especificados não existirem, a função retornará a **entrada de blob NMERR \_ \_ \_ \_ não \_ existir**.</span><span class="sxs-lookup"><span data-stu-id="c2bd5-120">If the specified **Owner**, **Category**, or **Tag** data does not exist, the function returns **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2bd5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2bd5-121">Requirements</span></span>



| <span data-ttu-id="c2bd5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2bd5-122">Requirement</span></span> | <span data-ttu-id="c2bd5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c2bd5-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2bd5-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2bd5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c2bd5-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2bd5-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c2bd5-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2bd5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c2bd5-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2bd5-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c2bd5-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c2bd5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2bd5-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2bd5-129"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="c2bd5-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c2bd5-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2bd5-131"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2bd5-131"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="c2bd5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c2bd5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2bd5-133"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2bd5-133"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2bd5-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2bd5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2bd5-135">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="c2bd5-135">SetStringInBlob</span></span>](setstringinblob.md)
</dt> <dt>

[<span data-ttu-id="c2bd5-136">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="c2bd5-136">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="c2bd5-137">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="c2bd5-137">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="c2bd5-138">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="c2bd5-138">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="c2bd5-139">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="c2bd5-139">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="c2bd5-140">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="c2bd5-140">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="c2bd5-141">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="c2bd5-141">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="c2bd5-142">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="c2bd5-142">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="c2bd5-143">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="c2bd5-143">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="c2bd5-144">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="c2bd5-144">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




