---
description: O método DecideAllocator negocia um alocador com o pino de saída.
ms.assetid: 5c04f440-b177-4caa-989f-3aa783c4b348
title: Método CPullPin. DecideAllocator (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91ffa139b916b1594e0729a0f8d52f07c62eda12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789957"
---
# <a name="cpullpindecideallocator-method"></a><span data-ttu-id="44d19-103">Método CPullPin. DecideAllocator</span><span class="sxs-lookup"><span data-stu-id="44d19-103">CPullPin.DecideAllocator method</span></span>

<span data-ttu-id="44d19-104">O `DecideAllocator` método negocia um alocador com o pino de saída.</span><span class="sxs-lookup"><span data-stu-id="44d19-104">The `DecideAllocator` method negotiates an allocator with the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="44d19-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44d19-105">Syntax</span></span>


```C++
virtual HRESULT DecideAllocator(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="44d19-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44d19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44d19-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="44d19-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="44d19-108">Ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador preferencial do pino de entrada ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="44d19-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the input pin's preferred allocator, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="44d19-109">*pProps*</span><span class="sxs-lookup"><span data-stu-id="44d19-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="44d19-110">Ponteiro para uma estrutura [**de \_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) opcional que contém os requisitos de buffer do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="44d19-110">Pointer to an optional [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44d19-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44d19-111">Return value</span></span>

<span data-ttu-id="44d19-112">Retorna S \_ OK se for bem-sucedido ou um código de erro do contrário.</span><span class="sxs-lookup"><span data-stu-id="44d19-112">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="44d19-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="44d19-113">Remarks</span></span>

<span data-ttu-id="44d19-114">Esse método chama o método [**IAsyncReader:: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) para negociar um alocador.</span><span class="sxs-lookup"><span data-stu-id="44d19-114">This method calls the [**IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) method to negotiate an allocator.</span></span> <span data-ttu-id="44d19-115">Ele passa o parâmetro *pAlloc* diretamente para o método **RequestAllocator** .</span><span class="sxs-lookup"><span data-stu-id="44d19-115">It passes the *pAlloc* parameter directly to the **RequestAllocator** method.</span></span> <span data-ttu-id="44d19-116">Ele passa o parâmetro *pProps* para **RequestAllocator** se *pProps* não for **nulo**; caso contrário, ele cria uma estrutura de **\_ Propriedades de alocador** com uma solicitação padrão de três buffers de 64K.</span><span class="sxs-lookup"><span data-stu-id="44d19-116">It passes the *pProps* parameter to **RequestAllocator** if *pProps* is non-**NULL**; otherwise, it creates an **ALLOCATOR\_PROPERTIES** structure with a default request of three 64K buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="44d19-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44d19-117">Requirements</span></span>



| <span data-ttu-id="44d19-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="44d19-118">Requirement</span></span> | <span data-ttu-id="44d19-119">Valor</span><span class="sxs-lookup"><span data-stu-id="44d19-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44d19-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44d19-120">Header</span></span><br/>  | <dl> <span data-ttu-id="44d19-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="44d19-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="44d19-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="44d19-122">Library</span></span><br/> | <dl> <span data-ttu-id="44d19-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="44d19-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44d19-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="44d19-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44d19-125">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="44d19-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> <dt>

[<span data-ttu-id="44d19-126">**CPullPin:: conectar**</span><span class="sxs-lookup"><span data-stu-id="44d19-126">**CPullPin::Connect**</span></span>](cpullpin-connect.md)
</dt> </dl>

 

 




