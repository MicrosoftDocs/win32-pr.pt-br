---
description: Suporte a MPEG-2 no DirectShow
ms.assetid: a4fe4cc9-86a5-4c83-94be-8901b97c8280
title: Suporte a MPEG-2 no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f42b0d49159a28b3ad29a0141c296c0fd0076fdd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500586"
---
# <a name="mpeg-2-support-in-directshow"></a><span data-ttu-id="632ba-103">Suporte a MPEG-2 no DirectShow</span><span class="sxs-lookup"><span data-stu-id="632ba-103">MPEG-2 Support in DirectShow</span></span>

<span data-ttu-id="632ba-104">Esta seção descreve os componentes que você pode usar para reproduzir conteúdo MPEG-2 no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="632ba-104">This section describes the components that you can use to play MPEG-2 content in DirectShow.</span></span>

> [!Note]  
> <span data-ttu-id="632ba-105">Embora o vídeo de DVD seja baseado em MPEG-2, esta seção não descreve a reprodução ou a navegação em DVD.</span><span class="sxs-lookup"><span data-stu-id="632ba-105">Although DVD video is based on MPEG-2, this section does not describe DVD playback or navigation.</span></span> <span data-ttu-id="632ba-106">Para obter informações sobre o DVD no DirectShow, consulte [aplicativos de DVD](dvd-applications.md).</span><span class="sxs-lookup"><span data-stu-id="632ba-106">For information about DVD in DirectShow, see [DVD Applications](dvd-applications.md).</span></span>

 

<span data-ttu-id="632ba-107">Os dados MPEG-2 podem vir de um arquivo local ou de uma fonte dinâmica, como uma difusão de rede ou um dispositivo D-VHS.</span><span class="sxs-lookup"><span data-stu-id="632ba-107">MPEG-2 data can come from a local file, or from a live source, such as a network broadcast or D-VHS device.</span></span> <span data-ttu-id="632ba-108">A reprodução de arquivo é chamada de *modo de pull* porque o filtro do analisador efetua pull de dados do arquivo para o grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="632ba-108">File playback is called *pull mode* because the parser filter pulls data from the file into the filter graph.</span></span> <span data-ttu-id="632ba-109">As fontes dinâmicas são chamadas de *modo de push* porque o filtro de origem envia dados por push para o grafo.</span><span class="sxs-lookup"><span data-stu-id="632ba-109">Live sources are called *push mode* because the source filter pushes data into the graph.</span></span>

<span data-ttu-id="632ba-110">O DirectShow fornece dois filtros que podem analisar fluxos de sistema MPEG-2:</span><span class="sxs-lookup"><span data-stu-id="632ba-110">DirectShow provides two filters that can parse MPEG-2 system streams:</span></span>

-   <span data-ttu-id="632ba-111">[Demultiplexador MPEG-2](mpeg-2-demultiplexer.md) ("Demux"): esse filtro dá suporte ao modo de push para fluxos de programa e fluxos de transporte.</span><span class="sxs-lookup"><span data-stu-id="632ba-111">[MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux"): This filter supports push mode for program streams and transport streams.</span></span> <span data-ttu-id="632ba-112">No Windows XP e posterior, ele também dá suporte ao modo de pull para fluxos de programa.</span><span class="sxs-lookup"><span data-stu-id="632ba-112">In Windows XP and later, it also supports pull mode for program streams.</span></span>
-   <span data-ttu-id="632ba-113">[Divisor MPEG-2](mpeg-2-splitter.md): esse filtro dá suporte ao modo de pull para fluxos de programa em plataformas de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="632ba-113">[MPEG-2 Splitter](mpeg-2-splitter.md): This filter supports pull mode for program streams on downlevel platforms.</span></span> <span data-ttu-id="632ba-114">Esse filtro foi preterido no Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="632ba-114">This filter is deprecated in Windows XP and later.</span></span>

<span data-ttu-id="632ba-115">Para usar o divisor MPEG-2 Demux ou MPEG-2, você deve ter decodificadores de áudio e vídeo MPEG-2 compatíveis com DirectShow que aceitem PES (fluxos elementares) em pacotes.</span><span class="sxs-lookup"><span data-stu-id="632ba-115">To use the MPEG-2 demux or MPEG-2 splitter, you must have DirectShow-compatible MPEG-2 audio and video decoders that accept packetized elementary streams (PES).</span></span>

<span data-ttu-id="632ba-116">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="632ba-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="632ba-117">Visão geral dos sistemas MPEG-2</span><span class="sxs-lookup"><span data-stu-id="632ba-117">Overview of MPEG-2 Systems</span></span>](overview-of-mpeg-2-systems.md)
-   [<span data-ttu-id="632ba-118">Usando o demultiplexador MPEG-2</span><span class="sxs-lookup"><span data-stu-id="632ba-118">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
-   [<span data-ttu-id="632ba-119">Usando o divisor MPEG-2</span><span class="sxs-lookup"><span data-stu-id="632ba-119">Using the MPEG-2 Splitter</span></span>](using-the-mpeg-2-splitter.md)
-   [<span data-ttu-id="632ba-120">Propriedades de exemplo de MPEG</span><span class="sxs-lookup"><span data-stu-id="632ba-120">MPEG Sample Properties</span></span>](mpeg-sample-properties.md)

## <a name="related-topics"></a><span data-ttu-id="632ba-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="632ba-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="632ba-122">Exemplo de filtro do analisador PSI</span><span class="sxs-lookup"><span data-stu-id="632ba-122">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 



