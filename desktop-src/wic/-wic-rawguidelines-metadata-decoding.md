---
description: Decodificação
ms.assetid: ff7e5e66-e1ea-49fc-909f-de361214afc3
title: Decodificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6700865d55ba7349447f5e41285d60446f0e4630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829489"
---
# <a name="decoding"></a><span data-ttu-id="25cbc-103">Decodificação</span><span class="sxs-lookup"><span data-stu-id="25cbc-103">Decoding</span></span>

<span data-ttu-id="25cbc-104">Para dar suporte adequado aos metadados, os autores de decodificador devem fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="25cbc-104">To properly support metadata, decoder authors must do the following:</span></span>

-   <span data-ttu-id="25cbc-105">Implemente as interfaces [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="25cbc-105">Implement [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interfaces.</span></span>
-   <span data-ttu-id="25cbc-106">Implemente o [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) no decodificador de quadro.</span><span class="sxs-lookup"><span data-stu-id="25cbc-106">Implement [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) on the frame decoder.</span></span> <span data-ttu-id="25cbc-107">Se o codec oferecer suporte a metadados em nível de contêiner, essa interface deverá ser implementada no decodificador de nível de contêiner, bem como no decodificador de quadro.</span><span class="sxs-lookup"><span data-stu-id="25cbc-107">If the codec supports container-level metadata, this interface must be implemented on the container-level decoder as well as on the frame decoder.</span></span>
-   <span data-ttu-id="25cbc-108">Ao decodificar o fluxo de imagem, chame [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) para instanciar um leitor de metadados para cada bloco de metadados.</span><span class="sxs-lookup"><span data-stu-id="25cbc-108">While decoding the image stream, call [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) to instantiate a metadata reader for each metadata block.</span></span> <span data-ttu-id="25cbc-109">(Quaisquer novos leitores de metadados implementados pelo codec devem ser registrados com o WIC.)</span><span class="sxs-lookup"><span data-stu-id="25cbc-109">(Any new metadata readers that the codec implements must be registered with WIC.)</span></span>

    <span data-ttu-id="25cbc-110">O decodificador não deve criar leitores de metadados por conta própria, mas sim usar o WIC para criá-los com base nos blocos de metadados no fluxo.</span><span class="sxs-lookup"><span data-stu-id="25cbc-110">The decoder should not create metadata readers on its own, but rather use WIC to create them based on the metadata blocks in the stream.</span></span> <span data-ttu-id="25cbc-111">O decodificador deve fazer isso em todos os blocos que encontrar, mesmo que eles não sejam nativamente conhecidos pelo docodificador, pois os leitores de metadados futuros podem ser instalados no sistema que entenda como lidar com esses blocos de metadados.</span><span class="sxs-lookup"><span data-stu-id="25cbc-111">The decoder must do this on all blocks that it finds, even if they are not natively known to the docoder, because future metadata readers might be installed on the system that do understand how to handle these metadata blocks.</span></span>

-   <span data-ttu-id="25cbc-112">Se não houver nenhum manipulador de metadados para um bloco, crie uma instância do leitor de metadados desconhecido usando as opções de criação de metadados.</span><span class="sxs-lookup"><span data-stu-id="25cbc-112">If there is no metadata handler for a block, instantiate the unknown metadata reader by using the metadata creation options.</span></span>
-   <span data-ttu-id="25cbc-113">Expor a coleção de leitores de metadados por meio da interface [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .</span><span class="sxs-lookup"><span data-stu-id="25cbc-113">Expose the collection of metadata readers through the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25cbc-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="25cbc-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="25cbc-115">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="25cbc-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="25cbc-116">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="25cbc-116">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="25cbc-117">Diretrizes do WIC para formatos de imagem bruta de câmera</span><span class="sxs-lookup"><span data-stu-id="25cbc-117">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="25cbc-118">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="25cbc-118">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



