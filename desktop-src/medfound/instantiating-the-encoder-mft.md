---
description: Criando uma instância de um MFT do codificador
ms.assetid: 50b71c00-b7cf-4c38-8114-bb36b358fda5
title: Criando uma instância de um MFT do codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5344c19a3a00c659efbbfd88d42176b876528380
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170520"
---
# <a name="instantiating-an-encoder-mft"></a><span data-ttu-id="33a19-103">Criando uma instância de um MFT do codificador</span><span class="sxs-lookup"><span data-stu-id="33a19-103">Instantiating an Encoder MFT</span></span>

<span data-ttu-id="33a19-104">Em Microsoft Media Foundation, os codificadores são implementados como [transformações de Media Foundation](media-foundation-transforms.md) (MFTs).</span><span class="sxs-lookup"><span data-stu-id="33a19-104">In Microsoft Media Foundation, encoders are implemented as [Media Foundation transforms](media-foundation-transforms.md) (MFTs).</span></span> <span data-ttu-id="33a19-105">Antes de criar um codificador, você deve primeiro encontrar o codificador mais adequado às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="33a19-105">Before creating an encoder, you must first find the encoder that is most suited to your needs.</span></span>

-   <span data-ttu-id="33a19-106">Codecs de áudio do Windows Media</span><span class="sxs-lookup"><span data-stu-id="33a19-106">Windows Media audio codecs</span></span>

    <span data-ttu-id="33a19-107">Categoria: **\_ \_ \_ codificador de áudio de categoria de MFT**</span><span class="sxs-lookup"><span data-stu-id="33a19-107">Category: **MFT\_CATEGORY\_AUDIO\_ENCODER**</span></span>

    <span data-ttu-id="33a19-108">Tipo principal: \_ áudio MFMediaType</span><span class="sxs-lookup"><span data-stu-id="33a19-108">Major type: MFMediaType\_Audio</span></span>

    <span data-ttu-id="33a19-109">Subtipo: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF</span><span class="sxs-lookup"><span data-stu-id="33a19-109">SubType: MFAudioFormat\_WMAudioV9, MFAudioFormat\_WMAudioV8, MFAudioFormat\_WMAudio\_Lossless, MFAudioFormat\_WMASPDIF</span></span>

-   <span data-ttu-id="33a19-110">Codecs de vídeo do Windows Media</span><span class="sxs-lookup"><span data-stu-id="33a19-110">Windows Media video codecs</span></span>

    <span data-ttu-id="33a19-111">Categoria: **\_ \_ \_ codificador de vídeo de categoria MFT**</span><span class="sxs-lookup"><span data-stu-id="33a19-111">Category: **MFT\_CATEGORY\_VIDEO\_ENCODER**</span></span>

    <span data-ttu-id="33a19-112">Tipo principal: \_ vídeo MFMediaType</span><span class="sxs-lookup"><span data-stu-id="33a19-112">Major type: MFMediaType\_Video</span></span>

    <span data-ttu-id="33a19-113">Subtipo: MFVideoFormat \_ WVC1, MFVideoFormat \_ WMV3, MFVideoFormat \_ WMV2, MFVideoFormat \_ WMV1</span><span class="sxs-lookup"><span data-stu-id="33a19-113">SubType: MFVideoFormat\_WVC1, MFVideoFormat\_WMV3, MFVideoFormat\_WMV2, MFVideoFormat\_WMV1</span></span>

<span data-ttu-id="33a19-114">O Media Foundation fornece várias funções que seu aplicativo pode chamar para enumerar os vários codificadores disponíveis no seu sistema.</span><span class="sxs-lookup"><span data-stu-id="33a19-114">Media Foundation provides several functions that your application can call to enumerate the various encoders available in your system.</span></span> <span data-ttu-id="33a19-115">Os codificadores são registrados como objetos COM e a entrada do registro segue o formato padrão para fábricas de classes COM.</span><span class="sxs-lookup"><span data-stu-id="33a19-115">Encoders are registered as COM objects and the registry entry follows the standard format for COM class factories.</span></span> <span data-ttu-id="33a19-116">O registro mantém os CLSIDs para os codificadores, que são categorizados pelo formato de mídia (áudio ou vídeo).</span><span class="sxs-lookup"><span data-stu-id="33a19-116">The registry maintains the CLSIDs for the encoders, which are categorized by the media format (audio or video).</span></span> <span data-ttu-id="33a19-117">Os identificadores de classe dos codificadores de mídia do Windows são definidos como constantes no arquivo de cabeçalho wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="33a19-117">The class identifiers of the Windows Media encoders are defined as constants in the wmcodecdsp.h header file.</span></span> <span data-ttu-id="33a19-118">No Media Foundation, os codificadores podem ser registrados por meio de chamadas para [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) ou [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) especificando o catergory, os tipos de entrada com suporte e os tipos de saída com suporte.</span><span class="sxs-lookup"><span data-stu-id="33a19-118">In Media Foundation, the encoders can be registered through calls to [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) by specifying the catergory, the supported input types, and the supported output types.</span></span> <span data-ttu-id="33a19-119">Após o registro bem-sucedido por meio dessas funções, os MFTs são considerados pelas funções de enumeração de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="33a19-119">Upon successful registration through these functions, the MFTs are considered by the Media Foundation enumeration functions.</span></span>

<span data-ttu-id="33a19-120">Para criar uma instância de um MFT do codificador, um aplicativo tem as seguintes opções.</span><span class="sxs-lookup"><span data-stu-id="33a19-120">For creating an instance of an encoder MFT, an application has the following choices.</span></span>

-   <span data-ttu-id="33a19-121">Crie o MFT do codificador diretamente e receba um ponteiro para a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="33a19-121">Create the encoder MFT directly and receive a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="33a19-122">Para obter mais informações, consulte [criando um codificador usando CoCreateInstance](using-an-encoder-s-imftransform--interface.md).</span><span class="sxs-lookup"><span data-stu-id="33a19-122">For more information, see [Creating an Encoder by Using CoCreateInstance](using-an-encoder-s-imftransform--interface.md).</span></span>
-   <span data-ttu-id="33a19-123">Crie uma instância do objeto de ativação para o MFT do codificador e receba um ponteiro para a interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="33a19-123">Create an instance of the activation object for the encoder MFT and receive a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span> <span data-ttu-id="33a19-124">Para obter mais informações, consulte [usando objetos de ativação de um codificador](using-an-encoder-s-activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="33a19-124">For more information, see [Using an Encoder's Activation Objects](using-an-encoder-s-activation-objects.md).</span></span>

<span data-ttu-id="33a19-125">Se seu aplicativo estiver usando [componentes ASF da camada de pipeline](pipeline-layer-asf-components.md) para codificar um arquivo para o formato ASF, você deverá inserir o MFT do codificador no pipeline como um nó de transformação.</span><span class="sxs-lookup"><span data-stu-id="33a19-125">If your application is using [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) to encode a file to ASF format, you must insert the encoder MFT into the pipeline as a transform node.</span></span> <span data-ttu-id="33a19-126">Ao criar o nó de transformação na topologia de codificação, você pode definir o tipo de objeto como um ponteiro para a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ou o objeto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="33a19-126">While creating the transform node in the encoding topology, you can either set the object type as a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface or the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object.</span></span> <span data-ttu-id="33a19-127">O Media Foundation fornece objetos de ativação para codificadores de mídia do Windows para que possam ser definidos convenientemente como o nó de transformação na topologia de codificação.</span><span class="sxs-lookup"><span data-stu-id="33a19-127">Media Foundation provides activation objects for Windows Media encoders so that they can be conveniently set as the transform node in the encoding topology.</span></span> <span data-ttu-id="33a19-128">Quando a topologia é resolvida, a sessão de mídia usa o objeto de ativação para criar uma instância do MFT do codificador.</span><span class="sxs-lookup"><span data-stu-id="33a19-128">When the topology is resolved, the Media Session uses the activation object to create an instance of the encoder MFT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33a19-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="33a19-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33a19-130">Codificadores de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="33a19-130">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



