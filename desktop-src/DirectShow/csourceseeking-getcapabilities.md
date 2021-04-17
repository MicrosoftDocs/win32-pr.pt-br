---
description: 'O método GetCapabilities recupera todos os recursos de busca do fluxo. Esse método implementa o método IMediaSeeking:: GetCapabilities.'
ms.assetid: a2ff7ea2-09bd-49a7-8e1b-d6360939036e
title: Método CSourceSeeking. GetCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eda23944fd039576bb5de74fbb7c32e375415670
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752283"
---
# <a name="csourceseekinggetcapabilities-method"></a><span data-ttu-id="706bb-104">Método CSourceSeeking. GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="706bb-104">CSourceSeeking.GetCapabilities method</span></span>

<span data-ttu-id="706bb-105">O `GetCapabilities` método recupera todos os recursos de busca do fluxo.</span><span class="sxs-lookup"><span data-stu-id="706bb-105">The `GetCapabilities` method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="706bb-106">Esse método implementa o método [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="706bb-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="706bb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="706bb-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="706bb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="706bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="706bb-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="706bb-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="706bb-110">O ponteiro para uma variável que recebe uma combinação de bits bit a procurar sinalizadores de [**\_ \_ \_ recursos de busca**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="706bb-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="706bb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="706bb-111">Return value</span></span>

<span data-ttu-id="706bb-112">Retorna um dos valores **HRESULT** listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="706bb-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="706bb-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="706bb-113">Return code</span></span>                                                                               | <span data-ttu-id="706bb-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="706bb-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="706bb-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="706bb-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="706bb-116">Sucesso</span><span class="sxs-lookup"><span data-stu-id="706bb-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="706bb-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="706bb-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="706bb-118">Valor de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="706bb-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="706bb-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="706bb-119">Remarks</span></span>

<span data-ttu-id="706bb-120">Os recursos de busca são especificados pela variável de membro [**CSourceSeeking:: m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="706bb-120">The seeking capabilities are specified by the [**CSourceSeeking::m\_dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="706bb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="706bb-121">Requirements</span></span>



| <span data-ttu-id="706bb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="706bb-122">Requirement</span></span> | <span data-ttu-id="706bb-123">Valor</span><span class="sxs-lookup"><span data-stu-id="706bb-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="706bb-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="706bb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="706bb-125"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="706bb-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="706bb-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="706bb-126">Library</span></span><br/> | <dl> <span data-ttu-id="706bb-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="706bb-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="706bb-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="706bb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="706bb-129">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="706bb-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




