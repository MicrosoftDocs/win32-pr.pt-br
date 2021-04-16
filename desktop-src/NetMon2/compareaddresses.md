---
description: A função CompareAddresses compara dois endereços, indicando que um dos endereços é maior que, menor ou igual ao outro endereço.
ms.assetid: 76ff37d2-714f-4bac-adcc-eab78c8f25d3
title: Função CompareAddresses (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: fd72ef0281615c0b56176e86ee9bb3659b498a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758943"
---
# <a name="compareaddresses-function"></a><span data-ttu-id="66ede-103">Função CompareAddresses</span><span class="sxs-lookup"><span data-stu-id="66ede-103">CompareAddresses function</span></span>

<span data-ttu-id="66ede-104">A função **CompareAddresses** compara dois endereços, indicando que um dos endereços é maior que, menor ou igual ao outro endereço.</span><span class="sxs-lookup"><span data-stu-id="66ede-104">The **CompareAddresses** function compares two addresses, indicating that one of the addresses is greater than, less than, or equal to the other address.</span></span>

## <a name="syntax"></a><span data-ttu-id="66ede-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66ede-105">Syntax</span></span>


```C++
int WINAPI CompareAddresses(
  _In_ LPADDRESS lpAddress1,
  _In_ LPADDRESS lpAddress2
);
```



## <a name="parameters"></a><span data-ttu-id="66ede-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66ede-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66ede-107">*lpAddress1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66ede-107">*lpAddress1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66ede-108">Ponteiro para o primeiro endereço.</span><span class="sxs-lookup"><span data-stu-id="66ede-108">Pointer to the first address.</span></span>

</dd> <dt>

<span data-ttu-id="66ede-109">*lpAddress2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="66ede-109">*lpAddress2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66ede-110">Ponteiro para o segundo endereço.</span><span class="sxs-lookup"><span data-stu-id="66ede-110">Pointer to the second address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66ede-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66ede-111">Return value</span></span>

<span data-ttu-id="66ede-112">Se os endereços forem iguais, a função retornará zero.</span><span class="sxs-lookup"><span data-stu-id="66ede-112">If the addresses are the same, the function returns zero.</span></span>

<span data-ttu-id="66ede-113">Se o parâmetro *lpAddress1* especificar um endereço menor que o endereço especificado pelo parâmetro *lpAddress2* , o valor de retorno será um número negativo.</span><span class="sxs-lookup"><span data-stu-id="66ede-113">If the *lpAddress1* parameter specifies an address that is less than the address that the *lpAddress2* parameter specifies, the return value is a negative number.</span></span>

<span data-ttu-id="66ede-114">Se o parâmetro *lpAddress1* especificar um endereço maior do que o endereço especificado pelo parâmetro *lpAddress2* , o valor de retorno será um número positivo.</span><span class="sxs-lookup"><span data-stu-id="66ede-114">If the *lpAddress1* parameter specifies an address that is greater than the address that the *lpAddress2* parameter specifies, the return value is a positive number.</span></span>

## <a name="remarks"></a><span data-ttu-id="66ede-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="66ede-115">Remarks</span></span>

<span data-ttu-id="66ede-116">Um endereço menor que outro endereço indica um quadro anterior.</span><span class="sxs-lookup"><span data-stu-id="66ede-116">An address that is less than another address indicates a previous frame.</span></span> <span data-ttu-id="66ede-117">Um endereço maior que outro endereço indica um quadro posterior.</span><span class="sxs-lookup"><span data-stu-id="66ede-117">An address that is greater than another address indicates a later frame.</span></span>

<span data-ttu-id="66ede-118">Monitor de Rede fornece duas outras funções, [CompareFrameDestAddress](compareframedestaddress.md) e [CompareFrameSourceAddress](compareframesourceaddress.md), que você pode usar para comparar endereços.</span><span class="sxs-lookup"><span data-stu-id="66ede-118">Network Monitor provides two other functions, [CompareFrameDestAddress](compareframedestaddress.md) and [CompareFrameSourceAddress](compareframesourceaddress.md), which you can use to compare addresses.</span></span> <span data-ttu-id="66ede-119">A função **CompareFrameDestAddress** compara um determinado endereço com o endereço de destino do quadro e a função **CompareFrameSourceAddress** compara um determinado endereço com o endereço de origem do quadro.</span><span class="sxs-lookup"><span data-stu-id="66ede-119">The **CompareFrameDestAddress** function compares a given address to the frame's destination address, and the **CompareFrameSourceAddress** function compares a given address to the frame's source address.</span></span>

## <a name="requirements"></a><span data-ttu-id="66ede-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66ede-120">Requirements</span></span>



| <span data-ttu-id="66ede-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="66ede-121">Requirement</span></span> | <span data-ttu-id="66ede-122">Valor</span><span class="sxs-lookup"><span data-stu-id="66ede-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="66ede-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66ede-123">Minimum supported client</span></span><br/> | <span data-ttu-id="66ede-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="66ede-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="66ede-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66ede-125">Minimum supported server</span></span><br/> | <span data-ttu-id="66ede-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="66ede-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="66ede-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="66ede-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="66ede-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="66ede-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="66ede-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66ede-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="66ede-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66ede-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="66ede-131">DLL</span><span class="sxs-lookup"><span data-stu-id="66ede-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66ede-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66ede-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66ede-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="66ede-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66ede-134">CompareFrameDestAddress</span><span class="sxs-lookup"><span data-stu-id="66ede-134">CompareFrameDestAddress</span></span>](compareframedestaddress.md)
</dt> <dt>

[<span data-ttu-id="66ede-135">CompareFrameSourceAddress</span><span class="sxs-lookup"><span data-stu-id="66ede-135">CompareFrameSourceAddress</span></span>](compareframesourceaddress.md)
</dt> </dl>

 

 




