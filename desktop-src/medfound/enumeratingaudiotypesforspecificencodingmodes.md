---
description: Enumerando tipos de áudio para modos de codificação específicos
ms.assetid: d44960eb-da5e-4379-ba9d-cb804559dc53
title: Enumerando tipos de áudio para modos de codificação específicos (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16a8b97afdd48cb1d7828f80778aa9fcf8dc1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370525"
---
# <a name="enumerating-audio-types-for-specific-encoding-modes-microsoft-media-foundation"></a><span data-ttu-id="5a0f3-103">Enumerando tipos de áudio para modos de codificação específicos (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="5a0f3-103">Enumerating Audio Types for Specific Encoding Modes (Microsoft Media Foundation)</span></span>

<span data-ttu-id="5a0f3-104">Os tipos de mídia de entrada e saída aceitos pelo codificador de áudio são muito estruturados.</span><span class="sxs-lookup"><span data-stu-id="5a0f3-104">The input and output media types accepted by the audio encoder are very structured.</span></span> <span data-ttu-id="5a0f3-105">Você deve obter os tipos de saída com suporte chamando o método **IMediaObject:: GetOutputType** ou **IMFTransform:: GetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="5a0f3-105">You must obtain supported output types by calling **IMediaObject::GetOutputType** method or **IMFTransform::GetOutputType**.</span></span> <span data-ttu-id="5a0f3-106">Depois de obter um tipo de saída, você não deve alterá-lo.</span><span class="sxs-lookup"><span data-stu-id="5a0f3-106">After you get an output type, you must not alter it.</span></span>

<span data-ttu-id="5a0f3-107">Se você quiser usar um modo de codificação diferente de uma passagem CBR, deverá definir o modo e, em seguida, enumerar os tipos de saída para esse modo; o codificador altera os tipos de saída com suporte, dependendo do conjunto de modos.</span><span class="sxs-lookup"><span data-stu-id="5a0f3-107">If you want to use an encoding mode other than one-pass CBR, you must set the mode and then enumerate the output types for that mode; the encoder changes the supported output types depending upon the mode set.</span></span> <span data-ttu-id="5a0f3-108">As propriedades que controlam o modo de codificação são [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) e [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md).</span><span class="sxs-lookup"><span data-stu-id="5a0f3-108">The properties that control the encoding mode are [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) and [**MFPKEY\_PASSESUSED**](mfpkey-passesusedproperty.md).</span></span> <span data-ttu-id="5a0f3-109">Quando o modo é definido no codificador, você deve enumerar e selecionar um tipo de saída, usando-o sem alteração, assim como acontece com a CBR.</span><span class="sxs-lookup"><span data-stu-id="5a0f3-109">When the mode is set in the encoder, you must enumerate and select an output type, using it without alteration, just as with CBR.</span></span>

## <a name="identifying-quality-based-vbr-types"></a><span data-ttu-id="5a0f3-110">Identificando tipos de VBR com base na qualidade</span><span class="sxs-lookup"><span data-stu-id="5a0f3-110">Identifying Quality Based VBR Types</span></span>

<span data-ttu-id="5a0f3-111">O procedimento para identificar tipos de VBR com base na qualidade depende se o codificador está agindo como um DMO (objeto de mídia do DirectX) ou atuando como uma MFT (Media Foundation transformação).</span><span class="sxs-lookup"><span data-stu-id="5a0f3-111">The procedure for identifying quality based VBR types depends on whether the encoder is acting as a DirectX Media Object (DMO) or acting as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="5a0f3-112">Para obter informações sobre quando um codificador atua como um DMO ou uma MFT, consulte as páginas de referência do codec individual em [objetos de codec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="5a0f3-112">For information on when an encoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="5a0f3-113">Quando um codificador de áudio está agindo como DMO e você configura o codificador para usar a VBR de uma passagem, ele enumera todos os tipos de saída com suporte.</span><span class="sxs-lookup"><span data-stu-id="5a0f3-113">When an audio encoder is acting as a DMO and you configure the encoder to use one-pass VBR, it enumerates all of the supported output types.</span></span> <span data-ttu-id="5a0f3-114">No entanto, normalmente você desejará selecionar um tipo de VBR de passagem com base no parâmetro de qualidade.</span><span class="sxs-lookup"><span data-stu-id="5a0f3-114">However, you will typically want to select a one-pass VBR type based on the quality parameter.</span></span> <span data-ttu-id="5a0f3-115">O codificador coloca o valor de qualidade para os tipos de saída de VBR de uma passagem no membro **nAvgBytesPerSec** da estrutura **WAVEFORMATEX** apontada pelo **tipo de \_ mídia DMO \_ . pbFormat**.</span><span class="sxs-lookup"><span data-stu-id="5a0f3-115">The encoder puts the quality value for one-pass VBR output types in the **nAvgBytesPerSec** member of the **WAVEFORMATEX** structure pointed to by **DMO\_MEDIA\_TYPE.pbFormat**.</span></span>

<span data-ttu-id="5a0f3-116">Esse valor é armazenado no seguinte formato: 0x7FFFFFXX, em que XX é o valor de qualidade (de 0 a 100).</span><span class="sxs-lookup"><span data-stu-id="5a0f3-116">This value is stored in the following format: 0x7FFFFFXX, where XX is the quality value (from 0 to 100).</span></span> <span data-ttu-id="5a0f3-117">Por exemplo, o valor de **nAvgBytesPerSec** de 0x7FFFFF62 especifica o nível de qualidade 98 (0x62 = 98).</span><span class="sxs-lookup"><span data-stu-id="5a0f3-117">For example, the **nAvgBytesPerSec** value of 0x7FFFFF62 specifies quality level 98 (0x62 = 98).</span></span>

<span data-ttu-id="5a0f3-118">O exemplo a seguir mostra como verificar o nível de qualidade de um formato quando o codificador está agindo como um DMO.</span><span class="sxs-lookup"><span data-stu-id="5a0f3-118">The following example shows how to check the quality level of a format when the encoder is acting as a DMO.</span></span>


```
void ShowQuality(WAVEFORMATEX* pWave)
{
    // Store the average bytes per second in a local variable
    // with a more manageable name.
    DWORD dwBps = pWave->nAvgBytesPerSec;

    // Verify that the value is a VBR quality level by using 
    // a bitmask to check for the bit pattern 0x7FFFFFXX. 
    if(dwBps & 0x7FFFFF00 == 0x7FFFFF00)
        printf("VBR Quality: %d%%\n",(dwBps & 0x000000FF));
    else // Not a valid VBR quality value.
        printf("Not a valid one-pass VBR audio format.\n");
}
```



<span data-ttu-id="5a0f3-119">Quando o codificador está agindo como um MFT e enumera um tipo de saída em uma chamada para **GetAvailableOutputType**, você pode consultar o MFT para a **propriedade \_ \_ \_ \_ VBRQUALITY enumerada mais recentemente do MFPKEY** .</span><span class="sxs-lookup"><span data-stu-id="5a0f3-119">When the encoder is acting as an MFT and it enumerates an output type on a call to **GetAvailableOutputType**, you can query the MFT for the **MFPKEY\_MOST\_RECENTLY\_ENUMERATED\_VBRQUALITY** property.</span></span> <span data-ttu-id="5a0f3-120">O valor retornado indica a qualidade de VBR do tipo de mídia de saída retornado mais recentemente.</span><span class="sxs-lookup"><span data-stu-id="5a0f3-120">The value returned indicates the VBR quality of the most recently returned output media type.</span></span> <span data-ttu-id="5a0f3-121">Em seguida, você pode usar esse valor para definir a propriedade [**MFPKEY \_ desejada \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) do codificador.</span><span class="sxs-lookup"><span data-stu-id="5a0f3-121">Then you can use that value to set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property of the encoder.</span></span>

## <a name="setting-peak-constraints"></a><span data-ttu-id="5a0f3-122">Definindo restrições de pico</span><span class="sxs-lookup"><span data-stu-id="5a0f3-122">Setting Peak Constraints</span></span>

<span data-ttu-id="5a0f3-123">Para uma taxa de bits variável baseada em qualidade (uma passagem) e uma VBR de duas passagens não restringida, nenhuma configuração adicional é necessária após a recuperação do tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="5a0f3-123">For quality based VBR (one-pass) and unconstrained two-pass VBR, no additional settings are required after retrieving the output type.</span></span> <span data-ttu-id="5a0f3-124">Para usar a taxa de bits de pico restrito, recupere um tipo de saída com VBR habilitado e duas passagens definidas.</span><span class="sxs-lookup"><span data-stu-id="5a0f3-124">To use peak-constrained VBR, retrieve an output type with VBR enabled and two passes set.</span></span> <span data-ttu-id="5a0f3-125">Esse tipo, sem alteração, descreve as configurações de VBR não restringidas.</span><span class="sxs-lookup"><span data-stu-id="5a0f3-125">This type, without alteration, describes unconstrained VBR settings.</span></span> <span data-ttu-id="5a0f3-126">Para definir as restrições de pico, defina as propriedades [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) e [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="5a0f3-126">To set peak constraints, set the [MFPKEY\_RMAX](mfpkey-rmaxproperty.md) and [MFPKEY\_BMAX](mfpkey-bmaxproperty.md) properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a0f3-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a0f3-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a0f3-128">Configurando codificação de áudio</span><span class="sxs-lookup"><span data-stu-id="5a0f3-128">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> <dt>

[<span data-ttu-id="5a0f3-129">Localizando tipos de saída do codificador de áudio</span><span class="sxs-lookup"><span data-stu-id="5a0f3-129">Finding Audio Encoder Output Types</span></span>](findingaudioencoderoutputtypes.md)
</dt> <dt>

[<span data-ttu-id="5a0f3-130">Usando a codificação Two-Pass</span><span class="sxs-lookup"><span data-stu-id="5a0f3-130">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
</dt> <dt>

[<span data-ttu-id="5a0f3-131">Usando a codificação de VBR</span><span class="sxs-lookup"><span data-stu-id="5a0f3-131">Using VBR Encoding</span></span>](usingvbrencoding.md)
</dt> </dl>

 

 



