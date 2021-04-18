---
description: A interface IAMTimelineTrans fornece métodos para manipular transições em serviços de edição do DirectShow (DES).
ms.assetid: e29ff0cc-0e48-4a72-8a1b-051ed62c8130
title: Interface IAMTimelineTrans (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cd3c39d0a5434befdd5607b340fef936644bf48e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779234"
---
# <a name="iamtimelinetrans-interface"></a><span data-ttu-id="49bd6-103">Interface IAMTimelineTrans</span><span class="sxs-lookup"><span data-stu-id="49bd6-103">IAMTimelineTrans interface</span></span>

> [!Note]  
> <span data-ttu-id="49bd6-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="49bd6-104">\[Deprecated.</span></span> <span data-ttu-id="49bd6-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="49bd6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="49bd6-106">A `IAMTimelineTrans` interface fornece métodos para manipular transições em [serviços de edição do DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="49bd6-106">The `IAMTimelineTrans` interface provides methods for manipulating transitions in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="49bd6-107">Uma transição é uma progressão entre uma camada de vídeo e a composição renderizada de todas as camadas de vídeo com uma prioridade mais baixa.</span><span class="sxs-lookup"><span data-stu-id="49bd6-107">A transition is a progression between one video layer and the rendered composite of all video layers with a lower priority.</span></span> <span data-ttu-id="49bd6-108">Uma transição pode ser adicionada a qualquer objeto de linha do tempo que expõe a interface [**IAMTimelineTransable**](iamtimelinetransable.md) .</span><span class="sxs-lookup"><span data-stu-id="49bd6-108">A transition can be added to any timeline object that exposes the [**IAMTimelineTransable**](iamtimelinetransable.md) interface.</span></span> <span data-ttu-id="49bd6-109">Para definir propriedades em uma transição, use a interface [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="49bd6-109">To set properties on a transition, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="49bd6-110">O objeto de transição DES é, na verdade, um wrapper para um objeto de transformação do DirectX.</span><span class="sxs-lookup"><span data-stu-id="49bd6-110">The DES transition object is actually a wrapper for a DirectX Transform object.</span></span> <span data-ttu-id="49bd6-111">Qualquer objeto de transformação DirectX de entrada 2 pode ser usado para implementar o efeito visual para a transição.</span><span class="sxs-lookup"><span data-stu-id="49bd6-111">Any 2-input DirectX Transform object can be used to implement the visual effect for the transition.</span></span> <span data-ttu-id="49bd6-112">A Microsoft não dá mais suporte ao desenvolvimento de objetos de transformação DirectX de terceiros.</span><span class="sxs-lookup"><span data-stu-id="49bd6-112">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span> <span data-ttu-id="49bd6-113">Para especificar o objeto de transformação DirectX para uma transição, chame o método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .</span><span class="sxs-lookup"><span data-stu-id="49bd6-113">To specify the DirectX Transform object for a transition, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="49bd6-114">Para criar um objeto de transição, chame [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) com o valor linha de tempo de \_ \_ tipo principal \_ TRANSITION.</span><span class="sxs-lookup"><span data-stu-id="49bd6-114">To create a transition object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_TRANSITION.</span></span> <span data-ttu-id="49bd6-115">Você pode consultar o ponteiro [**IAMTimelineObj**](iamtimelineobj.md) retornado para a `IAMTimelineTrans` interface.</span><span class="sxs-lookup"><span data-stu-id="49bd6-115">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineTrans` interface.</span></span>

## <a name="members"></a><span data-ttu-id="49bd6-116">Membros</span><span class="sxs-lookup"><span data-stu-id="49bd6-116">Members</span></span>

<span data-ttu-id="49bd6-117">A interface **IAMTimelineTrans** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="49bd6-117">The **IAMTimelineTrans** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="49bd6-118">**IAMTimelineTrans** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="49bd6-118">**IAMTimelineTrans** also has these types of members:</span></span>

-   [<span data-ttu-id="49bd6-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="49bd6-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="49bd6-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="49bd6-120">Methods</span></span>

<span data-ttu-id="49bd6-121">A interface **IAMTimelineTrans** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="49bd6-121">The **IAMTimelineTrans** interface has these methods.</span></span>



| <span data-ttu-id="49bd6-122">Método</span><span class="sxs-lookup"><span data-stu-id="49bd6-122">Method</span></span>                                                  | <span data-ttu-id="49bd6-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="49bd6-123">Description</span></span>                                                                            |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="49bd6-124">**GetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="49bd6-124">**GetCutPoint**</span></span>](iamtimelinetrans-getcutpoint.md)     | <span data-ttu-id="49bd6-125">Recupera o ponto de recorte.</span><span class="sxs-lookup"><span data-stu-id="49bd6-125">Retrieves the cut point.</span></span><br/>                                                    |
| [<span data-ttu-id="49bd6-126">**GetCutPoint2**</span><span class="sxs-lookup"><span data-stu-id="49bd6-126">**GetCutPoint2**</span></span>](iamtimelinetrans-getcutpoint2.md)   | <span data-ttu-id="49bd6-127">Recupera o ponto de recorte, como um valor [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="49bd6-127">Retrieves the cut point, as a [**REFTIME**](reftime.md) value.</span></span><br/>             |
| [<span data-ttu-id="49bd6-128">**GetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="49bd6-128">**GetCutsOnly**</span></span>](iamtimelinetrans-getcutsonly.md)     | <span data-ttu-id="49bd6-129">Determina se a transição é renderizada como um recorte.</span><span class="sxs-lookup"><span data-stu-id="49bd6-129">Determines whether the transition is rendered as a cut.</span></span><br/>                     |
| [<span data-ttu-id="49bd6-130">**GetSwapInputs**</span><span class="sxs-lookup"><span data-stu-id="49bd6-130">**GetSwapInputs**</span></span>](iamtimelinetrans-getswapinputs.md) | <span data-ttu-id="49bd6-131">Recupera um valor que indica se as entradas de transição são trocadas.</span><span class="sxs-lookup"><span data-stu-id="49bd6-131">Retrieves a value that indicates whether the transition inputs are swapped.</span></span><br/> |
| [<span data-ttu-id="49bd6-132">**SetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="49bd6-132">**SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)     | <span data-ttu-id="49bd6-133">Define o ponto de recorte.</span><span class="sxs-lookup"><span data-stu-id="49bd6-133">Sets the cut point.</span></span><br/>                                                         |
| [<span data-ttu-id="49bd6-134">**SetCutPoint2**</span><span class="sxs-lookup"><span data-stu-id="49bd6-134">**SetCutPoint2**</span></span>](iamtimelinetrans-setcutpoint2.md)   | <span data-ttu-id="49bd6-135">Define o ponto de recorte, como um valor [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="49bd6-135">Sets the cut point, as a [**REFTIME**](reftime.md) value.</span></span><br/>                  |
| [<span data-ttu-id="49bd6-136">**SetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="49bd6-136">**SetCutsOnly**</span></span>](iamtimelinetrans-setcutsonly.md)     | <span data-ttu-id="49bd6-137">Especifica se a transição é renderizada como um recorte.</span><span class="sxs-lookup"><span data-stu-id="49bd6-137">Specifies whether the transition is rendered as a cut.</span></span><br/>                      |
| [<span data-ttu-id="49bd6-138">**SetSwapInputs**</span><span class="sxs-lookup"><span data-stu-id="49bd6-138">**SetSwapInputs**</span></span>](iamtimelinetrans-setswapinputs.md) | <span data-ttu-id="49bd6-139">Especifica se as entradas de transição são trocadas.</span><span class="sxs-lookup"><span data-stu-id="49bd6-139">Specifies whether the transition inputs are swapped.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="49bd6-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="49bd6-140">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="49bd6-141">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="49bd6-141">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="49bd6-142">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="49bd6-142">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="49bd6-143">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="49bd6-143">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="49bd6-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49bd6-144">Requirements</span></span>



| <span data-ttu-id="49bd6-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="49bd6-145">Requirement</span></span> | <span data-ttu-id="49bd6-146">Valor</span><span class="sxs-lookup"><span data-stu-id="49bd6-146">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49bd6-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="49bd6-147">Header</span></span><br/>  | <dl> <span data-ttu-id="49bd6-148"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="49bd6-148"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="49bd6-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="49bd6-149">Library</span></span><br/> | <dl> <span data-ttu-id="49bd6-150"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49bd6-150"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49bd6-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="49bd6-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49bd6-152">Trabalhando com efeitos e transições</span><span class="sxs-lookup"><span data-stu-id="49bd6-152">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
