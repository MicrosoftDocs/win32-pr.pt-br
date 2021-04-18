---
description: O \_ método Get DevSyncOffset recupera o desvio padrão do tempo em milissegundos entre quando cada quadro esteve devido e quando ele foi realmente renderizado, para todos os quadros desde o início do streaming.
ms.assetid: 86f60064-f913-4377-bad0-148a213171fc
title: Método de CBaseVideoRenderer.get_DevSyncOffset (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_DevSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9926e809901f7290738e2e2cf3d094e54e068580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751697"
---
# <a name="cbasevideorendererget_devsyncoffset-method"></a><span data-ttu-id="31dd8-103">CBaseVideoRenderer. obter \_ método DevSyncOffset</span><span class="sxs-lookup"><span data-stu-id="31dd8-103">CBaseVideoRenderer.get\_DevSyncOffset method</span></span>

<span data-ttu-id="31dd8-104">O `get_DevSyncOffset` método recupera o desvio padrão do tempo em milissegundos entre quando cada quadro esteve devido e quando ele foi realmente renderizado, para todos os quadros desde o início do streaming.</span><span class="sxs-lookup"><span data-stu-id="31dd8-104">The `get_DevSyncOffset` method retrieves the standard deviation of the time in milliseconds between when each frame was due and when it was actually rendered, for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="31dd8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31dd8-105">Syntax</span></span>


```C++
HRESULT get_DevSyncOffset(
   int *piDev
);
```



## <a name="parameters"></a><span data-ttu-id="31dd8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31dd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31dd8-107">*piDev*</span><span class="sxs-lookup"><span data-stu-id="31dd8-107">*piDev*</span></span> 
</dt> <dd>

<span data-ttu-id="31dd8-108">Ponteiro para o desvio padrão do tempo conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="31dd8-108">Pointer to the standard deviation of the time as previously described.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31dd8-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31dd8-109">Return value</span></span>

<span data-ttu-id="31dd8-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="31dd8-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="31dd8-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="31dd8-111">Remarks</span></span>

<span data-ttu-id="31dd8-112">Essa função de membro implementa o método [**IQualProp:: get \_ DevSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) .</span><span class="sxs-lookup"><span data-stu-id="31dd8-112">This member function implements the [**IQualProp::get\_DevSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="31dd8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31dd8-113">Requirements</span></span>



| <span data-ttu-id="31dd8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="31dd8-114">Requirement</span></span> | <span data-ttu-id="31dd8-115">Valor</span><span class="sxs-lookup"><span data-stu-id="31dd8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31dd8-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31dd8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="31dd8-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31dd8-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="31dd8-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31dd8-118">Library</span></span><br/> | <dl> <span data-ttu-id="31dd8-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="31dd8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31dd8-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="31dd8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31dd8-121">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="31dd8-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




