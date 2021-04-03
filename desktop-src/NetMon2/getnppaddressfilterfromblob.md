---
description: A função GetNPPAddressFilterFromBlob preenche o filtro de endereço fornecido com as informações armazenadas no BLOB.
ms.assetid: b34e0e52-1b2a-4d61-b60c-f1b19ff8ff38
title: Função GetNPPAddressFilterFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPAddressFilterFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 944821620123d63f654e286a77018232c79981e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922618"
---
# <a name="getnppaddressfilterfromblob-function"></a><span data-ttu-id="1a092-103">Função GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="1a092-103">GetNPPAddressFilterFromBlob function</span></span>

<span data-ttu-id="1a092-104">A função **GetNPPAddressFilterFromBlob** preenche o filtro de endereço fornecido com as informações armazenadas no BLOB.</span><span class="sxs-lookup"><span data-stu-id="1a092-104">The **GetNPPAddressFilterFromBlob** function fills in the given address filter with information stored in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a092-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a092-105">Syntax</span></span>


```C++
DWORD GetNPPAddressFilterFromBlob(
  _In_    HBLOB          hBlob,
  _Inout_ LPADDRESSTABLE pAddressTable,
  _Out_   HBLOB          hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="1a092-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a092-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a092-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a092-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a092-108">Identificador para um BLOB.</span><span class="sxs-lookup"><span data-stu-id="1a092-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="1a092-109">*pAddressTable* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1a092-109">*pAddressTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a092-110">Ponteiro para a tabela de endereços alocada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="1a092-110">Pointer to the user-allocated address table.</span></span>

</dd> <dt>

<span data-ttu-id="1a092-111">*hErrorBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1a092-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a092-112">Identificador para um BLOB de erro que especifica onde ocorreu o erro (se houver) no BLOB original.</span><span class="sxs-lookup"><span data-stu-id="1a092-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a092-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a092-113">Return value</span></span>

<span data-ttu-id="1a092-114">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="1a092-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1a092-115">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que descreve o erro.</span><span class="sxs-lookup"><span data-stu-id="1a092-115">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a092-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a092-116">Remarks</span></span>

<span data-ttu-id="1a092-117">As informações de endereço são armazenadas na seção de **configuração** da categoria blob NPP do **proprietário** .</span><span class="sxs-lookup"><span data-stu-id="1a092-117">The address information is stored in the **Config** section of the BLOB NPP **Owner** category.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a092-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a092-118">Requirements</span></span>



| <span data-ttu-id="1a092-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a092-119">Requirement</span></span> | <span data-ttu-id="1a092-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1a092-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a092-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a092-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1a092-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1a092-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1a092-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a092-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1a092-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1a092-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1a092-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1a092-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a092-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a092-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="1a092-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a092-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="1a092-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a092-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="1a092-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1a092-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a092-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a092-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a092-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a092-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a092-132">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="1a092-132">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="1a092-133">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="1a092-133">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="1a092-134">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="1a092-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="1a092-135">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="1a092-135">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="1a092-136">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="1a092-136">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="1a092-137">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="1a092-137">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="1a092-138">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="1a092-138">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="1a092-139">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="1a092-139">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="1a092-140">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="1a092-140">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="1a092-141">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="1a092-141">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




