---
title: Trabalhando com High-Resolution áudio PCM
description: Trabalhando com High-Resolution áudio PCM
ms.assetid: 422a78f9-0f43-4edb-acaf-7f6e3f4a1cb8
keywords:
- ASF (Advanced Systems Format), áudio PCM de alta resolução
- ASF (formato de sistemas avançados), áudio PCM de alta resolução
- perfis, áudio PCM de alta resolução
- codecs, áudio PCM de alta resolução
- ASF (Advanced Systems Format), áudio PCM
- ASF (formato de sistemas avançados), áudio PCM
- perfis, áudio PCM
- codecs, áudio PCM
- áudio PCM de alta resolução
- Áudio PCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73a45904072307e915065ba3a5946d5ef774c73b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917419"
---
# <a name="working-with-high-resolution-pcm-audio"></a><span data-ttu-id="5a3ca-113">Trabalhando com High-Resolution áudio PCM</span><span class="sxs-lookup"><span data-stu-id="5a3ca-113">Working with High-Resolution PCM Audio</span></span>

<span data-ttu-id="5a3ca-114">Alguns dos formatos de entrada para o codec do Windows Media Audio 9 Professional e o codec do Windows Media Audio 9 sem perdas são formatos PCM de alta resolução.</span><span class="sxs-lookup"><span data-stu-id="5a3ca-114">Some of the input formats for the Windows Media Audio 9 Professional codec and the Windows Media Audio 9 Lossless codec are high-resolution PCM formats.</span></span> <span data-ttu-id="5a3ca-115">Esses são formatos PCM que têm mais de dois canais, ou mais de 16 bits por amostra (áudio com mais de dois canais também é chamado de áudio de multicanal).</span><span class="sxs-lookup"><span data-stu-id="5a3ca-115">These are PCM formats that have more than two channels, or more than 16 bits per sample (audio with more than two channels is also called multichannel audio).</span></span>

<span data-ttu-id="5a3ca-116">Esses formatos são configurados usando uma extensão estruturada da estrutura [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) , chamada [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5a3ca-116">These formats are configured by using a structured extension of the [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)) structure, called [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)).</span></span> <span data-ttu-id="5a3ca-117">A estrutura **WAVEFORMATEXTENSIBLE** inclui informações sobre os canais incluídos no áudio.</span><span class="sxs-lookup"><span data-stu-id="5a3ca-117">The **WAVEFORMATEXTENSIBLE** structure includes information about the channels included in the audio.</span></span> <span data-ttu-id="5a3ca-118">Essa estrutura é necessária ao usar áudio PCM de alta resolução, pois algumas APIs do Windows não aceitarão estruturas **WAVEFORMATEX** que contenham valores de alta resolução.</span><span class="sxs-lookup"><span data-stu-id="5a3ca-118">This structure is required when using high-resolution PCM audio, because some Windows APIs will not accept **WAVEFORMATEX** structures that contain high-resolution values.</span></span>

<span data-ttu-id="5a3ca-119">Os formatos PCM de alta resolução têm 22 bytes de dados estendidos, que é especificado no membro **cbSize** da estrutura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="5a3ca-119">High-resolution PCM formats have 22 bytes of extended data, which is specified in the **cbSize** member of the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="5a3ca-120">Os formatos de áudio do Windows Media de alta resolução não usam a estrutura **WAVEFORMATEXTENSIBLE** , mas têm dados estendidos anexados à estrutura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="5a3ca-120">High-resolution Windows Media audio formats do not use the **WAVEFORMATEXTENSIBLE** structure, but do have extended data appended to the **WAVEFORMATEX** structure.</span></span>

<span data-ttu-id="5a3ca-121">Os codecs de áudio do Windows Media só dão suporte à decodificação de formatos PCM de alta resolução quando o aplicativo está em execução no Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="5a3ca-121">The Windows Media audio codecs only support decoding to high-resolution PCM formats when the application is running on Windows XP or later.</span></span> <span data-ttu-id="5a3ca-122">Nas versões anteriores do Microsoft Windows, os codecs decodificam para um formato com um máximo de 16 bits por amostra e 2 canais.</span><span class="sxs-lookup"><span data-stu-id="5a3ca-122">On previous versions of Microsoft Windows, the codecs decode to a format with a maximum of 16 bits per sample and 2 channels.</span></span> <span data-ttu-id="5a3ca-123">Além disso, você deve especificar que deseja que o codec decodifique para o PCM de alta definição definindo a \_ configuração de saída g wszEnableDiscreteOutput como **true** usando o método [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) .</span><span class="sxs-lookup"><span data-stu-id="5a3ca-123">In addition, you must specify that you want the codec to decode to high-definition PCM by setting the g\_wszEnableDiscreteOutput output setting to **TRUE** using the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method.</span></span> <span data-ttu-id="5a3ca-124">Depois de fazer essa chamada, as saídas enumeradas pelo leitor incluirão formatos de alta definição.</span><span class="sxs-lookup"><span data-stu-id="5a3ca-124">After making this call, the outputs enumerated by the reader will include high-definition formats.</span></span>

<span data-ttu-id="5a3ca-125">O áudio de multicanal requer mais configuração.</span><span class="sxs-lookup"><span data-stu-id="5a3ca-125">Multichannel audio requires more configuration.</span></span> <span data-ttu-id="5a3ca-126">Para obter mais informações, consulte [lendo áudio multicanal](reading-multichannel-audio.md).</span><span class="sxs-lookup"><span data-stu-id="5a3ca-126">For more information, see [Reading Multichannel Audio](reading-multichannel-audio.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a3ca-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a3ca-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a3ca-128">**Trabalhando com entradas**</span><span class="sxs-lookup"><span data-stu-id="5a3ca-128">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 