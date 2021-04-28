---
description: 'Método CTransformOutputPin. Notify – o método Notify notifica o PIN de que uma alteração de qualidade é solicitada. Esse método implementa o método IQualityControl:: Notify.'
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: Método CTransformOutputPin. Notify (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a55e493c737b5a5864ec0a8dd38eee3abbfa586
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084804"
---
# <a name="ctransformoutputpinnotify-method"></a><span data-ttu-id="5fa4a-104">Método CTransformOutputPin. Notify</span><span class="sxs-lookup"><span data-stu-id="5fa4a-104">CTransformOutputPin.Notify method</span></span>

<span data-ttu-id="5fa4a-105">O `Notify` método notifica o PIN de que uma alteração de qualidade é solicitada.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="5fa4a-106">Esse método implementa o método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .</span><span class="sxs-lookup"><span data-stu-id="5fa4a-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fa4a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fa4a-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="5fa4a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fa4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fa4a-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="5fa4a-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="5fa4a-110">Ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro que forneceu a mensagem de controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-110">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality control message.</span></span>

</dd> <dt>

<span data-ttu-id="5fa4a-111">*perguntas*</span><span class="sxs-lookup"><span data-stu-id="5fa4a-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="5fa4a-112">Estrutura de [**qualidade**](/windows/win32/api/strmif/ns-strmif-quality) que contém a mensagem de controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fa4a-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5fa4a-113">Return value</span></span>

<span data-ttu-id="5fa4a-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5fa4a-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5fa4a-115">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="5fa4a-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5fa4a-116">Return code</span></span>                                                                                       | <span data-ttu-id="5fa4a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="5fa4a-117">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="5fa4a-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5fa4a-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="5fa4a-119">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-119">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="5fa4a-120"><dt>**VFW \_ E \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="5fa4a-120"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="5fa4a-121">Não foi possível encontrar um objeto para aceitar a mensagem.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-121">Could not find an object to accept the message.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5fa4a-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="5fa4a-122">Remarks</span></span>

<span data-ttu-id="5fa4a-123">Esse método chama o método [**CTransformFilter:: AlterQuality**](ctransformfilter-alterquality.md) do filtro.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-123">This method calls the filter's [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md) method.</span></span> <span data-ttu-id="5fa4a-124">Se o filtro não tratar a mensagem de qualidade, esse método chamará o método [**CBaseInputPin::P assnotify**](cbaseinputpin-passnotify.md) no PIN de entrada do filtro.</span><span class="sxs-lookup"><span data-stu-id="5fa4a-124">If the filter does not handle the quality message, this method calls the [**CBaseInputPin::PassNotify**](cbaseinputpin-passnotify.md) method on the filter's input pin.</span></span> <span data-ttu-id="5fa4a-125">O método **PassNotify** passa a mensagem de qualidade upstream (ou para um Gerenciador de qualidade personalizado, se um tiver sido instalado).</span><span class="sxs-lookup"><span data-stu-id="5fa4a-125">The **PassNotify** method passes the quality message upstream (or to a custom quality manager, if one was installed).</span></span>

## <a name="requirements"></a><span data-ttu-id="5fa4a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fa4a-126">Requirements</span></span>



| <span data-ttu-id="5fa4a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fa4a-127">Requirement</span></span> | <span data-ttu-id="5fa4a-128">Valor</span><span class="sxs-lookup"><span data-stu-id="5fa4a-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa4a-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5fa4a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5fa4a-130"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5fa4a-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5fa4a-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5fa4a-131">Library</span></span><br/> | <dl> <span data-ttu-id="5fa4a-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5fa4a-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




