---
description: Sobre o filtro de leitor ASF do WM
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: Sobre o filtro de leitor ASF do WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350e6597aa6aa66193af37a30ed54c37139d5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825937"
---
# <a name="about-the-wm-asf-reader-filter"></a><span data-ttu-id="64667-103">Sobre o filtro de leitor ASF do WM</span><span class="sxs-lookup"><span data-stu-id="64667-103">About the WM ASF Reader Filter</span></span>

<span data-ttu-id="64667-104">A reprodução de arquivos ASF é tratada pelo filtro de [leitor ASF do WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="64667-104">Playback of ASF files is handled by the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="64667-105">Quando o leitor ASF do WM lê um arquivo, ele cria automaticamente um PIN de saída para cada fluxo, incluindo fluxos da Web, fluxos de comando de script e qualquer outro tipo de fluxo arbitrário.</span><span class="sxs-lookup"><span data-stu-id="64667-105">When the WM ASF Reader reads a file, it automatically creates an output pin for each stream, including web streams, script command streams, and any other type of arbitrary stream.</span></span> <span data-ttu-id="64667-106">No caso de vários arquivos de taxa de bits, os Pins são criados somente para os fluxos selecionados no momento.</span><span class="sxs-lookup"><span data-stu-id="64667-106">In the case of multiple bit rate files, pins are created only for the currently selected streams.</span></span> <span data-ttu-id="64667-107">Para reproduzir um arquivo ASF com o filtro de leitor ASF do WM, chame [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) ou [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span><span class="sxs-lookup"><span data-stu-id="64667-107">To play an ASF file with the WM ASF Reader filter, call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span></span>

<span data-ttu-id="64667-108">O leitor ASF do WM dá suporte à interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) do DirectShow, que permite que os aplicativos executem a busca temporal dentro do arquivo.</span><span class="sxs-lookup"><span data-stu-id="64667-108">The WM ASF Reader supports the DirectShow [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, which enables applications to perform temporal seeking within the file.</span></span> <span data-ttu-id="64667-109">No entanto, a reprodução em velocidades diferentes de 1,0 (conforme especificado em [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)) não é suportada.</span><span class="sxs-lookup"><span data-stu-id="64667-109">However, playback at speeds other than 1.0 (as specified in [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)) is not supported.</span></span>

<span data-ttu-id="64667-110">O filtro de leitor ASF do WM também expõe várias interfaces SDK do Windows Media Format, conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="64667-110">The WM ASF Reader filter also exposes several Windows Media Format SDK interfaces as described in the following table.</span></span> <span data-ttu-id="64667-111">Essas interfaces estão documentadas na documentação do Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="64667-111">These interfaces are documented in the Windows Media Format SDK documentation.</span></span>



| <span data-ttu-id="64667-112">Interface</span><span class="sxs-lookup"><span data-stu-id="64667-112">Interface</span></span>                                             | <span data-ttu-id="64667-113">Quão expostos</span><span class="sxs-lookup"><span data-stu-id="64667-113">How exposed</span></span>                                 | <span data-ttu-id="64667-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="64667-114">Comments</span></span>                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64667-115">**IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="64667-115">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | <span data-ttu-id="64667-116">Por meio de **IServiceProvider** no filtro.</span><span class="sxs-lookup"><span data-stu-id="64667-116">Through **IServiceProvider** on the filter.</span></span> | <span data-ttu-id="64667-117">Fornecido para aplicativos que precisam reproduzir conteúdo protegido por DRM (Rights Management digital).</span><span class="sxs-lookup"><span data-stu-id="64667-117">Provided for applications that need to play content protected by Digital Rights Management (DRM)..</span></span>                             |
| [<span data-ttu-id="64667-118">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="64667-118">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="64667-119">**QueryInterface** no filtro.</span><span class="sxs-lookup"><span data-stu-id="64667-119">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="64667-120">Fornecido para que os aplicativos possam ler atributos de arquivo e conteúdo, bem como informações de marcador e script e metadados.</span><span class="sxs-lookup"><span data-stu-id="64667-120">Provided so that applications can read file and content attributes, as well as marker and script information and metadata.</span></span>     |
| [<span data-ttu-id="64667-121">**IWMReaderAdvanced**</span><span class="sxs-lookup"><span data-stu-id="64667-121">**IWMReaderAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | <span data-ttu-id="64667-122">**QueryInterface** no filtro.</span><span class="sxs-lookup"><span data-stu-id="64667-122">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="64667-123">Parcialmente implementado no filtro para que os aplicativos possam acessar os métodos informativos no objeto do WM Reader.</span><span class="sxs-lookup"><span data-stu-id="64667-123">Partially implemented on the filter so that applications can access the informational methods on the WM Reader object.</span></span>         |
| [<span data-ttu-id="64667-124">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="64667-124">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | <span data-ttu-id="64667-125">**QueryInterface** no filtro.</span><span class="sxs-lookup"><span data-stu-id="64667-125">**QueryInterface** on the filter.</span></span>           | <span data-ttu-id="64667-126">Parcialmente implementado no filtro para que os aplicativos possam acessar os métodos informativos no formato do objeto leitor SDK.</span><span class="sxs-lookup"><span data-stu-id="64667-126">Partially implemented on the filter so that applications can access the informational methods on the Format SDK Reader Object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="64667-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="64667-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64667-128">Lendo arquivos ASF no DirectShow</span><span class="sxs-lookup"><span data-stu-id="64667-128">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



