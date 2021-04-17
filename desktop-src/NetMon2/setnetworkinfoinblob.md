---
description: A função SetNetworkInfoInBlob preenche a estrutura NETWORKINFO no BLOB.
ms.assetid: 1a511c26-2fa7-4fe4-a5a9-23188c59bc34
title: Função SetNetworkInfoInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNetworkInfoInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a0019bfaf802b5d4dc80d73e75affa3c50d95de1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759062"
---
# <a name="setnetworkinfoinblob-function"></a><span data-ttu-id="94929-103">Função SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="94929-103">SetNetworkInfoInBlob function</span></span>

<span data-ttu-id="94929-104">A função **SetNetworkInfoInBlob** preenche a estrutura **NETWORKINFO** no BLOB.</span><span class="sxs-lookup"><span data-stu-id="94929-104">The **SetNetworkInfoInBlob** function fills in the **NETWORKINFO** structure in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="94929-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94929-105">Syntax</span></span>


```C++
DWORD SetNetworkInfoInBlob(
  _In_ HBLOB         hBlob,
  _In_ LPNETWORKINFO lpNetworkInfo
);
```



## <a name="parameters"></a><span data-ttu-id="94929-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94929-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94929-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="94929-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94929-108">Identificador para um BLOB.</span><span class="sxs-lookup"><span data-stu-id="94929-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="94929-109">*lpNetworkInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="94929-109">*lpNetworkInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94929-110">Ponteiro para a estrutura [NETWORKINFO](networkinfo.md) alocada pelo usuário que a função preenche.</span><span class="sxs-lookup"><span data-stu-id="94929-110">Pointer to the user-allocated [NETWORKINFO](networkinfo.md) structure that the function fills in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94929-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="94929-111">Return value</span></span>

<span data-ttu-id="94929-112">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="94929-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="94929-113">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="94929-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="94929-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94929-114">Requirements</span></span>



| <span data-ttu-id="94929-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="94929-115">Requirement</span></span> | <span data-ttu-id="94929-116">Valor</span><span class="sxs-lookup"><span data-stu-id="94929-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94929-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94929-117">Minimum supported client</span></span><br/> | <span data-ttu-id="94929-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="94929-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="94929-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94929-119">Minimum supported server</span></span><br/> | <span data-ttu-id="94929-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="94929-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="94929-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="94929-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="94929-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="94929-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="94929-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="94929-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="94929-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94929-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="94929-125">DLL</span><span class="sxs-lookup"><span data-stu-id="94929-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94929-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94929-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94929-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="94929-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94929-128">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="94929-128">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="94929-129">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="94929-129">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="94929-130">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="94929-130">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="94929-131">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="94929-131">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="94929-132">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="94929-132">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="94929-133">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="94929-133">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="94929-134">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="94929-134">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="94929-135">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="94929-135">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="94929-136">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="94929-136">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




