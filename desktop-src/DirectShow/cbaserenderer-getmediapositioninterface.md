---
description: O método GetMediaPositionInterface recupera os ponteiros de interface IMediaPosition e IMediaSeeking do filtro.
ms.assetid: aeca4484-cecc-4d07-aa77-56221ff75699
title: Método CBaseRenderer. GetMediaPositionInterface (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetMediaPositionInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d41d777b88f0e18ae1510c32b7e89024ea7bdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811749"
---
# <a name="cbaserenderergetmediapositioninterface-method"></a><span data-ttu-id="ccd5c-103">Método CBaseRenderer. GetMediaPositionInterface</span><span class="sxs-lookup"><span data-stu-id="ccd5c-103">CBaseRenderer.GetMediaPositionInterface method</span></span>

<span data-ttu-id="ccd5c-104">O `GetMediaPositionInterface` método recupera os ponteiros de interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) do filtro.</span><span class="sxs-lookup"><span data-stu-id="ccd5c-104">The `GetMediaPositionInterface` method retrieves the filter's [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface pointers.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccd5c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccd5c-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaPositionInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="ccd5c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccd5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccd5c-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="ccd5c-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="ccd5c-108">Identificador de referência da interface.</span><span class="sxs-lookup"><span data-stu-id="ccd5c-108">Reference identifier of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="ccd5c-109">*ppv*</span><span class="sxs-lookup"><span data-stu-id="ccd5c-109">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="ccd5c-110">Endereço de uma variável que recebe o ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="ccd5c-110">Address of a variable that receives the interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccd5c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ccd5c-111">Return value</span></span>

<span data-ttu-id="ccd5c-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ccd5c-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ccd5c-113">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ccd5c-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="ccd5c-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ccd5c-114">Return code</span></span>                                                                                   | <span data-ttu-id="ccd5c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="ccd5c-115">Description</span></span>                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="ccd5c-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd5c-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ccd5c-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="ccd5c-117">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="ccd5c-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd5c-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ccd5c-119">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="ccd5c-119">Insufficient memory.</span></span><br/>     |
| <dl> <span data-ttu-id="ccd5c-120"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="ccd5c-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="ccd5c-121">Interface sem suporte.</span><span class="sxs-lookup"><span data-stu-id="ccd5c-121">Interface not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ccd5c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccd5c-122">Remarks</span></span>

<span data-ttu-id="ccd5c-123">O filtro Delega todos os comandos de busca a um objeto [**CRendererPosPassThru**](crendererpospassthru.md) , que passa por upstream.</span><span class="sxs-lookup"><span data-stu-id="ccd5c-123">The filter delegates all seeking commands to a [**CRendererPosPassThru**](crendererpospassthru.md) object, which passes them upstream.</span></span> <span data-ttu-id="ccd5c-124">Esse método criará o objeto **CRendererPosPassThru** , se ele ainda não existir, e o consultará para a interface solicitada.</span><span class="sxs-lookup"><span data-stu-id="ccd5c-124">This method creates the **CRendererPosPassThru** object, if it does not yet exist, and queries it for the requested interface.</span></span>

<span data-ttu-id="ccd5c-125">A variável de membro [**CBaseRenderer:: m \_ pPosition**](cbaserenderer-m-pposition.md) armazena um ponteiro para o objeto **CRendererPosPassThru** .</span><span class="sxs-lookup"><span data-stu-id="ccd5c-125">The [**CBaseRenderer::m\_pPosition**](cbaserenderer-m-pposition.md) member variable stores a pointer to the **CRendererPosPassThru** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccd5c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccd5c-126">Requirements</span></span>



| <span data-ttu-id="ccd5c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccd5c-127">Requirement</span></span> | <span data-ttu-id="ccd5c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ccd5c-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd5c-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ccd5c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ccd5c-130"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ccd5c-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ccd5c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ccd5c-131">Library</span></span><br/> | <dl> <span data-ttu-id="ccd5c-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ccd5c-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccd5c-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccd5c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccd5c-134">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="ccd5c-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




