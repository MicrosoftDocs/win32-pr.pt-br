---
description: O método de trocador é chamado quando a taxa de reprodução é alterada.
ms.assetid: c4f1f9d0-6c09-4cab-8a37-dd1ff3f5619f
title: Método CSourceSeeking. Disqueteiraize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02fab05d65929233b97f7d53e497bae6593c472a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782852"
---
# <a name="csourceseekingchangerate-method"></a><span data-ttu-id="521f1-103">Método CSourceSeeking. peralterador</span><span class="sxs-lookup"><span data-stu-id="521f1-103">CSourceSeeking.ChangeRate method</span></span>

<span data-ttu-id="521f1-104">O `ChangeRate` método é chamado quando a taxa de reprodução é alterada.</span><span class="sxs-lookup"><span data-stu-id="521f1-104">The `ChangeRate` method is called when the playback rate changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="521f1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="521f1-105">Syntax</span></span>


```C++
virtual HRESULT ChangeRate() = 0;
```



## <a name="parameters"></a><span data-ttu-id="521f1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="521f1-106">Parameters</span></span>

<span data-ttu-id="521f1-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="521f1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="521f1-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="521f1-108">Return value</span></span>

<span data-ttu-id="521f1-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="521f1-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="521f1-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="521f1-110">Remarks</span></span>

<span data-ttu-id="521f1-111">O método [**CSourceSeeking:: SetRate**](csourceseeking-setrate.md) chama esse método, que a classe derivada deve implementar.</span><span class="sxs-lookup"><span data-stu-id="521f1-111">The [**CSourceSeeking::SetRate**](csourceseeking-setrate.md) method calls this method, which the derived class must implement.</span></span> <span data-ttu-id="521f1-112">O método **SetRate** atualiza a variável de membro [**CSourceSeeking:: m \_ dRateSeeking**](csourceseeking-m-drateseeking.md) , mas não valida o novo valor.</span><span class="sxs-lookup"><span data-stu-id="521f1-112">The **SetRate** method updates the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable, but does not validate the new value.</span></span> <span data-ttu-id="521f1-113">Uma taxa de zero sempre deve ser rejeitada.</span><span class="sxs-lookup"><span data-stu-id="521f1-113">A rate of zero should always be rejected.</span></span> <span data-ttu-id="521f1-114">Taxas menores que zero indicam reprodução negativa.</span><span class="sxs-lookup"><span data-stu-id="521f1-114">Rates less than zero indicate negative playback.</span></span> <span data-ttu-id="521f1-115">A maioria dos filtros não oferece suporte a taxas negativas.</span><span class="sxs-lookup"><span data-stu-id="521f1-115">Most filters do not support negative rates.</span></span>

<span data-ttu-id="521f1-116">O exemplo a seguir mostra uma possível implementação:</span><span class="sxs-lookup"><span data-stu-id="521f1-116">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeRate( )
{
    {   // Scope for critical section lock.
        CAutoLock cAutoLockSeeking(CSourceSeeking::m_pLock);
        if( m_dRateSeeking <= 0 ) {
            m_dRateSeeking = 1.0;  // Reset to a reasonable value.
            return E_FAIL;
        }
    }
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="521f1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="521f1-117">Requirements</span></span>



| <span data-ttu-id="521f1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="521f1-118">Requirement</span></span> | <span data-ttu-id="521f1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="521f1-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="521f1-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="521f1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="521f1-121"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="521f1-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="521f1-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="521f1-122">Library</span></span><br/> | <dl> <span data-ttu-id="521f1-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="521f1-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="521f1-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="521f1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="521f1-125">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="521f1-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




