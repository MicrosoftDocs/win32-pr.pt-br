---
description: Codificação
ms.assetid: 501e63bf-26ef-42fb-b181-f1a8b26c122c
title: Codificação (Windows Imaging Component)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6d15b983b7455d0fe0c406cbad64dbbb77588b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765046"
---
# <a name="encoding-windows-imaging-component"></a><span data-ttu-id="d6ff2-103">Codificação (Windows Imaging Component)</span><span class="sxs-lookup"><span data-stu-id="d6ff2-103">Encoding (Windows Imaging Component)</span></span>

<span data-ttu-id="d6ff2-104">O autor do codificador deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d6ff2-104">The encoder author must do the following:</span></span>

-   <span data-ttu-id="d6ff2-105">Implemente as interfaces [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) e [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="d6ff2-105">Implement [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) interfaces.</span></span>
-   <span data-ttu-id="d6ff2-106">Implemente [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) no codificador de quadros.</span><span class="sxs-lookup"><span data-stu-id="d6ff2-106">Implement [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) on the frame encoder.</span></span> <span data-ttu-id="d6ff2-107">Se o codec oferecer suporte a metadados em nível de contêiner, essa interface deverá ser implementada no codificador de nível de contêiner, bem como no codificador de quadros.</span><span class="sxs-lookup"><span data-stu-id="d6ff2-107">If the codec supports container-level metadata, this interface must be implemented on the container-level encoder as well as on the frame encoder.</span></span>
-   <span data-ttu-id="d6ff2-108">Se o formato do contêiner contiver implicitamente quaisquer blocos de metadados obrigatórios, crie uma instância de um gravador de metadados para cada bloco.</span><span class="sxs-lookup"><span data-stu-id="d6ff2-108">If the container format implicitly contains any mandatory metadata blocks, instantiate a metadata writer for each such block.</span></span> <span data-ttu-id="d6ff2-109">Por exemplo, o formato TIFF requer um dispositivo de interface (IFD) para cada quadro, de modo que o gravador IFD sempre deve ser exposto.</span><span class="sxs-lookup"><span data-stu-id="d6ff2-109">For example, the TIFF format requires an interface device (IFD) for each frame, so the IFD writer must always be exposed.</span></span>
-   <span data-ttu-id="d6ff2-110">Implemente o suporte para gerenciar a coleção de gravadores de metadados.</span><span class="sxs-lookup"><span data-stu-id="d6ff2-110">Implement support for managing the collection of metadata writers.</span></span> <span data-ttu-id="d6ff2-111">O gravador de bloco gerencia quaisquer requisitos de pedido ou restrições de contêiner nos tipos de blocos de metadados que podem ser codificados.</span><span class="sxs-lookup"><span data-stu-id="d6ff2-111">The block writer manages any order requirements or container restrictions on the kinds of metadata blocks that can be encoded.</span></span> <span data-ttu-id="d6ff2-112">O gravador de bloco deve verificar se os novos gravadores de metadados podem ser inseridos dentro do formato de contêiner.</span><span class="sxs-lookup"><span data-stu-id="d6ff2-112">The block writer must verify that any new metadata writers can be embedded within the container format.</span></span>
-   <span data-ttu-id="d6ff2-113">Ao codificar o fluxo de imagem, chame [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) para serializar o conteúdo de cada gravador de metadados no fluxo.</span><span class="sxs-lookup"><span data-stu-id="d6ff2-113">When encoding the image stream, call [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) to serialize each metadata writer’s content into the stream.</span></span> <span data-ttu-id="d6ff2-114">Se o bloco de metadados contiver metadados "críticos", o codificador deverá definir os itens de metadados críticos antes de solicitar que o gravador de metadados Serialize o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d6ff2-114">If the metadata block contains "critical" metadata the encoder must set the critical metadata items before asking the metadata writer to serialize content.</span></span>
-   <span data-ttu-id="d6ff2-115">Verifique se há manipuladores de metadados desconhecidos para garantir que os blocos de metadados redundantes não estejam presentes.</span><span class="sxs-lookup"><span data-stu-id="d6ff2-115">Check for any unknown metadata handlers to ensure that redundant metadata blocks are not present.</span></span> <span data-ttu-id="d6ff2-116">Isso é importante porque, enquanto preserva os metadados em um cenário de decodificação ou codificação, os blocos desconhecidos podem ser uma duplicata de blocos de metadados obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="d6ff2-116">This is important because, while preserving metadata in a decode or encode scenario, unknown blocks might be a duplicate of mandatory metadata blocks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6ff2-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6ff2-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d6ff2-118">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="d6ff2-118">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d6ff2-119">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="d6ff2-119">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="d6ff2-120">Diretrizes do WIC para formatos de imagem bruta de câmera</span><span class="sxs-lookup"><span data-stu-id="d6ff2-120">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="d6ff2-121">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="d6ff2-121">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



