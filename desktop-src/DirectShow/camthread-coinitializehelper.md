---
description: O método CoInitializeHelper chama a função CoInitializeEx no início do thread.
ms.assetid: 1a981e1e-c059-4e51-81d8-33bcb39ee580
title: Método CAMThread. CoInitializeHelper (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CoInitializeHelper
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6c3eb7fbcb9e4abada43098339a29d208ded0d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753761"
---
# <a name="camthreadcoinitializehelper-method"></a><span data-ttu-id="fa037-103">Método CAMThread. CoInitializeHelper</span><span class="sxs-lookup"><span data-stu-id="fa037-103">CAMThread.CoInitializeHelper method</span></span>

<span data-ttu-id="fa037-104">O `CoInitializeHelper` método chama a função CoInitializeEx no início do thread.</span><span class="sxs-lookup"><span data-stu-id="fa037-104">The `CoInitializeHelper` method calls the CoInitializeEx function at the start of the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa037-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa037-105">Syntax</span></span>


```C++
static HRESULT CoInitializeHelper();
```



## <a name="parameters"></a><span data-ttu-id="fa037-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa037-106">Parameters</span></span>

<span data-ttu-id="fa037-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fa037-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa037-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa037-108">Return value</span></span>

<span data-ttu-id="fa037-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fa037-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="fa037-110">Os valores a seguir são possíveis.</span><span class="sxs-lookup"><span data-stu-id="fa037-110">The following are possible values.</span></span>



| <span data-ttu-id="fa037-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fa037-111">Return code</span></span>                                                                             | <span data-ttu-id="fa037-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa037-112">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="fa037-113"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="fa037-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="fa037-114">A função CoInitializeEx não está disponível.</span><span class="sxs-lookup"><span data-stu-id="fa037-114">The CoInitializeEx function is not available.</span></span><br/> |
| <dl> <span data-ttu-id="fa037-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fa037-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="fa037-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="fa037-116">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="fa037-117"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="fa037-117"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="fa037-118">Falha.</span><span class="sxs-lookup"><span data-stu-id="fa037-118">Failure.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="fa037-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa037-119">Remarks</span></span>

<span data-ttu-id="fa037-120">O método [**CAMThread:: InitialThreadProc**](camthread-initialthreadproc.md) chama esse método auxiliar, que chama a função CoInitializeEx.</span><span class="sxs-lookup"><span data-stu-id="fa037-120">The [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method calls this helper method, which calls the CoInitializeEx function.</span></span> <span data-ttu-id="fa037-121">Ele usa o sinalizador de \_ desabilitar OLE1DDE do coinit \_ para desabilitar o troca dinâmica de dados (DDE).</span><span class="sxs-lookup"><span data-stu-id="fa037-121">It uses the COINIT\_DISABLE\_OLE1DDE flag, to disable Dynamic Data Exchange (DDE).</span></span> <span data-ttu-id="fa037-122">Para obter mais informações, consulte o SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="fa037-122">For more information, see the Platform SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa037-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa037-123">Requirements</span></span>



| <span data-ttu-id="fa037-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa037-124">Requirement</span></span> | <span data-ttu-id="fa037-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fa037-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa037-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa037-126">Header</span></span><br/>  | <dl> <span data-ttu-id="fa037-127"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa037-127"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="fa037-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa037-128">Library</span></span><br/> | <dl> <span data-ttu-id="fa037-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fa037-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa037-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa037-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa037-131">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="fa037-131">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




