---
description: Este exemplo demonstra a decodificação de vários quadros em um arquivo GIF, a leitura de metadados apropriados para cada quadro, a composição de quadros e a renderização da animação com Direct2D.
ms.assetid: d71c66b5-d37c-4c8a-bfd7-b97c69c3b8e9
title: Exemplo de GIF animado por WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: afb0c1368e2c66d40d1be4095ec56d5daeb5ab53
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "105748109"
---
# <a name="wic-animated-gif-sample"></a><span data-ttu-id="ccf41-103">Exemplo de GIF animado por WIC</span><span class="sxs-lookup"><span data-stu-id="ccf41-103">WIC animated GIF sample</span></span>

<span data-ttu-id="ccf41-104">Este exemplo demonstra a decodificação de vários quadros em um arquivo GIF, a leitura de metadados apropriados para cada quadro, a composição de quadros e a renderização da animação com Direct2D.</span><span class="sxs-lookup"><span data-stu-id="ccf41-104">This sample demonstrates decoding various frames in a GIF file, reading appropriate metadata for each frame, composing frames, and rendering the animation with Direct2D.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccf41-105">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccf41-105">Requirements</span></span>

<span data-ttu-id="ccf41-106">Este exemplo tem os seguintes requisitos.</span><span class="sxs-lookup"><span data-stu-id="ccf41-106">This sample has the following requirements.</span></span>

| <span data-ttu-id="ccf41-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccf41-107">Requirement</span></span> | <span data-ttu-id="ccf41-108">Valor</span><span class="sxs-lookup"><span data-stu-id="ccf41-108">Value</span></span> |
|-|-|
| <span data-ttu-id="ccf41-109">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccf41-109">Minimum supported client</span></span> | <span data-ttu-id="ccf41-110">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ccf41-110">Windows 7</span></span> |
| <span data-ttu-id="ccf41-111">SDK do Windows mínimo</span><span class="sxs-lookup"><span data-stu-id="ccf41-111">Minimum Windows SDK</span></span> | <span data-ttu-id="ccf41-112">[SDK (Software Development Kit)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) do Windows para Windows 7</span><span class="sxs-lookup"><span data-stu-id="ccf41-112">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="ccf41-113">Baixar o exemplo</span><span class="sxs-lookup"><span data-stu-id="ccf41-113">Downloading the sample</span></span>

<span data-ttu-id="ccf41-114">Este exemplo está disponível em [GIF animado por WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif).</span><span class="sxs-lookup"><span data-stu-id="ccf41-114">This sample is available at [WIC animated GIF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="ccf41-115">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="ccf41-115">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="ccf41-116">Usando o Visual Studio (método preferencial)</span><span class="sxs-lookup"><span data-stu-id="ccf41-116">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="ccf41-117">Abra o Windows Explorer e navegue para o diretório.</span><span class="sxs-lookup"><span data-stu-id="ccf41-117">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="ccf41-118">Clique duas vezes no ícone do arquivo. sln (solução) para abrir o arquivo no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ccf41-118">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="ccf41-119">No menu **Compilar**, selecione **Compilar Solução**.</span><span class="sxs-lookup"><span data-stu-id="ccf41-119">In the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="ccf41-120">O aplicativo será criado no \\ diretório de depuração ou de \\ lançamento padrão.</span><span class="sxs-lookup"><span data-stu-id="ccf41-120">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="ccf41-121">Usando o prompt de comando</span><span class="sxs-lookup"><span data-stu-id="ccf41-121">Using the command prompt</span></span>

<span data-ttu-id="ccf41-122">Para criar o exemplo usando um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="ccf41-122">To build the sample by using a command prompt.</span></span>

1. <span data-ttu-id="ccf41-123">Abra o prompt de comando e navegue até o diretório de exemplo.</span><span class="sxs-lookup"><span data-stu-id="ccf41-123">Open the command prompt and navigate to the sample directory.</span></span>
2. <span data-ttu-id="ccf41-124">Digite `msbuild WICAnimatedGif.sln`</span><span class="sxs-lookup"><span data-stu-id="ccf41-124">Type `msbuild WICAnimatedGif.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="ccf41-125">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="ccf41-125">Running the sample</span></span>

<span data-ttu-id="ccf41-126">Depois que o aplicativo for iniciado, carregue um arquivo de imagem usando o comando **abrir** do menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="ccf41-126">After the application is launched, load an image file by using the **Open** command of the **File** menu.</span></span> <span data-ttu-id="ccf41-127">Há suporte para o redimensionamento de janela.</span><span class="sxs-lookup"><span data-stu-id="ccf41-127">Window resizing is supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="ccf41-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccf41-128">See also</span></span>

[<span data-ttu-id="ccf41-129">Codec de imagem do Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="ccf41-129">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="ccf41-130">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="ccf41-130">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="ccf41-131">Referência</span><span class="sxs-lookup"><span data-stu-id="ccf41-131">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="ccf41-132">Direct2D</span><span class="sxs-lookup"><span data-stu-id="ccf41-132">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="ccf41-133">Amostras e exemplos de código</span><span class="sxs-lookup"><span data-stu-id="ccf41-133">Samples and code examples</span></span>](-wic-samples.md)
