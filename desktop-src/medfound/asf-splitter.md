---
description: Divisor de ASF
ms.assetid: 383b1cc6-4a77-4e0e-a766-6213c64b025c
title: Divisor de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f61bcd17a81197106d2f7c43fa1fdc25d9da2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089798"
---
# <a name="asf-splitter"></a><span data-ttu-id="d8f8c-103">Divisor de ASF</span><span class="sxs-lookup"><span data-stu-id="d8f8c-103">ASF Splitter</span></span>

<span data-ttu-id="d8f8c-104">O objeto *divisor* de ASF é um componente de camada WMContainer que analisa o objeto de dados ASF de um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="d8f8c-104">The ASF *splitter* object is a WMContainer layer component that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="d8f8c-105">Você pode usar o divisor para ler os pacotes de dados no objeto de dados e gerar amostras de fluxo.</span><span class="sxs-lookup"><span data-stu-id="d8f8c-105">You can use the splitter to read the data packets in the Data Object and generate stream samples.</span></span> <span data-ttu-id="d8f8c-106">Para obter informações sobre a estrutura de um arquivo ASF, consulte [estrutura de arquivo ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="d8f8c-106">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="d8f8c-107">O divisor expõe a interface [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="d8f8c-107">The splitter exposes the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span> <span data-ttu-id="d8f8c-108">O divisor analisa os pacotes de dados ASF para os fluxos selecionados e os reempacota em objetos de exemplo individuais que expõem a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .</span><span class="sxs-lookup"><span data-stu-id="d8f8c-108">The splitter parses ASF data packets for the selected streams and repackages them into individual sample objects that expose the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span> <span data-ttu-id="d8f8c-109">O divisor é um dos componentes de nível de plataforma do Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d8f8c-109">The splitter is one of the platform-level components of Media Foundation.</span></span> <span data-ttu-id="d8f8c-110">A fonte de mídia do ASF usa o divisor internamente para analisar arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="d8f8c-110">The ASF media source uses the splitter internally to parse ASF files.</span></span>

<span data-ttu-id="d8f8c-111">O diagrama a seguir ilustra a geração de amostra para um arquivo ASF por meio do divisor.</span><span class="sxs-lookup"><span data-stu-id="d8f8c-111">The following diagram illustrates sample generation for an ASF file through the splitter.</span></span>

![diagrama mostrando a geração de exemplo de um arquivo ASF](images/1eb9789c-c586-4f44-b907-b086cf288cc1.gif)

<span data-ttu-id="d8f8c-113">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="d8f8c-113">This section contains the following topics:</span></span>



| <span data-ttu-id="d8f8c-114">Tópico</span><span class="sxs-lookup"><span data-stu-id="d8f8c-114">Topic</span></span>                                                                                                                        | <span data-ttu-id="d8f8c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8f8c-115">Description</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="d8f8c-116">Criando o objeto divisor de ASF</span><span class="sxs-lookup"><span data-stu-id="d8f8c-116">Creating the ASF Splitter Object</span></span>](creating-the-asf-splitter-object.md)                                                     | <span data-ttu-id="d8f8c-117">Como criar e inicializar o divisor.</span><span class="sxs-lookup"><span data-stu-id="d8f8c-117">How to create and initialize the splitter.</span></span>                              |
| [<span data-ttu-id="d8f8c-118">Configurando o objeto divisor de ASF</span><span class="sxs-lookup"><span data-stu-id="d8f8c-118">Configuring the ASF Splitter Object</span></span>](configuring-the-asf-splitter-object.md)                                               | <span data-ttu-id="d8f8c-119">Definições de configuração para o divisor.</span><span class="sxs-lookup"><span data-stu-id="d8f8c-119">Configuration settings for the splitter.</span></span>                                |
| [<span data-ttu-id="d8f8c-120">Gerando amostras de fluxo de um objeto de dados ASF existente</span><span class="sxs-lookup"><span data-stu-id="d8f8c-120">Generating Stream Samples from an Existing ASF Data Object</span></span>](generating-stream-samples-from-an-existing-asf-data-object.md) | <span data-ttu-id="d8f8c-121">Como analisar o objeto de dados ASF e gerar amostras de fluxo em pacotes.</span><span class="sxs-lookup"><span data-stu-id="d8f8c-121">How to parse the ASF Data Object and generate packetized steam samples.</span></span> |



 

<span data-ttu-id="d8f8c-122">A tabela a seguir mostra os atributos de objeto de dados relevantes.</span><span class="sxs-lookup"><span data-stu-id="d8f8c-122">The following table shows the relevant Data Object attributes.</span></span>



| <span data-ttu-id="d8f8c-123">Atributo</span><span class="sxs-lookup"><span data-stu-id="d8f8c-123">Attribute</span></span>                                                                                                    | <span data-ttu-id="d8f8c-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8f8c-124">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8f8c-125">**\_ \_ \_ pacotes FileProperties do MF PD ASF \_**</span><span class="sxs-lookup"><span data-stu-id="d8f8c-125">**MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS**</span></span>](mf-pd-asf-fileproperties-packets-attribute.md)                   | <span data-ttu-id="d8f8c-126">Número de pacotes de dados no objeto de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="d8f8c-126">Number of data packets in the ASF Data Object.</span></span>                                                       |
| [<span data-ttu-id="d8f8c-127">**\_tamanho de \_ \_ pacote FileProperties \_ min \_ do MF PD ASF \_**</span><span class="sxs-lookup"><span data-stu-id="d8f8c-127">**MF\_PD\_ASF\_FILEPROPERTIES\_MIN\_PACKET\_SIZE**</span></span>](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | <span data-ttu-id="d8f8c-128">Tamanho mínimo dos pacotes de dados no arquivo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="d8f8c-128">Minimum size of the data packets in the file, in bytes.</span></span>                                              |
| [<span data-ttu-id="d8f8c-129">**\_ \_ \_ \_ tamanho máximo do pacote FileProperties \_ do MF PD ASF \_**</span><span class="sxs-lookup"><span data-stu-id="d8f8c-129">**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_PACKET\_SIZE**</span></span>](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | <span data-ttu-id="d8f8c-130">Tamanho máximo dos pacotes de dados no arquivo, em bytes</span><span class="sxs-lookup"><span data-stu-id="d8f8c-130">Maximum size of the data packets in the file, in bytes</span></span>                                               |
| [<span data-ttu-id="d8f8c-131">**\_comprimento de \_ \_ dados ASF \_ do MF PD**</span><span class="sxs-lookup"><span data-stu-id="d8f8c-131">**MF\_PD\_ASF\_DATA\_LENGTH**</span></span>](mf-pd-asf-data-length-attribute.md)                                         | <span data-ttu-id="d8f8c-132">Tamanho do objeto de dados ASF, em bytes.</span><span class="sxs-lookup"><span data-stu-id="d8f8c-132">Size of the ASF Data Object, in bytes.</span></span>                                                               |
| [<span data-ttu-id="d8f8c-133">**deslocamento de início de dados do MF \_ PD \_ ASF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8f8c-133">**MF\_PD\_ASF\_DATA\_START\_OFFSET**</span></span>](mf-pd-asf-data-start-offset-attribute.md)                            | <span data-ttu-id="d8f8c-134">Deslocamento, em bytes, para o primeiro pacote de dados no objeto de dados ASF relativo ao início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d8f8c-134">Offset, in bytes, to the first data packet in the ASF Data Object relative to the start of the file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d8f8c-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d8f8c-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8f8c-136">Componentes ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="d8f8c-136">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="d8f8c-137">Tutorial: lendo um arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="d8f8c-137">Tutorial: Reading an ASF File</span></span>](tutorial--reading-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="d8f8c-138">Suporte a ASF no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d8f8c-138">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



