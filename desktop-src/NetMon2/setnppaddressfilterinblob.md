---
description: A função SetNPPAddressFilterInBlob define o filtro de endereço fornecido no BLOB.
ms.assetid: bdd1482d-8be0-4999-9a7a-16b0400412fb
title: Função SetNPPAddressFilterInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPAddressFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 39e8a85599fa63b1320d707f648731a195dbb48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812758"
---
# <a name="setnppaddressfilterinblob-function"></a><span data-ttu-id="ac80a-103">Função SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="ac80a-103">SetNPPAddressFilterInBlob function</span></span>

<span data-ttu-id="ac80a-104">A função **SetNPPAddressFilterInBlob** define o filtro de endereço fornecido no BLOB.</span><span class="sxs-lookup"><span data-stu-id="ac80a-104">The **SetNPPAddressFilterInBlob** function sets the given address filter in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac80a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac80a-105">Syntax</span></span>


```C++
DWORD SetNPPAddressFilterInBlob(
  _In_ HBLOB          hBlob,
  _In_ LPADDRESSTABLE pAddressTable
);
```



## <a name="parameters"></a><span data-ttu-id="ac80a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac80a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac80a-107">*hBlob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac80a-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac80a-108">Identificador para um BLOB.</span><span class="sxs-lookup"><span data-stu-id="ac80a-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="ac80a-109">*pAddressTable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac80a-109">*pAddressTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac80a-110">Ponteiro para uma estrutura de [**AddressTable**](addresstable.md) que define a tabela de endereços alocada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="ac80a-110">Pointer to an [**ADDRESSTABLE**](addresstable.md) structure that defines the user-allocated address table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac80a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac80a-111">Return value</span></span>

<span data-ttu-id="ac80a-112">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="ac80a-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ac80a-113">Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="ac80a-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac80a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac80a-114">Requirements</span></span>



| <span data-ttu-id="ac80a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac80a-115">Requirement</span></span> | <span data-ttu-id="ac80a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ac80a-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac80a-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac80a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ac80a-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ac80a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ac80a-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac80a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ac80a-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ac80a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ac80a-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ac80a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac80a-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac80a-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="ac80a-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ac80a-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="ac80a-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac80a-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="ac80a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ac80a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac80a-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac80a-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac80a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac80a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac80a-128">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="ac80a-128">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="ac80a-129">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="ac80a-129">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="ac80a-130">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="ac80a-130">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="ac80a-131">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="ac80a-131">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="ac80a-132">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="ac80a-132">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="ac80a-133">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="ac80a-133">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="ac80a-134">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="ac80a-134">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="ac80a-135">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="ac80a-135">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="ac80a-136">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="ac80a-136">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




