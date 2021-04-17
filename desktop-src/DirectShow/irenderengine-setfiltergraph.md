---
description: O método SetFilterGraph especifica um grafo de filtro para o mecanismo de renderização usar.
ms.assetid: 6a245864-7d22-4608-995b-b28662a6ab90
title: 'Método IRenderEngine:: SetFilterGraph (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72c93ef6610fd301c497589858a8941e2b8f71b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789934"
---
# <a name="irenderenginesetfiltergraph-method"></a><span data-ttu-id="de328-103">Método IRenderEngine:: SetFilterGraph</span><span class="sxs-lookup"><span data-stu-id="de328-103">IRenderEngine::SetFilterGraph method</span></span>

> [!Note]  
> <span data-ttu-id="de328-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="de328-104">\[Deprecated.</span></span> <span data-ttu-id="de328-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="de328-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="de328-106">O `SetFilterGraph` método especifica um grafo de filtro para o mecanismo de renderização usar.</span><span class="sxs-lookup"><span data-stu-id="de328-106">The `SetFilterGraph` method specifies a filter graph for the render engine to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="de328-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de328-107">Syntax</span></span>


```C++
HRESULT SetFilterGraph(
   IGraphBuilder *pFG
);
```



## <a name="parameters"></a><span data-ttu-id="de328-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de328-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de328-109">*pFG*</span><span class="sxs-lookup"><span data-stu-id="de328-109">*pFG*</span></span> 
</dt> <dd>

<span data-ttu-id="de328-110">Ponteiro para a interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="de328-110">Pointer to the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface of the filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de328-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de328-111">Return value</span></span>

<span data-ttu-id="de328-112">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="de328-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="de328-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="de328-113">Return code</span></span>                                                                                            | <span data-ttu-id="de328-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="de328-114">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="de328-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="de328-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="de328-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="de328-116">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="de328-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="de328-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="de328-118">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="de328-118">Invalid argument.</span></span><br/>                   |
| <dl> <span data-ttu-id="de328-119"><dt>**E \_ deve \_ iniciar o \_ renderizador**</dt></span><span class="sxs-lookup"><span data-stu-id="de328-119"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="de328-120">Falha ao inicializar o mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="de328-120">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="de328-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="de328-121">Remarks</span></span>

<span data-ttu-id="de328-122">A maioria dos aplicativos não precisa chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="de328-122">Most applications do not need to call this method.</span></span> <span data-ttu-id="de328-123">É mais comum deixar o mecanismo de renderização criar o grafo para você, chamando o método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) .</span><span class="sxs-lookup"><span data-stu-id="de328-123">It is more typical to let the render engine build the graph for you, by calling the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span>

<span data-ttu-id="de328-124">Esse método falhará se o mecanismo de processamento já tiver um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="de328-124">This method fails if the render engine already has a filter graph.</span></span>

<span data-ttu-id="de328-125">Nunca recupere um ponteiro para um grafo de filtro criado por um mecanismo de renderização e, em seguida, use-o como o parâmetro para esse método em outro mecanismo de renderização.</span><span class="sxs-lookup"><span data-stu-id="de328-125">Never retrieve a pointer to a filter graph created by one render engine and then use it as the parameter to this method on another render engine.</span></span> <span data-ttu-id="de328-126">Isso causará resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="de328-126">Doing so will cause unpredictable results.</span></span>

<span data-ttu-id="de328-127">O método **ConnectFrontEnd** destrói qualquer grafo de filtro existente, mas mantém a mesma instância de Gerenciador de gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="de328-127">The **ConnectFrontEnd** method tears down any existing filter graph, but keeps the same Filter Graph Manager instance.</span></span>

> [!Note]  
> <span data-ttu-id="de328-128">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="de328-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="de328-129">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="de328-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="de328-130">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="de328-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="de328-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de328-131">Requirements</span></span>



| <span data-ttu-id="de328-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="de328-132">Requirement</span></span> | <span data-ttu-id="de328-133">Valor</span><span class="sxs-lookup"><span data-stu-id="de328-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de328-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de328-134">Header</span></span><br/>  | <dl> <span data-ttu-id="de328-135"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="de328-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="de328-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="de328-136">Library</span></span><br/> | <dl> <span data-ttu-id="de328-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de328-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de328-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="de328-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de328-139">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="de328-139">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="de328-140">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="de328-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




