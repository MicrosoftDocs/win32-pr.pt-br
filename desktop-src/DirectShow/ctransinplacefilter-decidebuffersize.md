---
description: O método DecideBufferSize define os requisitos de buffer do pino de saída.
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
ms.openlocfilehash: 55227510eee3c1afdcd14ed390edf21eccfcf1de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758649"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a><span data-ttu-id="afffc-103">Método CTransInPlaceFilter. DecideBufferSize</span><span class="sxs-lookup"><span data-stu-id="afffc-103">CTransInPlaceFilter.DecideBufferSize method</span></span>

<span data-ttu-id="afffc-104">O `DecideBufferSize` método define os requisitos de buffer do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="afffc-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="afffc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="afffc-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProperties
);
```



## <a name="parameters"></a><span data-ttu-id="afffc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="afffc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afffc-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="afffc-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="afffc-108">Ponteiro para o objeto [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) usado pelo pino de saída.</span><span class="sxs-lookup"><span data-stu-id="afffc-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) object used by the output pin.</span></span>

</dd> <dt>

<span data-ttu-id="afffc-109">*pProperties*</span><span class="sxs-lookup"><span data-stu-id="afffc-109">*pProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="afffc-110">Ponteiro para as propriedades de alocador solicitadas para contagem, tamanho e alinhamento, conforme especificado pela estrutura de [**\_ Propriedades do alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) .</span><span class="sxs-lookup"><span data-stu-id="afffc-110">Pointer to the requested allocator properties for count, size, and alignment, as specified by the [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afffc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="afffc-111">Return value</span></span>

<span data-ttu-id="afffc-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="afffc-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="afffc-113">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="afffc-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="afffc-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="afffc-114">Return code</span></span>                                                                            | <span data-ttu-id="afffc-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="afffc-115">Description</span></span>        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="afffc-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="afffc-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="afffc-117">Sucesso</span><span class="sxs-lookup"><span data-stu-id="afffc-117">Success</span></span><br/> |
| <dl> <span data-ttu-id="afffc-118"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="afffc-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="afffc-119">Falha</span><span class="sxs-lookup"><span data-stu-id="afffc-119">Failure</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="afffc-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="afffc-120">Remarks</span></span>

<span data-ttu-id="afffc-121">Esse método é chamado quando a classe **CTransInPlaceFilter** precisa fornecer um tamanho de buffer para o filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="afffc-121">This method is called when the **CTransInPlaceFilter** class needs to provide a buffer size to the downstream filter.</span></span> <span data-ttu-id="afffc-122">Se o filtro **CTransInPlaceFilter** já estiver conectado ao upstream, ele usará as propriedades de alocador na conexão de PIN upstream.</span><span class="sxs-lookup"><span data-stu-id="afffc-122">If the **CTransInPlaceFilter** filter is already connected upstream, it uses the allocator properties on the upstream pin connection.</span></span> <span data-ttu-id="afffc-123">Caso contrário, ele define o tamanho do buffer como 1 byte como um valor de espaço reservado temporário.</span><span class="sxs-lookup"><span data-stu-id="afffc-123">Otherwise, it sets the buffer size to 1 byte as a temporary place-holder value.</span></span> <span data-ttu-id="afffc-124">Quando o filtro upstream se conecta, a classe **CTransInPlaceFilter** renegocia o alocador downstream.</span><span class="sxs-lookup"><span data-stu-id="afffc-124">When the upstream filter connects, the **CTransInPlaceFilter** class renegotiates the downstream allocator.</span></span> <span data-ttu-id="afffc-125">Para obter mais informações sobre o processo de conexão de PIN nessa classe, consulte [**classe CTransInPlaceFilter**](ctransinplacefilter.md).</span><span class="sxs-lookup"><span data-stu-id="afffc-125">For more information about the pin connection process in this class, see [**CTransInPlaceFilter Class**](ctransinplacefilter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="afffc-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afffc-126">Requirements</span></span>



| <span data-ttu-id="afffc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="afffc-127">Requirement</span></span> | <span data-ttu-id="afffc-128">Valor</span><span class="sxs-lookup"><span data-stu-id="afffc-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afffc-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="afffc-129">Header</span></span><br/>  | <dl> <span data-ttu-id="afffc-130"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="afffc-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="afffc-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="afffc-131">Library</span></span><br/> | <dl> <span data-ttu-id="afffc-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="afffc-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afffc-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="afffc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afffc-134">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="afffc-134">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




