---
description: O método RenderOutputPins cria a parte de visualização do grafo de filtro.
ms.assetid: 66bcb698-cd85-4c22-bfef-2e51973958f1
title: 'Método IRenderEngine:: RenderOutputPins (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.RenderOutputPins
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7356df1bb79aa3b1901ee6d3de22510a6df1a9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782229"
---
# <a name="irenderenginerenderoutputpins-method"></a><span data-ttu-id="5efdc-103">Método IRenderEngine:: RenderOutputPins</span><span class="sxs-lookup"><span data-stu-id="5efdc-103">IRenderEngine::RenderOutputPins method</span></span>

> [!Note]  
> <span data-ttu-id="5efdc-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="5efdc-104">\[Deprecated.</span></span> <span data-ttu-id="5efdc-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5efdc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5efdc-106">O `RenderOutputPins` método cria a parte de visualização do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="5efdc-106">The `RenderOutputPins` method creates the previewing portion of the filter graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="5efdc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5efdc-107">Syntax</span></span>


```C++
HRESULT RenderOutputPins();
```



## <a name="parameters"></a><span data-ttu-id="5efdc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5efdc-108">Parameters</span></span>

<span data-ttu-id="5efdc-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5efdc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5efdc-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5efdc-110">Return value</span></span>

<span data-ttu-id="5efdc-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5efdc-111">Returns an **HRESULT** values.</span></span> <span data-ttu-id="5efdc-112">O valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="5efdc-112">The following are possible values:</span></span>



| <span data-ttu-id="5efdc-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5efdc-113">Return code</span></span>                                                                                                  | <span data-ttu-id="5efdc-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5efdc-114">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5efdc-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5efdc-115"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="5efdc-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="5efdc-116">Success.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="5efdc-117"><dt>**\_áudio VFW \_ S \_ não \_ processado**</dt></span><span class="sxs-lookup"><span data-stu-id="5efdc-117"><dt>**VFW\_S\_AUDIO\_NOT\_RENDERED**</dt></span></span> </dl>  | <span data-ttu-id="5efdc-118">Não é possível reproduzir o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="5efdc-118">Cannot play back the audio stream.</span></span><br/>                              |
| <dl> <span data-ttu-id="5efdc-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5efdc-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="5efdc-120">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="5efdc-120">Invalid argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="5efdc-121"><dt>**o \_ mecanismo de renderização E \_ \_ está \_ desfeito**</dt></span><span class="sxs-lookup"><span data-stu-id="5efdc-121"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="5efdc-122">Falha na operação porque o projeto não foi renderizado com êxito.</span><span class="sxs-lookup"><span data-stu-id="5efdc-122">Operation failed because project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="5efdc-123"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="5efdc-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="5efdc-124">Erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="5efdc-124">Unexpected error.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="5efdc-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="5efdc-125">Remarks</span></span>

<span data-ttu-id="5efdc-126">Antes de chamar esse método, chame [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) para criar o front-end do grafo.</span><span class="sxs-lookup"><span data-stu-id="5efdc-126">Before calling this method, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span> <span data-ttu-id="5efdc-127">Para executar uma operação diferente de preview, não chame esse método.</span><span class="sxs-lookup"><span data-stu-id="5efdc-127">To perform an operation other than preview, do not call this method.</span></span> <span data-ttu-id="5efdc-128">Em vez disso, chame [**IRenderEngine:: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) para obter ponteiros para os Pins de saída.</span><span class="sxs-lookup"><span data-stu-id="5efdc-128">Instead, call [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) to obtain pointers to the output pins.</span></span>

<span data-ttu-id="5efdc-129">Se não houver placa de som no computador do usuário, esse método retornará VFW \_ s de \_ áudio \_ não \_ processado.</span><span class="sxs-lookup"><span data-stu-id="5efdc-129">If there is no sound card on the user's computer, this method returns VFW\_S\_AUDIO\_NOT\_RENDERED.</span></span> <span data-ttu-id="5efdc-130">Não haverá visualização de áudio nesse caso, mas a visualização de vídeo não será afetada.</span><span class="sxs-lookup"><span data-stu-id="5efdc-130">There will not be audio preview in this case, but video preview is unaffected.</span></span>

<span data-ttu-id="5efdc-131">Se o PIN for de um grupo de vídeos, esse método criará uma janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5efdc-131">If the pin is from a video group, this method creates a video window.</span></span> <span data-ttu-id="5efdc-132">O thread de chamada deve enviar mensagens, por exemplo, para mover a janela ou responder a cliques do mouse na área do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="5efdc-132">The calling thread must dispatch messages—for example, to move the window, or respond to mouse clicks in the window's client area.</span></span>

> [!Note]  
> <span data-ttu-id="5efdc-133">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="5efdc-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5efdc-134">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5efdc-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5efdc-135">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5efdc-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5efdc-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5efdc-136">Requirements</span></span>



| <span data-ttu-id="5efdc-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="5efdc-137">Requirement</span></span> | <span data-ttu-id="5efdc-138">Valor</span><span class="sxs-lookup"><span data-stu-id="5efdc-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5efdc-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5efdc-139">Header</span></span><br/>  | <dl> <span data-ttu-id="5efdc-140"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5efdc-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5efdc-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5efdc-141">Library</span></span><br/> | <dl> <span data-ttu-id="5efdc-142"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5efdc-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5efdc-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="5efdc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5efdc-144">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="5efdc-144">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="5efdc-145">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="5efdc-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




