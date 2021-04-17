---
description: O \_ método obter tremulação recupera o desvio padrão do tempo em milissegundos entre cada quadro e o próximo para todos os quadros desde o início do streaming.
ms.assetid: 629e725e-7dee-4824-8f79-cd3335f4901b
title: Método de CBaseVideoRenderer.get_Jitter (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_Jitter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef39cdb1b7a77dab22db9728268bf7b23b9fcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787000"
---
# <a name="cbasevideorendererget_jitter-method"></a><span data-ttu-id="d5ccd-103">Método de variação CBaseVideoRenderer. get \_</span><span class="sxs-lookup"><span data-stu-id="d5ccd-103">CBaseVideoRenderer.get\_Jitter method</span></span>

<span data-ttu-id="d5ccd-104">O `get_Jitter` método recupera o desvio padrão de tempo em milissegundos entre cada quadro e o próximo para todos os quadros desde o streaming iniciado.</span><span class="sxs-lookup"><span data-stu-id="d5ccd-104">The `get_Jitter` method retrieves the standard deviation of time in milliseconds between each frame and the next for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5ccd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5ccd-105">Syntax</span></span>


```C++
HRESULT get_Jitter(
   int *piJitter
);
```



## <a name="parameters"></a><span data-ttu-id="d5ccd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5ccd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5ccd-107">*piJitter*</span><span class="sxs-lookup"><span data-stu-id="d5ccd-107">*piJitter*</span></span> 
</dt> <dd>

<span data-ttu-id="d5ccd-108">Ponteiro para o desvio padrão do tempo entre quadros, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="d5ccd-108">Pointer to the standard deviation of the interframe time, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5ccd-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5ccd-109">Return value</span></span>

<span data-ttu-id="d5ccd-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d5ccd-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5ccd-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5ccd-111">Remarks</span></span>

<span data-ttu-id="d5ccd-112">Essa função de membro implementa o método de [**\_ variação IQualProp:: Get**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) .</span><span class="sxs-lookup"><span data-stu-id="d5ccd-112">This member function implements the [**IQualProp::get\_Jitter**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5ccd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5ccd-113">Requirements</span></span>



| <span data-ttu-id="d5ccd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5ccd-114">Requirement</span></span> | <span data-ttu-id="d5ccd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d5ccd-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ccd-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5ccd-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d5ccd-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5ccd-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d5ccd-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5ccd-118">Library</span></span><br/> | <dl> <span data-ttu-id="d5ccd-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d5ccd-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5ccd-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5ccd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5ccd-121">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="d5ccd-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




