---
description: O método InitialThreadProc chama o procedimento de thread principal.
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: CAMThread.Inimétodo tialThreadProc (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd7fd0aa12d0659776db7e39fb223095762fc209
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757049"
---
# <a name="camthreadinitialthreadproc-method"></a><span data-ttu-id="77ece-103">CAMThread.Inimétodo tialThreadProc</span><span class="sxs-lookup"><span data-stu-id="77ece-103">CAMThread.InitialThreadProc method</span></span>

<span data-ttu-id="77ece-104">O `InitialThreadProc` método chama o procedimento de thread principal.</span><span class="sxs-lookup"><span data-stu-id="77ece-104">The `InitialThreadProc` method calls the main thread procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="77ece-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77ece-105">Syntax</span></span>


```C++
DWORD InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a><span data-ttu-id="77ece-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77ece-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77ece-107">*PV*</span><span class="sxs-lookup"><span data-stu-id="77ece-107">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="77ece-108">`this` refere.</span><span class="sxs-lookup"><span data-stu-id="77ece-108">`this` pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77ece-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77ece-109">Return value</span></span>

<span data-ttu-id="77ece-110">Retorna o **DWORD** retornado por [**CAMThread:: ThreadProc**](camthread-threadproc.md).</span><span class="sxs-lookup"><span data-stu-id="77ece-110">Returns the **DWORD** returned by [**CAMThread::ThreadProc**](camthread-threadproc.md).</span></span> <span data-ttu-id="77ece-111">A classe derivada define esse valor.</span><span class="sxs-lookup"><span data-stu-id="77ece-111">The derived class defines this value.</span></span>

## <a name="remarks"></a><span data-ttu-id="77ece-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="77ece-112">Remarks</span></span>

<span data-ttu-id="77ece-113">O método [**CAMThread:: Create**](camthread-create.md) usa esse método para o procedimento de thread quando ele cria o thread.</span><span class="sxs-lookup"><span data-stu-id="77ece-113">The [**CAMThread::Create**](camthread-create.md) method uses this method for the thread procedure when it creates the thread.</span></span> <span data-ttu-id="77ece-114">Ele usa o `this` ponteiro como o argumento de thread.</span><span class="sxs-lookup"><span data-stu-id="77ece-114">It uses the `this` pointer as the thread argument.</span></span>

<span data-ttu-id="77ece-115">Esse método chama o método [**CAMThread:: CoInitializeHelper**](camthread-coinitializehelper.md) e, em seguida, ThreadProc.</span><span class="sxs-lookup"><span data-stu-id="77ece-115">This method calls the [**CAMThread::CoInitializeHelper**](camthread-coinitializehelper.md) method and then ThreadProc.</span></span>

## <a name="requirements"></a><span data-ttu-id="77ece-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77ece-116">Requirements</span></span>



| <span data-ttu-id="77ece-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="77ece-117">Requirement</span></span> | <span data-ttu-id="77ece-118">Valor</span><span class="sxs-lookup"><span data-stu-id="77ece-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77ece-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77ece-119">Header</span></span><br/>  | <dl> <span data-ttu-id="77ece-120"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="77ece-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="77ece-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77ece-121">Library</span></span><br/> | <dl> <span data-ttu-id="77ece-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="77ece-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77ece-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="77ece-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77ece-124">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="77ece-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




