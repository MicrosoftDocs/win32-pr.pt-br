---
description: Configurando codificação de áudio
ms.assetid: 40004f07-0b8c-49cd-9e17-1f6ad7604fbb
title: Configurando codificação de áudio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47595f440d10ad0d3c5695f117204f357035d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164211"
---
# <a name="configuring-audio-encoding-microsoft-media-foundation"></a><span data-ttu-id="1672c-103">Configurando codificação de áudio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="1672c-103">Configuring Audio Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="1672c-104">O codificador de áudio do Windows Media enumera todos os tipos de saída com suporte em seu formato completo.</span><span class="sxs-lookup"><span data-stu-id="1672c-104">The Windows Media Audio encoder enumerates all of its supported output types in their complete form.</span></span> <span data-ttu-id="1672c-105">Recupere o tipo desejado chamando **IMediaObject:: GetOutputType** ou **IMFTransform:: GetAvailableOutputType** e, em seguida, defina o tipo recuperado, inalterado, como o tipo de saída chamando **IMediaObject:: SetOutputType** ou **IMFTransform:: SetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="1672c-105">Retrieve the type that you want by calling **IMediaObject::GetOutputType** or **IMFTransform::GetAvailableOutputType**, and then set the retrieved type, unaltered, as the output type by calling **IMediaObject::SetOutputType** or **IMFTransform::SetOutputType**.</span></span>

<span data-ttu-id="1672c-106">Os tipos de mídia de saída com suporte do codificador de áudio mudam conforme as propriedades do codificador são configuradas.</span><span class="sxs-lookup"><span data-stu-id="1672c-106">The output media types supported by the audio encoder change as encoder properties are configured.</span></span> <span data-ttu-id="1672c-107">Você deve configurar todas as propriedades do codificador que deseja usar antes de enumerar o tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="1672c-107">You must configure all of the encoder properties you want to use before you enumerate the output type.</span></span>

<span data-ttu-id="1672c-108">Os modos de dois passos e VBR são compatíveis com os codificadores de áudio, mas são configurados de forma diferente de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1672c-108">Two-pass and VBR modes are supported by the audio encoders, but are configured differently than for video.</span></span> <span data-ttu-id="1672c-109">Para obter mais informações, consulte [enumerando tipos de áudio para modos de codificação específicos](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="1672c-109">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="1672c-110">Os tipos de entrada com suporte pelo codificador de áudio não estarão disponíveis até que você defina o tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="1672c-110">The input types supported by the audio encoder are not available until you set the output type.</span></span> <span data-ttu-id="1672c-111">Se você chamar **IMediaObject:: GetInputType** ou **IMFTransform:: GetInputType** antes de definir um tipo de saída, o método retornará DMO \_ e não mais nenhum \_ tipo de \_ \_ MFT \_ e \_ nenhum mais, \_ \_ respectivamente.</span><span class="sxs-lookup"><span data-stu-id="1672c-111">If you call **IMediaObject::GetInputType** or **IMFTransform::GetInputType** before setting an output type, the method returns DMO\_E\_NO\_MORE\_ITEMS or MFT\_E\_NO\_MORE\_TYPES respectively.</span></span> <span data-ttu-id="1672c-112">Depois que o tipo de saída é definido, o codificador enumera os tipos de entrada aos quais ele dá suporte para o tipo de saída selecionado.</span><span class="sxs-lookup"><span data-stu-id="1672c-112">After the output type is set, the encoder enumerates the input types that it supports for the selected output type.</span></span>

<span data-ttu-id="1672c-113">Nenhuma reamostragem de áudio é executada pelo codificador de áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="1672c-113">No audio resampling is performed by the Windows Media Audio encoder.</span></span> <span data-ttu-id="1672c-114">Isso significa que o tipo de saída do codificador e o tipo de entrada do codificador devem ter o mesmo número de canais, bits por amostra e taxa de amostragem.</span><span class="sxs-lookup"><span data-stu-id="1672c-114">This means that the encoder output type and the encoder input type must have the same number of channels, bits per sample, and sample rate.</span></span> <span data-ttu-id="1672c-115">Para obter mais informações, consulte [localizando tipos de saída do codificador de áudio](findingaudioencoderoutputtypes.md).</span><span class="sxs-lookup"><span data-stu-id="1672c-115">For more information, see [Finding Audio Encoder Output Types](findingaudioencoderoutputtypes.md).</span></span>

> [!Note]  
>    <span data-ttu-id="1672c-116">Cada tipo de saída enumerado pelo codificador de áudio contém uma estrutura **WAVEFORMATEX** (apontada por **am \_ Media \_ Type. pbFormat**) com dados estendidos anexados a ela.</span><span class="sxs-lookup"><span data-stu-id="1672c-116">Each output type enumerated by the audio encoder contains a **WAVEFORMATEX** structure (pointed to by **AM\_MEDIA\_TYPE.pbFormat**) with extended data appended to it.</span></span> <span data-ttu-id="1672c-117">O tamanho dos dados estendidos é especificado por **WAVEFORMATEX. cbSize**.</span><span class="sxs-lookup"><span data-stu-id="1672c-117">The size of the extended data is specified by **WAVEFORMATEX.cbSize**.</span></span> <span data-ttu-id="1672c-118">Esses dados devem ser mantidos com o conteúdo codificado para que possam ser entregues ao decodificador.</span><span class="sxs-lookup"><span data-stu-id="1672c-118">This data must be kept with the encoded content so that it can be delivered to the decoder.</span></span> <span data-ttu-id="1672c-119">O conteúdo não pode ser descompactado sem os dados de formato estendido.</span><span class="sxs-lookup"><span data-stu-id="1672c-119">The content cannot be decompressed without the extended format data.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1672c-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1672c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1672c-121">Trabalhando com áudio</span><span class="sxs-lookup"><span data-stu-id="1672c-121">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



