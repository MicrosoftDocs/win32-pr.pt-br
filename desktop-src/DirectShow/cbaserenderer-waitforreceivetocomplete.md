---
description: 'O método WaitForReceiveToComplete aguarda o método CBaseRenderer:: Receive ser concluído.'
ms.assetid: 3c722680-e54b-4ba1-8e98-36647cd027bc
title: Método CBaseRenderer. WaitForReceiveToComplete (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForReceiveToComplete
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9033474c71d23fed106205839071bad200df6a23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757427"
---
# <a name="cbaserendererwaitforreceivetocomplete-method"></a><span data-ttu-id="70ef3-103">Método CBaseRenderer. WaitForReceiveToComplete</span><span class="sxs-lookup"><span data-stu-id="70ef3-103">CBaseRenderer.WaitForReceiveToComplete method</span></span>

<span data-ttu-id="70ef3-104">O `WaitForReceiveToComplete` método aguarda o método [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) ser concluído.</span><span class="sxs-lookup"><span data-stu-id="70ef3-104">The `WaitForReceiveToComplete` method waits for the [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method to complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="70ef3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70ef3-105">Syntax</span></span>


```C++
void WaitForReceiveToComplete();
```



## <a name="parameters"></a><span data-ttu-id="70ef3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70ef3-106">Parameters</span></span>

<span data-ttu-id="70ef3-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="70ef3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="70ef3-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70ef3-108">Return value</span></span>

<span data-ttu-id="70ef3-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="70ef3-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="70ef3-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="70ef3-110">Remarks</span></span>

<span data-ttu-id="70ef3-111">Os métodos [**CBaseRenderer:: Stop**](cbaserenderer-stop.md) e [**CBaseRenderer:: BeginFlush**](cbaserenderer-beginflush.md) chamam esse método para sincronizar a alteração de estado com o método **Receive** .</span><span class="sxs-lookup"><span data-stu-id="70ef3-111">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call this method to synchronize the state change with the **Receive** method.</span></span>

<span data-ttu-id="70ef3-112">Especificamente, esse método despacha mensagens enquanto aguarda que o sinalizador [**CBaseRenderer:: m \_ bInReceive**](cbaserenderer-m-binreceive.md) se torne **falso**.</span><span class="sxs-lookup"><span data-stu-id="70ef3-112">Specifically, this method dispatches messages while it waits for the [**CBaseRenderer::m\_bInReceive**](cbaserenderer-m-binreceive.md) flag to become **FALSE**.</span></span> <span data-ttu-id="70ef3-113">O sinalizador se torna **verdadeiro** no [**método CBaseRenderer::P reparereceive**](cbaserenderer-preparereceive.md) e alterna de volta para **false** depois que o método **Receive** chama o método [**CBaseRenderer::P reparerender**](cbaserenderer-preparerender.md) .</span><span class="sxs-lookup"><span data-stu-id="70ef3-113">The flag becomes **TRUE** in the [**CBaseRenderer::PrepareReceive**](cbaserenderer-preparereceive.md) method and switches back to **FALSE** after the **Receive** method calls the [**CBaseRenderer::PrepareRender**](cbaserenderer-preparerender.md) method.</span></span> <span data-ttu-id="70ef3-114">A classe derivada pode usar **PrepareRender** para definir a paleta.</span><span class="sxs-lookup"><span data-stu-id="70ef3-114">The derived class can use **PrepareRender** to set the palette.</span></span> <span data-ttu-id="70ef3-115">Aguardar a conclusão de **PrepareRender** garante que as mensagens de alteração de paleta sejam expedidas antes que a alteração de estado ocorra.</span><span class="sxs-lookup"><span data-stu-id="70ef3-115">Waiting for **PrepareRender** to complete ensures that palette-change messages are dispatched before the state change occurs.</span></span> <span data-ttu-id="70ef3-116">Isso evita um deadlock potencial.</span><span class="sxs-lookup"><span data-stu-id="70ef3-116">This avoids a potential deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="70ef3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70ef3-117">Requirements</span></span>



| <span data-ttu-id="70ef3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="70ef3-118">Requirement</span></span> | <span data-ttu-id="70ef3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="70ef3-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70ef3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70ef3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="70ef3-121"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70ef3-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="70ef3-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="70ef3-122">Library</span></span><br/> | <dl> <span data-ttu-id="70ef3-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="70ef3-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70ef3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="70ef3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70ef3-125">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="70ef3-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




