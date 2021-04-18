---
description: A função WaitDispatchingMessages aguarda que um objeto seja sinalizado, ao mesmo tempo que distribui mensagens de janela.
ms.assetid: d15f6736-d141-47a3-b767-fbf774982fb4
title: Função WaitDispatchingMessages (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WaitDispatchingMessages
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e509a081243f28293dc2d8abf8311f69eaf9a44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784013"
---
# <a name="waitdispatchingmessages-function"></a><span data-ttu-id="2fce6-103">Função WaitDispatchingMessages</span><span class="sxs-lookup"><span data-stu-id="2fce6-103">WaitDispatchingMessages function</span></span>

<span data-ttu-id="2fce6-104">A `WaitDispatchingMessages` função espera que um objeto seja sinalizado, ao mesmo tempo em que distribui mensagens de janela.</span><span class="sxs-lookup"><span data-stu-id="2fce6-104">The `WaitDispatchingMessages` function waits for an object to be signaled, while dispatching window messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fce6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2fce6-105">Syntax</span></span>


```C++
DWORD WINAPI WaitDispatchingMessages(
   HANDLE hObject,
   DWORD  dwWait,
   HWND   hwnd = NULL,
   UINT   uMsg = 0,
   HANDLE hEvent = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="2fce6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2fce6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fce6-107">*hObject*</span><span class="sxs-lookup"><span data-stu-id="2fce6-107">*hObject*</span></span> 
</dt> <dd>

<span data-ttu-id="2fce6-108">Identificador do objeto a ser aguardado.</span><span class="sxs-lookup"><span data-stu-id="2fce6-108">Handle of the object to wait for.</span></span>

</dd> <dt>

<span data-ttu-id="2fce6-109">*dwWait*</span><span class="sxs-lookup"><span data-stu-id="2fce6-109">*dwWait*</span></span> 
</dt> <dd>

<span data-ttu-id="2fce6-110">Intervalo de tempo limite, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="2fce6-110">Time-out interval, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="2fce6-111">*HWND*</span><span class="sxs-lookup"><span data-stu-id="2fce6-111">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="2fce6-112">Identificador opcional para uma janela.</span><span class="sxs-lookup"><span data-stu-id="2fce6-112">Optional handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="2fce6-113">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="2fce6-113">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="2fce6-114">Mensagem de janela opcional, especificando uma mensagem a ser expedida.</span><span class="sxs-lookup"><span data-stu-id="2fce6-114">Optional window message, specifying a message to dispatch.</span></span>

</dd> <dt>

<span data-ttu-id="2fce6-115">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="2fce6-115">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="2fce6-116">Identificador opcional para um evento a ser aguardado.</span><span class="sxs-lookup"><span data-stu-id="2fce6-116">Optional handle to an event to wait for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fce6-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2fce6-117">Return value</span></span>

<span data-ttu-id="2fce6-118">Retorna o valor da função **WaitForMultipleObjects** .</span><span class="sxs-lookup"><span data-stu-id="2fce6-118">Returns the value from the **WaitForMultipleObjects** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fce6-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2fce6-119">Remarks</span></span>

<span data-ttu-id="2fce6-120">Se um objeto possuir uma janela, ele deverá enviar mensagens da janela enquanto aguarda.</span><span class="sxs-lookup"><span data-stu-id="2fce6-120">If an object owns a window, it should dispatch window messages while waiting.</span></span> <span data-ttu-id="2fce6-121">Essa função permite que o objeto Aguarde um evento, um semáforo ou outro objeto de exclusão mútua ao expedir mensagens.</span><span class="sxs-lookup"><span data-stu-id="2fce6-121">This function enables the object to wait for an event, semaphore, or other mutual exclusion object while dispatching messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fce6-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fce6-122">Requirements</span></span>



| <span data-ttu-id="2fce6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fce6-123">Requirement</span></span> | <span data-ttu-id="2fce6-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2fce6-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fce6-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2fce6-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2fce6-126"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2fce6-126"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2fce6-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2fce6-127">Library</span></span><br/> | <dl> <span data-ttu-id="2fce6-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2fce6-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fce6-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="2fce6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fce6-130">Funções auxiliares diversas</span><span class="sxs-lookup"><span data-stu-id="2fce6-130">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




