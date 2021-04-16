---
description: Define o valor de tempo limite de depuração. Ignorado em compilações de varejo.
ms.assetid: d0f60d8b-34f2-44b2-bdd6-5e8e6f7806d8
title: Função DbgSetWaitTimeout (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetWaitTimeout
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5805112b19132045e0245ef7baf29cb5c844e290
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751236"
---
# <a name="dbgsetwaittimeout-function"></a><span data-ttu-id="4a733-104">Função DbgSetWaitTimeout</span><span class="sxs-lookup"><span data-stu-id="4a733-104">DbgSetWaitTimeout function</span></span>

<span data-ttu-id="4a733-105">Define o valor de tempo limite de depuração.</span><span class="sxs-lookup"><span data-stu-id="4a733-105">Sets the debugging time-out value.</span></span> <span data-ttu-id="4a733-106">Ignorado em compilações de varejo.</span><span class="sxs-lookup"><span data-stu-id="4a733-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a733-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a733-107">Syntax</span></span>


```C++
void DbgSetWaitTimeout(
   DWORD dwTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="4a733-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a733-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a733-109">*dwTimeout*</span><span class="sxs-lookup"><span data-stu-id="4a733-109">*dwTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="4a733-110">Valor de tempo limite em milissegundos ou infinito para aguardar indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="4a733-110">Time-out value in milliseconds, or INFINITE to wait indefinitely.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a733-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a733-111">Return value</span></span>

<span data-ttu-id="4a733-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4a733-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a733-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a733-113">Remarks</span></span>

<span data-ttu-id="4a733-114">Em compilações de depuração, as funções [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) e [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) usam esse valor como o intervalo de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="4a733-114">In debug builds, the [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) and [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) functions use this value as the time-out interval.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a733-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a733-115">Requirements</span></span>



| <span data-ttu-id="4a733-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a733-116">Requirement</span></span> | <span data-ttu-id="4a733-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4a733-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a733-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4a733-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4a733-119"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a733-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4a733-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a733-120">Library</span></span><br/> | <dl> <span data-ttu-id="4a733-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4a733-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a733-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a733-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a733-123">Aguardar funções de depuração</span><span class="sxs-lookup"><span data-stu-id="4a733-123">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




