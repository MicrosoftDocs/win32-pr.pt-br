---
description: Esta seção descreve como configurar fluxos de VBR.
ms.assetid: 9dd3ff5b-4c7c-41a8-b1b9-7ea380175193
title: Usando a codificação de VBR (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd1f317308d79c696e26a8671cc9d84ca8effa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164879"
---
# <a name="using-vbr-encoding-microsoft-media-foundation"></a><span data-ttu-id="ed298-103">Usando a codificação de VBR (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="ed298-103">Using VBR Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="ed298-104">Conforme detalhado no tópico [métodos de codificação](encodingmethods.md) , a codificação taxa de bits variável (VBR) é usada para melhorar a consistência da qualidade do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ed298-104">As detailed in the [Encoding Methods](encodingmethods.md) topic, variable bit rate (VBR) encoding is used to improve the consistency of content quality.</span></span> <span data-ttu-id="ed298-105">Configure fluxos de VBR da mesma maneira que você codifica fluxos de taxa de bits constante (CBR), exceto para os parâmetros de buffer (taxa de bits e janela de buffer).</span><span class="sxs-lookup"><span data-stu-id="ed298-105">You configure VBR streams in the same way that you encode constant bit rate (CBR) streams, except for the buffer parameters (bit rate and buffer window).</span></span> <span data-ttu-id="ed298-106">Esta seção descreve como configurar fluxos de VBR.</span><span class="sxs-lookup"><span data-stu-id="ed298-106">This section describes how to configure VBR streams.</span></span>

## <a name="configuring-quality-based-vbr"></a><span data-ttu-id="ed298-107">Configuração da VBR com base na qualidade</span><span class="sxs-lookup"><span data-stu-id="ed298-107">Configuring Quality Based VBR</span></span>

<span data-ttu-id="ed298-108">A codificação usando o método de taxa de bits baseada em qualidade não requer nenhum parâmetro de buffer predefinido.</span><span class="sxs-lookup"><span data-stu-id="ed298-108">Encoding using the quality based VBR method does not require any predefined buffer parameters.</span></span> <span data-ttu-id="ed298-109">Em vez disso, você especifica um nível de qualidade (de 0 a 100) que o codificador usa para determinar os parâmetros de buffer apropriados dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="ed298-109">Instead, you specify a quality level (from 0 to 100) which the encoder uses to determine the appropriate buffer parameters dynamically.</span></span> <span data-ttu-id="ed298-110">Esse modo de codificação usa apenas uma passagem de codificação.</span><span class="sxs-lookup"><span data-stu-id="ed298-110">This encoding mode uses only one encoding pass.</span></span>

<span data-ttu-id="ed298-111">Você pode enumerar os tipos de saída de VBR com base em qualidade com suporte para os codecs de áudio.</span><span class="sxs-lookup"><span data-stu-id="ed298-111">You can enumerate the supported quality-based VBR output types for the audio codecs.</span></span> <span data-ttu-id="ed298-112">Você deve usar um dos tipos retornados pelo DMO ao definir o tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="ed298-112">You must use one of the types returned by the DMO when setting the output type.</span></span> <span data-ttu-id="ed298-113">Para obter mais informações, consulte [enumerando tipos de áudio para modos de codificação específicos](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="ed298-113">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="ed298-114">Para configurar um fluxo de vídeo VBR com base na qualidade, você deve definir as propriedades listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed298-114">To configure a quality-based VBR video stream, you must set the properties that are listed in the following table.</span></span>



| <span data-ttu-id="ed298-115">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ed298-115">Property</span></span>                                            | <span data-ttu-id="ed298-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed298-116">Description</span></span>                                                                                                                                             |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed298-117">MFPKEY \_ VBRENABLED</span><span class="sxs-lookup"><span data-stu-id="ed298-117">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="ed298-118">Defina como VARIANT \_ true.</span><span class="sxs-lookup"><span data-stu-id="ed298-118">Set to VARIANT\_TRUE.</span></span>                                                                                                                                   |
| [<span data-ttu-id="ed298-119">MFPKEY \_ VBRQUALITY</span><span class="sxs-lookup"><span data-stu-id="ed298-119">MFPKEY\_VBRQUALITY</span></span>](mfpkey-vbrqualityproperty.md) | <span data-ttu-id="ed298-120">Defina para o valor de qualidade desejado, de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="ed298-120">Set to the desired quality value, from 0 to 100.</span></span> <span data-ttu-id="ed298-121">Nem todos os valores de qualidade representam configurações discretas.</span><span class="sxs-lookup"><span data-stu-id="ed298-121">Not all quality values represent discrete settings.</span></span> <span data-ttu-id="ed298-122">Consulte a descrição da propriedade para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="ed298-122">See the property description for more information.</span></span> |



 

## <a name="configuring-unconstrained-vbr"></a><span data-ttu-id="ed298-123">Configurando a VBR não restringida</span><span class="sxs-lookup"><span data-stu-id="ed298-123">Configuring Unconstrained VBR</span></span>

<span data-ttu-id="ed298-124">A codificação de VBR não restringida permite que o codificador varie o tamanho de amostras individuais sem nenhum limite de buffer explícito.</span><span class="sxs-lookup"><span data-stu-id="ed298-124">Unconstrained VBR encoding enables the encoder to vary the size of individual samples without any explicit buffer limits.</span></span> <span data-ttu-id="ed298-125">No entanto, a taxa média de bits sobre a duração do conteúdo resultante deve ser menor ou igual ao valor especificado.</span><span class="sxs-lookup"><span data-stu-id="ed298-125">However, the average bit rate over the duration of the resulting content must be less than or equal to the specified value.</span></span> <span data-ttu-id="ed298-126">A VBR não restringida requer duas passagens de codificação.</span><span class="sxs-lookup"><span data-stu-id="ed298-126">Unconstrained VBR requires two encoding passes.</span></span>

<span data-ttu-id="ed298-127">Você pode enumerar os tipos de saída de VBR de dois passos com suporte para os codecs de áudio.</span><span class="sxs-lookup"><span data-stu-id="ed298-127">You can enumerate the supported two-pass VBR output types for the audio codecs.</span></span> <span data-ttu-id="ed298-128">Você deve usar um dos tipos retornados pelo DMO ao definir o tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="ed298-128">You must use one of the types returned by the DMO when setting the output type.</span></span> <span data-ttu-id="ed298-129">Para obter mais informações, consulte [enumerando tipos de áudio para modos de codificação específicos](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="ed298-129">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="ed298-130">Para configurar um fluxo de vídeo de taxa de bits variável irrestrita, você deve definir as propriedades listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed298-130">To configure an unconstrained VBR video stream, you must set the properties that are listed in the following table.</span></span>



| <span data-ttu-id="ed298-131">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ed298-131">Property</span></span>                                            | <span data-ttu-id="ed298-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed298-132">Description</span></span>                          |
|-----------------------------------------------------|--------------------------------------|
| [<span data-ttu-id="ed298-133">MFPKEY \_ VBRENABLED</span><span class="sxs-lookup"><span data-stu-id="ed298-133">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="ed298-134">Defina como VARIANT \_ true.</span><span class="sxs-lookup"><span data-stu-id="ed298-134">Set to VARIANT\_TRUE.</span></span>                |
| [<span data-ttu-id="ed298-135">MFPKEY \_ PASSESUSED</span><span class="sxs-lookup"><span data-stu-id="ed298-135">MFPKEY\_PASSESUSED</span></span>](mfpkey-passesusedproperty.md) | <span data-ttu-id="ed298-136">Defina como 2.</span><span class="sxs-lookup"><span data-stu-id="ed298-136">Set to 2.</span></span>                            |
| [<span data-ttu-id="ed298-137">MFPKEY \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="ed298-137">MFPKEY\_RAVG</span></span>](mfpkey-ravgproperty.md)             | <span data-ttu-id="ed298-138">Defina para a taxa de bits média desejada.</span><span class="sxs-lookup"><span data-stu-id="ed298-138">Set to the desired average bit rate.</span></span> |



 

## <a name="configuring-peak-constrained-vbr"></a><span data-ttu-id="ed298-139">Configurando Peak-Constrained VBR</span><span class="sxs-lookup"><span data-stu-id="ed298-139">Configuring Peak-Constrained VBR</span></span>

<span data-ttu-id="ed298-140">A VBR com restrição de pico é como uma VBR não restrita, pois ela é confinada a uma taxa média de bits durante a duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="ed298-140">Peak-constrained VBR is like unconstrained VBR in that it is confined to an average bit rate over the duration of the stream.</span></span> <span data-ttu-id="ed298-141">Além disso, a taxa de bits com restrição de pico está em conformidade com um buffer de pico.</span><span class="sxs-lookup"><span data-stu-id="ed298-141">In addition, peak-constrained VBR conforms to a peak buffer.</span></span> <span data-ttu-id="ed298-142">Esse buffer é descrito usando uma taxa de bits de pico e uma janela de buffer de pico, assim como um buffer de CBR é descrito por uma taxa média de bits e uma janela de buffer.</span><span class="sxs-lookup"><span data-stu-id="ed298-142">This buffer is described using a peak bit rate and a peak buffer window, just as a CBR buffer is described by an average bit rate and a buffer window.</span></span> <span data-ttu-id="ed298-143">Esse modo fornece a flexibilidade do codificador em como ele codifica exemplos individuais enquanto obedece às limitações de pico.</span><span class="sxs-lookup"><span data-stu-id="ed298-143">This mode gives the encoder flexibility in how it encodes individual samples while adhering to the peak limitations.</span></span> <span data-ttu-id="ed298-144">Isso é particularmente útil quando a decodificação é executada por um chip em um dispositivo, como um DVD Player, onde há limitações de hardware que devem ser consideradas.</span><span class="sxs-lookup"><span data-stu-id="ed298-144">This is particularly useful when decoding is performed by a chip in a device, like a DVD player, where there are hardware limitations that must be considered.</span></span>

<span data-ttu-id="ed298-145">Os tipos de saída do codificador de áudio VBR e com restrição de pico têm os mesmos tipos enumerados para a VBR não restrita.</span><span class="sxs-lookup"><span data-stu-id="ed298-145">The supported peak-constrained, VBR audio encoder output types are the same types enumerated for unconstrained VBR.</span></span> <span data-ttu-id="ed298-146">Defina os valores de pico no DMO e use o tipo entregue.</span><span class="sxs-lookup"><span data-stu-id="ed298-146">Set the peak values on the DMO and use the delivered type.</span></span> <span data-ttu-id="ed298-147">Para obter mais informações, consulte [enumerando tipos de áudio para modos de codificação específicos](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="ed298-147">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="ed298-148">Para configurar um fluxo de vídeo VBR com restrição de pico, você deve definir as propriedades listadas na tabela a seguir usando o método **IPropertyBag:: Write** .</span><span class="sxs-lookup"><span data-stu-id="ed298-148">To configure a peak-constrained VBR video stream, you must set the properties that are listed in the following table using the **IPropertyBag::Write** method.</span></span>



| <span data-ttu-id="ed298-149">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ed298-149">Property</span></span>                                            | <span data-ttu-id="ed298-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed298-150">Description</span></span>                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="ed298-151">MFPKEY \_ VBRENABLED</span><span class="sxs-lookup"><span data-stu-id="ed298-151">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="ed298-152">Defina como VARIANT \_ true.</span><span class="sxs-lookup"><span data-stu-id="ed298-152">Set to VARIANT\_TRUE.</span></span>                                           |
| [<span data-ttu-id="ed298-153">MFPKEY \_ PASSESUSED</span><span class="sxs-lookup"><span data-stu-id="ed298-153">MFPKEY\_PASSESUSED</span></span>](mfpkey-passesusedproperty.md) | <span data-ttu-id="ed298-154">Defina como 2.</span><span class="sxs-lookup"><span data-stu-id="ed298-154">Set to 2.</span></span>                                                       |
| [<span data-ttu-id="ed298-155">MFPKEY \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="ed298-155">MFPKEY\_RAVG</span></span>](mfpkey-ravgproperty.md)             | <span data-ttu-id="ed298-156">Defina para a taxa de bits média desejada.</span><span class="sxs-lookup"><span data-stu-id="ed298-156">Set to the desired average bit rate.</span></span>                            |
| [<span data-ttu-id="ed298-157">MFPKEY \_ RMAX</span><span class="sxs-lookup"><span data-stu-id="ed298-157">MFPKEY\_RMAX</span></span>](mfpkey-rmaxproperty.md)             | <span data-ttu-id="ed298-158">Defina para a taxa de bits de pico desejada.</span><span class="sxs-lookup"><span data-stu-id="ed298-158">Set to the desired peak bit rate.</span></span>                               |
| [<span data-ttu-id="ed298-159">MFPKEY \_ BMAX</span><span class="sxs-lookup"><span data-stu-id="ed298-159">MFPKEY\_BMAX</span></span>](mfpkey-bmaxproperty.md)             | <span data-ttu-id="ed298-160">Defina para a janela de buffer que corresponde à taxa de bits de pico.</span><span class="sxs-lookup"><span data-stu-id="ed298-160">Set to the buffer window that corresponds to the peak bit rate.</span></span> |



 

> [!Note]  
> <span data-ttu-id="ed298-161">É recomendável que você defina a taxa de bits de pico para pelo menos duas vezes a taxa média de bits.</span><span class="sxs-lookup"><span data-stu-id="ed298-161">It is recommended that you set the peak bit rate to at least twice the average bit rate.</span></span> <span data-ttu-id="ed298-162">Definir a taxa de pico para um valor mais baixo pode fazer com que o codec Codifique o conteúdo como CBR de duas passagens em vez da taxa de bits de pico restrita.</span><span class="sxs-lookup"><span data-stu-id="ed298-162">Setting the peak rate to a lower value may cause the codec to encode the content as two-pass CBR instead of peak-constrained VBR.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ed298-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed298-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed298-164">Codificações de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="ed298-164">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> <dt>

[<span data-ttu-id="ed298-165">Usando a codificação Two-Pass</span><span class="sxs-lookup"><span data-stu-id="ed298-165">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
</dt> <dt>

[<span data-ttu-id="ed298-166">Trabalhando com áudio</span><span class="sxs-lookup"><span data-stu-id="ed298-166">Working with Audio</span></span>](workingwithaudio.md)
</dt> <dt>

[<span data-ttu-id="ed298-167">Trabalhando com vídeo</span><span class="sxs-lookup"><span data-stu-id="ed298-167">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



