---
description: Define uma cadeia de caracteres em um determinado local dentro de um BLOB.
ms.assetid: 645e6b8b-aaaf-429f-ad2f-bf4364ef4e80
title: Função SetStringInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetStringInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 37278b9111818957e6d5fb3032f1bf33ad3a6ec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164619"
---
# <a name="setstringinblob-function"></a><span data-ttu-id="997b7-103">Função SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="997b7-103">SetStringInBlob function</span></span>

<span data-ttu-id="997b7-104">A função **SetStringInBlob** define uma cadeia de caracteres em um determinado local dentro de um blob.</span><span class="sxs-lookup"><span data-stu-id="997b7-104">The **SetStringInBlob** function sets a string at a given location within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="997b7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="997b7-105">Syntax</span></span>


```C++
DWORD SetStringInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const char  *pString
);
```



## <a name="parameters"></a><span data-ttu-id="997b7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="997b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="997b7-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="997b7-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="997b7-108">Um identificador para o BLOB.</span><span class="sxs-lookup"><span data-stu-id="997b7-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="997b7-109">*pOwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="997b7-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="997b7-110">Um ponteiro para a seção de **proprietário** do blob, em que a cadeia de caracteres é definida.</span><span class="sxs-lookup"><span data-stu-id="997b7-110">A pointer to the **Owner** section of the BLOB, where the string is set.</span></span>

</dd> <dt>

<span data-ttu-id="997b7-111">*pCategoryName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="997b7-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="997b7-112">Um ponteiro para a seção de **categoria** do blob, em que a cadeia de caracteres é definida.</span><span class="sxs-lookup"><span data-stu-id="997b7-112">A pointer to the **Category** section of the BLOB, where the string is set.</span></span>

</dd> <dt>

<span data-ttu-id="997b7-113">*pTagName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="997b7-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="997b7-114">Um ponteiro para a **marca** da cadeia de caracteres solicitada.</span><span class="sxs-lookup"><span data-stu-id="997b7-114">A pointer to the **Tag** of the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="997b7-115">*pString* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="997b7-115">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="997b7-116">Um ponteiro para a variável em que um ponteiro para a cadeia de caracteres será retornado.</span><span class="sxs-lookup"><span data-stu-id="997b7-116">A pointer to the variable where a pointer to the string will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="997b7-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="997b7-117">Return value</span></span>

<span data-ttu-id="997b7-118">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="997b7-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="997b7-119">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o problema.</span><span class="sxs-lookup"><span data-stu-id="997b7-119">If the function is unsuccessful, the return value is a NMERR value that indicates the problem.</span></span>

<span data-ttu-id="997b7-120">Se as informações de **proprietário**, **categoria** ou **marca** especificadas não existirem, o valor de retorno será \_ NMERR \_ blob \_ \_ \_ inexistente.</span><span class="sxs-lookup"><span data-stu-id="997b7-120">If the specified **Owner**, **Category**, or **Tag** information does not exist, the return value is NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST.</span></span>

## <a name="requirements"></a><span data-ttu-id="997b7-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="997b7-121">Requirements</span></span>



| <span data-ttu-id="997b7-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="997b7-122">Requirement</span></span> | <span data-ttu-id="997b7-123">Valor</span><span class="sxs-lookup"><span data-stu-id="997b7-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="997b7-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="997b7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="997b7-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="997b7-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="997b7-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="997b7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="997b7-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="997b7-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="997b7-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="997b7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="997b7-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="997b7-129"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="997b7-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="997b7-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="997b7-131"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="997b7-131"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="997b7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="997b7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="997b7-133"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="997b7-133"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="997b7-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="997b7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="997b7-135">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="997b7-135">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="997b7-136">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="997b7-136">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="997b7-137">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="997b7-137">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="997b7-138">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="997b7-138">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="997b7-139">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="997b7-139">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="997b7-140">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="997b7-140">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="997b7-141">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="997b7-141">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="997b7-142">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="997b7-142">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="997b7-143">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="997b7-143">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> </dl>

 

 




