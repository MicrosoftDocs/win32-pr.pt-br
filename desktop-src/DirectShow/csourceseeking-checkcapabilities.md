---
description: 'O método CheckCapabilities consulta se o fluxo especificou recursos de busca. Esse método implementa o método IMediaSeeking:: CheckCapabilities.'
ms.assetid: 5d37e179-9e04-44e1-acbc-dfd2682830c0
title: Método CSourceSeeking. CheckCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f537973ac6c8f084ea42ba915a6293e581debef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748622"
---
# <a name="csourceseekingcheckcapabilities-method"></a><span data-ttu-id="5bd09-104">Método CSourceSeeking. CheckCapabilities</span><span class="sxs-lookup"><span data-stu-id="5bd09-104">CSourceSeeking.CheckCapabilities method</span></span>

<span data-ttu-id="5bd09-105">O `CheckCapabilities` método consulta se o fluxo especificou recursos de busca.</span><span class="sxs-lookup"><span data-stu-id="5bd09-105">The `CheckCapabilities` method queries whether the stream has specified seeking capabilities.</span></span> <span data-ttu-id="5bd09-106">Esse método implementa o método [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="5bd09-106">This method implements the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bd09-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bd09-107">Syntax</span></span>


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="5bd09-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bd09-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bd09-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="5bd09-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="5bd09-110">Ponteiro para uma combinação de bits de um ou mais atributos de [**\_ \_ \_ recursos de busca**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) em busca.</span><span class="sxs-lookup"><span data-stu-id="5bd09-110">Pointer to a bitwise combination of one or more [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bd09-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5bd09-111">Return value</span></span>

<span data-ttu-id="5bd09-112">Retorna um dos valores **HRESULT** listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5bd09-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="5bd09-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5bd09-113">Return code</span></span>                                                                               | <span data-ttu-id="5bd09-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5bd09-114">Description</span></span>                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5bd09-115"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="5bd09-115"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="5bd09-116">Nem todos os recursos do *pCapabilities* estão presentes.</span><span class="sxs-lookup"><span data-stu-id="5bd09-116">Not all of the capabilities in *pCapabilities* are present.</span></span><br/> |
| <dl> <span data-ttu-id="5bd09-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5bd09-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="5bd09-118">Todos os recursos do *pCapabilities* estão presentes.</span><span class="sxs-lookup"><span data-stu-id="5bd09-118">All capabilities in *pCapabilities* are present.</span></span><br/>            |
| <dl> <span data-ttu-id="5bd09-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="5bd09-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="5bd09-120">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="5bd09-120">**NULL** pointer argument.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="5bd09-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bd09-121">Remarks</span></span>

<span data-ttu-id="5bd09-122">Conforme implementado, esse método verifica o valor de *\* pCapabilities* em relação à variável de membro [**CSourceSeeking:: m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="5bd09-122">As implemented, this method checks the value of *\*pCapabilities* against the [**CSourceSeeking::m\_dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) member variable.</span></span> <span data-ttu-id="5bd09-123">No entanto, ele não define *\* pCapabilities* igual a **m \_ dwSeekingCaps**, conforme descrito para o método [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="5bd09-123">However, it does not set *\*pCapabilities* equal to **m\_dwSeekingCaps**, as described for the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span> <span data-ttu-id="5bd09-124">Além disso, no caso em que nenhum dos recursos especificados está disponível, o método não retorna E \_ falha.</span><span class="sxs-lookup"><span data-stu-id="5bd09-124">Also, in the case where none of the specified capabilities are available, the method does not return E\_FAIL.</span></span> <span data-ttu-id="5bd09-125">Uma implementação mais completa seria a seguinte:</span><span class="sxs-lookup"><span data-stu-id="5bd09-125">A more complete implementation would be as follows:</span></span>


```C++
STDMETHODIMP CheckCapabilities(DWORD *pCapabilities)
{
    CheckPointer(pCapabilities, E_POINTER)
;
    DWORD dwCaps;
    HRESULT hr = GetCapabilities(&dwCaps);
    if (SUCCEEDED(hr))
    {
        dwCaps &= *pCapabilities;
        if (dwCaps)
        {
            hr =  (dwCaps == *pCapabilities ? S_OK : S_FALSE );
        }
        else 
        {
            hr = E_FAIL;
        }
        *pCapabilities = dwCaps;
    }
    else 
    {
        *pCapabilities = 0;
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="5bd09-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bd09-126">Requirements</span></span>



| <span data-ttu-id="5bd09-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bd09-127">Requirement</span></span> | <span data-ttu-id="5bd09-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5bd09-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bd09-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5bd09-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5bd09-130"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5bd09-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5bd09-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5bd09-131">Library</span></span><br/> | <dl> <span data-ttu-id="5bd09-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5bd09-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bd09-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bd09-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bd09-134">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="5bd09-134">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




