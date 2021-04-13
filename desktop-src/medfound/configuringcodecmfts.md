---
description: Configurando o codec MFTs
ms.assetid: 0de0cb2e-67bc-4db5-879a-95879f16b98d
title: Configurando o codec MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0065f05d10eae367b13ef6f7caf3fe2ab322163a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457219"
---
# <a name="configuring-codec-mfts"></a><span data-ttu-id="c08be-103">Configurando o codec MFTs</span><span class="sxs-lookup"><span data-stu-id="c08be-103">Configuring Codec MFTs</span></span>

<span data-ttu-id="c08be-104">Este tópico descreve o processo de configuração do codec MFTs.</span><span class="sxs-lookup"><span data-stu-id="c08be-104">This topic describes the process of configuring the codec MFTs.</span></span> <span data-ttu-id="c08be-105">Cada codec tem procedimentos específicos, mas as informações comuns a todos são descritas aqui.</span><span class="sxs-lookup"><span data-stu-id="c08be-105">Each codec has specific procedures, but the information common to all is described here.</span></span>

## <a name="configuring-mft-inputs-and-outputs"></a><span data-ttu-id="c08be-106">Configurando entradas e saídas de MFT</span><span class="sxs-lookup"><span data-stu-id="c08be-106">Configuring MFT Inputs and Outputs</span></span>

<span data-ttu-id="c08be-107">Cada MFT dá suporte a tipos específicos de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="c08be-107">Every MFT supports specific input and output types.</span></span> <span data-ttu-id="c08be-108">Você pode recuperar tipos de entrada com suporte chamando repetidamente [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype), incrementando o índice de tipo com cada chamada.</span><span class="sxs-lookup"><span data-stu-id="c08be-108">You can retrieve supported input types by repeatedly calling [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype), incrementing the type index with each call.</span></span> <span data-ttu-id="c08be-109">Quando você encontrar um tipo apropriado, defina o tipo de entrada chamando [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span><span class="sxs-lookup"><span data-stu-id="c08be-109">When you find an appropriate type, set the input type by calling [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span> <span data-ttu-id="c08be-110">Em seguida, você pode repetir o processo para o tipo de saída usando as chamadas [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) e [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="c08be-110">You can then repeat the process for the output type using the calls [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) and [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <span data-ttu-id="c08be-111">Você deve consultar ou definir os tipos de saída disponíveis somente depois de definir o tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="c08be-111">You must query or set the available output types only after setting the input type.</span></span>

## <a name="configuring-the-codec-mfts-for-encoding"></a><span data-ttu-id="c08be-112">Configurando o codec MFTs para codificação</span><span class="sxs-lookup"><span data-stu-id="c08be-112">Configuring the Codec MFTs for Encoding</span></span>

<span data-ttu-id="c08be-113">Todos os codecs de vídeo e áudio do Windows Media oferecem suporte a uma variedade de recursos de codificação.</span><span class="sxs-lookup"><span data-stu-id="c08be-113">All of the Windows Media Audio and Video codecs support a variety of encoding features.</span></span> <span data-ttu-id="c08be-114">Esses recursos geralmente são configurados definindo as propriedades no MFT usando os métodos da interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="c08be-114">These features are generally configured by setting properties on the MFT by using the methods of the **IPropertyStore** interface.</span></span> <span data-ttu-id="c08be-115">Algumas propriedades são configuradas usando interfaces de codec especializadas.</span><span class="sxs-lookup"><span data-stu-id="c08be-115">Some properties are configured using specialized codec interfaces.</span></span> <span data-ttu-id="c08be-116">Essas interfaces são listadas para cada codec na seção [objetos de codec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="c08be-116">These interfaces are listed for each codec in the section [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="c08be-117">A ordem geral das operações para configurar uma MFT de codificação é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="c08be-117">The general order of operations for configuring an encoding MFT is as follows:</span></span>

1.  <span data-ttu-id="c08be-118">Configure os recursos de codec conforme desejado usando os métodos de **IPropertyStore**.</span><span class="sxs-lookup"><span data-stu-id="c08be-118">Configure codec features as desired by using the methods of **IPropertyStore**.</span></span>
2.  <span data-ttu-id="c08be-119">Use as interfaces de MFT do codec para configurar recursos adicionais, se necessário.</span><span class="sxs-lookup"><span data-stu-id="c08be-119">Use the codec MFT interfaces to configure additional features, if needed.</span></span>
3.  <span data-ttu-id="c08be-120">Configure os tipos de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="c08be-120">Configure the input and output types.</span></span> <span data-ttu-id="c08be-121">A ordem na qual os tipos devem ser configurados varia de acordo com os codecs individuais.</span><span class="sxs-lookup"><span data-stu-id="c08be-121">The order in which the types should be configured varies for individual codecs.</span></span> <span data-ttu-id="c08be-122">Para obter mais informações, consulte [trabalhando com áudio](workingwithaudio.md) e [trabalhando com vídeo](workingwithvideo.md).</span><span class="sxs-lookup"><span data-stu-id="c08be-122">For more information, see [Working with Audio](workingwithaudio.md) and [Working with Video](workingwithvideo.md).</span></span>

## <a name="configuring-the-codec-mfts-for-decoding"></a><span data-ttu-id="c08be-123">Configurando o codec MFTs para decodificação</span><span class="sxs-lookup"><span data-stu-id="c08be-123">Configuring the Codec MFTs for Decoding</span></span>

<span data-ttu-id="c08be-124">A decodificação é mais simples do que a codificação, pois há suporte para menos recursos de decodificador.</span><span class="sxs-lookup"><span data-stu-id="c08be-124">Decoding is simpler than encoding, as fewer decoder features are supported.</span></span>

<span data-ttu-id="c08be-125">A ordem geral das operações para configurar uma MFT de decodificação é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="c08be-125">The general order of operations for configuring a decoding MFT is as follows:</span></span>

1.  <span data-ttu-id="c08be-126">Configure os recursos do decodificador conforme desejado usando os métodos de **IPropertyStore**.</span><span class="sxs-lookup"><span data-stu-id="c08be-126">Configure decoder features as desired by using the methods of **IPropertyStore**.</span></span>
2.  <span data-ttu-id="c08be-127">Defina o tipo de entrada para o tipo usado para a saída do codificador.</span><span class="sxs-lookup"><span data-stu-id="c08be-127">Set the input type to the type used for the encoder output.</span></span>
3.  <span data-ttu-id="c08be-128">Configure o tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="c08be-128">Configure the output type.</span></span> <span data-ttu-id="c08be-129">Os tipos de saída com suporte são diferentes para entradas diferentes.</span><span class="sxs-lookup"><span data-stu-id="c08be-129">The supported output types are different for different inputs.</span></span>

> [!Note]  
> <span data-ttu-id="c08be-130">É importante usar o mesmo tipo de mídia para a entrada do decodificador como foi usado para a saída do codificador.</span><span class="sxs-lookup"><span data-stu-id="c08be-130">It is important to use the same media type for the decoder input as was used for the encoder output.</span></span> <span data-ttu-id="c08be-131">Isso ocorre porque os codecs de áudio e vídeo do Windows Media usam formatos de mídia com dados adicionais.</span><span class="sxs-lookup"><span data-stu-id="c08be-131">This is because the Windows Media Audio and Video codecs use media formats with extra data.</span></span> <span data-ttu-id="c08be-132">Sem os dados de formato estendidos, você não pode decodificar o conteúdo compactado.</span><span class="sxs-lookup"><span data-stu-id="c08be-132">Without the extended format data, you cannot decode the compressed content.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c08be-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c08be-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c08be-134">Trabalhando com codec MFTs</span><span class="sxs-lookup"><span data-stu-id="c08be-134">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



