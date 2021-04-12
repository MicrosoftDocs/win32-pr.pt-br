---
description: A função CompareFrameSourceAddress compara um endereço com o endereço de origem de um quadro.
ms.assetid: 7221c0cc-d6c1-4ec9-bf11-3ba1fefb35da
title: Função CompareFrameSourceAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a100273c37e25a7b1deba86ed2704886dbfccc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170827"
---
# <a name="compareframesourceaddress-function"></a><span data-ttu-id="7cebc-103">Função CompareFrameSourceAddress</span><span class="sxs-lookup"><span data-stu-id="7cebc-103">CompareFrameSourceAddress function</span></span>

<span data-ttu-id="7cebc-104">A função **CompareFrameSourceAddress** compara um endereço com o endereço de origem de um quadro.</span><span class="sxs-lookup"><span data-stu-id="7cebc-104">The **CompareFrameSourceAddress** function compares an address to the source address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cebc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7cebc-105">Syntax</span></span>


```C++
BOOL WINAPI CompareFrameSourceAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="7cebc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7cebc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cebc-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7cebc-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cebc-108">Identificador para um quadro.</span><span class="sxs-lookup"><span data-stu-id="7cebc-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="7cebc-109">*lpAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7cebc-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cebc-110">Ponteiro para um endereço.</span><span class="sxs-lookup"><span data-stu-id="7cebc-110">Pointer to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cebc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7cebc-111">Return value</span></span>

<span data-ttu-id="7cebc-112">Se os endereços forem iguais, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="7cebc-112">If the addresses are the same, the return value is **TRUE**.</span></span>

<span data-ttu-id="7cebc-113">Se os endereços não forem iguais, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="7cebc-113">If the addresses are not the same, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cebc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7cebc-114">Remarks</span></span>

<span data-ttu-id="7cebc-115">Para que a função **CompareFrameSourceAddress** tenha sucesso, o tipo de endereço de origem deve corresponder ao tipo de endereço especificado no parâmetro *lpAddress* .</span><span class="sxs-lookup"><span data-stu-id="7cebc-115">For the **CompareFrameSourceAddress** function to succeed, the source address type must match the type of address specified in the *lpAddress* parameter.</span></span>

<span data-ttu-id="7cebc-116">Monitor de Rede fornece duas outras funções para comparar endereços: [CompareFrameDestAddress](compareframedestaddress.md) e [CompareAddresses](compareaddresses.md).</span><span class="sxs-lookup"><span data-stu-id="7cebc-116">Network Monitor provides two other functions for comparing addresses: [CompareFrameDestAddress](compareframedestaddress.md) and [CompareAddresses](compareaddresses.md).</span></span> <span data-ttu-id="7cebc-117">A função **CompareFrameDestAddress** compara um determinado endereço com o endereço de destino do quadro e a função **CompareAddress** compara dois endereços fornecidos.</span><span class="sxs-lookup"><span data-stu-id="7cebc-117">The **CompareFrameDestAddress** function compares a given address to the frame's destination address, and the **CompareAddress** function compares two given addresses.</span></span>

<span data-ttu-id="7cebc-118">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **CompareFrameSourceAddress** .</span><span class="sxs-lookup"><span data-stu-id="7cebc-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **CompareFrameSourceAddress** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cebc-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cebc-119">Requirements</span></span>



| <span data-ttu-id="7cebc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cebc-120">Requirement</span></span> | <span data-ttu-id="7cebc-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7cebc-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7cebc-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cebc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7cebc-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7cebc-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7cebc-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cebc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7cebc-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7cebc-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7cebc-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7cebc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cebc-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cebc-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7cebc-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7cebc-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="7cebc-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7cebc-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7cebc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7cebc-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cebc-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cebc-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cebc-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="7cebc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cebc-133">CompareAddresses</span><span class="sxs-lookup"><span data-stu-id="7cebc-133">CompareAddresses</span></span>](compareaddresses.md)
</dt> <dt>

[<span data-ttu-id="7cebc-134">CompareFrameDestAddress</span><span class="sxs-lookup"><span data-stu-id="7cebc-134">CompareFrameDestAddress</span></span>](compareframedestaddress.md)
</dt> </dl>

 

 




