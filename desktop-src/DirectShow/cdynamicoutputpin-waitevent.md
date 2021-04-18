---
description: O método WaitEvent aguarda até que o evento especificado seja sinalizado.
ms.assetid: 64880f46-7b8f-4823-9d50-052e30ecf04b
title: Método CDynamicOutputPin. WaitEvent (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.WaitEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b27f3c387c82eaeebc119f967deaca8e7314ccd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780874"
---
# <a name="cdynamicoutputpinwaitevent-method"></a><span data-ttu-id="621b1-103">Método CDynamicOutputPin. WaitEvent</span><span class="sxs-lookup"><span data-stu-id="621b1-103">CDynamicOutputPin.WaitEvent method</span></span>

<span data-ttu-id="621b1-104">O `WaitEvent` método aguarda até que o evento especificado seja sinalizado.</span><span class="sxs-lookup"><span data-stu-id="621b1-104">The `WaitEvent` method waits until the specified event is signaled.</span></span>

## <a name="syntax"></a><span data-ttu-id="621b1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="621b1-105">Syntax</span></span>


```C++
static HRESULT WaitEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="621b1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="621b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="621b1-107">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="621b1-107">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="621b1-108">Identificador para um evento.</span><span class="sxs-lookup"><span data-stu-id="621b1-108">Handle to an event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="621b1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="621b1-109">Return value</span></span>

<span data-ttu-id="621b1-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="621b1-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="621b1-111">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="621b1-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="621b1-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="621b1-112">Return code</span></span>                                                                                  | <span data-ttu-id="621b1-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="621b1-113">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="621b1-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="621b1-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="621b1-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="621b1-115">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="621b1-116"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="621b1-116"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="621b1-117">Erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="621b1-117">Unexpected error.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="621b1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="621b1-118">Requirements</span></span>



| <span data-ttu-id="621b1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="621b1-119">Requirement</span></span> | <span data-ttu-id="621b1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="621b1-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="621b1-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="621b1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="621b1-122"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="621b1-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="621b1-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="621b1-123">Library</span></span><br/> | <dl> <span data-ttu-id="621b1-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="621b1-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="621b1-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="621b1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="621b1-126">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="621b1-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




