---
title: Sobre o IMFTransform
description: Sobre o IMFTransform
ms.assetid: 889f2d82-148a-4a7e-b78c-37ec86b37e0b
keywords:
- Plug-ins do Windows Media Player, interfaces
- plug-ins, interfaces
- plug-ins de processamento de sinal digital, interfaces
- Plug-ins do DSP, interfaces
- interfaces, plug-ins do DSP
- Plug-ins do Windows Media Player, interface IMFTransform
- plug-ins, interface IMFTransform
- plug-ins de processamento de sinal digital, interface IMFTransform
- Plug-ins do DSP, interface IMFTransform
- Interface IMFTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb58ab84070a8cb9390e4525b9b642f15a29f14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781289"
---
# <a name="about-imftransform"></a><span data-ttu-id="bdc86-113">Sobre o IMFTransform</span><span class="sxs-lookup"><span data-stu-id="bdc86-113">About IMFTransform</span></span>

<span data-ttu-id="bdc86-114">A interface **IMFTransform** é uma das interfaces que devem ser implementadas por um plug-in DSP de modo duplo.</span><span class="sxs-lookup"><span data-stu-id="bdc86-114">The **IMFTransform** interface is one of the interfaces that must be implemented by a dual-mode DSP plug-in.</span></span> <span data-ttu-id="bdc86-115">O Windows Media Player chama os métodos da interface **IMFTransform** para fornecer dados ao plug-in e recuperar dados processados de volta do plug-in.</span><span class="sxs-lookup"><span data-stu-id="bdc86-115">Windows Media Player calls the methods of the **IMFTransform** interface to provide data to the plug-in and to retrieve processed data back from the plug-in.</span></span> <span data-ttu-id="bdc86-116">Para obter a documentação completa da interface **IMFTransform** , consulte a seção Media Foundation do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="bdc86-116">For complete documentation of the **IMFTransform** interface, see the Media Foundation section of the Windows SDK.</span></span>

<span data-ttu-id="bdc86-117">Os métodos de **IMFTransform** podem ser categorizados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="bdc86-117">The methods of **IMFTransform** can be categorized as follows.</span></span>

## <a name="methods-that-handle-format-negotiation"></a><span data-ttu-id="bdc86-118">Métodos que manipulam a negociação de formato</span><span class="sxs-lookup"><span data-stu-id="bdc86-118">Methods That Handle Format Negotiation</span></span>

<span data-ttu-id="bdc86-119">O Windows Media Player chama os seguintes métodos para obter informações sobre os formatos de dados com suporte pelo plug-in.</span><span class="sxs-lookup"><span data-stu-id="bdc86-119">Windows Media Player calls the following methods to get information about the data formats supported by the plug-in.</span></span>

-   <span data-ttu-id="bdc86-120">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="bdc86-120">**GetStreamCount**</span></span>
-   <span data-ttu-id="bdc86-121">**GetStreamLimits**</span><span class="sxs-lookup"><span data-stu-id="bdc86-121">**GetStreamLimits**</span></span>
-   <span data-ttu-id="bdc86-122">**GetInputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="bdc86-122">**GetInputStreamInfo**</span></span>
-   <span data-ttu-id="bdc86-123">**GetOutputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="bdc86-123">**GetOutputStreamInfo**</span></span>
-   <span data-ttu-id="bdc86-124">**GetInputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="bdc86-124">**GetInputAvailableType**</span></span>
-   <span data-ttu-id="bdc86-125">**GetOutputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="bdc86-125">**GetOutputAvailableType**</span></span>
-   <span data-ttu-id="bdc86-126">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="bdc86-126">**SetInputType**</span></span>
-   <span data-ttu-id="bdc86-127">**Setoutputtypetype**</span><span class="sxs-lookup"><span data-stu-id="bdc86-127">**SetOutputType**</span></span>
-   <span data-ttu-id="bdc86-128">**Falha GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="bdc86-128">**GetAttributes**</span></span>
-   <span data-ttu-id="bdc86-129">**GetInputStreamAttributes**</span><span class="sxs-lookup"><span data-stu-id="bdc86-129">**GetInputStreamAttributes**</span></span>
-   <span data-ttu-id="bdc86-130">**GetOutputStreamAttributes**</span><span class="sxs-lookup"><span data-stu-id="bdc86-130">**GetOutputStreamAttributes**</span></span>
-   <span data-ttu-id="bdc86-131">**GetStreamIDs**</span><span class="sxs-lookup"><span data-stu-id="bdc86-131">**GetStreamIDs**</span></span>

## <a name="methods-that-specify-or-retrieve-state-information"></a><span data-ttu-id="bdc86-132">Métodos que especificam ou recuperam informações de estado</span><span class="sxs-lookup"><span data-stu-id="bdc86-132">Methods That Specify or Retrieve State Information</span></span>

<span data-ttu-id="bdc86-133">O Windows Media Player chama os seguintes métodos para obter ou definir valores relacionados ao estado atual do plug-in.</span><span class="sxs-lookup"><span data-stu-id="bdc86-133">Windows Media Player calls the following methods to get or set values related to the current state of the plug-in.</span></span>

-   <span data-ttu-id="bdc86-134">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="bdc86-134">**SetInputType**</span></span>
-   <span data-ttu-id="bdc86-135">**Setoutputtypetype**</span><span class="sxs-lookup"><span data-stu-id="bdc86-135">**SetOutputType**</span></span>
-   <span data-ttu-id="bdc86-136">**GetInputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="bdc86-136">**GetInputCurrentType**</span></span>
-   <span data-ttu-id="bdc86-137">**GetOutputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="bdc86-137">**GetOutputCurrentType**</span></span>
-   <span data-ttu-id="bdc86-138">**GetInputStatus**</span><span class="sxs-lookup"><span data-stu-id="bdc86-138">**GetInputStatus**</span></span>
-   <span data-ttu-id="bdc86-139">**AddInputStreams**</span><span class="sxs-lookup"><span data-stu-id="bdc86-139">**AddInputStreams**</span></span>
-   <span data-ttu-id="bdc86-140">**DeleteInputStreams**</span><span class="sxs-lookup"><span data-stu-id="bdc86-140">**DeleteInputStreams**</span></span>
-   <span data-ttu-id="bdc86-141">**GetOutputStatus**</span><span class="sxs-lookup"><span data-stu-id="bdc86-141">**GetOutputStatus**</span></span>
-   <span data-ttu-id="bdc86-142">**SetOutputBounds**</span><span class="sxs-lookup"><span data-stu-id="bdc86-142">**SetOutputBounds**</span></span>

> [!Note]  
> <span data-ttu-id="bdc86-143">**SetInputType** e **setoutputtypetype** são usados para a negociação de formato e para especificar e recuperar informações de estado.</span><span class="sxs-lookup"><span data-stu-id="bdc86-143">**SetInputType** and **SetOutputType** are used both for format negotiation and for specifying and retrieving state information.</span></span>

 

## <a name="methods-that-handle-buffering-and-processing-data"></a><span data-ttu-id="bdc86-144">Métodos que lidam com buffer e processando dados</span><span class="sxs-lookup"><span data-stu-id="bdc86-144">Methods That Handle Buffering and Processing Data</span></span>

<span data-ttu-id="bdc86-145">O Windows Media Player chama os seguintes métodos para iniciar os vários processos que o plug-in executa para fazer o processamento de sinal digital.</span><span class="sxs-lookup"><span data-stu-id="bdc86-145">Windows Media Player calls the following methods to initiate the various processes that the plug-in performs to do the digital signal processing.</span></span>

-   <span data-ttu-id="bdc86-146">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="bdc86-146">**ProcessInput**</span></span>
-   <span data-ttu-id="bdc86-147">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="bdc86-147">**ProcessOutput**</span></span>
-   <span data-ttu-id="bdc86-148">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="bdc86-148">**ProcessMessage**</span></span>
-   <span data-ttu-id="bdc86-149">**ProcessEvent**</span><span class="sxs-lookup"><span data-stu-id="bdc86-149">**ProcessEvent**</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdc86-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bdc86-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdc86-151">**Interfaces necessárias**</span><span class="sxs-lookup"><span data-stu-id="bdc86-151">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




