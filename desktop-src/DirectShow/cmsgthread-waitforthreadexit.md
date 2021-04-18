---
description: Bloqueia até que o thread saia.
ms.assetid: 1ee547b5-cd73-4ce8-8e66-c2062714d0f0
title: Método CMsgThread. WaitForThreadExit (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.WaitForThreadExit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b48573c4297a2d5d5d008eba88fd8ea437333c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756193"
---
# <a name="cmsgthreadwaitforthreadexit-method"></a><span data-ttu-id="b943f-103">Método CMsgThread. WaitForThreadExit</span><span class="sxs-lookup"><span data-stu-id="b943f-103">CMsgThread.WaitForThreadExit method</span></span>

<span data-ttu-id="b943f-104">Bloqueia até que o thread saia.</span><span class="sxs-lookup"><span data-stu-id="b943f-104">Blocks until the thread exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="b943f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b943f-105">Syntax</span></span>


```C++
BOOL WaitForThreadExit(
   LPDWORD lpdwExitCode
);
```



## <a name="parameters"></a><span data-ttu-id="b943f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b943f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b943f-107">*lpdwExitCode*</span><span class="sxs-lookup"><span data-stu-id="b943f-107">*lpdwExitCode*</span></span> 
</dt> <dd>

<span data-ttu-id="b943f-108">Ponteiro para o código de saída retornado pelo thread.</span><span class="sxs-lookup"><span data-stu-id="b943f-108">Pointer to the exit code returned by the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b943f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b943f-109">Return value</span></span>

<span data-ttu-id="b943f-110">Retorna **true** ou **false**, o significado do que é determinado pela classe que fornece a função de membro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) substituída e a função de membro de chamada.</span><span class="sxs-lookup"><span data-stu-id="b943f-110">Returns either **TRUE** or **FALSE**, the meaning of which is determined by the class supplying the overridden [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function and the calling member function.</span></span>

## <a name="remarks"></a><span data-ttu-id="b943f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b943f-111">Remarks</span></span>

<span data-ttu-id="b943f-112">Verifique se o thread de trabalho foi encerrado completamente antes de concluir a destruição da classe derivada; caso contrário, o thread ainda poderá ser executado depois que a DLL (biblioteca de vínculo dinâmico) tiver sido descarregada do espaço de endereço do processo.</span><span class="sxs-lookup"><span data-stu-id="b943f-112">Ensure that the worker thread has exited completely before completing the destruction of your derived class; otherwise, the thread might still execute after your dynamic-link library (DLL) has been unloaded from the address space of the process.</span></span> <span data-ttu-id="b943f-113">Mesmo que a única instrução restante para sair seja uma instrução de retorno único, isso causaria uma exceção.</span><span class="sxs-lookup"><span data-stu-id="b943f-113">Even if the only instruction left to exit is a single-return instruction, this would cause an exception.</span></span> <span data-ttu-id="b943f-114">A única maneira confiável de garantir que o thread foi encerrado é sinalizar o thread para sair (usando um objeto [**CMsg**](cmsg.md) negociado privadamente enviado para a função membro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ) e, em seguida, chamar essa função de membro.</span><span class="sxs-lookup"><span data-stu-id="b943f-114">The only reliable way to ensure that the thread has exited is to signal the thread to exit (using a privately negotiated [**CMsg**](cmsg.md) object sent to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function) and then call this member function.</span></span> <span data-ttu-id="b943f-115">Você deve fazer isso no destruidor para sua classe derivada.</span><span class="sxs-lookup"><span data-stu-id="b943f-115">You should do this in the destructor for your derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="b943f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b943f-116">Requirements</span></span>



| <span data-ttu-id="b943f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b943f-117">Requirement</span></span> | <span data-ttu-id="b943f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b943f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b943f-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b943f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b943f-120"><dt>Msgthrd. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b943f-120"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b943f-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b943f-121">Library</span></span><br/> | <dl> <span data-ttu-id="b943f-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b943f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b943f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b943f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b943f-124">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="b943f-124">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




