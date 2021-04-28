---
description: Método CTransInPlaceFilter. DecideBufferSize – o método DecideBufferSize define os requisitos de buffer do pino de saída.
ms.assetid: f1ddc39e-dcd5-4a44-8a8e-e384692408e1
title: Método CTransInPlaceFilter. DecideBufferSize (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b3ffb3ec7b1ef59c6e7f3d49e39fbe69e8cc1c08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094824"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a><span data-ttu-id="68c6a-103">Método CTransInPlaceFilter. DecideBufferSize</span><span class="sxs-lookup"><span data-stu-id="68c6a-103">CTransInPlaceFilter.DecideBufferSize method</span></span>

<span data-ttu-id="68c6a-104">O `DecideBufferSize` método define os requisitos de buffer do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="68c6a-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="68c6a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68c6a-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProperties
);
```



## <a name="parameters"></a><span data-ttu-id="68c6a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68c6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68c6a-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="68c6a-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="68c6a-108">Ponteiro para o objeto [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) usado pelo pino de saída.</span><span class="sxs-lookup"><span data-stu-id="68c6a-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) object used by the output pin.</span></span>

</dd> <dt>

<span data-ttu-id="68c6a-109">*pProperties*</span><span class="sxs-lookup"><span data-stu-id="68c6a-109">*pProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="68c6a-110">Ponteiro para as propriedades de alocador solicitadas para contagem, tamanho e alinhamento, conforme especificado pela estrutura de [**\_ Propriedades do alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) .</span><span class="sxs-lookup"><span data-stu-id="68c6a-110">Pointer to the requested allocator properties for count, size, and alignment, as specified by the [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68c6a-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="68c6a-111">Return value</span></span>

<span data-ttu-id="68c6a-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="68c6a-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="68c6a-113">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="68c6a-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="68c6a-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="68c6a-114">Return code</span></span>                                                                            | <span data-ttu-id="68c6a-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="68c6a-115">Description</span></span>        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="68c6a-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="68c6a-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="68c6a-117">Êxito</span><span class="sxs-lookup"><span data-stu-id="68c6a-117">Success</span></span><br/> |
| <dl> <span data-ttu-id="68c6a-118"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="68c6a-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="68c6a-119">Falha</span><span class="sxs-lookup"><span data-stu-id="68c6a-119">Failure</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="68c6a-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="68c6a-120">Remarks</span></span>

<span data-ttu-id="68c6a-121">Esse método é chamado quando a classe **CTransInPlaceFilter** precisa fornecer um tamanho de buffer para o filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="68c6a-121">This method is called when the **CTransInPlaceFilter** class needs to provide a buffer size to the downstream filter.</span></span> <span data-ttu-id="68c6a-122">Se o filtro **CTransInPlaceFilter** já estiver conectado ao upstream, ele usará as propriedades de alocador na conexão de PIN upstream.</span><span class="sxs-lookup"><span data-stu-id="68c6a-122">If the **CTransInPlaceFilter** filter is already connected upstream, it uses the allocator properties on the upstream pin connection.</span></span> <span data-ttu-id="68c6a-123">Caso contrário, ele define o tamanho do buffer como 1 byte como um valor de espaço reservado temporário.</span><span class="sxs-lookup"><span data-stu-id="68c6a-123">Otherwise, it sets the buffer size to 1 byte as a temporary place-holder value.</span></span> <span data-ttu-id="68c6a-124">Quando o filtro upstream se conecta, a classe **CTransInPlaceFilter** renegocia o alocador downstream.</span><span class="sxs-lookup"><span data-stu-id="68c6a-124">When the upstream filter connects, the **CTransInPlaceFilter** class renegotiates the downstream allocator.</span></span> <span data-ttu-id="68c6a-125">Para obter mais informações sobre o processo de conexão de PIN nessa classe, consulte [**classe CTransInPlaceFilter**](ctransinplacefilter.md).</span><span class="sxs-lookup"><span data-stu-id="68c6a-125">For more information about the pin connection process in this class, see [**CTransInPlaceFilter Class**](ctransinplacefilter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68c6a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68c6a-126">Requirements</span></span>



| <span data-ttu-id="68c6a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="68c6a-127">Requirement</span></span> | <span data-ttu-id="68c6a-128">Valor</span><span class="sxs-lookup"><span data-stu-id="68c6a-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68c6a-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68c6a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="68c6a-130"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="68c6a-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="68c6a-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68c6a-131">Library</span></span><br/> | <dl> <span data-ttu-id="68c6a-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="68c6a-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68c6a-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="68c6a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68c6a-134">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="68c6a-134">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




