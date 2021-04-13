---
description: O gravador do coletor é um componente para codificar arquivos de áudio ou de vídeo.
ms.assetid: 23AF25B8-B94C-48BC-83D8-5863ACFFD4CA
title: Gravador do coletor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b30d75e369de343bae61ba56dfd05c0d5d12a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296526"
---
# <a name="sink-writer"></a><span data-ttu-id="3e76e-103">Gravador do coletor</span><span class="sxs-lookup"><span data-stu-id="3e76e-103">Sink Writer</span></span>

<span data-ttu-id="3e76e-104">O gravador do coletor é um componente para codificar arquivos de áudio ou de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3e76e-104">The sink writer is a component for encoding audio or video files.</span></span>

<span data-ttu-id="3e76e-105">O diagrama a seguir mostra, em um alto nível, como um aplicativo usa o gravador de coletor para codificar e áudio/vídeo.</span><span class="sxs-lookup"><span data-stu-id="3e76e-105">The following diagram shows, at a high level, how an application uses the sink writer to encode and audio/video file.</span></span>

![um diagrama que mostra o gravador do coletor.](images/encoding09.png)

<span data-ttu-id="3e76e-107">O gravador de coletor hospeda um coletor de mídia e, opcionalmente, um ou mais codificadores.</span><span class="sxs-lookup"><span data-stu-id="3e76e-107">The sink writer hosts a media sink and optionally one or more encoders.</span></span> <span data-ttu-id="3e76e-108">Os codificadores convertem dados não compactados de áudio ou vídeo em fragmentado codificados.</span><span class="sxs-lookup"><span data-stu-id="3e76e-108">The encoders convert uncompressed audio or video data to encoded bitstreams.</span></span> <span data-ttu-id="3e76e-109">O coletor de mídia gera o fragmentado para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="3e76e-109">The media sink outputs the bitstreams to a file.</span></span> <span data-ttu-id="3e76e-110">O gravador do coletor executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="3e76e-110">The sink writer performs the following tasks:</span></span>

-   <span data-ttu-id="3e76e-111">Carrega o coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="3e76e-111">Loads the media sink.</span></span>
-   <span data-ttu-id="3e76e-112">Localiza e carrega os codificadores.</span><span class="sxs-lookup"><span data-stu-id="3e76e-112">Finds and loads the encoders.</span></span>
-   <span data-ttu-id="3e76e-113">Gerencia o fluxo de dados para os codificadores e o coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="3e76e-113">Manages the data flow to the encoders and the media sink.</span></span>

<span data-ttu-id="3e76e-114">O aplicativo passa dados de áudio/vídeo para o gravador de coletor como entrada.</span><span class="sxs-lookup"><span data-stu-id="3e76e-114">The application passes audio/video data to the sink writer as input.</span></span> <span data-ttu-id="3e76e-115">Não importa como o aplicativo obtém ou gera os dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="3e76e-115">It does not matter how the application obtains or generates the input data.</span></span> <span data-ttu-id="3e76e-116">Uma opção é usar o [leitor de origem](source-reader.md), conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="3e76e-116">One option is to use the [Source Reader](source-reader.md), as shown in the following diagram.</span></span> <span data-ttu-id="3e76e-117">No entanto, o gravador de coletor não requer o uso do leitor de origem.</span><span class="sxs-lookup"><span data-stu-id="3e76e-117">However, the sink writer does not require the use of the source reader.</span></span> <span data-ttu-id="3e76e-118">Esses dois componentes são independentes.</span><span class="sxs-lookup"><span data-stu-id="3e76e-118">These two components are independent.</span></span>

![um diagrama que mostra o leitor de origem e o gravador de coletor.](images/encoding02.png)

## <a name="in-this-section"></a><span data-ttu-id="3e76e-120">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="3e76e-120">In this section</span></span>

-   [<span data-ttu-id="3e76e-121">Usando o gravador do coletor</span><span class="sxs-lookup"><span data-stu-id="3e76e-121">Using the Sink Writer</span></span>](using-the-sink-writer.md)
-   [<span data-ttu-id="3e76e-122">Tutorial: usando o gravador de coletor para codificar vídeo</span><span class="sxs-lookup"><span data-stu-id="3e76e-122">Tutorial: Using the Sink Writer to Encode Video</span></span>](tutorial--using-the-sink-writer-to-encode-video.md)

## <a name="related-topics"></a><span data-ttu-id="3e76e-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e76e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e76e-124">Codificando e criando arquivos</span><span class="sxs-lookup"><span data-stu-id="3e76e-124">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="3e76e-125">Visão geral da codificação no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3e76e-125">Overview of Encoding in Media Foundation</span></span>](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 



