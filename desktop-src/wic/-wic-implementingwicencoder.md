---
description: Implementando um codificador de WIC-Enabled
ms.assetid: 9c1a4fa4-30b9-445f-8aee-46711355ace7
title: Implementando um codificador de WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e65f969ba7c65e6860009b2fc998024d358301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170456"
---
# <a name="implementing-a-wic-enabled-encoder"></a><span data-ttu-id="4160f-103">Implementando um codificador de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="4160f-103">Implementing a WIC-Enabled Encoder</span></span>

## <a name="introduction"></a><span data-ttu-id="4160f-104">Introdução</span><span class="sxs-lookup"><span data-stu-id="4160f-104">Introduction</span></span>

<span data-ttu-id="4160f-105">A implementação de um codificador do Windows Imaging Component (WIC) requer a escrita de duas classes, como também é verdadeira para implementar um decodificador de WIC.</span><span class="sxs-lookup"><span data-stu-id="4160f-105">Implementing a Windows Imaging Component (WIC) encoder requires writing two classes, as is also true for implementing a WIC decoder.</span></span> <span data-ttu-id="4160f-106">As interfaces dessas classes correspondem diretamente às responsabilidades do codificador descritas na seção [codificação](-wic-howwicworks.md) de como o Windows Imaging Component funciona.</span><span class="sxs-lookup"><span data-stu-id="4160f-106">The interfaces on these classes correspond directly to the encoder responsibilities outlined in the [Encoding](-wic-howwicworks.md) section of How The Windows Imaging Component Works.</span></span>

<span data-ttu-id="4160f-107">Uma das classes fornece serviços de nível de contêiner e gerencia a serialização dos quadros de imagem individuais dentro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="4160f-107">One of the classes provides container-level services and manages the serialization of the individual image frames within the container.</span></span> <span data-ttu-id="4160f-108">Essa classe implementa a interface [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="4160f-108">This class implements the [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) interface.</span></span> <span data-ttu-id="4160f-109">Se o formato de imagem der suporte a metadados em nível de contêiner, você também deverá implementar a interface [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) nessa classe.</span><span class="sxs-lookup"><span data-stu-id="4160f-109">If your image format supports container-level metadata, you must also implement the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface on this class.</span></span>

<span data-ttu-id="4160f-110">A outra classe fornece serviços de nível de quadro e faz a codificação real dos bits de imagem para cada quadro no contêiner.</span><span class="sxs-lookup"><span data-stu-id="4160f-110">The other class provides frame-level services and does the actual encoding of the image bits for each frame in the container.</span></span> <span data-ttu-id="4160f-111">Ele também itera nos blocos de metadados de cada quadro e solicita os gravadores de metadados apropriados para serializar os blocos.</span><span class="sxs-lookup"><span data-stu-id="4160f-111">It also iterates through the metadata blocks for each frame and requests the appropriate metadata writers to serialize the blocks.</span></span> <span data-ttu-id="4160f-112">Essa classe implementa a interface **IWICBitmapFrameEncode** e a interface [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) .</span><span class="sxs-lookup"><span data-stu-id="4160f-112">This class implements the **IWICBitmapFrameEncode** interface and the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface.</span></span> <span data-ttu-id="4160f-113">Essa classe deve ter um membro IStream que a classe de nível de contêiner inicialize na instanciação, na qual o método **Commit** serializará os dados do quadro.</span><span class="sxs-lookup"><span data-stu-id="4160f-113">This class should have an IStream member that the container-level class initializes on instantiation, into which the **Commit** method will serialize the frame data.</span></span>

<span data-ttu-id="4160f-114">Em alguns casos, como formatos brutos, o autor do codec pode não querer que os aplicativos sejam capazes de codificar ou recodificar no formato bruto, pois a finalidade de um arquivo bruto é conter os dados do sensor exatamente como vieram da câmera.</span><span class="sxs-lookup"><span data-stu-id="4160f-114">In some cases, such as raw formats, the codec author may not want applications to be able to encode or re-encode to the raw format, because the purpose of a raw file is to contain the sensor data exactly as it came from the camera.</span></span> <span data-ttu-id="4160f-115">Nos casos em que o autor do codec não deseja habilitar a codificação, ainda é necessário implementar um codificador rudimentar apenas para habilitar a adição de metadados.</span><span class="sxs-lookup"><span data-stu-id="4160f-115">In cases where the codec author doesn’t want to enable encoding, it is still necessary to implement a rudimentary encoder just to enable adding metadata.</span></span> <span data-ttu-id="4160f-116">Nesse caso, o codificador precisa dar suporte apenas a esses métodos necessários para gravar metadados e pode copiar os bits da imagem intocados do decodificador.</span><span class="sxs-lookup"><span data-stu-id="4160f-116">In that case, the encoder need only support those methods necessary for writing metadata, and can copy the image bits untouched from the decoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4160f-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4160f-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4160f-118">**Referência**</span><span class="sxs-lookup"><span data-stu-id="4160f-118">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4160f-119">**IWICBitmapEncoder**</span><span class="sxs-lookup"><span data-stu-id="4160f-119">**IWICBitmapEncoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

<span data-ttu-id="4160f-120">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="4160f-120">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4160f-121">Implementando IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="4160f-121">Implementing IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[<span data-ttu-id="4160f-122">Interfaces do codificador</span><span class="sxs-lookup"><span data-stu-id="4160f-122">Encoder Interfaces</span></span>](-wic-encoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="4160f-123">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="4160f-123">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="4160f-124">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="4160f-124">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



