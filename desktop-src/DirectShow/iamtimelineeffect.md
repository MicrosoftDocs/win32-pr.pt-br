---
description: A interface IAMTimelineEffect fornece métodos para manipular efeitos de áudio e vídeo em DES (serviços de edição do DirectShow).
ms.assetid: 3cc8a5f8-3f57-4e2b-82dd-827e04c771f7
title: Interface IAMTimelineEffect (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8b9936616b9c4487849053d36c6a63290bd16b5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789948"
---
# <a name="iamtimelineeffect-interface"></a><span data-ttu-id="b1a0e-103">Interface IAMTimelineEffect</span><span class="sxs-lookup"><span data-stu-id="b1a0e-103">IAMTimelineEffect interface</span></span>

> [!Note]  
> <span data-ttu-id="b1a0e-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-104">\[Deprecated.</span></span> <span data-ttu-id="b1a0e-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b1a0e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b1a0e-106">A `IAMTimelineEffect` interface fornece métodos para manipular efeitos de áudio e vídeo em des ( [serviços de edição do DirectShow](directshow-editing-services.md) ).</span><span class="sxs-lookup"><span data-stu-id="b1a0e-106">The `IAMTimelineEffect` interface provides methods for manipulating audio and video effects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="b1a0e-107">Um efeito pode ser adicionado a qualquer objeto de linha do tempo que expõe a interface [**IAMTimelineEffectable**](iamtimelineeffectable.md) .</span><span class="sxs-lookup"><span data-stu-id="b1a0e-107">An effect can be added to any timeline object that exposes the [**IAMTimelineEffectable**](iamtimelineeffectable.md) interface.</span></span> <span data-ttu-id="b1a0e-108">Para definir propriedades em um efeito, use a interface [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="b1a0e-108">To set properties on an effect, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="b1a0e-109">O objeto de efeito DES é, na verdade, um wrapper para um dos dois outros objetos:</span><span class="sxs-lookup"><span data-stu-id="b1a0e-109">The DES effect object is actually a wrapper for one of two other objects:</span></span>

-   <span data-ttu-id="b1a0e-110">Para efeitos de áudio, qualquer filtro de efeito de áudio do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-110">For audio effects, any DirectShow audio effect filter.</span></span>
-   <span data-ttu-id="b1a0e-111">Para efeitos de vídeo, e um objeto de transformação DirectX de entrada.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-111">For video effects, and 1-input DirectX Transform object.</span></span>

<span data-ttu-id="b1a0e-112">A Microsoft não dá mais suporte ao desenvolvimento de objetos de transformação DirectX de terceiros.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-112">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span>

<span data-ttu-id="b1a0e-113">Para especificar o filtro ou o objeto de transformação DirectX para um efeito, chame o método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .</span><span class="sxs-lookup"><span data-stu-id="b1a0e-113">To specify the filter or DirectX Transform object for an effect, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="b1a0e-114">Para criar um objeto de efeito, chame [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) com o valor linha de tempo \_ principal \_ efeito de tipo \_ .</span><span class="sxs-lookup"><span data-stu-id="b1a0e-114">To create an effect object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_EFFECT.</span></span> <span data-ttu-id="b1a0e-115">Você pode consultar o ponteiro [**IAMTimelineObj**](iamtimelineobj.md) retornado para a `IAMTimelineEffect` interface.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-115">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineEffect` interface.</span></span>

## <a name="members"></a><span data-ttu-id="b1a0e-116">Membros</span><span class="sxs-lookup"><span data-stu-id="b1a0e-116">Members</span></span>

<span data-ttu-id="b1a0e-117">A interface **IAMTimelineEffect** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b1a0e-117">The **IAMTimelineEffect** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b1a0e-118">**IAMTimelineEffect** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b1a0e-118">**IAMTimelineEffect** also has these types of members:</span></span>

-   [<span data-ttu-id="b1a0e-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="b1a0e-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b1a0e-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="b1a0e-120">Methods</span></span>

<span data-ttu-id="b1a0e-121">A interface **IAMTimelineEffect** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-121">The **IAMTimelineEffect** interface has these methods.</span></span>



| <span data-ttu-id="b1a0e-122">Método</span><span class="sxs-lookup"><span data-stu-id="b1a0e-122">Method</span></span>                                                           | <span data-ttu-id="b1a0e-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1a0e-123">Description</span></span>                                       |
|:-----------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="b1a0e-124">**EffectGetPriority**</span><span class="sxs-lookup"><span data-stu-id="b1a0e-124">**EffectGetPriority**</span></span>](iamtimelineeffect-effectgetpriority.md) | <span data-ttu-id="b1a0e-125">Recupera o nível de prioridade do efeito.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-125">Retrieves the effect's priority level.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b1a0e-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1a0e-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b1a0e-127">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b1a0e-128">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1a0e-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b1a0e-129">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b1a0e-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b1a0e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1a0e-130">Requirements</span></span>



| <span data-ttu-id="b1a0e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1a0e-131">Requirement</span></span> | <span data-ttu-id="b1a0e-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b1a0e-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a0e-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1a0e-133">Header</span></span><br/>  | <dl> <span data-ttu-id="b1a0e-134"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1a0e-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b1a0e-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1a0e-135">Library</span></span><br/> | <dl> <span data-ttu-id="b1a0e-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1a0e-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1a0e-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1a0e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1a0e-138">Trabalhando com efeitos e transições</span><span class="sxs-lookup"><span data-stu-id="b1a0e-138">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
