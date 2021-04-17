---
description: O método GetFilterGraph recupera o grafo de filtro que o mecanismo de processamento construiu, se houver.
ms.assetid: 509b2c9c-c21b-4855-880f-f09ad342e758
title: 'Método IRenderEngine:: GetFilterGraph (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c4750e6127c0d57758e46b2309f4d91afc110e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780633"
---
# <a name="irenderenginegetfiltergraph-method"></a><span data-ttu-id="01792-103">Método IRenderEngine:: GetFilterGraph</span><span class="sxs-lookup"><span data-stu-id="01792-103">IRenderEngine::GetFilterGraph method</span></span>

> [!Note]  
> <span data-ttu-id="01792-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="01792-104">\[Deprecated.</span></span> <span data-ttu-id="01792-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="01792-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="01792-106">O `GetFilterGraph` método recupera o gráfico de filtro que o mecanismo de processamento construiu, se houver.</span><span class="sxs-lookup"><span data-stu-id="01792-106">The `GetFilterGraph` method retrieves the filter graph that the render engine has constructed, if any.</span></span>

## <a name="syntax"></a><span data-ttu-id="01792-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01792-107">Syntax</span></span>


```C++
HRESULT GetFilterGraph(
  [out] IGraphBuilder **ppFG
);
```



## <a name="parameters"></a><span data-ttu-id="01792-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01792-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01792-109">*ppFG* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="01792-109">*ppFG* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01792-110">Recebe um ponteiro para a interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="01792-110">Receives a pointer to the filter graph's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="01792-111">Ele receberá o valor **NULL** se não houver nenhum grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="01792-111">It receives the value **NULL** if there is no filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01792-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01792-112">Return value</span></span>

<span data-ttu-id="01792-113">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="01792-113">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="01792-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="01792-114">Return code</span></span>                                                                                            | <span data-ttu-id="01792-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="01792-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="01792-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="01792-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="01792-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="01792-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="01792-118"><dt>**E \_ deve \_ iniciar o \_ renderizador**</dt></span><span class="sxs-lookup"><span data-stu-id="01792-118"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="01792-119">Falha ao inicializar o mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="01792-119">Render engine failed to initialize.</span></span><br/> |
| <dl> <span data-ttu-id="01792-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="01792-120"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="01792-121">Ponteiro inválido.</span><span class="sxs-lookup"><span data-stu-id="01792-121">Invalid pointer.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="01792-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="01792-122">Remarks</span></span>

<span data-ttu-id="01792-123">Use o método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) para criar o front-end do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="01792-123">Use the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method to build the front end of the filter graph.</span></span> <span data-ttu-id="01792-124">Para a versão prévia, use [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md) para concluir o grafo.</span><span class="sxs-lookup"><span data-stu-id="01792-124">For preview, use the [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md) to complete the graph.</span></span> <span data-ttu-id="01792-125">Para saída de arquivo, conecte o front-end a uma combinação de gravador de MUX/arquivo.</span><span class="sxs-lookup"><span data-stu-id="01792-125">For file output, connect the front end to a mux/file writer combination.</span></span> <span data-ttu-id="01792-126">Para obter mais informações, consulte [renderizando um projeto](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="01792-126">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="01792-127">O grafo resultante pode ser executado, pausado, parado e buscado; no entanto, a taxa de reprodução não pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="01792-127">The resulting graph can be run, paused, stopped, and seeked; the playback rate cannot be changed, however.</span></span>

<span data-ttu-id="01792-128">No retorno, se o valor de *\* ppFG* for não **nulo**, a interface **IGraphBuilder** terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="01792-128">On return, if the value of *\*ppFG* is non-**NULL**, the **IGraphBuilder** interface has an outstanding reference count.</span></span> <span data-ttu-id="01792-129">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="01792-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="01792-130">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="01792-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="01792-131">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="01792-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="01792-132">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="01792-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="01792-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01792-133">Requirements</span></span>



| <span data-ttu-id="01792-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="01792-134">Requirement</span></span> | <span data-ttu-id="01792-135">Valor</span><span class="sxs-lookup"><span data-stu-id="01792-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01792-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01792-136">Header</span></span><br/>  | <dl> <span data-ttu-id="01792-137"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="01792-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="01792-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01792-138">Library</span></span><br/> | <dl> <span data-ttu-id="01792-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01792-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01792-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="01792-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01792-141">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="01792-141">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="01792-142">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="01792-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




