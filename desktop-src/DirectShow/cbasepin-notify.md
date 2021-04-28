---
description: 'Método CBasePin. Notify – o método Notify notifica o PIN de que uma alteração de qualidade é solicitada. Esse método implementa o método IQualityControl:: Notify.'
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: Método CBasePin. Notify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35e751fb583010402df53e1a85eca11f751eda24
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096014"
---
# <a name="cbasepinnotify-method"></a><span data-ttu-id="4e7df-104">Método CBasePin. Notify</span><span class="sxs-lookup"><span data-stu-id="4e7df-104">CBasePin.Notify method</span></span>

<span data-ttu-id="4e7df-105">O `Notify` método notifica o PIN de que uma alteração de qualidade é solicitada.</span><span class="sxs-lookup"><span data-stu-id="4e7df-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="4e7df-106">Esse método implementa o método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .</span><span class="sxs-lookup"><span data-stu-id="4e7df-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e7df-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e7df-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="4e7df-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e7df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e7df-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="4e7df-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="4e7df-110">Ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro que forneceu a mensagem de controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="4e7df-110">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="4e7df-111">*perguntas*</span><span class="sxs-lookup"><span data-stu-id="4e7df-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="4e7df-112">Especifica uma estrutura de [**qualidade**](/windows/win32/api/strmif/ns-strmif-quality) que contém a mensagem de controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="4e7df-112">Specifies a [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e7df-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4e7df-113">Return value</span></span>

<span data-ttu-id="4e7df-114">A classe base retorna E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="4e7df-114">The base class returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e7df-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e7df-115">Remarks</span></span>

<span data-ttu-id="4e7df-116">Os Pins de saída devem substituir esse método para aceitar mensagens de controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="4e7df-116">Output pins should override this method to accept quality-control messages.</span></span>

<span data-ttu-id="4e7df-117">Se um Gerenciador de qualidade externo foi instalado (consulte [**CBasePin:: SetSink**](cbasepin-setsink.md)), passe a mensagem para esse Gerenciador de qualidade.</span><span class="sxs-lookup"><span data-stu-id="4e7df-117">If an external quality manager was installed (see [**CBasePin::SetSink**](cbasepin-setsink.md)), pass the message to that quality manager.</span></span> <span data-ttu-id="4e7df-118">Caso contrário, o filtro deve tratar a própria mensagem ou passar a mensagem upstream.</span><span class="sxs-lookup"><span data-stu-id="4e7df-118">Otherwise, the filter should handle the message itself, or pass the message upstream.</span></span> <span data-ttu-id="4e7df-119">Para obter mais informações, consulte [Gerenciamento de controle de qualidade](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="4e7df-119">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e7df-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e7df-120">Requirements</span></span>



| <span data-ttu-id="4e7df-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e7df-121">Requirement</span></span> | <span data-ttu-id="4e7df-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4e7df-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e7df-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e7df-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4e7df-124"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e7df-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4e7df-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e7df-125">Library</span></span><br/> | <dl> <span data-ttu-id="4e7df-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4e7df-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e7df-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4e7df-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e7df-128">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="4e7df-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




