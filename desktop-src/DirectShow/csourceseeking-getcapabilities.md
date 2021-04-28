---
description: 'Método CSourceSeeking. GetCapabilities – o método GetCapabilities recupera todos os recursos de busca do fluxo. Esse método implementa o método IMediaSeeking:: GetCapabilities.'
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
ms.openlocfilehash: f1f354381c4c99cf880c75cbbc4b13355e386030
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098774"
---
# <a name="csourceseekinggetcapabilities-method"></a><span data-ttu-id="dc0c1-104">Método CSourceSeeking. GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="dc0c1-104">CSourceSeeking.GetCapabilities method</span></span>

<span data-ttu-id="dc0c1-105">O `GetCapabilities` método recupera todos os recursos de busca do fluxo.</span><span class="sxs-lookup"><span data-stu-id="dc0c1-105">The `GetCapabilities` method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="dc0c1-106">Esse método implementa o método [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="dc0c1-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc0c1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc0c1-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="dc0c1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc0c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc0c1-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="dc0c1-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="dc0c1-110">O ponteiro para uma variável que recebe uma combinação de bits bit a procurar sinalizadores de [**\_ \_ \_ recursos de busca**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="dc0c1-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc0c1-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="dc0c1-111">Return value</span></span>

<span data-ttu-id="dc0c1-112">Retorna um dos valores **HRESULT** listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="dc0c1-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="dc0c1-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="dc0c1-113">Return code</span></span>                                                                               | <span data-ttu-id="dc0c1-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc0c1-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="dc0c1-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dc0c1-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="dc0c1-116">Êxito</span><span class="sxs-lookup"><span data-stu-id="dc0c1-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="dc0c1-117"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="dc0c1-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="dc0c1-118">Valor de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="dc0c1-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dc0c1-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc0c1-119">Remarks</span></span>

<span data-ttu-id="dc0c1-120">Os recursos de busca são especificados pela variável de membro [**CSourceSeeking:: m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="dc0c1-120">The seeking capabilities are specified by the [**CSourceSeeking::m\_dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc0c1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc0c1-121">Requirements</span></span>



| <span data-ttu-id="dc0c1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc0c1-122">Requirement</span></span> | <span data-ttu-id="dc0c1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="dc0c1-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc0c1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dc0c1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="dc0c1-125"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc0c1-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dc0c1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc0c1-126">Library</span></span><br/> | <dl> <span data-ttu-id="dc0c1-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="dc0c1-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc0c1-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="dc0c1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc0c1-129">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="dc0c1-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




