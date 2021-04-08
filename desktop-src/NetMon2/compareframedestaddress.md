---
description: A função CompareFrameDestAddress compara um endereço com o endereço de destino de um quadro.
ms.assetid: 739b3b9f-f989-459d-ac3e-6be7769adc06
title: Função CompareFrameDestAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: a9ce0ff776588c06b8fddc34240e9c2170ceca69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828228"
---
# <a name="compareframedestaddress-function"></a><span data-ttu-id="d66e5-103">Função CompareFrameDestAddress</span><span class="sxs-lookup"><span data-stu-id="d66e5-103">CompareFrameDestAddress function</span></span>

<span data-ttu-id="d66e5-104">A função **CompareFrameDestAddress** compara um endereço com o endereço de destino de um quadro.</span><span class="sxs-lookup"><span data-stu-id="d66e5-104">The **CompareFrameDestAddress** function compares an address to the destination address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="d66e5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d66e5-105">Syntax</span></span>


```C++
BOOL WINAPI CompareFrameDestAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="d66e5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d66e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d66e5-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d66e5-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d66e5-108">Identificador para um quadro.</span><span class="sxs-lookup"><span data-stu-id="d66e5-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="d66e5-109">*lpAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d66e5-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d66e5-110">Ponteiro para um endereço.</span><span class="sxs-lookup"><span data-stu-id="d66e5-110">Pointer to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d66e5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d66e5-111">Return value</span></span>

<span data-ttu-id="d66e5-112">Se os endereços forem iguais, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="d66e5-112">If the addresses are the same, the return value is **TRUE**.</span></span>

<span data-ttu-id="d66e5-113">Se os endereços não forem iguais, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="d66e5-113">If the addresses are not the same, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d66e5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d66e5-114">Remarks</span></span>

<span data-ttu-id="d66e5-115">Para que a função **CompareFrameDestAddress** seja retornada com êxito, o tipo de endereço de destino deve corresponder ao tipo de endereço especificado no parâmetro *lpAddress* .</span><span class="sxs-lookup"><span data-stu-id="d66e5-115">For the **CompareFrameDestAddress** function to return successfully, the destination address type must match the type of address specified in the *lpAddress* parameter.</span></span>

<span data-ttu-id="d66e5-116">Monitor de Rede fornece duas outras funções, [CompareFrameSourceAddress](compareframesourceaddress.md) e [CompareAddresses](compareaddresses.md), que você pode usar para comparar endereços.</span><span class="sxs-lookup"><span data-stu-id="d66e5-116">Network Monitor provides two other functions, [CompareFrameSourceAddress](compareframesourceaddress.md) and [CompareAddresses](compareaddresses.md), which you can use to compare addresses.</span></span> <span data-ttu-id="d66e5-117">A função **CompareFrameSourceAddress** compara um determinado endereço com o endereço de origem do quadro e a função **CompareAddress** compara dois endereços fornecidos.</span><span class="sxs-lookup"><span data-stu-id="d66e5-117">The **CompareFrameSourceAddress** function compares a given address to the frame's source address, and the **CompareAddress** function compares two given addresses.</span></span>

<span data-ttu-id="d66e5-118">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **CompareFrameDestAddress** .</span><span class="sxs-lookup"><span data-stu-id="d66e5-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **CompareFrameDestAddress** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d66e5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d66e5-119">Requirements</span></span>



| <span data-ttu-id="d66e5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d66e5-120">Requirement</span></span> | <span data-ttu-id="d66e5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d66e5-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d66e5-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d66e5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d66e5-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d66e5-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d66e5-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d66e5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d66e5-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d66e5-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d66e5-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d66e5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d66e5-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d66e5-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d66e5-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d66e5-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="d66e5-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d66e5-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d66e5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d66e5-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d66e5-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d66e5-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d66e5-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="d66e5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d66e5-133">CompareAddresses</span><span class="sxs-lookup"><span data-stu-id="d66e5-133">CompareAddresses</span></span>](compareaddresses.md)
</dt> <dt>

[<span data-ttu-id="d66e5-134">CompareFrameSourceAddress</span><span class="sxs-lookup"><span data-stu-id="d66e5-134">CompareFrameSourceAddress</span></span>](compareframesourceaddress.md)
</dt> </dl>

 

 




