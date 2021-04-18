---
description: A função SetClassIDInBlob define o valor do identificador de classe nomeado de um BLOB.
ms.assetid: d17dd48b-2e35-4c57-ba33-688180910b63
title: Função SetClassIDInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetClassIDInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: b617c39767038bac51d749a640ebcf2301e0c63f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766986"
---
# <a name="setclassidinblob-function"></a><span data-ttu-id="ecaa3-103">Função SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="ecaa3-103">SetClassIDInBlob function</span></span>

<span data-ttu-id="ecaa3-104">A função **SetClassIDInBlob** define o valor do identificador de classe nomeado de um blob.</span><span class="sxs-lookup"><span data-stu-id="ecaa3-104">The **SetClassIDInBlob** function sets the named class identifier value of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecaa3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ecaa3-105">Syntax</span></span>


```C++
DWORD SetClassIDInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="ecaa3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ecaa3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecaa3-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecaa3-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecaa3-108">Identificador para um BLOB.</span><span class="sxs-lookup"><span data-stu-id="ecaa3-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="ecaa3-109">*pOwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecaa3-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecaa3-110">Ponteiro para o nome do **proprietário** do blob que está definido.</span><span class="sxs-lookup"><span data-stu-id="ecaa3-110">Pointer to the BLOB **Owner** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="ecaa3-111">*pCategoryName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecaa3-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecaa3-112">Ponteiro para o nome da **categoria** de BLOB que está definido.</span><span class="sxs-lookup"><span data-stu-id="ecaa3-112">Pointer to the BLOB **Category** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="ecaa3-113">*pTagName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecaa3-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecaa3-114">Ponteiro para o nome da **marca** de BLOB que está definido.</span><span class="sxs-lookup"><span data-stu-id="ecaa3-114">Pointer to the BLOB **Tag** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="ecaa3-115">*pCLSID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ecaa3-115">*pClsID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecaa3-116">Ponteiro para o identificador de classe do BLOB que está definido.</span><span class="sxs-lookup"><span data-stu-id="ecaa3-116">Pointer to the class identifier of the BLOB that is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecaa3-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ecaa3-117">Return value</span></span>

<span data-ttu-id="ecaa3-118">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="ecaa3-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ecaa3-119">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="ecaa3-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecaa3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecaa3-120">Requirements</span></span>



| <span data-ttu-id="ecaa3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecaa3-121">Requirement</span></span> | <span data-ttu-id="ecaa3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ecaa3-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecaa3-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecaa3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ecaa3-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ecaa3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ecaa3-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecaa3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ecaa3-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ecaa3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ecaa3-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ecaa3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecaa3-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecaa3-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="ecaa3-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ecaa3-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="ecaa3-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ecaa3-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="ecaa3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ecaa3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecaa3-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecaa3-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecaa3-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ecaa3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecaa3-134">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="ecaa3-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="ecaa3-135">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="ecaa3-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="ecaa3-136">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="ecaa3-136">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="ecaa3-137">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="ecaa3-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="ecaa3-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="ecaa3-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="ecaa3-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="ecaa3-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="ecaa3-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="ecaa3-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="ecaa3-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="ecaa3-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="ecaa3-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="ecaa3-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




