---
description: O Tablet PC inclui a tecnologia para interagir com os dados da caneta do Tablet enquanto eles estão sendo coletados.
ms.assetid: e026f860-be4d-40a5-b951-15b8be3cd626
title: Acessando e manipulando a entrada da caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333126f195154241333127ec585864bd9d592a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756519"
---
# <a name="accessing-and-manipulating-stylus-input"></a><span data-ttu-id="17084-103">Acessando e manipulando a entrada da caneta</span><span class="sxs-lookup"><span data-stu-id="17084-103">Accessing and Manipulating Stylus Input</span></span>

<span data-ttu-id="17084-104">O Tablet PC inclui a tecnologia para interagir com os dados da caneta do Tablet enquanto eles estão sendo coletados.</span><span class="sxs-lookup"><span data-stu-id="17084-104">The Tablet PC includes technology for interacting with tablet pen data as it is being gathered.</span></span> <span data-ttu-id="17084-105">A classe [**RealTimeStylus**](realtimestylus-class.md) faz parte das interfaces de programação de aplicativo (API) do StylusInput, que fornecem acesso ao fluxo de dados da caneta do Tablet.</span><span class="sxs-lookup"><span data-stu-id="17084-105">The [**RealTimeStylus**](realtimestylus-class.md) class is part of the StylusInput application programming interfaces (API), which provide access to the tablet pen data stream.</span></span> <span data-ttu-id="17084-106">Essas APIs permitem capturar, interromper e modificar o fluxo independentemente da renderização e da coleta de tinta.</span><span class="sxs-lookup"><span data-stu-id="17084-106">These APIs allow you to capture, interrupt, and modify the stream independently from rendering and collecting ink.</span></span>

<span data-ttu-id="17084-107">As APIs StylusInput são projetadas para:</span><span class="sxs-lookup"><span data-stu-id="17084-107">The StylusInput APIs are designed to:</span></span>

-   <span data-ttu-id="17084-108">Forneça acesso em tempo real ao fluxo de dados da caneta eletrônica.</span><span class="sxs-lookup"><span data-stu-id="17084-108">Provide real-time access to the tablet pen data stream.</span></span>
-   <span data-ttu-id="17084-109">Mantenha o thread da interface do usuário para bloquear a renderização de tinta dinâmica ao enfileirar os dados de pacote no thread da interface do usuário e fazer uma coleta de tinta thread único.</span><span class="sxs-lookup"><span data-stu-id="17084-109">Keep the user interface (UI) thread from blocking dynamic ink rendering by queuing the packet data on the UI thread and making ink collection single threaded.</span></span>
-   <span data-ttu-id="17084-110">Aumente o desempenho e reduza o uso geral do thread usando o objeto [**InkCollector**](inkcollector-class.md) , o objeto [**InkOverlay**](inkoverlay-class.md) , o controle [InkPicture](inkpicture-control-reference.md) ou o controle [InkEdit](inkedit-control-reference.md) para coletar tinta.</span><span class="sxs-lookup"><span data-stu-id="17084-110">Increase the performance and lower the overall thread usage over using the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control to collect ink.</span></span>

<span data-ttu-id="17084-111">As APIs StylusInput não foram projetadas para trabalhar com o objeto [**InkCollector**](inkcollector-class.md) , o objeto [**InkOverlay**](inkoverlay-class.md) , o controle [InkPicture](inkpicture-control-reference.md) ou o controle [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="17084-111">The StylusInput APIs are not designed to work with the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control.</span></span>

<span data-ttu-id="17084-112">Quando você precisa interagir diretamente com o fluxo de dados da caneta do Tablet ou quando seu aplicativo pode bloquear a escrita em tempo real, use o objeto [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="17084-112">When you need to interact directly with the tablet pen data stream or when your application may block real-time inking, use the [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="17084-113">Use o controle objeto [**InkCollector**](inkcollector-class.md) , objeto [**InkOverlay**](inkoverlay-class.md) , controle [InkPicture](inkpicture-control-reference.md) ou [InkEdit](inkedit-control-reference.md) quando o comportamento padrão desses objetos fornecer o comportamento de que você precisa.</span><span class="sxs-lookup"><span data-stu-id="17084-113">Use the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control when the default behavior of these objects provides the behavior you need.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="17084-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="17084-114">In This Section</span></span>

<span data-ttu-id="17084-115">As seções a seguir descrevem os elementos das APIs StylusInput:</span><span class="sxs-lookup"><span data-stu-id="17084-115">The following sections describe elements of the StylusInput APIs:</span></span>

-   [<span data-ttu-id="17084-116">Arquitetura das APIs do StylusInput</span><span class="sxs-lookup"><span data-stu-id="17084-116">Architecture of the StylusInput APIs</span></span>](architecture-of-the-stylusinput-apis.md)
-   [<span data-ttu-id="17084-117">Trabalhando com as APIs do StylusInput</span><span class="sxs-lookup"><span data-stu-id="17084-117">Working with the StylusInput APIs</span></span>](working-with-the-stylusinput-apis.md)
    -   [<span data-ttu-id="17084-118">Trabalhando com a classe RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="17084-118">Working with the RealTimeStylus Class</span></span>](working-with-the-realtimestylus-class.md)
    -   [<span data-ttu-id="17084-119">Plug-ins e a classe RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="17084-119">Plug-ins and the RealTimeStylus Class</span></span>](plug-ins-and-the-realtimestylus-class.md)
    -   [<span data-ttu-id="17084-120">Dados de plug-in e a classe RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="17084-120">Plug-in Data and the RealTimeStylus Class</span></span>](plug-in-data-and-the-realtimestylus-class.md)
    -   [<span data-ttu-id="17084-121">Notas de implementação para as APIs StylusInput</span><span class="sxs-lookup"><span data-stu-id="17084-121">Implementation Notes for the StylusInput APIs</span></span>](implementation-notes-for-the-stylusinput-apis.md)
    -   [<span data-ttu-id="17084-122">Plug-ins de coleta de tinta</span><span class="sxs-lookup"><span data-stu-id="17084-122">Ink-Collection Plug-ins</span></span>](ink-collection-plug-ins.md)
    -   [<span data-ttu-id="17084-123">Plug-ins de processamento dinâmico</span><span class="sxs-lookup"><span data-stu-id="17084-123">Dynamic-Renderer Plug-ins</span></span>](dynamic-renderer-plug-ins.md)
    -   [<span data-ttu-id="17084-124">Plug-ins do Recognizer</span><span class="sxs-lookup"><span data-stu-id="17084-124">Recognizer Plug-ins</span></span>](recognizer-plug-ins.md)
-   [<span data-ttu-id="17084-125">Considerações ao usar as APIs StylusInput</span><span class="sxs-lookup"><span data-stu-id="17084-125">Considerations when Using the StylusInput APIs</span></span>](considerations-when-using-the-stylusinput-apis.md)
    -   [<span data-ttu-id="17084-126">Considerações de design para as APIs StylusInput</span><span class="sxs-lookup"><span data-stu-id="17084-126">Design Considerations for the StylusInput APIs</span></span>](design-considerations-for-the-stylusinput-apis.md)
    -   [<span data-ttu-id="17084-127">Considerações de threading para as APIs StylusInput</span><span class="sxs-lookup"><span data-stu-id="17084-127">Threading Considerations for the StylusInput APIs</span></span>](threading-considerations-for-the-stylusinput-apis.md)

[<span data-ttu-id="17084-128">O modelo RealTimeStylus em cascata</span><span class="sxs-lookup"><span data-stu-id="17084-128">The Cascaded RealTimeStylus Model</span></span>](the-cascaded-realtimestylus-model.md)

-   [<span data-ttu-id="17084-129">Considerações de tratamento de erro para as APIs StylusInput</span><span class="sxs-lookup"><span data-stu-id="17084-129">Error Handling Considerations for the StylusInput APIs</span></span>](error-handling-considerations-for-the-stylusinput-apis.md)
-   [<span data-ttu-id="17084-130">Considerações de desempenho para as APIs StylusInput</span><span class="sxs-lookup"><span data-stu-id="17084-130">Performance Considerations for the StylusInput APIs</span></span>](performance-considerations-for-the-stylusinput-apis.md)
-   [<span data-ttu-id="17084-131">Considerações de confiança parcial para as APIs StylusInput</span><span class="sxs-lookup"><span data-stu-id="17084-131">Partial Trust Considerations for the StylusInput APIs</span></span>](partial-trust-considerations-for-the-stylusinput-apis.md)

## <a name="related-topics"></a><span data-ttu-id="17084-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="17084-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17084-133">Exemplo de plug-in RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="17084-133">RealTimeStylus Plug-in Sample</span></span>](realtimestylus-plug-in-sample.md)
</dt> <dt>

[<span data-ttu-id="17084-134">Exemplo de coleção de tinta do RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="17084-134">RealTimeStylus Ink Collection Sample</span></span>](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 



