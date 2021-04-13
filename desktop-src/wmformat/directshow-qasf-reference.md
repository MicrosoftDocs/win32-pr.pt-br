---
title: Referência do QASF do DirectShow
description: Referência do QASF do DirectShow
ms.assetid: 66f483b5-3886-48b4-bc43-7c3517abd20d
keywords:
- SDK do Windows Media Format, QASF
- SDK do Windows Media Format, DirectShow
- DirectShow, referência de QASF
- Filtros QASF, referência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c509030f676b83a84f67590a242aea623656a514
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366333"
---
# <a name="directshow-qasf-reference"></a><span data-ttu-id="ae785-107">Referência do QASF do DirectShow</span><span class="sxs-lookup"><span data-stu-id="ae785-107">DirectShow QASF Reference</span></span>

<span data-ttu-id="ae785-108">Esta seção contém referências de programação para os seguintes filtros, interfaces e enumerações do QASF do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ae785-108">This section contains programming references for the following DirectShow QASF filters, interfaces and enumerations.</span></span> <span data-ttu-id="ae785-109">A documentação do SDK do DirectShow contém materiais de referência e de guia de programação para interfaces genéricas adicionais expostas por esses filtros, como **IBaseFilter** e **IPin**, e para versões anteriores dos componentes do QASF.</span><span class="sxs-lookup"><span data-stu-id="ae785-109">The DirectShow SDK documentation contains reference and programming guide materials for additional generic interfaces exposed by these filters, such as **IBaseFilter** and **IPin**, and for earlier versions of the QASF components.</span></span>

<span data-ttu-id="ae785-110">Para obter uma explicação do nome do QASF, consulte [sobre o DirectShow](about-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="ae785-110">For an explanation of the QASF name, see [About DirectShow](about-directshow.md).</span></span>

<span data-ttu-id="ae785-111">Os filtros a seguir estão incluídos nos componentes do QASF do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ae785-111">The following filters are included with the DirectShow QASF components.</span></span>



| <span data-ttu-id="ae785-112">Filtrar</span><span class="sxs-lookup"><span data-stu-id="ae785-112">Filter</span></span>                                           | <span data-ttu-id="ae785-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae785-113">Description</span></span>                                                      |
|--------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="ae785-114">Filtro de leitor ASF do WM</span><span class="sxs-lookup"><span data-stu-id="ae785-114">WM ASF Reader Filter</span></span>](wm-asf-reader-filter.md) | <span data-ttu-id="ae785-115">Lê e analisa arquivos ASF locais ou remotos.</span><span class="sxs-lookup"><span data-stu-id="ae785-115">Reads and parses local or remote ASF files.</span></span>                      |
| [<span data-ttu-id="ae785-116">Filtro de gravador ASF do WM</span><span class="sxs-lookup"><span data-stu-id="ae785-116">WM ASF Writer Filter</span></span>](wm-asf-writer-filter.md) | <span data-ttu-id="ae785-117">Cria arquivos ASF a partir de fluxos de entrada compactados ou não compactados.</span><span class="sxs-lookup"><span data-stu-id="ae785-117">Creates ASF files from compressed or uncompressed input streams.</span></span> |



 

<span data-ttu-id="ae785-118">As interfaces a seguir são definidas para uso com os componentes do QASF do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ae785-118">The following interfaces are defined for use with the DirectShow QASF components.</span></span>



| <span data-ttu-id="ae785-119">Interface</span><span class="sxs-lookup"><span data-stu-id="ae785-119">Interface</span></span>                                                  | <span data-ttu-id="ae785-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae785-120">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae785-121">**IAMWMBufferPass**</span><span class="sxs-lookup"><span data-stu-id="ae785-121">**IAMWMBufferPass**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)                 | <span data-ttu-id="ae785-122">Fornece um método que permite que os aplicativos se registrem para retornos de chamada dos Pins de entrada do [gravador ASF do WM](wm-asf-writer-filter.md) ou dos Pins de saída do filtro de [leitor ASF do WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="ae785-122">Provides a method that enables applications to register for callbacks from the input pins of the [WM ASF Writer](wm-asf-writer-filter.md) or the output pins of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="ae785-123">Usado na indexação e ao adicionar extensões de unidade de dados.</span><span class="sxs-lookup"><span data-stu-id="ae785-123">Used in indexing and when adding data unit extensions.</span></span> |
| [<span data-ttu-id="ae785-124">**IAMWMBufferPassCallback**</span><span class="sxs-lookup"><span data-stu-id="ae785-124">**IAMWMBufferPassCallback**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) | <span data-ttu-id="ae785-125">Implementado por aplicativos e chamados pelos filtros.</span><span class="sxs-lookup"><span data-stu-id="ae785-125">Implemented by applications and called by the filters.</span></span> <span data-ttu-id="ae785-126">Os aplicativos usam o método One nessa interface para obter informações sobre exemplos individuais no fluxo.</span><span class="sxs-lookup"><span data-stu-id="ae785-126">Applications use the one method on this interface to obtain information about individual samples in the stream.</span></span> <span data-ttu-id="ae785-127">Usado na indexação e ao adicionar extensões de unidade de dados.</span><span class="sxs-lookup"><span data-stu-id="ae785-127">Used in indexing and when adding data unit extensions.</span></span>                                                 |
| <span data-ttu-id="ae785-128">[**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ae785-128">[**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>               | <span data-ttu-id="ae785-129">Implementado no gravador ASF do WM.</span><span class="sxs-lookup"><span data-stu-id="ae785-129">Implemented on the WM ASF Writer.</span></span> <span data-ttu-id="ae785-130">Usado por aplicativos para especificar perfis e parâmetros de indexação para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="ae785-130">Used by applications to specify profiles and indexing parameters for the file.</span></span>                                                                                                                                                              |
| <span data-ttu-id="ae785-131">[**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ae785-131">[**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>             | <span data-ttu-id="ae785-132">Fornece funções de configuração adicionais no gravador ASF do WM.</span><span class="sxs-lookup"><span data-stu-id="ae785-132">Provides additional configuration functions on the WM ASF Writer.</span></span>                                                                                                                                                                                                             |



 

<span data-ttu-id="ae785-133">A enumeração, a estrutura e os eventos a seguir são definidos para uso com os componentes do QASF do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ae785-133">The following enumeration, structure, and events are defined for use with the DirectShow QASF components.</span></span>



| <span data-ttu-id="ae785-134">Enumeração</span><span class="sxs-lookup"><span data-stu-id="ae785-134">Enumeration</span></span>                                                               | <span data-ttu-id="ae785-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae785-135">Description</span></span>                                                                                                                                                                       |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae785-136">[\_\_parâmetro am ASFWRITERCONFIG \_](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ae785-136">[\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))</span></span> | <span data-ttu-id="ae785-137">Define os parâmetros de configuração de filtro usados nos métodos [**IConfigAsfWriter2:: GetParam**](iconfigasfwriter2-getparam.md) e [**SetParam**](iconfigasfwriter2-setparam.md) .</span><span class="sxs-lookup"><span data-stu-id="ae785-137">Defines filter configuration parameters used in the [**IConfigAsfWriter2::GetParam**](iconfigasfwriter2-getparam.md) and [**SetParam**](iconfigasfwriter2-setparam.md) methods.</span></span> |



 



| <span data-ttu-id="ae785-138">Estrutura</span><span class="sxs-lookup"><span data-stu-id="ae785-138">Structure</span></span>                                         | <span data-ttu-id="ae785-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae785-139">Description</span></span>                                                                                                                                           |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae785-140">**\_dados de \_ evento am WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ae785-140">**AM\_WMT\_EVENT\_DATA**</span></span>](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) | <span data-ttu-id="ae785-141">Contém informações referentes a um evento de [**\_ status WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) e o código de status associado retornado pelo Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="ae785-141">Contains information pertaining to a [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) event and the associated status code returned by the Windows Media Format SDK.</span></span> |



 



| <span data-ttu-id="ae785-142">Evento</span><span class="sxs-lookup"><span data-stu-id="ae785-142">Event</span></span>                                           | <span data-ttu-id="ae785-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae785-143">Description</span></span>                                                                                                     |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae785-144">\_evento de WMT do EC \_</span><span class="sxs-lookup"><span data-stu-id="ae785-144">EC\_WMT\_EVENT</span></span>](ec-wmt-event.md)              | <span data-ttu-id="ae785-145">Evento encaminhado do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="ae785-145">Event forwarded from the Windows Media Format SDK.</span></span>                                                              |
| [<span data-ttu-id="ae785-146">evento de índice do EC \_ WMT \_ \_</span><span class="sxs-lookup"><span data-stu-id="ae785-146">EC\_WMT\_INDEX\_EVENT</span></span>](ec-wmt-index-event.md) | <span data-ttu-id="ae785-147">Enviado quando um aplicativo usa o [gravador ASF do WM](wm-asf-writer-filter.md) para indexar arquivos de vídeo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ae785-147">Sent when an application uses the [WM ASF Writer](wm-asf-writer-filter.md) to index Windows Media Video files.</span></span> |



 

 

 