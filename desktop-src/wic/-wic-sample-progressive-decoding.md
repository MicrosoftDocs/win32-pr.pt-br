---
description: Este exemplo demonstra o uso do Windows Imaging Component (WIC) para decodificar uma imagem que é codificada com níveis progressivos.
ms.assetid: 14018dce-26f0-4e1e-9d19-c5b42dd2cdab
title: Exemplo de decodificação progressiva de WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 2e4b1fc560af0ee8c817208fec628ddb068676bb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "105812251"
---
# <a name="wic-progressive-decoding-sample"></a><span data-ttu-id="a14ef-103">Exemplo de decodificação progressiva de WIC</span><span class="sxs-lookup"><span data-stu-id="a14ef-103">WIC progressive decoding sample</span></span>

<span data-ttu-id="a14ef-104">Este exemplo demonstra o uso do Windows Imaging Component (WIC) para decodificar uma imagem que é codificada com níveis progressivos.</span><span class="sxs-lookup"><span data-stu-id="a14ef-104">This sample demonstrates the use of Windows Imaging Component (WIC) to decode an image that is encoded with progressive levels.</span></span> <span data-ttu-id="a14ef-105">Este exemplo usa Direct2D para renderizar os diferentes níveis progressivos na tela.</span><span class="sxs-lookup"><span data-stu-id="a14ef-105">This sample uses Direct2D to render the different progressive levels to the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="a14ef-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a14ef-106">Requirements</span></span>

<span data-ttu-id="a14ef-107">Este exemplo tem os seguintes requisitos.</span><span class="sxs-lookup"><span data-stu-id="a14ef-107">This sample has the following requirements.</span></span>

| <span data-ttu-id="a14ef-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="a14ef-108">Requirement</span></span> | <span data-ttu-id="a14ef-109">Valor</span><span class="sxs-lookup"><span data-stu-id="a14ef-109">Value</span></span> |
|-|
| <span data-ttu-id="a14ef-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a14ef-110">Minimum supported client</span></span> | <span data-ttu-id="a14ef-111">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a14ef-111">Windows 7</span></span> |
| <span data-ttu-id="a14ef-112">SDK do Windows mínimo</span><span class="sxs-lookup"><span data-stu-id="a14ef-112">Minimum Windows SDK</span></span> | <span data-ttu-id="a14ef-113">[SDK (Software Development Kit)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) do Windows para Windows 7</span><span class="sxs-lookup"><span data-stu-id="a14ef-113">[Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for Windows 7</span></span> |

## <a name="downloading-the-sample"></a><span data-ttu-id="a14ef-114">Baixar o exemplo</span><span class="sxs-lookup"><span data-stu-id="a14ef-114">Downloading the sample</span></span>

<span data-ttu-id="a14ef-115">Este exemplo está disponível na [codificação progressiva do WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding).</span><span class="sxs-lookup"><span data-stu-id="a14ef-115">This sample is available at [WIC progressive encoding](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding).</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="a14ef-116">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="a14ef-116">Building the sample</span></span>

### <a name="using-visual-studio-preferred-method"></a><span data-ttu-id="a14ef-117">Usando o Visual Studio (método preferencial)</span><span class="sxs-lookup"><span data-stu-id="a14ef-117">Using Visual Studio (preferred method)</span></span>

1. <span data-ttu-id="a14ef-118">Abra o Windows Explorer e navegue para o diretório.</span><span class="sxs-lookup"><span data-stu-id="a14ef-118">Open Windows Explorer and navigate to the directory.</span></span>
2. <span data-ttu-id="a14ef-119">Clique duas vezes no ícone do arquivo. sln (solução) para abrir o arquivo no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a14ef-119">Double-click the icon for the .sln (solution) file to open the file in Visual Studio.</span></span>
3. <span data-ttu-id="a14ef-120">No menu Compilar, selecione Compilar Solução.</span><span class="sxs-lookup"><span data-stu-id="a14ef-120">In the Build menu, select Build Solution.</span></span> <span data-ttu-id="a14ef-121">O aplicativo será criado no \\ diretório de depuração ou de \\ lançamento padrão.</span><span class="sxs-lookup"><span data-stu-id="a14ef-121">The application will be built in the default \\Debug or \\Release directory.</span></span>

### <a name="using-the-command-prompt"></a><span data-ttu-id="a14ef-122">Usando o prompt de comando</span><span class="sxs-lookup"><span data-stu-id="a14ef-122">Using the command prompt</span></span>

<span data-ttu-id="a14ef-123">Para criar o exemplo usando o prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="a14ef-123">To build the sample using the command prompt.</span></span>

1. <span data-ttu-id="a14ef-124">Abra o prompt de comando e navegue até o diretório de exemplo.</span><span class="sxs-lookup"><span data-stu-id="a14ef-124">Open the command prompt and navigate to the sample directory.</span></span>
2. <span data-ttu-id="a14ef-125">Digite `msbuild WICProgressiveDecoding.sln`</span><span class="sxs-lookup"><span data-stu-id="a14ef-125">Type `msbuild WICProgressiveDecoding.sln`</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="a14ef-126">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="a14ef-126">Running the sample</span></span>

<span data-ttu-id="a14ef-127">Depois que o aplicativo for iniciado, carregue um arquivo de imagem por meio do menu abrir arquivo.</span><span class="sxs-lookup"><span data-stu-id="a14ef-127">After the application is launched, load an image file through file open menu.</span></span> <span data-ttu-id="a14ef-128">Ao carregar, o nível progressivo padrão é definido como 0.</span><span class="sxs-lookup"><span data-stu-id="a14ef-128">On loading, the default progressive level is set to 0.</span></span> <span data-ttu-id="a14ef-129">Você pode navegar para diferentes níveis progressivos por meio de menu ou de uma tecla para cima/para baixo.</span><span class="sxs-lookup"><span data-stu-id="a14ef-129">You can navigate to different progressive levels either through menu or Up/Down key.</span></span> <span data-ttu-id="a14ef-130">O texto do nível progressivo atual é exibido na barra de status da janela principal.</span><span class="sxs-lookup"><span data-stu-id="a14ef-130">The current progressive level text is displayed on the main window status bar.</span></span> <span data-ttu-id="a14ef-131">Há suporte para o redimensionamento de janela.</span><span class="sxs-lookup"><span data-stu-id="a14ef-131">Window resizing is supported.</span></span>

> [!NOTE]
> <span data-ttu-id="a14ef-132">A decodificação progressiva está disponível apenas para imagens que foram codificadas progressivamente.</span><span class="sxs-lookup"><span data-stu-id="a14ef-132">Progressive decoding is available only for images that have been progressively encoded.</span></span> <span data-ttu-id="a14ef-133">A imagem fornecida com este exemplo foi codificada progressivamente.</span><span class="sxs-lookup"><span data-stu-id="a14ef-133">The image provided with this sample has been progressively encoded.</span></span>

## <a name="see-also"></a><span data-ttu-id="a14ef-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="a14ef-134">See also</span></span>

[<span data-ttu-id="a14ef-135">Codec de imagem do Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="a14ef-135">Microsoft Windows Imaging Codec</span></span>](-wic-lh.md)

[<span data-ttu-id="a14ef-136">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="a14ef-136">Programming guide</span></span>](-wic-programming-guide.md)

[<span data-ttu-id="a14ef-137">Referência</span><span class="sxs-lookup"><span data-stu-id="a14ef-137">Reference</span></span>](-wic-codec-reference.md)

[<span data-ttu-id="a14ef-138">Direct2D</span><span class="sxs-lookup"><span data-stu-id="a14ef-138">Direct2D</span></span>](../direct2d/direct2d-portal.md)

[<span data-ttu-id="a14ef-139">Amostras e exemplos de código</span><span class="sxs-lookup"><span data-stu-id="a14ef-139">Samples and code examples</span></span>](-wic-samples.md)

[<span data-ttu-id="a14ef-140">Visão geral da decodificação progressiva</span><span class="sxs-lookup"><span data-stu-id="a14ef-140">Progressive decoding overview</span></span>](-wic-progressive-decoding.md)
