---
description: Mostra como usar Microsoft Media Foundation para decodificar áudio de um arquivo de mídia.
ms.assetid: 29822e6b-8598-4133-b181-7fb0854553b7
title: Exemplo de clipe de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0e4a3e515d08e2cafd2ab2ba451a528f3d5677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105794452"
---
# <a name="audio-clip-sample"></a><span data-ttu-id="42d3e-103">Exemplo de clipe de áudio</span><span class="sxs-lookup"><span data-stu-id="42d3e-103">Audio Clip Sample</span></span>

<span data-ttu-id="42d3e-104">Mostra como usar Microsoft Media Foundation para decodificar áudio de um arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="42d3e-104">Shows how to use Microsoft Media Foundation to decode audio from a media file.</span></span>

<span data-ttu-id="42d3e-105">O aplicativo de exemplo clipe de áudio lê dados de áudio de um arquivo de mídia e grava o áudio descompactado em um arquivo WAVE.</span><span class="sxs-lookup"><span data-stu-id="42d3e-105">The Audio Clip sample application reads audio data from a media file and writes the uncompressed audio to a WAVE file.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="42d3e-106">APIs demonstradas</span><span class="sxs-lookup"><span data-stu-id="42d3e-106">APIs Demonstrated</span></span>

<span data-ttu-id="42d3e-107">Este exemplo demonstra as seguintes interfaces de Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="42d3e-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="42d3e-108">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="42d3e-108">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)

## <a name="usage"></a><span data-ttu-id="42d3e-109">Uso</span><span class="sxs-lookup"><span data-stu-id="42d3e-109">Usage</span></span>

<span data-ttu-id="42d3e-110">Este exemplo é um aplicativo de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="42d3e-110">This sample is a command-line application.</span></span> <span data-ttu-id="42d3e-111">Ele usa os seguintes argumentos de linha de comando:</span><span class="sxs-lookup"><span data-stu-id="42d3e-111">It uses the following command-line arguments:</span></span>

``` syntax
audioclip.exe inputfile outputfile.wav
```

-   <span data-ttu-id="42d3e-112">arquivo_de_entrada: o nome de um arquivo que contém um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="42d3e-112">inputfile: The name of a file that contains an audio stream.</span></span>
-   <span data-ttu-id="42d3e-113">arquivo_de_saída. wav: o nome do arquivo de som WAVE a ser gravado.</span><span class="sxs-lookup"><span data-stu-id="42d3e-113">outputfile.wav: The name of the WAVE file to write.</span></span>

## <a name="requirements"></a><span data-ttu-id="42d3e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42d3e-114">Requirements</span></span>



| <span data-ttu-id="42d3e-115">Produto</span><span class="sxs-lookup"><span data-stu-id="42d3e-115">Product</span></span>                                                        | <span data-ttu-id="42d3e-116">Versão</span><span class="sxs-lookup"><span data-stu-id="42d3e-116">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="42d3e-117">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="42d3e-117">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="42d3e-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="42d3e-118">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="42d3e-119">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="42d3e-119">Downloading the Sample</span></span>

<span data-ttu-id="42d3e-120">Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span><span class="sxs-lookup"><span data-stu-id="42d3e-120">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span></span>

## <a name="related-topics"></a><span data-ttu-id="42d3e-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="42d3e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42d3e-122">Exemplos de SDK do Media Foundation</span><span class="sxs-lookup"><span data-stu-id="42d3e-122">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="42d3e-123">Leitor de origem</span><span class="sxs-lookup"><span data-stu-id="42d3e-123">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="42d3e-124">Tutorial: decodificando áudio</span><span class="sxs-lookup"><span data-stu-id="42d3e-124">Tutorial: Decoding Audio</span></span>](tutorial--decoding-audio.md)
</dt> </dl>

 

 



