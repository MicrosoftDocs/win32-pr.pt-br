---
description: Método de construtor.
ms.assetid: 3f758c45-21ec-4728-ba7d-41da7b2fa02f
title: Construtor CMsgThread. CMsgThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CMsgThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e77d3a84e349ab370b6319cd973f6ba86d632366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758543"
---
# <a name="cmsgthreadcmsgthread-constructor"></a><span data-ttu-id="2ce65-103">Construtor CMsgThread. CMsgThread</span><span class="sxs-lookup"><span data-stu-id="2ce65-103">CMsgThread.CMsgThread constructor</span></span>

<span data-ttu-id="2ce65-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="2ce65-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ce65-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ce65-105">Syntax</span></span>


```C++
CMsgThread();
```



## <a name="parameters"></a><span data-ttu-id="2ce65-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ce65-106">Parameters</span></span>

<span data-ttu-id="2ce65-107">Este construtor não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2ce65-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ce65-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ce65-108">Remarks</span></span>

<span data-ttu-id="2ce65-109">A construção de um objeto de thread de mensagem não cria automaticamente o thread.</span><span class="sxs-lookup"><span data-stu-id="2ce65-109">Constructing a message thread object does not automatically create the thread.</span></span> <span data-ttu-id="2ce65-110">Você deve chamar a função de membro [**CMsgThread:: CreateThread**](cmsgthread-createthread.md) para criar o thread.</span><span class="sxs-lookup"><span data-stu-id="2ce65-110">You must call the [**CMsgThread::CreateThread**](cmsgthread-createthread.md) member function to create the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ce65-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ce65-111">Requirements</span></span>



| <span data-ttu-id="2ce65-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ce65-112">Requirement</span></span> | <span data-ttu-id="2ce65-113">Valor</span><span class="sxs-lookup"><span data-stu-id="2ce65-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ce65-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ce65-114">Header</span></span><br/>  | <dl> <span data-ttu-id="2ce65-115"><dt>Msgthrd. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ce65-115"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2ce65-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ce65-116">Library</span></span><br/> | <dl> <span data-ttu-id="2ce65-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2ce65-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ce65-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ce65-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ce65-119">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="2ce65-119">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




