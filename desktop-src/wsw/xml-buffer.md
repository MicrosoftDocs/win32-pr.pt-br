---
title: Buffer XML
description: Um buffer XML fornece armazenamento eficiente na memória para dados XML arbitrários.
ms.assetid: e379628b-c6f8-48b1-8109-59fb604f2bcb
keywords:
- Serviços Web de buffer XML para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab71121dc451c9ccb186c754d537836f9e899fa9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917796"
---
# <a name="xml-buffer"></a><span data-ttu-id="15c65-106">Buffer XML</span><span class="sxs-lookup"><span data-stu-id="15c65-106">XML Buffer</span></span>

<span data-ttu-id="15c65-107">Um buffer XML fornece armazenamento eficiente na memória para dados XML arbitrários.</span><span class="sxs-lookup"><span data-stu-id="15c65-107">An XML Buffer provides efficient in-memory storage for arbitrary XML data.</span></span>


<span data-ttu-id="15c65-108">Para ler dados de um buffer XML, use um [leitor de XML](xml-reader.md) e chame [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) com o buffer XML.</span><span class="sxs-lookup"><span data-stu-id="15c65-108">To read data from an XML Buffer, use a [XML Reader](xml-reader.md) and call [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) with the XML Buffer.</span></span> <span data-ttu-id="15c65-109">O leitor será posicionado no início do documento.</span><span class="sxs-lookup"><span data-stu-id="15c65-109">The reader will be positioned at the start of the document.</span></span>

<span data-ttu-id="15c65-110">Para inserir dados em um buffer, use um [gravador de XML](xml-writer.md) e chame [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) com o buffer XML.</span><span class="sxs-lookup"><span data-stu-id="15c65-110">To insert data into a buffer, use a [XML Writer](xml-writer.md) and call [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) with the XML Buffer.</span></span> <span data-ttu-id="15c65-111">O gravador será posicionado no final do documento.</span><span class="sxs-lookup"><span data-stu-id="15c65-111">The writer will be positioned at the end of the document.</span></span>

<span data-ttu-id="15c65-112">Depois que um leitor tiver sido definido como um buffer XML, além de todas as APIs do leitor XML, [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) poderá ser usado para navegar pelo leitor pelo documento.</span><span class="sxs-lookup"><span data-stu-id="15c65-112">Once a reader has been set to an XML Buffer, in addition to all of the XML Reader APIs, [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) may be used to navigate the reader through the document.</span></span> <span data-ttu-id="15c65-113">[**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) e [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) também podem ser usados para registrar uma posição no documento e retornar a ela mais tarde.</span><span class="sxs-lookup"><span data-stu-id="15c65-113">[**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) and [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) may also be used to record a position in the document and return to it later.</span></span>

<span data-ttu-id="15c65-114">Depois que um gravador tiver sido definido como um buffer XML, além de todas as APIs do gravador de XML, [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) poderá ser usado para navegar pelo gravador por meio do documento.</span><span class="sxs-lookup"><span data-stu-id="15c65-114">Once a writer has been set to an XML Buffer, in addition to all of the XML Writer APIs, [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) may be used to navigate the writer through the document.</span></span> <span data-ttu-id="15c65-115">[**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) e [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) também podem ser usados para registrar uma posição no documento e retornar a ela mais tarde.</span><span class="sxs-lookup"><span data-stu-id="15c65-115">[**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) and [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) may also be used to record a position in the document and return to it later.</span></span> <span data-ttu-id="15c65-116">O gravador sempre insere dados antes do nó no qual ele está posicionado.</span><span class="sxs-lookup"><span data-stu-id="15c65-116">The writer always inserts data before the node to which it is positioned.</span></span>

<span data-ttu-id="15c65-117">Os nós podem ser excluídos do buffer XML obtendo a posição do nó usando [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) ou [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) e, em seguida, chamando [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) com essa posição.</span><span class="sxs-lookup"><span data-stu-id="15c65-117">Nodes may be deleted from the XML Buffer by obtaining the position of the node using [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) or [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) and then calling [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) with that position.</span></span> <span data-ttu-id="15c65-118">Para elementos, isso excluirá o elemento, todos os seus filhos, incluindo seu elemento final correspondente.</span><span class="sxs-lookup"><span data-stu-id="15c65-118">For elements, this will delete the element, all its children including its matching end element.</span></span>

<span data-ttu-id="15c65-119">Uma posição é representada pelo valor [**posição do \_ \_ nó WS \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position).</span><span class="sxs-lookup"><span data-stu-id="15c65-119">A position is represented by the value [**WS\_XML\_NODE\_POSITION**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position).</span></span> <span data-ttu-id="15c65-120">As posições são específicas para um buffer XML específico e só são válidas desde que o buffer XML seja válido.</span><span class="sxs-lookup"><span data-stu-id="15c65-120">Positions are specific to a particular XML Buffer, and are only valid as long as the XML Buffer is valid.</span></span>

<span data-ttu-id="15c65-121">As seguintes enumerações são usadas com buffers XML:</span><span class="sxs-lookup"><span data-stu-id="15c65-121">The following enumerations are used with XML buffers:</span></span>

-   [<span data-ttu-id="15c65-122">**WS \_ mover \_ para**</span><span class="sxs-lookup"><span data-stu-id="15c65-122">**WS\_MOVE\_TO**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_move_to)
-   [<span data-ttu-id="15c65-123">**\_ID da \_ Propriedade do buffer XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="15c65-123">**WS\_XML\_BUFFER\_PROPERTY\_ID**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id)

<span data-ttu-id="15c65-124">As funções a seguir são usadas com buffers XML:</span><span class="sxs-lookup"><span data-stu-id="15c65-124">The following functions are used with XML buffers:</span></span>

-   [<span data-ttu-id="15c65-125">**WsCreateXmlBuffer**</span><span class="sxs-lookup"><span data-stu-id="15c65-125">**WsCreateXmlBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlbuffer)
-   [<span data-ttu-id="15c65-126">**WsRemoveNode**</span><span class="sxs-lookup"><span data-stu-id="15c65-126">**WsRemoveNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsremovenode)

<span data-ttu-id="15c65-127">O seguinte identificador é usado com buffers XML:</span><span class="sxs-lookup"><span data-stu-id="15c65-127">The following handle is used with XML buffers:</span></span>

-   [<span data-ttu-id="15c65-128">\_buffer XML do WS \_</span><span class="sxs-lookup"><span data-stu-id="15c65-128">WS\_XML\_BUFFER</span></span>](ws-xml-buffer.md)

<span data-ttu-id="15c65-129">As seguintes estruturas são usadas com buffers XML:</span><span class="sxs-lookup"><span data-stu-id="15c65-129">The following structures are used with XML buffers:</span></span>

-   [<span data-ttu-id="15c65-130">**\_propriedade de \_ buffer \_ XML do WS**</span><span class="sxs-lookup"><span data-stu-id="15c65-130">**WS\_XML\_BUFFER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_buffer_property)
-   [<span data-ttu-id="15c65-131">**\_posição do \_ nó \_ XML do WS**</span><span class="sxs-lookup"><span data-stu-id="15c65-131">**WS\_XML\_NODE\_POSITION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)

 

 




