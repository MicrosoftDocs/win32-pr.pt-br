---
description: A função GetNetworkInfoFromBlob recupera informações de rede de um determinado BLOB.
ms.assetid: 217c33f4-e548-4072-9edd-ded61e6cd743
title: Função GetNetworkInfoFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNetworkInfoFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2f8b15dce010febdc952c2527a9f4ad31054fa3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760813"
---
# <a name="getnetworkinfofromblob-function"></a><span data-ttu-id="02d10-103">Função GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="02d10-103">GetNetworkInfoFromBlob function</span></span>

<span data-ttu-id="02d10-104">A função **GetNetworkInfoFromBlob** recupera informações de rede de um determinado BLOB.</span><span class="sxs-lookup"><span data-stu-id="02d10-104">The **GetNetworkInfoFromBlob** function retrieves network information from a given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="02d10-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02d10-105">Syntax</span></span>


```C++
DWORD GetNetworkInfoFromBlob(
  _In_    HBLOB         hBlob,
  _Inout_ LPNETWORKINFO lpNetworkInfo
);
```



## <a name="parameters"></a><span data-ttu-id="02d10-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02d10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02d10-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="02d10-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02d10-108">Identificador para um BLOB.</span><span class="sxs-lookup"><span data-stu-id="02d10-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="02d10-109">*lpNetworkInfo* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="02d10-109">*lpNetworkInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="02d10-110">Um ponteiro para a estrutura [NETWORKINFO](networkinfo.md) alocada pelo usuário que está preenchida.</span><span class="sxs-lookup"><span data-stu-id="02d10-110">A pointer to the user-allocated [NETWORKINFO](networkinfo.md) structure that is filled in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02d10-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="02d10-111">Return value</span></span>

<span data-ttu-id="02d10-112">Se a função **GetNetworkInfoFromBlob** for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="02d10-112">If the **GetNetworkInfoFromBlob** function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="02d10-113">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que descreve o erro.</span><span class="sxs-lookup"><span data-stu-id="02d10-113">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="02d10-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="02d10-114">Remarks</span></span>

<span data-ttu-id="02d10-115">As informações de rede são armazenadas na seção BLOB **NetworkInfo** da categoria blob NPP do **proprietário** .</span><span class="sxs-lookup"><span data-stu-id="02d10-115">The network information is stored in the BLOB **NetworkInfo** section of the BLOB NPP **Owner** category.</span></span>

## <a name="requirements"></a><span data-ttu-id="02d10-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02d10-116">Requirements</span></span>



| <span data-ttu-id="02d10-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="02d10-117">Requirement</span></span> | <span data-ttu-id="02d10-118">Valor</span><span class="sxs-lookup"><span data-stu-id="02d10-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02d10-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02d10-119">Minimum supported client</span></span><br/> | <span data-ttu-id="02d10-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="02d10-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="02d10-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02d10-121">Minimum supported server</span></span><br/> | <span data-ttu-id="02d10-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="02d10-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="02d10-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="02d10-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="02d10-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="02d10-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="02d10-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="02d10-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="02d10-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02d10-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="02d10-127">DLL</span><span class="sxs-lookup"><span data-stu-id="02d10-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02d10-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02d10-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02d10-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="02d10-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02d10-130">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="02d10-130">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="02d10-131">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="02d10-131">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="02d10-132">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="02d10-132">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="02d10-133">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="02d10-133">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="02d10-134">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="02d10-134">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="02d10-135">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="02d10-135">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="02d10-136">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="02d10-136">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="02d10-137">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="02d10-137">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="02d10-138">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="02d10-138">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="02d10-139">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="02d10-139">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




