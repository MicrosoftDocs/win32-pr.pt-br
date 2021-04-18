---
description: O método ConnectFrontEnd cria o front-end do grafo de filtro a partir da linha do tempo atual.
ms.assetid: ac484fd6-b88d-4c3a-bc4d-f118083d706d
title: 'Método IRenderEngine:: ConnectFrontEnd (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ConnectFrontEnd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 58ebd8e162f376b6ef942397e601139c46d8e4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778433"
---
# <a name="irenderengineconnectfrontend-method"></a><span data-ttu-id="223a0-103">Método IRenderEngine:: ConnectFrontEnd</span><span class="sxs-lookup"><span data-stu-id="223a0-103">IRenderEngine::ConnectFrontEnd method</span></span>

> [!Note]  
> <span data-ttu-id="223a0-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="223a0-104">\[Deprecated.</span></span> <span data-ttu-id="223a0-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="223a0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="223a0-106">O `ConnectFrontEnd` método cria o front-end do grafo de filtro a partir da linha do tempo atual.</span><span class="sxs-lookup"><span data-stu-id="223a0-106">The `ConnectFrontEnd` method builds the front end of the filter graph from the current timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="223a0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="223a0-107">Syntax</span></span>


```C++
HRESULT ConnectFrontEnd();
```



## <a name="parameters"></a><span data-ttu-id="223a0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="223a0-108">Parameters</span></span>

<span data-ttu-id="223a0-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="223a0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="223a0-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="223a0-110">Return value</span></span>

<span data-ttu-id="223a0-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="223a0-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="223a0-112">Os possíveis valores de retorno incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="223a0-112">Possible return values include the following:</span></span>



| <span data-ttu-id="223a0-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="223a0-113">Return code</span></span>                                                                                                  | <span data-ttu-id="223a0-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="223a0-114">Description</span></span>                                                                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="223a0-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="223a0-115"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="223a0-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="223a0-116">Success.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="223a0-117"><dt>**S \_ avisar \_ OUTPUTRESET**</dt></span><span class="sxs-lookup"><span data-stu-id="223a0-117"><dt>**S\_WARN\_OUTPUTRESET**</dt></span></span> </dl>          | <span data-ttu-id="223a0-118">A parte de renderização do grafo foi excluída.</span><span class="sxs-lookup"><span data-stu-id="223a0-118">Rendering portion of the graph was deleted.</span></span><br/>                         |
| <dl> <span data-ttu-id="223a0-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="223a0-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="223a0-120">Nenhuma linha do tempo definida para este mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="223a0-120">No timeline set for this render engine.</span></span><br/>                             |
| <dl> <span data-ttu-id="223a0-121"><dt>**E \_ deve \_ iniciar o \_ renderizador**</dt></span><span class="sxs-lookup"><span data-stu-id="223a0-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="223a0-122">Falha ao inicializar o mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="223a0-122">Render engine failed to initialize.</span></span><br/>                                 |
| <dl> <span data-ttu-id="223a0-123"><dt>**o \_ mecanismo de renderização E \_ \_ está \_ desfeito**</dt></span><span class="sxs-lookup"><span data-stu-id="223a0-123"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="223a0-124">Falha na operação porque o projeto não foi renderizado com êxito.</span><span class="sxs-lookup"><span data-stu-id="223a0-124">Operation failed because the project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="223a0-125"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="223a0-125"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="223a0-126">Erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="223a0-126">Unexpected error.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="223a0-127"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="223a0-127"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl>      | <span data-ttu-id="223a0-128">Tipo de mídia inválido.</span><span class="sxs-lookup"><span data-stu-id="223a0-128">Invalid media type.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="223a0-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="223a0-129">Remarks</span></span>

<span data-ttu-id="223a0-130">Esse método não cria a parte de renderização do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="223a0-130">This method does not build the rendering portion of the filter graph.</span></span> <span data-ttu-id="223a0-131">O aplicativo deve conectar os Pins de saída no front-end para os filtros de renderização desejados:</span><span class="sxs-lookup"><span data-stu-id="223a0-131">The application must connect the output pins on the front end to the desired rendering filters:</span></span>

-   <span data-ttu-id="223a0-132">Para visualizar, chame o método [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md) .</span><span class="sxs-lookup"><span data-stu-id="223a0-132">To preview, call the [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md) method.</span></span>
-   <span data-ttu-id="223a0-133">Para gerar um arquivo, chame [**IRenderEngine:: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) para recuperar o pino de saída para cada grupo e, em seguida, conecte os Pins a um filtro Multiplexador.</span><span class="sxs-lookup"><span data-stu-id="223a0-133">To output a file, call [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) to retrieve the output pin for each group, then connect the pins to a multiplexer filter.</span></span>

<span data-ttu-id="223a0-134">Se você estiver usando o mecanismo de processamento básico, os Pins de saída no front-end produzirão dados descompactados.</span><span class="sxs-lookup"><span data-stu-id="223a0-134">If you are using the basic render engine, the output pins on the front end produce uncompressed data.</span></span> <span data-ttu-id="223a0-135">Se você estiver usando o mecanismo de processamento inteligente, os Pins de saída produzirão dados compactados.</span><span class="sxs-lookup"><span data-stu-id="223a0-135">If you are using the smart render engine, the output pins produce compressed data.</span></span>

<span data-ttu-id="223a0-136">Se você alterar a linha do tempo depois de criar o gráfico de filtro, deverá chamar `ConnectFrontEnd` novamente para recriar o front-end.</span><span class="sxs-lookup"><span data-stu-id="223a0-136">If you change the timeline after you build the filter graph, you must call `ConnectFrontEnd` again to rebuild the front end.</span></span> <span data-ttu-id="223a0-137">O método preserva a parte de renderização do grafo sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="223a0-137">The method preserves the rendering portion of the graph whenever possible.</span></span> <span data-ttu-id="223a0-138">No entanto, se você adicionar ou excluir um grupo, ou alterar a ordem dos grupos, `ConnectFrontEnd` o excluirá a parte de renderização e seu aplicativo deverá reconstruí-la.</span><span class="sxs-lookup"><span data-stu-id="223a0-138">However, if you add or delete a group, or change the order of the groups, `ConnectFrontEnd` deletes the rendering portion and your application must rebuild it.</span></span> <span data-ttu-id="223a0-139">Se o método excluir a parte de renderização, ele retornará S \_ Warn \_ OUTPUTRESET.</span><span class="sxs-lookup"><span data-stu-id="223a0-139">If the method deletes the rendering portion, it returns S\_WARN\_OUTPUTRESET.</span></span>

> [!Note]  
> <span data-ttu-id="223a0-140">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="223a0-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="223a0-141">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="223a0-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="223a0-142">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="223a0-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="223a0-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="223a0-143">Requirements</span></span>



| <span data-ttu-id="223a0-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="223a0-144">Requirement</span></span> | <span data-ttu-id="223a0-145">Valor</span><span class="sxs-lookup"><span data-stu-id="223a0-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="223a0-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="223a0-146">Header</span></span><br/>  | <dl> <span data-ttu-id="223a0-147"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="223a0-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="223a0-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="223a0-148">Library</span></span><br/> | <dl> <span data-ttu-id="223a0-149"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="223a0-149"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="223a0-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="223a0-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="223a0-151">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="223a0-151">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="223a0-152">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="223a0-152">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




