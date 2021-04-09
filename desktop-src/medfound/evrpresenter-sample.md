---
description: Exemplo de EVRPresenter
ms.assetid: 791a9816-4c40-4683-8b32-22f73d7fe84d
title: Exemplo de EVRPresenter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde85de152c41f348b1aae74a8c0d67ca746cab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089741"
---
# <a name="evrpresenter-sample"></a><span data-ttu-id="ce1c3-103">Exemplo de EVRPresenter</span><span class="sxs-lookup"><span data-stu-id="ce1c3-103">EVRPresenter Sample</span></span>

<span data-ttu-id="ce1c3-104">Mostra como implementar um apresentador personalizado para o [processador de vídeo avançado](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="ce1c3-104">Shows how to implement a custom presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="ce1c3-105">O apresentador personalizado pode ser usado com o filtro EVR do DirectShow ou com o coletor de EVR Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-105">The custom presenter can be used with either the DirectShow EVR filter or the Microsoft Media Foundation EVR sink.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="ce1c3-106">APIs demonstradas</span><span class="sxs-lookup"><span data-stu-id="ce1c3-106">APIs Demonstrated</span></span>

<span data-ttu-id="ce1c3-107">Este exemplo demonstra as seguintes interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="ce1c3-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="ce1c3-108">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="ce1c3-108">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [<span data-ttu-id="ce1c3-109">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="ce1c3-109">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="ce1c3-110">**IMFTopologyServiceLookupClient**</span><span class="sxs-lookup"><span data-stu-id="ce1c3-110">**IMFTopologyServiceLookupClient**</span></span>](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient)
-   [<span data-ttu-id="ce1c3-111">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="ce1c3-111">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)
-   [<span data-ttu-id="ce1c3-112">**IMFVideoDisplayControl**</span><span class="sxs-lookup"><span data-stu-id="ce1c3-112">**IMFVideoDisplayControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)
-   [<span data-ttu-id="ce1c3-113">**IMFVideoPresenter**</span><span class="sxs-lookup"><span data-stu-id="ce1c3-113">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)

## <a name="usage"></a><span data-ttu-id="ce1c3-114">Uso</span><span class="sxs-lookup"><span data-stu-id="ce1c3-114">Usage</span></span>

<span data-ttu-id="ce1c3-115">O exemplo EVRPresenter cria uma DLL que é um servidor COM para o apresentador.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-115">The EVRPresenter sample builds a DLL that is a COM server for the presenter.</span></span> <span data-ttu-id="ce1c3-116">Antes de usar o apresentador personalizado, você deve registrar a DLL.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-116">Before using the custom presenter, you must register the DLL.</span></span>

<span data-ttu-id="ce1c3-117">Para usar este exemplo no Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="ce1c3-117">To use this sample in Media Foundation:</span></span>

1.  <span data-ttu-id="ce1c3-118">Compile o exemplo.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-118">Build the sample.</span></span>
2.  <span data-ttu-id="ce1c3-119">Regsvr32 EvrPresenter.dll.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-119">Regsvr32 EvrPresenter.dll.</span></span>
3.  <span data-ttu-id="ce1c3-120">Compile e execute o [exemplo MFPlayer](/previous-versions//bb970516(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ce1c3-120">Build and run the [MFPlayer Sample](/previous-versions//bb970516(v=vs.85)).</span></span>
4.  <span data-ttu-id="ce1c3-121">No menu **arquivo** , selecione **abrir** arquivo.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-121">From the **File** menu, select **Open** File.</span></span>
5.  <span data-ttu-id="ce1c3-122">Na caixa de diálogo **Abrir arquivo** , selecione **apresentador personalizado do EVR.**</span><span class="sxs-lookup"><span data-stu-id="ce1c3-122">In the **Open File** dialog box, select **Custom EVR Presenter.**</span></span>
6.  <span data-ttu-id="ce1c3-123">Selecione um arquivo para reprodução.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-123">Select a file for playback.</span></span>

<span data-ttu-id="ce1c3-124">Para usar este exemplo no DirectShow:</span><span class="sxs-lookup"><span data-stu-id="ce1c3-124">To use this sample in DirectShow:</span></span>

1.  <span data-ttu-id="ce1c3-125">Compile o exemplo.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-125">Build the sample.</span></span>
2.  <span data-ttu-id="ce1c3-126">Registrar EvrPresenter.dll.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-126">Register EvrPresenter.dll.</span></span>
3.  <span data-ttu-id="ce1c3-127">Compile e execute o exemplo EVRPlayer.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-127">Build and run the EVRPlayer sample.</span></span> <span data-ttu-id="ce1c3-128">Este exemplo está incluído com os exemplos do DirectShow no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-128">This sample is included with the DirectShow samples in the Windows SDK.</span></span>
4.  <span data-ttu-id="ce1c3-129">No menu **arquivo** , selecione **apresentador de EVR**.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-129">From the **File** menu, select **EVR Presenter**.</span></span>
5.  <span data-ttu-id="ce1c3-130">Selecione um arquivo para reprodução.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-130">Select a file for playback.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce1c3-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce1c3-131">Requirements</span></span>



| <span data-ttu-id="ce1c3-132">Produto</span><span class="sxs-lookup"><span data-stu-id="ce1c3-132">Product</span></span>                                                        | <span data-ttu-id="ce1c3-133">Versão</span><span class="sxs-lookup"><span data-stu-id="ce1c3-133">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="ce1c3-134">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="ce1c3-134">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="ce1c3-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ce1c3-135">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="ce1c3-136">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="ce1c3-136">Downloading the Sample</span></span>

<span data-ttu-id="ce1c3-137">Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span><span class="sxs-lookup"><span data-stu-id="ce1c3-137">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce1c3-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ce1c3-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce1c3-139">Processador de vídeo aprimorado</span><span class="sxs-lookup"><span data-stu-id="ce1c3-139">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="ce1c3-140">Como escrever um apresentador EVR</span><span class="sxs-lookup"><span data-stu-id="ce1c3-140">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> <dt>

[<span data-ttu-id="ce1c3-141">Exemplos de SDK do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ce1c3-141">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 
