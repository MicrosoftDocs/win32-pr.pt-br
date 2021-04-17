---
description: Constrói um objeto CMsg.
ms.assetid: b7ee0643-73e4-450d-bff4-ca5006fdcc14
title: Construtor CMsg. CMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg.CMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b26a9572b51d4a476b70c3dd7ddae8c896a4d648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789966"
---
# <a name="cmsgcmsg-constructor"></a><span data-ttu-id="0c66a-103">Construtor CMsg. CMsg</span><span class="sxs-lookup"><span data-stu-id="0c66a-103">CMsg.CMsg constructor</span></span>

<span data-ttu-id="0c66a-104">Constrói um objeto [**CMsg**](cmsg.md) .</span><span class="sxs-lookup"><span data-stu-id="0c66a-104">Constructs a [**CMsg**](cmsg.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c66a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c66a-105">Syntax</span></span>


```C++
CMsg(
   UINT     u,
   DWORD    dw,
   LPVOID   lp,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a><span data-ttu-id="0c66a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c66a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c66a-107">*u*</span><span class="sxs-lookup"><span data-stu-id="0c66a-107">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="0c66a-108">Código de solicitação, definido pelo cliente da classe thread e compreendido pela função de thread de trabalho substituída.</span><span class="sxs-lookup"><span data-stu-id="0c66a-108">Request code, defined by the client of the thread class and understood by the overridden worker thread function.</span></span>

</dd> <dt>

<span data-ttu-id="0c66a-109">*dw*</span><span class="sxs-lookup"><span data-stu-id="0c66a-109">*dw*</span></span> 
</dt> <dd>

<span data-ttu-id="0c66a-110">Sinalizador de parâmetro para o código de solicitação.</span><span class="sxs-lookup"><span data-stu-id="0c66a-110">Flag parameter to the request code.</span></span>

</dd> <dt>

<span data-ttu-id="0c66a-111">*LP*</span><span class="sxs-lookup"><span data-stu-id="0c66a-111">*lp*</span></span> 
</dt> <dd>

<span data-ttu-id="0c66a-112">Ponteiro para dados exigidos pelo thread de trabalho como valores de parâmetro ou retorno.</span><span class="sxs-lookup"><span data-stu-id="0c66a-112">Pointer to data required by the worker thread as parameter or return values.</span></span> <span data-ttu-id="0c66a-113">Esses dados não devem ser baseados em pilha, pois serão referenciados algum tempo após a conclusão da operação de enfileiramento.</span><span class="sxs-lookup"><span data-stu-id="0c66a-113">This data should not be stack-based, as it will be referenced some time after completing the queuing operation.</span></span>

</dd> <dt>

<span data-ttu-id="0c66a-114">*pEvent*</span><span class="sxs-lookup"><span data-stu-id="0c66a-114">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="0c66a-115">Ponteiro para o objeto de evento que um thread de trabalho pode sinalizar para indicar a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="0c66a-115">Pointer to the event object that a worker thread can signal to indicate the completion of the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c66a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c66a-116">Remarks</span></span>

<span data-ttu-id="0c66a-117">Essa função de membro contém uma solicitação para que um thread de trabalho do [**CMsgThread**](cmsgthread.md) atue.</span><span class="sxs-lookup"><span data-stu-id="0c66a-117">This member function contains a request for a [**CMsgThread**](cmsgthread.md) worker thread to act on.</span></span> <span data-ttu-id="0c66a-118">Todos os parâmetros são passados para a função de thread de trabalho como parâmetros quando essa mensagem é processada.</span><span class="sxs-lookup"><span data-stu-id="0c66a-118">All the parameters are passed to the worker thread function as parameters when this message gets processed.</span></span> <span data-ttu-id="0c66a-119">Os significados dos parâmetros são definidos pela função de cliente que chama o thread de trabalho e a classe derivada que fornece a função de execução do thread de trabalho.</span><span class="sxs-lookup"><span data-stu-id="0c66a-119">The meanings of the parameters are defined by the client function that calls the worker thread and the derived class that supplies the worker thread's execution function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c66a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c66a-120">Requirements</span></span>



| <span data-ttu-id="0c66a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c66a-121">Requirement</span></span> | <span data-ttu-id="0c66a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0c66a-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c66a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c66a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0c66a-124"><dt>Msgthrd. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c66a-124"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0c66a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c66a-125">Library</span></span><br/> | <dl> <span data-ttu-id="0c66a-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0c66a-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




