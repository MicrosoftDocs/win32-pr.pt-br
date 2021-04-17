---
description: 'O método AlterQuality notifica o filtro de que uma alteração de qualidade é solicitada. Esse método substitui o método CTransformFilter:: AlterQuality.'
ms.assetid: 9a1d1379-8557-4b33-ab49-b5c6a684f685
title: Método CVideoTransformFilter. AlterQuality (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1de0985b8cb3a8db6f45c247e717042cf344655f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752681"
---
# <a name="cvideotransformfilteralterquality-method"></a><span data-ttu-id="a9a46-104">Método CVideoTransformFilter. AlterQuality</span><span class="sxs-lookup"><span data-stu-id="a9a46-104">CVideoTransformFilter.AlterQuality method</span></span>

<span data-ttu-id="a9a46-105">O `AlterQuality` método notifica o filtro de que uma alteração de qualidade é solicitada.</span><span class="sxs-lookup"><span data-stu-id="a9a46-105">The `AlterQuality` method notifies the filter that a quality change is requested.</span></span> <span data-ttu-id="a9a46-106">Esse método substitui o método [**CTransformFilter:: AlterQuality**](ctransformfilter-alterquality.md) .</span><span class="sxs-lookup"><span data-stu-id="a9a46-106">This method overrides the [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9a46-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9a46-107">Syntax</span></span>


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="a9a46-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9a46-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9a46-109">*perguntas*</span><span class="sxs-lookup"><span data-stu-id="a9a46-109">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="a9a46-110">Estrutura de [**qualidade**](/windows/win32/api/strmif/ns-strmif-quality) que contém a mensagem de controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="a9a46-110">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9a46-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a9a46-111">Return value</span></span>

<span data-ttu-id="a9a46-112">Retorna E \_ falha.</span><span class="sxs-lookup"><span data-stu-id="a9a46-112">Returns E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9a46-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9a46-113">Remarks</span></span>

<span data-ttu-id="a9a46-114">Esse método é chamado quando o PIN de saída recebe uma mensagem de qualidade (por meio do método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) ).</span><span class="sxs-lookup"><span data-stu-id="a9a46-114">This method is called when the output pin receives a quality message (through the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method).</span></span>

<span data-ttu-id="a9a46-115">O valor de atraso de *q* é armazenado na variável de membro **m \_ itrLate** .</span><span class="sxs-lookup"><span data-stu-id="a9a46-115">The lateness value from *q* is stored in the **m\_itrLate** member variable.</span></span> <span data-ttu-id="a9a46-116">O valor de retorno de E \_ falha indica que o renderizador deve ser atualizado descartando os quadros, embora a classe **CVideoTransformFilter** também solte quadros sob as condições corretas.</span><span class="sxs-lookup"><span data-stu-id="a9a46-116">The return value of E\_FAIL indicates that the renderer should catch up by dropping frames, although the **CVideoTransformFilter** class will also drop frames under the right conditions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9a46-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9a46-117">Requirements</span></span>



| <span data-ttu-id="a9a46-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9a46-118">Requirement</span></span> | <span data-ttu-id="a9a46-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a9a46-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a46-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9a46-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a9a46-121"><dt>Vtrans. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9a46-121"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a9a46-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a9a46-122">Library</span></span><br/> | <dl> <span data-ttu-id="a9a46-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a9a46-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9a46-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9a46-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a46-125">**Classe CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="a9a46-125">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> <dt>

[<span data-ttu-id="a9a46-126">**CVideoTransformFilter::ShouldSkipFrame**</span><span class="sxs-lookup"><span data-stu-id="a9a46-126">**CVideoTransformFilter::ShouldSkipFrame**</span></span>](cvideotransformfilter-shouldskipframe.md)
</dt> </dl>

 

 




