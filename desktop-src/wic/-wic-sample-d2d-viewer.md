---
description: Este exemplo demonstra o uso do Windows Imaging Component (WIC) para decodificar um arquivo de imagem e Direct2D para renderizar a imagem na tela.
ms.assetid: 4f989ff6-b513-4354-a1bb-8d9521f693a2
title: Visualizador de imagem de WIC usando o exemplo de Direct2D
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: a18bf17e7f43d3c4ad935bae9f8ed42e7b48db01
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "105751160"
---
# <a name="wic-image-viewer-using-direct2d-sample"></a><span data-ttu-id="1864b-103">Visualizador de imagem de WIC usando o exemplo de Direct2D</span><span class="sxs-lookup"><span data-stu-id="1864b-103">WIC image viewer using Direct2D sample</span></span>

<span data-ttu-id="1864b-104">Este exemplo demonstra o uso do Windows Imaging Component (WIC) para decodificar um arquivo de imagem e Direct2D para renderizar a imagem na tela.</span><span class="sxs-lookup"><span data-stu-id="1864b-104">This sample demonstrates the use of Windows Imaging Component (WIC) to decode an image file and Direct2D to render the image to the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="1864b-105">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1864b-105">Requirements</span></span>

<span data-ttu-id="1864b-106">Este exemplo tem os seguintes requisitos.</span><span class="sxs-lookup"><span data-stu-id="1864b-106">This sample has the following requirements.</span></span>

| <span data-ttu-id="1864b-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="1864b-107">Requirement</span></span> | <span data-ttu-id="1864b-108">Valor</span><span class="sxs-lookup"><span data-stu-id="1864b-108">Value</span></span> |
|-|-|
| <span data-ttu-id="1864b-109">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1864b-109">Minimum supported client</span></span> | <span data-ttu-id="1864b-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1864b-110">Windows Vista</span></span> |
| <span data-ttu-id="1864b-111">SDK do Windows mínimo</span><span class="sxs-lookup"><span data-stu-id="1864b-111">Minimum Windows SDK</span></span> | <span data-ttu-id="1864b-112">[SDK (Software Development Kit)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) do Windows para Windows 7</span><span class="sxs-lookup"><span data-stu-id="1864b-112">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="1864b-113">Baixar o exemplo</span><span class="sxs-lookup"><span data-stu-id="1864b-113">Downloading the sample</span></span>

<span data-ttu-id="1864b-114">Este exemplo está disponível no [Visualizador do WIC D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d).</span><span class="sxs-lookup"><span data-stu-id="1864b-114">This sample is available at [WIC Viewer D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="1864b-115">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="1864b-115">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="1864b-116">Usando o Visual Studio (método preferencial)</span><span class="sxs-lookup"><span data-stu-id="1864b-116">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="1864b-117">Abra o Windows Explorer e navegue para o diretório.</span><span class="sxs-lookup"><span data-stu-id="1864b-117">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="1864b-118">Clique duas vezes no ícone do arquivo. sln (solução) para abrir o arquivo no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1864b-118">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="1864b-119">No menu **Compilar**, selecione **Compilar Solução**.</span><span class="sxs-lookup"><span data-stu-id="1864b-119">In the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="1864b-120">O aplicativo será criado no \\ diretório de depuração ou de \\ lançamento padrão.</span><span class="sxs-lookup"><span data-stu-id="1864b-120">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="1864b-121">Usando o prompt de comando</span><span class="sxs-lookup"><span data-stu-id="1864b-121">Using the command prompt</span></span>

<span data-ttu-id="1864b-122">Para criar o exemplo usando um prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="1864b-122">To build the sample by using a command prompt:</span></span>

1. <span data-ttu-id="1864b-123">Abra uma janela de prompt de comando e navegue até o diretório de exemplo.</span><span class="sxs-lookup"><span data-stu-id="1864b-123">Open a command prompt window and navigate to the sample directory.</span></span>
2. <span data-ttu-id="1864b-124">Digite `msbuild WICViewerD2D.sln`</span><span class="sxs-lookup"><span data-stu-id="1864b-124">Type `msbuild WICViewerD2D.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="1864b-125">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="1864b-125">Running the sample</span></span>

<span data-ttu-id="1864b-126">Depois de iniciar o aplicativo, carregue um arquivo de imagem usando o comando **abrir** do menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="1864b-126">After you start the application, load an image file by using the **Open** command of the **File** menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="1864b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1864b-127">See also</span></span>

[<span data-ttu-id="1864b-128">Codec de imagem do Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="1864b-128">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="1864b-129">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="1864b-129">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="1864b-130">Referência</span><span class="sxs-lookup"><span data-stu-id="1864b-130">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="1864b-131">Direct2D</span><span class="sxs-lookup"><span data-stu-id="1864b-131">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="1864b-132">Amostras e exemplos de código</span><span class="sxs-lookup"><span data-stu-id="1864b-132">Samples and code examples</span></span>](-wic-samples.md)
