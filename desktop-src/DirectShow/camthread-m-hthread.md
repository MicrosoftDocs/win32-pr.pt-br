---
description: Identificador para o thread.
ms.assetid: 93d1182a-58f0-4570-8568-fe0fded762cb
title: 'Membro CAMThread:: m_hThread (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hThread
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e83dd225da0c3673f9c7f423e0bf56da7431b097
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784035"
---
# <a name="camthreadm_hthread-member"></a><span data-ttu-id="5fa86-103">Membro de CAMThread:: m \_ hThread</span><span class="sxs-lookup"><span data-stu-id="5fa86-103">CAMThread::m\_hThread member</span></span>

<span data-ttu-id="5fa86-104">Identificador para o thread.</span><span class="sxs-lookup"><span data-stu-id="5fa86-104">Handle to the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fa86-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fa86-105">Syntax</span></span>


```C++
HANDLE m_hThread;
```



## <a name="remarks"></a><span data-ttu-id="5fa86-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="5fa86-106">Remarks</span></span>

<span data-ttu-id="5fa86-107">Esta variável foi inicializada como **nula**.</span><span class="sxs-lookup"><span data-stu-id="5fa86-107">This variable is initialized as **NULL**.</span></span> <span data-ttu-id="5fa86-108">O método [**CAMThread:: Create**](camthread-create.md) define essa variável como o identificador de thread.</span><span class="sxs-lookup"><span data-stu-id="5fa86-108">The [**CAMThread::Create**](camthread-create.md) method sets this variable to the thread handle.</span></span> <span data-ttu-id="5fa86-109">Para determinar se o thread existe, chame o método [**CAMThread:: ThreadExists**](camthread-threadexists.md) .</span><span class="sxs-lookup"><span data-stu-id="5fa86-109">To determine whether the thread exists, call the [**CAMThread::ThreadExists**](camthread-threadexists.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fa86-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fa86-110">Requirements</span></span>



| <span data-ttu-id="5fa86-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fa86-111">Requirement</span></span> | <span data-ttu-id="5fa86-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5fa86-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa86-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5fa86-113">Header</span></span><br/>  | <dl> <span data-ttu-id="5fa86-114"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5fa86-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5fa86-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5fa86-115">Library</span></span><br/> | <dl> <span data-ttu-id="5fa86-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5fa86-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fa86-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fa86-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fa86-118">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="5fa86-118">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




