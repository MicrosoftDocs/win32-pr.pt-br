---
description: Usando o codec de voz de áudio do Windows Media
ms.assetid: 771acb04-33a4-4ea3-8f50-e5e3dbdf9495
title: Usando o codec de voz de áudio do Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d636bd97b76e23acc6b68da87c8a206b17dea60a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104506332"
---
# <a name="using-the-windows-media-audio-voice-codec"></a><span data-ttu-id="2d4a1-103">Usando o codec de voz de áudio do Windows Media</span><span class="sxs-lookup"><span data-stu-id="2d4a1-103">Using the Windows Media Audio Voice Codec</span></span>

<span data-ttu-id="2d4a1-104">O codec de voz de áudio do Windows Media fornece compactação de baixa taxa de bits otimizada para áudio contendo fala.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-104">The Windows Media Audio Voice codec provides low bit-rate compression optimized for audio containing speech.</span></span> <span data-ttu-id="2d4a1-105">A capacidade do codec de produzir esses pequenos exemplos é devido ao intervalo de frequência limitada dos sons da voz humana.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-105">The ability of the codec to produce such small samples is due to the limited frequency range of the sounds of the human voice.</span></span> <span data-ttu-id="2d4a1-106">Essa otimização significa que um codificador de voz dedicado cria uma saída de baixa qualidade para o conteúdo que contém sons mais complicados, como música.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-106">This optimization means that a dedicated voice encoder creates poor-quality output for content that contains more complicated sounds, like music.</span></span> <span data-ttu-id="2d4a1-107">No entanto, o codec de voz de áudio do Windows Media compensa esse possível problema de qualidade fornecendo modos separados para voz, música e conteúdo misto.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-107">However, the Windows Media Audio Voice codec compensates for this potential quality issue by providing separate modes for voice, music, and mixed content.</span></span> <span data-ttu-id="2d4a1-108">O codec analisa o conteúdo misto para determinar qual modo usar para cada parte do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-108">The codec analyzes mixed content to determine which mode to use for each portion of the file.</span></span>

<span data-ttu-id="2d4a1-109">O codec de voz do Windows Media Audio é implementado no objeto do codificador identificado pelo CLSID do identificador de classe \_ CWMSPEncMediaObject2 e no objeto decodificador identificado pelo CLSID do identificador de classe \_ CWMSPDecMediaObject.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-109">The Windows Media Audio Voice codec is implemented in the encoder object identified by the class identifier CLSID\_CWMSPEncMediaObject2, and in the decoder object identified by the class identifier CLSID\_CWMSPDecMediaObject.</span></span> <span data-ttu-id="2d4a1-110">A marca de formato dos tipos de mídia usando esse codec é 0x00a.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-110">The format tag of media types using this codec is 0x00A.</span></span>

## <a name="configuring-the-encoder"></a><span data-ttu-id="2d4a1-111">Configurando o codificador</span><span class="sxs-lookup"><span data-stu-id="2d4a1-111">Configuring the Encoder</span></span>

<span data-ttu-id="2d4a1-112">O codificador de voz dá suporte a três modos: fala, música e misto.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-112">The voice encoder supports three modes: speech, music, and mixed.</span></span> <span data-ttu-id="2d4a1-113">Cada modo é otimizado para obter os melhores resultados para esse tipo de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-113">Each mode is optimized to get the best results for that type of content.</span></span> <span data-ttu-id="2d4a1-114">Você pode configurar o modo do codificador de voz usando os métodos de **IPropertyStore** para definir a propriedade [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="2d4a1-114">You can configure the mode of the voice encoder by using the methods of **IPropertyStore** to set the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property.</span></span>

<span data-ttu-id="2d4a1-115">Quando configurado para conteúdo misto, o codec de voz de áudio do Windows Media detectará automaticamente passagens de música no conteúdo.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-115">When configured for mixed content, the Windows Media Audio Voice codec will automatically detect passages of music in the content.</span></span> <span data-ttu-id="2d4a1-116">Se você não estiver satisfeito com os resultados, poderá especificar o local de música no conteúdo usando uma EDL (lista de decisões de edição).</span><span class="sxs-lookup"><span data-stu-id="2d4a1-116">If you are not satisfied with the results, you can specify the location of music in the content using an editing decision list (EDL).</span></span> <span data-ttu-id="2d4a1-117">Para obter mais informações, consulte [usando uma lista de decisões de edição para codificação de voz](usingavoiceeditingdecisionlist.md).</span><span class="sxs-lookup"><span data-stu-id="2d4a1-117">For more information, see [Using an Editing Decision List for Encoding Voice](usingavoiceeditingdecisionlist.md).</span></span>

<span data-ttu-id="2d4a1-118">Ao contrário dos outros codificadores de áudio, você pode definir o valor da janela de buffer para o conteúdo de voz usando a propriedade [MFPKEY \_ WMAVOICE \_ ENC \_ BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="2d4a1-118">Unlike the other audio encoders, you can set the buffer window value for voice content by using the [MFPKEY\_WMAVOICE\_ENC\_BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) property.</span></span> <span data-ttu-id="2d4a1-119">No entanto, os valores padrão devem funcionar bem na maioria dos casos.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-119">However, the default values should work fine in most cases.</span></span>

> [!Note]  
>    <span data-ttu-id="2d4a1-120">Ao configurar o codificador de voz, é muito importante que você defina o tipo de saída antes de definir o tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-120">When configuring the voice encoder, it is very important that you set the output type before you set the input type.</span></span> <span data-ttu-id="2d4a1-121">Essa é a ordem recomendada de operações para todos os codecs de áudio, mas o codificador de voz pode relatar tipos de saída incorretos se uma entrada for definida quando você chamar **IMediaObject:: GetOutputType** ou **IMFTransform:: GetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-121">This is the recommended order of operations for all of the audio codecs, but the voice encoder can report erroneous output types if an input is set when you call **IMediaObject::GetOutputType** or **IMFTransform::GetOutputType**.</span></span>

 

## <a name="decoding"></a><span data-ttu-id="2d4a1-122">Decodificação</span><span class="sxs-lookup"><span data-stu-id="2d4a1-122">Decoding</span></span>

<span data-ttu-id="2d4a1-123">Não há requisitos especiais para decodificar áudio de voz.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-123">There are no special requirements for decoding voice audio.</span></span> <span data-ttu-id="2d4a1-124">Para obter mais informações, consulte [Configurando a decodificação de áudio](configuringaudiodecoding.md).</span><span class="sxs-lookup"><span data-stu-id="2d4a1-124">Form more information, see [Configuring Audio Decoding](configuringaudiodecoding.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d4a1-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d4a1-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d4a1-126">Trabalhando com áudio</span><span class="sxs-lookup"><span data-stu-id="2d4a1-126">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



