---
description: A interface ISampleGrabber é exposta pelo filtro de apoio de exemplo. Ele permite que um aplicativo recupere exemplos de mídia individuais à medida que eles se movem pelo grafo de filtro.
ms.assetid: 97cf1127-d5d7-4e6a-a371-19f24e497a7f
title: Interface ISampleGrabber (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f6e923032e74f88dceb1c2465e27dab9423bae1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810216"
---
# <a name="isamplegrabber-interface"></a><span data-ttu-id="8480a-104">Interface ISampleGrabber</span><span class="sxs-lookup"><span data-stu-id="8480a-104">ISampleGrabber interface</span></span>

> [!Note]  
> <span data-ttu-id="8480a-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="8480a-105">\[Deprecated.</span></span> <span data-ttu-id="8480a-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8480a-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8480a-107">A interface **ISampleGrabber** é exposta pelo filtro de [**apoio de exemplo**](sample-grabber-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="8480a-107">The **ISampleGrabber** interface is exposed by the [**Sample Grabber**](sample-grabber-filter.md) filter.</span></span> <span data-ttu-id="8480a-108">Ele permite que um aplicativo recupere exemplos de mídia individuais à medida que eles se movem pelo grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="8480a-108">It enables an application to retrieve individual media samples as they move through the filter graph.</span></span>

## <a name="members"></a><span data-ttu-id="8480a-109">Membros</span><span class="sxs-lookup"><span data-stu-id="8480a-109">Members</span></span>

<span data-ttu-id="8480a-110">A interface **ISampleGrabber** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8480a-110">The **ISampleGrabber** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8480a-111">**ISampleGrabber** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8480a-111">**ISampleGrabber** also has these types of members:</span></span>

-   [<span data-ttu-id="8480a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="8480a-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8480a-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="8480a-113">Methods</span></span>

<span data-ttu-id="8480a-114">A interface **ISampleGrabber** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8480a-114">The **ISampleGrabber** interface has these methods.</span></span>



| <span data-ttu-id="8480a-115">Método</span><span class="sxs-lookup"><span data-stu-id="8480a-115">Method</span></span>                                                                | <span data-ttu-id="8480a-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="8480a-116">Description</span></span>                                                                                                                       |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8480a-117">**GetConnectedMediaType**</span><span class="sxs-lookup"><span data-stu-id="8480a-117">**GetConnectedMediaType**</span></span>](isamplegrabber-getconnectedmediatype.md) | <span data-ttu-id="8480a-118">Recupera o tipo de mídia para a conexão no pino de entrada do exemplo de apoio.</span><span class="sxs-lookup"><span data-stu-id="8480a-118">Retrieves the media type for the connection on the input pin of Sample Grabber.</span></span><br/>                                        |
| [<span data-ttu-id="8480a-119">**GetCurrentBuffer**</span><span class="sxs-lookup"><span data-stu-id="8480a-119">**GetCurrentBuffer**</span></span>](isamplegrabber-getcurrentbuffer.md)           | <span data-ttu-id="8480a-120">Recupera uma cópia do exemplo que o filtro recebeu mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="8480a-120">Retrieves a copy of the sample that the filter received most recently.</span></span><br/>                                                 |
| [<span data-ttu-id="8480a-121">**GetCurrentSample**</span><span class="sxs-lookup"><span data-stu-id="8480a-121">**GetCurrentSample**</span></span>](isamplegrabber-getcurrentsample.md)           | <span data-ttu-id="8480a-122">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="8480a-122">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="8480a-123">**SetBufferSamples**</span><span class="sxs-lookup"><span data-stu-id="8480a-123">**SetBufferSamples**</span></span>](isamplegrabber-setbuffersamples.md)           | <span data-ttu-id="8480a-124">Especifica se os dados de exemplo devem ser copiados em um buffer conforme eles passam pelo filtro.</span><span class="sxs-lookup"><span data-stu-id="8480a-124">Specifies whether to copy sample data into a buffer as it goes through the filter.</span></span><br/>                                     |
| [<span data-ttu-id="8480a-125">**SetCallback**</span><span class="sxs-lookup"><span data-stu-id="8480a-125">**SetCallback**</span></span>](isamplegrabber-setcallback.md)                     | <span data-ttu-id="8480a-126">Especifica um método de retorno de chamada para chamar em exemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="8480a-126">Specifies a callback method to call on incoming samples.</span></span><br/>                                                               |
| [<span data-ttu-id="8480a-127">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="8480a-127">**SetMediaType**</span></span>](isamplegrabber-setmediatype.md)                   | <span data-ttu-id="8480a-128">Especifica o tipo de mídia para a conexão no pino de entrada do exemplo de apoio.</span><span class="sxs-lookup"><span data-stu-id="8480a-128">Specifies the media type for the connection on the input pin of the Sample Grabber.</span></span><br/>                                    |
| [<span data-ttu-id="8480a-129">**SetOneShot**</span><span class="sxs-lookup"><span data-stu-id="8480a-129">**SetOneShot**</span></span>](isamplegrabber-setoneshot.md)                       | <span data-ttu-id="8480a-130">Especifica se o filtro de [**apoio de exemplo**](sample-grabber-filter.md) é interrompido depois que o filtro recebe um exemplo.</span><span class="sxs-lookup"><span data-stu-id="8480a-130">Specifies whether the [**Sample Grabber**](sample-grabber-filter.md) filter halts after the filter receives a sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8480a-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="8480a-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8480a-132">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="8480a-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8480a-133">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8480a-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8480a-134">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8480a-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8480a-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8480a-135">Requirements</span></span>



| <span data-ttu-id="8480a-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8480a-136">Requirement</span></span> | <span data-ttu-id="8480a-137">Valor</span><span class="sxs-lookup"><span data-stu-id="8480a-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8480a-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8480a-138">Header</span></span><br/>  | <dl> <span data-ttu-id="8480a-139"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8480a-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8480a-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8480a-140">Library</span></span><br/> | <dl> <span data-ttu-id="8480a-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8480a-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8480a-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="8480a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8480a-143">Usando o exemplo de apoio</span><span class="sxs-lookup"><span data-stu-id="8480a-143">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 
