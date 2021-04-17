---
description: Fornece inicialização em um thread.
ms.assetid: a9c330bb-0a2b-45bf-9b24-d03dd61d7dbf
title: Método CMsgThread. OnThreadInit (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.OnThreadInit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80e15d6430da77c0f22f5566375394b8fe6994ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759567"
---
# <a name="cmsgthreadonthreadinit-method"></a><span data-ttu-id="87cf6-103">Método CMsgThread. OnThreadInit</span><span class="sxs-lookup"><span data-stu-id="87cf6-103">CMsgThread.OnThreadInit method</span></span>

<span data-ttu-id="87cf6-104">Fornece inicialização em um thread.</span><span class="sxs-lookup"><span data-stu-id="87cf6-104">Provides initialization on a thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="87cf6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87cf6-105">Syntax</span></span>


```C++
virtual void OnThreadInit();
```



## <a name="parameters"></a><span data-ttu-id="87cf6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87cf6-106">Parameters</span></span>

<span data-ttu-id="87cf6-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="87cf6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="87cf6-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87cf6-108">Return value</span></span>

<span data-ttu-id="87cf6-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="87cf6-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87cf6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="87cf6-110">Remarks</span></span>

<span data-ttu-id="87cf6-111">Substitua essa função se você quiser fazer sua própria inicialização específica na inicialização do thread.</span><span class="sxs-lookup"><span data-stu-id="87cf6-111">Override this function if you want to do your own specific initialization on thread startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="87cf6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87cf6-112">Requirements</span></span>



| <span data-ttu-id="87cf6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="87cf6-113">Requirement</span></span> | <span data-ttu-id="87cf6-114">Valor</span><span class="sxs-lookup"><span data-stu-id="87cf6-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87cf6-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="87cf6-115">Header</span></span><br/>  | <dl> <span data-ttu-id="87cf6-116"><dt>Msgthrd. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87cf6-116"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="87cf6-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87cf6-117">Library</span></span><br/> | <dl> <span data-ttu-id="87cf6-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="87cf6-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87cf6-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="87cf6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87cf6-120">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="87cf6-120">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




