---
description: Usa a função SetThreadPriority do Microsoft Win32 para definir a prioridade do thread para um novo valor.
ms.assetid: 5b8ad024-e651-47e5-b32a-c44d56c086cd
title: Método CMsgThread. SetThreadPriority (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cfa3cd81907a251d2acf7129405e187286df3c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754533"
---
# <a name="cmsgthreadsetthreadpriority-method"></a><span data-ttu-id="6630e-103">Método CMsgThread. SetThreadPriority</span><span class="sxs-lookup"><span data-stu-id="6630e-103">CMsgThread.SetThreadPriority method</span></span>

<span data-ttu-id="6630e-104">Usa a função **SetThreadPriority** do Microsoft Win32 para definir a prioridade do thread para um novo valor.</span><span class="sxs-lookup"><span data-stu-id="6630e-104">Uses the Microsoft Win32 **SetThreadPriority** function to set the priority of the thread to a new value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6630e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6630e-105">Syntax</span></span>


```C++
BOOL SetThreadPriority(
   int nPriority
);
```



## <a name="parameters"></a><span data-ttu-id="6630e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6630e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6630e-107">*nPriority*</span><span class="sxs-lookup"><span data-stu-id="6630e-107">*nPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="6630e-108">Prioridade do thread.</span><span class="sxs-lookup"><span data-stu-id="6630e-108">Priority of the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6630e-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6630e-109">Return value</span></span>

<span data-ttu-id="6630e-110">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6630e-110">Returns one of the following values.</span></span>



| <span data-ttu-id="6630e-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6630e-111">Return code</span></span>                                                                              | <span data-ttu-id="6630e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="6630e-112">Description</span></span>                               |
|------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="6630e-113"><dt>VERDADEIRO \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="6630e-113"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>  | <span data-ttu-id="6630e-114">A prioridade foi definida com êxito.</span><span class="sxs-lookup"><span data-stu-id="6630e-114">Priority was successfully set.</span></span><br/> |
| <dl> <span data-ttu-id="6630e-115"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="6630e-115"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="6630e-116">A prioridade não foi definida.</span><span class="sxs-lookup"><span data-stu-id="6630e-116">Priority was not set.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="6630e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6630e-117">Remarks</span></span>

<span data-ttu-id="6630e-118">O cliente e o thread de trabalho podem chamar essa função de membro.</span><span class="sxs-lookup"><span data-stu-id="6630e-118">The client and the worker thread can call this member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6630e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6630e-119">Requirements</span></span>



| <span data-ttu-id="6630e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6630e-120">Requirement</span></span> | <span data-ttu-id="6630e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6630e-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6630e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6630e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6630e-123"><dt>Msgthrd. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6630e-123"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6630e-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6630e-124">Library</span></span><br/> | <dl> <span data-ttu-id="6630e-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6630e-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6630e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6630e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6630e-127">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="6630e-127">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




