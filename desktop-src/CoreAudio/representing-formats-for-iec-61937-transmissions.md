---
description: Com o aumento nos dispositivos de armazenamento de mídia que exigem formatos de áudio compactados, os aplicativos devem identificar, descrever e usar uma variedade de novos conteúdos de áudio codificados para transmitir conteúdo de PCs para dispositivos como receptores de HDMI ou DisplayPort.
ms.assetid: 86f3396c-b32a-4d70-9f21-e38a745f78bf
title: Representando formatos para transmissões IEC 61937
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0700329aafe7e7bc0e09b532c1ac29b9957ca905
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755821"
---
# <a name="representing-formats-for-iec-61937-transmissions"></a><span data-ttu-id="f2e10-103">Representando formatos para transmissões IEC 61937</span><span class="sxs-lookup"><span data-stu-id="f2e10-103">Representing Formats for IEC 61937 Transmissions</span></span>

<span data-ttu-id="f2e10-104">Com o aumento nos dispositivos de armazenamento de mídia que exigem formatos de áudio compactados, os aplicativos devem identificar, descrever e usar uma variedade de novos conteúdos de áudio codificados para transmitir conteúdo de PCs para dispositivos como receptores de HDMI ou DisplayPort.</span><span class="sxs-lookup"><span data-stu-id="f2e10-104">With the increase in media storage devices that require compressed audio formats, applications must identify, describe, and use a variety of new encoded audio content for transmitting content from PCs to devices such as HDMI or DisplayPort receiver.</span></span>

<span data-ttu-id="f2e10-105">Para representar um fluxo de áudio codificado a ser transmitido em uma interface compatível com IEC 61937, um aplicativo deve fornecer:</span><span class="sxs-lookup"><span data-stu-id="f2e10-105">To represent an encoded audio stream to be transmitted over an IEC 61937-compatible interface, an application must provide:</span></span>

-   <span data-ttu-id="f2e10-106">As características de um fluxo de áudio codificado a ser transmitido.</span><span class="sxs-lookup"><span data-stu-id="f2e10-106">The characteristics of an encoded audio stream to be transmitted.</span></span>

-   <span data-ttu-id="f2e10-107">As características de um fluxo de áudio decodificado no dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="f2e10-107">The characteristics of a decoded audio stream on the target device.</span></span>

<span data-ttu-id="f2e10-108">No Windows Vista e em sistemas operacionais Windows anteriores, um aplicativo pode inferir o nível de qualidade de um formato de áudio a partir do número de canais, do tamanho da amostra e da taxa de dados de um fluxo de áudio que usa o formato.</span><span class="sxs-lookup"><span data-stu-id="f2e10-108">In Windows Vista and earlier Windows operating systems, an application can infer the quality level of an audio format from the number of channels, the sample size, and the data rate of an audio stream that uses the format.</span></span> <span data-ttu-id="f2e10-109">Para um formato PCM, essas informações estão disponíveis nos membros **nChannels**, **nSamplesPerSec** e **nAvgBytesPerSec** da estrutura **WAVEFORMATEX** que especifica o formato.</span><span class="sxs-lookup"><span data-stu-id="f2e10-109">For a PCM format, this information is available from the **nChannels**, **nSamplesPerSec**, and **nAvgBytesPerSec** members of the **WAVEFORMATEX** structure that specifies the format.</span></span> <span data-ttu-id="f2e10-110">Para um formato não PCM, esses três membros foram commandeered para armazenar informações sobre os dados compactados no fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="f2e10-110">For a non-PCM format, these three members have been commandeered to store information about the compressed data in the audio stream.</span></span> <span data-ttu-id="f2e10-111">Assim, a estrutura **WAVEFORMATEX** não tem informações sobre o número efetivo de canais, o tamanho da amostra e a taxa de dados do fluxo de áudio não PCM após o fluxo ser descompactado e reproduzido.</span><span class="sxs-lookup"><span data-stu-id="f2e10-111">Thus, the **WAVEFORMATEX** structure lacks information about the effective number of channels, sample size, and data rate of the non-PCM audio stream after the stream is decompressed and played.</span></span> <span data-ttu-id="f2e10-112">Com base nas informações dessa estrutura, um usuário ou um aplicativo pode ter dificuldade em inferir o nível de qualidade do fluxo não PCM.</span><span class="sxs-lookup"><span data-stu-id="f2e10-112">Based on the information in this structure, a user or an application might have difficulty inferring the quality level of the non-PCM stream.</span></span>

<span data-ttu-id="f2e10-113">O **WAVEFORMATEX** foi estendido para a estrutura **WAVEFORMATEXTENSIBLE** para fornecer as características do fluxo extra.</span><span class="sxs-lookup"><span data-stu-id="f2e10-113">The **WAVEFORMATEX** was extended to the **WAVEFORMATEXTENSIBLE** structure to provide the extra stream characteristics.</span></span> <span data-ttu-id="f2e10-114">No entanto, essa estrutura também não é adequada para descrever o fluxo de transmissões IEC 61937 porque ela pretendia representar um único conjunto de características e é usada para dados PCM não compactados de vários canais.</span><span class="sxs-lookup"><span data-stu-id="f2e10-114">However, this structure is also not adequate in describing the stream for IEC 61937 transmissions because it was intended to represent a single set of characteristics and used for uncompressed, multi-channel PCM data.</span></span>

<span data-ttu-id="f2e10-115">No Windows 7, o sistema operacional resolve esse problema fornecendo suporte a uma nova estrutura, **WAVEFORMATEXTENSIBLE \_ IEC61937** , que estende a estrutura **WAVEFORMATEXTENSIBLE** para armazenar dois conjuntos de características de fluxo de áudio: o formato de áudio codificado antes da transmissão e das características do fluxo de áudio depois que ele é decodificado.</span><span class="sxs-lookup"><span data-stu-id="f2e10-115">In Windows 7, the operating system addresses this problem by providing support for a new structure, **WAVEFORMATEXTENSIBLE\_IEC61937** which extends **WAVEFORMATEXTENSIBLE** structure to store two sets of audio stream characteristics: the encoded audio format before transmission and characteristics of the audio stream after it has been decoded.</span></span> <span data-ttu-id="f2e10-116">A nova estrutura especifica explicitamente o número efetivo de canais, o tamanho da amostra e a taxa de dados de um formato não PCM.</span><span class="sxs-lookup"><span data-stu-id="f2e10-116">The new structure explicitly specifies the effective number of channels, sample size, and data rate of a non-PCM format.</span></span> <span data-ttu-id="f2e10-117">Com essas informações, um aplicativo pode inferir o nível de qualidade do fluxo não PCM depois de ser descompactado e reproduzido.</span><span class="sxs-lookup"><span data-stu-id="f2e10-117">With this information, an application can infer the quality level of the non-PCM stream after it is decompressed and played.</span></span>

<span data-ttu-id="f2e10-118">A estrutura **WAVEFORMATEXTENSIBLE \_ IEC61937** é declarada no cabeçalho KsMedia. h incluído no SDK do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f2e10-118">The **WAVEFORMATEXTENSIBLE\_IEC61937** structure is declared in the KsMedia.h header included with the Windows 7 SDK.</span></span> <span data-ttu-id="f2e10-119">O membro **FormatExt** é a estrutura **WAVEFORMATEXTENSIBLE** que armazena as características do fluxo a ser transmitido.</span><span class="sxs-lookup"><span data-stu-id="f2e10-119">The **FormatExt** member is the **WAVEFORMATEXTENSIBLE** structure that stores the characteristics of the stream to be transmitted.</span></span> <span data-ttu-id="f2e10-120">O membro **Format** da estrutura **WAVEFORMATEXTENSIBLE** é a estrutura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="f2e10-120">The **Format** member of the **WAVEFORMATEXTENSIBLE** structure is the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="f2e10-121">O conteúdo desse **WAVEFORMATEX** e **WAVEFORMATEXTENSIBLE** indicam a um aplicativo se a estrutura pode ser interpretada como uma estrutura **WAVEFORMATEXTENSIBLE \_ IEC61937** .</span><span class="sxs-lookup"><span data-stu-id="f2e10-121">The contents of this **WAVEFORMATEX** and **WAVEFORMATEXTENSIBLE** indicate to an application whether the structure can be interpreted as a **WAVEFORMATEXTENSIBLE\_IEC61937** structure.</span></span> <span data-ttu-id="f2e10-122">Para uma estrutura **WAVEFORMATEXTENSIBLE \_ IEC61937** :</span><span class="sxs-lookup"><span data-stu-id="f2e10-122">For a **WAVEFORMATEXTENSIBLE\_IEC61937** structure:</span></span>

-   <span data-ttu-id="f2e10-123">O membro **wFormatTag** de **WAVEFORMATEX** deve conter \_ formato Wave \_ extensível ( `FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE` ).</span><span class="sxs-lookup"><span data-stu-id="f2e10-123">The **wFormatTag** member of **WAVEFORMATEX** must contain WAVE\_FORMAT\_EXTENSIBLE (`FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE`).</span></span>

-   <span data-ttu-id="f2e10-124">O membro **Subformal** da estrutura **WAVEFORMATEXTENSIBLE** especifica o GUID do formato codificado a ser transmitido.</span><span class="sxs-lookup"><span data-stu-id="f2e10-124">The **SubFormat** member of the **WAVEFORMATEXTENSIBLE** structure specifies the GUID of the encoded format to be transmitted.</span></span> <span data-ttu-id="f2e10-125">Por exemplo, `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` indica o formato Dolby Digital Plus.</span><span class="sxs-lookup"><span data-stu-id="f2e10-125">For example, `FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL` indicates the Dolby Digital Plus format.</span></span> <span data-ttu-id="f2e10-126">Para obter os GUIDs com suporte, consulte GUIDs de subformato.</span><span class="sxs-lookup"><span data-stu-id="f2e10-126">For the supported GUIDs, see SubFormat GUIDs.</span></span>

-   <span data-ttu-id="f2e10-127">O tamanho indicado pelo membro **cbSize** de WAVEFORMATEX é de 34 bytes.</span><span class="sxs-lookup"><span data-stu-id="f2e10-127">The size indicated by **cbSize** member of the WAVEFORMATEX is 34 bytes.</span></span> <span data-ttu-id="f2e10-128">(`FormatExt.Format.cbSize = 34`).</span><span class="sxs-lookup"><span data-stu-id="f2e10-128">(`FormatExt.Format.cbSize = 34`).</span></span> <span data-ttu-id="f2e10-129">O tamanho total de **WAVEFORMATEXTENSIBLE \_ IEC61937** é de 52 bytes.</span><span class="sxs-lookup"><span data-stu-id="f2e10-129">The total size of **WAVEFORMATEXTENSIBLE\_IEC61937** is 52 bytes.</span></span>

<span data-ttu-id="f2e10-130">Os membros **dwEncodedSamplesPerSec**, **dwEncodedChannelCount** e **dwAverageBytesPerSec** de **WAVEFORMATEXTENSIBLE \_ IEC61937** descrevem a taxa de amostragem, o número de canais e a taxa de bits em bytes do fluxo do fluxo de áudio depois que ele é decodificado.</span><span class="sxs-lookup"><span data-stu-id="f2e10-130">The **dwEncodedSamplesPerSec**, **dwEncodedChannelCount**, and **dwAverageBytesPerSec** members of **WAVEFORMATEXTENSIBLE\_IEC61937** describe the sampling rate, number of channels, and bit rate in bytes of the stream of the audio stream after it has been decoded.</span></span>

## <a name="subformat-guids"></a><span data-ttu-id="f2e10-131">GUIDs de subformatação</span><span class="sxs-lookup"><span data-stu-id="f2e10-131">SubFormat GUIDs</span></span>

<span data-ttu-id="f2e10-132">No Windows 7, o cabeçalho KsMedia. h contém definições para os GUIDs de subformato para os formatos de áudio compactados definidos por CEA-861-D.</span><span class="sxs-lookup"><span data-stu-id="f2e10-132">In Windows 7, the KsMedia.h header contains definitions for the SubFormat GUIDs for the compressed audio formats defined by CEA-861-D.</span></span> <span data-ttu-id="f2e10-133">Os GUIDs são especificados no membro de subformato do **WAVEFORMATEXTENSIBLE**, especificado no membro **FormatExt** da estrutura **WAVEFORMATEXTENSIBLE \_ IEC61937** ( `WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat` ).</span><span class="sxs-lookup"><span data-stu-id="f2e10-133">The GUIDs are specified in the SubFormat member of the **WAVEFORMATEXTENSIBLE**, specified in the **FormatExt** member of the **WAVEFORMATEXTENSIBLE\_IEC61937** structure (`WAVEFORMATEXTENSIBLE_IEC61937.FormatExt.Subformat`).</span></span>

<span data-ttu-id="f2e10-134">Os GUIDs para os formatos de áudio compactados que estão disponíveis como formatos de áudio codificados Standard IEC 61937 são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2e10-134">The GUIDs for the compressed audio formats that are available as standard IEC 61937 encoded audio formats are listed in the following table.</span></span> <span data-ttu-id="f2e10-135">Esses formatos são semelhantes às representações existentes de codificação ativa 3 (AC-3) e de som digital Theater (DTS) no Windows.</span><span class="sxs-lookup"><span data-stu-id="f2e10-135">These formats are similar to the existing Active Coding 3 (AC-3) and Digital Theater Sound (DTS) formats representations in Windows.</span></span>



| <span data-ttu-id="f2e10-136">Tipo CEA 861</span><span class="sxs-lookup"><span data-stu-id="f2e10-136">CEA 861 Type</span></span> | <span data-ttu-id="f2e10-137">GUID do subformato</span><span class="sxs-lookup"><span data-stu-id="f2e10-137">SubFormat GUID</span></span>                                                                                                          | <span data-ttu-id="f2e10-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2e10-138">Description</span></span>                                  |
|--------------|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="f2e10-139">0x00</span><span class="sxs-lookup"><span data-stu-id="f2e10-139">0x00</span></span>         |                                                                                                                         | <span data-ttu-id="f2e10-140">Consulte o fluxo.</span><span class="sxs-lookup"><span data-stu-id="f2e10-140">Refer to the stream.</span></span>                         |
| <span data-ttu-id="f2e10-141">0x01</span><span class="sxs-lookup"><span data-stu-id="f2e10-141">0x01</span></span>         | <span data-ttu-id="f2e10-142">00000000-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="f2e10-142">00000000-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="f2e10-143">KSDATAFORMAT \_ subtipo \_ WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="f2e10-143">KSDATAFORMAT\_SUBTYPE\_WAVEFORMATEX</span></span><br/>                          | <span data-ttu-id="f2e10-144">PCM IEC 60958</span><span class="sxs-lookup"><span data-stu-id="f2e10-144">IEC 60958 PCM</span></span>                                |
| <span data-ttu-id="f2e10-145">0x02</span><span class="sxs-lookup"><span data-stu-id="f2e10-145">0x02</span></span>         | <span data-ttu-id="f2e10-146">00000092-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="f2e10-146">00000092-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="f2e10-147">KSDATAFORMAT \_ subtipo \_ IEC61937 \_ Dolby \_ digital</span><span class="sxs-lookup"><span data-stu-id="f2e10-147">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL</span></span><br/>              | <span data-ttu-id="f2e10-148">AC-3</span><span class="sxs-lookup"><span data-stu-id="f2e10-148">AC-3</span></span>                                         |
| <span data-ttu-id="f2e10-149">0x03</span><span class="sxs-lookup"><span data-stu-id="f2e10-149">0x03</span></span>         | <span data-ttu-id="f2e10-150">00000003-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="f2e10-150">00000003-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="f2e10-151">KSDATAFORMAT \_ subtipo \_ IEC61937 \_ MPEG1</span><span class="sxs-lookup"><span data-stu-id="f2e10-151">KSDATAFORMAT\_SUBTYPE\_IEC61937\_MPEG1</span></span><br/>                       | <span data-ttu-id="f2e10-152">MPEG-1 (camada 1 & 2)</span><span class="sxs-lookup"><span data-stu-id="f2e10-152">MPEG-1 (Layer 1 & 2)</span></span>                         |
| <span data-ttu-id="f2e10-153">0x04</span><span class="sxs-lookup"><span data-stu-id="f2e10-153">0x04</span></span>         | <span data-ttu-id="f2e10-154">00000004-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="f2e10-154">00000004-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="f2e10-155">KSDATAFORMAT \_ subtipo \_ IEC61937 \_ MPEG3</span><span class="sxs-lookup"><span data-stu-id="f2e10-155">KSDATAFORMAT\_SUBTYPE\_IEC61937\_MPEG3</span></span><br/>                       | <span data-ttu-id="f2e10-156">MPEG-3 (camada 3)</span><span class="sxs-lookup"><span data-stu-id="f2e10-156">MPEG-3 (Layer 3)</span></span>                             |
| <span data-ttu-id="f2e10-157">0x05</span><span class="sxs-lookup"><span data-stu-id="f2e10-157">0x05</span></span>         | <span data-ttu-id="f2e10-158">00000005-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="f2e10-158">00000005-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="f2e10-159">KSDATAFORMAT \_ subtipo \_ IEC61937 \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="f2e10-159">KSDATAFORMAT\_SUBTYPE\_IEC61937\_MPEG2</span></span> <br/>                      | <span data-ttu-id="f2e10-160">MPEG-2 (multicanal)</span><span class="sxs-lookup"><span data-stu-id="f2e10-160">MPEG-2(multichannel)</span></span>                         |
| <span data-ttu-id="f2e10-161">0x06</span><span class="sxs-lookup"><span data-stu-id="f2e10-161">0x06</span></span>         | <span data-ttu-id="f2e10-162">00000006-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="f2e10-162">00000006-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="f2e10-163">KSDATAFORMAT \_ subtipo \_ IEC61937 \_ AAC</span><span class="sxs-lookup"><span data-stu-id="f2e10-163">KSDATAFORMAT\_SUBTYPE\_IEC61937\_AAC</span></span><br/>                         | <span data-ttu-id="f2e10-164">Codificação avançada de áudio (MPEG-2/4 AAC em ADTS)</span><span class="sxs-lookup"><span data-stu-id="f2e10-164">Advanced Audio Coding (MPEG-2/4 AAC in ADTS)</span></span> |
| <span data-ttu-id="f2e10-165">0x07</span><span class="sxs-lookup"><span data-stu-id="f2e10-165">0x07</span></span>         | <span data-ttu-id="f2e10-166">00000008-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="f2e10-166">00000008-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="f2e10-167">KSDATAFORMAT \_ subtipo \_ IEC61937 \_ Dts</span><span class="sxs-lookup"><span data-stu-id="f2e10-167">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTS</span></span><br/>                         | <span data-ttu-id="f2e10-168">DTS</span><span class="sxs-lookup"><span data-stu-id="f2e10-168">DTS</span></span>                                          |
| <span data-ttu-id="f2e10-169">0x0A</span><span class="sxs-lookup"><span data-stu-id="f2e10-169">0x0a</span></span>         | <span data-ttu-id="f2e10-170">0000000a-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="f2e10-170">0000000a-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="f2e10-171">KSDATAFORMAT \_ subtipo \_ IEC61937 \_ Dolby \_ digital \_ Plus</span><span class="sxs-lookup"><span data-stu-id="f2e10-171">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS</span></span><br/>        | <span data-ttu-id="f2e10-172">Dolby Digital Plus</span><span class="sxs-lookup"><span data-stu-id="f2e10-172">Dolby Digital Plus</span></span>                           |
| <span data-ttu-id="f2e10-173">0x0A</span><span class="sxs-lookup"><span data-stu-id="f2e10-173">0x0a</span></span>         | <span data-ttu-id="f2e10-174">0000010a-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="f2e10-174">0000010a-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="f2e10-175">KSDATAFORMAT \_ subtipo \_ IEC61937 \_ Dolby \_ digital \_ Plus \_ Atmos</span><span class="sxs-lookup"><span data-stu-id="f2e10-175">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS\_ATMOS</span></span><br/> | <span data-ttu-id="f2e10-176">Dolby Atmos codificado com Dolby Digital Plus</span><span class="sxs-lookup"><span data-stu-id="f2e10-176">Dolby Atmos encoded with Dolby Digital Plus</span></span>  |
| <span data-ttu-id="f2e10-177">0x0f</span><span class="sxs-lookup"><span data-stu-id="f2e10-177">0x0f</span></span>         |                                                                                                                         | <span data-ttu-id="f2e10-178">Não usado reservado</span><span class="sxs-lookup"><span data-stu-id="f2e10-178">Unused Reserved</span></span>                              |



 

<span data-ttu-id="f2e10-179">Os GUIDs dos formatos de áudio compactados que são transmitidos em pacotes de exemplo de alta taxa de bits são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2e10-179">The GUIDs for the compressed audio formats that are transmitted in high bit-rate audio sample packets are listed in the following table.</span></span>



| <span data-ttu-id="f2e10-180">Tipo CEA 861</span><span class="sxs-lookup"><span data-stu-id="f2e10-180">CEA 861 Type</span></span> | <span data-ttu-id="f2e10-181">GUID do subformato</span><span class="sxs-lookup"><span data-stu-id="f2e10-181">SubFormat GUID</span></span>                                                                                           | <span data-ttu-id="f2e10-182">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2e10-182">Description</span></span>                                                                                                                     |
|--------------|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e10-183">0x0b</span><span class="sxs-lookup"><span data-stu-id="f2e10-183">0x0b</span></span>         | <span data-ttu-id="f2e10-184">0000000b-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="f2e10-184">0000000b-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="f2e10-185">\_SUBTIPO KSDATAFORMAT \_ IEC61937 \_ DTS \_ HD</span><span class="sxs-lookup"><span data-stu-id="f2e10-185">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DTS\_HD</span></span><br/>      | <span data-ttu-id="f2e10-186">DTS-HD (96Khz de 24 bits)</span><span class="sxs-lookup"><span data-stu-id="f2e10-186">DTS-HD (24-bit, 96Khz)</span></span>                                                                                                          |
| <span data-ttu-id="f2e10-187">0x0c</span><span class="sxs-lookup"><span data-stu-id="f2e10-187">0x0c</span></span>         | <span data-ttu-id="f2e10-188">0000000c-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="f2e10-188">0000000c-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="f2e10-189">\_SUBTIPO KSDATAFORMAT \_ IEC61937 \_ Dolby \_ MLP</span><span class="sxs-lookup"><span data-stu-id="f2e10-189">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_MLP</span></span><br/>   | <span data-ttu-id="f2e10-190">Dolby-esteira 1,0:</span><span class="sxs-lookup"><span data-stu-id="f2e10-190">Dolby MAT 1.0:</span></span><br/> <span data-ttu-id="f2e10-191">Dolby TrueHD (MLP – embalagem do meridiano sem perdas) – 192KHz de 24 bits/até 18 Mbps, 8 canais)</span><span class="sxs-lookup"><span data-stu-id="f2e10-191">Dolby TrueHD (MLP – Meridian Lossless Packing) – 24-bit 192KHz/up to 18 Mbps, 8 channels)</span></span> <br/> |
| <span data-ttu-id="f2e10-192">0x0c</span><span class="sxs-lookup"><span data-stu-id="f2e10-192">0x0c</span></span>         | <span data-ttu-id="f2e10-193">0000010c-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="f2e10-193">0000010c-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="f2e10-194">KSDATAFORMAT \_ subtipo \_ IEC61937 \_ Dolby \_ MAT20</span><span class="sxs-lookup"><span data-stu-id="f2e10-194">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_MAT20</span></span><br/> | <span data-ttu-id="f2e10-195">Dolby-esteira 2,0:</span><span class="sxs-lookup"><span data-stu-id="f2e10-195">Dolby MAT 2.0:</span></span> <br/> <span data-ttu-id="f2e10-196">Dolby TrueHD – 192KHz de 24 bits/até 18 Mbps, 8 canais ou LPCM até 24 Mbps.</span><span class="sxs-lookup"><span data-stu-id="f2e10-196">Dolby TrueHD – 24-bit 192KHz/up to 18 Mbps, 8 channels, or LPCM up to 24 Mbps.</span></span> <br/>           |
| <span data-ttu-id="f2e10-197">0x0c</span><span class="sxs-lookup"><span data-stu-id="f2e10-197">0x0c</span></span>         | <span data-ttu-id="f2e10-198">0000030c-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="f2e10-198">0000030c-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="f2e10-199">KSDATAFORMAT \_ subtipo \_ IEC61937 \_ Dolby \_ MAT21</span><span class="sxs-lookup"><span data-stu-id="f2e10-199">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_MAT21</span></span><br/> | <span data-ttu-id="f2e10-200">Dolby-esteira 2,1:</span><span class="sxs-lookup"><span data-stu-id="f2e10-200">Dolby MAT 2.1:</span></span> <br/> <span data-ttu-id="f2e10-201">Dolby TrueHD – 192KHz de 24 bits/até 18 Mbps, 8 canais ou LPCM até 24 Mbps.</span><span class="sxs-lookup"><span data-stu-id="f2e10-201">Dolby TrueHD – 24-bit 192KHz/up to 18 Mbps, 8 channels, or LPCM up to 24 Mbps.</span></span> <br/>           |
| <span data-ttu-id="f2e10-202">0x0e</span><span class="sxs-lookup"><span data-stu-id="f2e10-202">0x0e</span></span>         | <span data-ttu-id="f2e10-203">00000164-0000-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="f2e10-203">00000164-0000-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="f2e10-204">\_SUBTIPO KSDATAFORMAT \_ IEC61937 \_ WMA \_ pro</span><span class="sxs-lookup"><span data-stu-id="f2e10-204">KSDATAFORMAT\_SUBTYPE\_IEC61937\_WMA\_PRO</span></span><br/>     | <span data-ttu-id="f2e10-205">Windows Media Audio (WMA) pro</span><span class="sxs-lookup"><span data-stu-id="f2e10-205">Windows Media Audio (WMA) Pro</span></span>                                                                                                   |



 

<span data-ttu-id="f2e10-206">O driver de classe de áudio HD fornecido pela Microsoft dá suporte aos formatos PCM, AC3, DTS, AAC, Dolby Digital Plus, WMA pro, com passe-partout (MLP).</span><span class="sxs-lookup"><span data-stu-id="f2e10-206">Microsoft-provided HD Audio class driver supports PCM, AC3, DTS, AAC, Dolby Digital Plus, WMA Pro, MAT(MLP) formats.</span></span> <span data-ttu-id="f2e10-207">Os GUIDs dos formatos de áudio compactados que não têm suporte do driver de classe de HD Audio e podem ser implementados por soluções de terceiros são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2e10-207">The GUIDs for the compressed audio formats that are not supported by the HD audio class driver and can be implemented by third-party solutions are listed in the following table.</span></span>



| <span data-ttu-id="f2e10-208">Tipo CEA 861</span><span class="sxs-lookup"><span data-stu-id="f2e10-208">CEA 861 Type</span></span> | <span data-ttu-id="f2e10-209">GUID do subformato</span><span class="sxs-lookup"><span data-stu-id="f2e10-209">SubFormat GUID</span></span>                                                                                              | <span data-ttu-id="f2e10-210">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2e10-210">Description</span></span>                                                                    |
|--------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="f2e10-211">0x08</span><span class="sxs-lookup"><span data-stu-id="f2e10-211">0x08</span></span>         | <span data-ttu-id="f2e10-212">00000008-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="f2e10-212">00000008-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="f2e10-213">KSDATAFORMAT \_ subtipo \_ IEC61937 \_ ATRAC</span><span class="sxs-lookup"><span data-stu-id="f2e10-213">KSDATAFORMAT\_SUBTYPE\_IEC61937\_ATRAC</span></span><br/>           | <span data-ttu-id="f2e10-214">Codificação acústica de transformação adaptável (ATRAC)</span><span class="sxs-lookup"><span data-stu-id="f2e10-214">Adaptive Transform Acoustic Coding (ATRAC)</span></span>                                     |
| <span data-ttu-id="f2e10-215">0x09</span><span class="sxs-lookup"><span data-stu-id="f2e10-215">0x09</span></span>         | <span data-ttu-id="f2e10-216">00000009-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="f2e10-216">00000009-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="f2e10-217">KSDATAFORMAT \_ subtipo \_ IEC61937 \_ áudio de um \_ bit \_</span><span class="sxs-lookup"><span data-stu-id="f2e10-217">KSDATAFORMAT\_SUBTYPE\_IEC61937\_ONE\_BIT\_AUDIO</span></span><br/> | <span data-ttu-id="f2e10-218">One-Bit áudio</span><span class="sxs-lookup"><span data-stu-id="f2e10-218">One-Bit Audio</span></span>                                                                  |
| <span data-ttu-id="f2e10-219">0x0D</span><span class="sxs-lookup"><span data-stu-id="f2e10-219">0x0d</span></span>         | <span data-ttu-id="f2e10-220">0000000d-0cea-0010-8000-00aa00389b71</span><span class="sxs-lookup"><span data-stu-id="f2e10-220">0000000d-0cea-0010-8000-00aa00389b71</span></span><br/> <span data-ttu-id="f2e10-221">KSDATAFORMAT \_ subtipo \_ IEC61937 \_ DST</span><span class="sxs-lookup"><span data-stu-id="f2e10-221">KSDATAFORMAT\_SUBTYPE\_IEC61937\_DST</span></span><br/>             | <span data-ttu-id="f2e10-222">DST (Direct Stream Transport) – DSD compactado sem perdas (Direct Stream digital).</span><span class="sxs-lookup"><span data-stu-id="f2e10-222">Direct Stream Transport (DST)—lossless compressed DSD (Direct Stream Digital).</span></span> |



 

## <a name="dolby-digital-plus-format"></a><span data-ttu-id="f2e10-223">Formato Dolby Digital Plus</span><span class="sxs-lookup"><span data-stu-id="f2e10-223">Dolby Digital Plus Format</span></span>

<span data-ttu-id="f2e10-224">Quando o conteúdo Dolby Digital Plus é transmitido pelo IEC 60958, a taxa de amostragem de link deve ser quatro vezes a taxa de amostragem do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="f2e10-224">When Dolby Digital Plus content is transmitted over IEC 60958, the link-sampling rate must be four times the sampling rate of the content.</span></span> <span data-ttu-id="f2e10-225">O Dolby Digital Plus dá suporte a taxas de exemplo de conteúdo de 32 KHz, 44,1 KHz e 48 KHz.</span><span class="sxs-lookup"><span data-stu-id="f2e10-225">Dolby Digital Plus supports content sample rates of 32 KHz, 44.1 KHz, and 48 KHz.</span></span> <span data-ttu-id="f2e10-226">Interfaces como HDMI não dão suporte a 128 KHz (32 KHz x 4), de modo que apenas taxas de amostra de conteúdo 44,1 e 48 KHz podem ter suporte.</span><span class="sxs-lookup"><span data-stu-id="f2e10-226">Interfaces such as HDMI do not support 128 KHz (32 KHz x 4), so only 44.1 and 48 KHz content sample rates can be supported.</span></span>

<span data-ttu-id="f2e10-227">Os valores definidos por um aplicativo na estrutura WAVEFORMATEXTENSIBLE \_ IEC61937 para representar o formato Dolby Digital Plus a uma taxa de amostra de conteúdo de 48 kHz são mostrados no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2e10-227">The values set by an application in the WAVEFORMATEXTENSIBLE\_IEC61937 structure to represent Dolby Digital Plus format at a content sample rate of 48 KHz are shown in the following example.</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;              // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 192000;    // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 768000;   // 192 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;            // 16 bits * 2 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;        // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                // Indicates that Format is part of a 
                                                   // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // Dolby 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL_PLUS;
wfext.dwEncodedSamplesPerSec = 48000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="dolby-truehd-mat"></a><span data-ttu-id="f2e10-228">Dolby TrueHD (passe-partout)</span><span class="sxs-lookup"><span data-stu-id="f2e10-228">Dolby TrueHD (MAT)</span></span>

<span data-ttu-id="f2e10-229">O conteúdo Dolby TrueHD é transmitido por meio de IEC 60958 em canais 176,4 kHz/8 (exigindo uma taxa de quadros IEC 60958 de 705,6 kHz) para taxas de amostra de conteúdo de 44,1, 88,2 e 176,4 kHz e 192 canais kHz/8 (exigindo uma taxa de quadros IEC 60958 de 768 kHz) para taxas de exemplo de conteúdo de 48, 96 e 192 kHz.</span><span class="sxs-lookup"><span data-stu-id="f2e10-229">Dolby TrueHD content is transmitted over IEC 60958 at 176.4 kHz / 8 channels (requiring an IEC 60958 frame rate of 705.6 kHz) for content sample rates of 44.1, 88.2 and 176.4 kHz, and 192 kHz / 8 channels (requiring an IEC 60958 frame rate of 768 kHz) for content sample rates of 48, 96 and 192 kHz.</span></span>

<span data-ttu-id="f2e10-230">Os valores definidos por um aplicativo na estrutura WAVEFORMATEXTENSIBLE \_ IEC61937 para representar o Dolby TrueHD em uma taxa de amostra de conteúdo de 96 kHz são mostrados nos exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2e10-230">The values set by an application in the WAVEFORMATEXTENSIBLE\_IEC61937 structure to represent Dolby TrueHD at a content sample rate of 96 KHz are shown in the following examples.</span></span>

<span data-ttu-id="f2e10-231">Dolby-esteira 1,0</span><span class="sxs-lookup"><span data-stu-id="f2e10-231">Dolby MAT 1.0</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MLP; // This structure indicates MLP (MAT 1.0) support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



<span data-ttu-id="f2e10-232">Dolby-esteira 2,0</span><span class="sxs-lookup"><span data-stu-id="f2e10-232">Dolby MAT 2.0</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT20; // This structure indicates MAT 2.0 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



<span data-ttu-id="f2e10-233">Dolby-esteira 2,1</span><span class="sxs-lookup"><span data-stu-id="f2e10-233">Dolby MAT 2.1</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 8;                // Four IEC 60958 Lines.
wfext.FormatExt.Format.nSamplesPerSec = 192000;      // Link runs at 192 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 3072000;    // 192 KHz * 16.
wfext.FormatExt.Format.nBlockAlign = 16;             // 16-bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;          // Always at 16 bits over IEC 60958.
wfext.FormatExt.Format.cbSize = 34;                  // Indicates that Format is part of a 
                                                     // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_7POINT1;    // Dolby 7.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_MAT21; // This structure indicates MAT 2.1 support.
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 8;                            // Encoded data contains 8 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



> [!Note]  
> <span data-ttu-id="f2e10-234">O suporte para uma versão do Dolby enquadrant não significa suporte para Dolbyout com um número de versão inferior.</span><span class="sxs-lookup"><span data-stu-id="f2e10-234">Support for one version of Dolby MAT does not imply support for Dolby MAT with a lower version number.</span></span> <span data-ttu-id="f2e10-235">Como o Dolby enquadramento 2,1 é compatível com versões anteriores do Dolbyout, um driver de classe que indica suporte para Dolby enquadrable 2,1 normalmente também indicará suporte para Dolby enquadrable 2,0 e Dolby PASSEs 1,0, usando uma \_ estrutura IEC61937 WAVEFORMATEXTENSIBLE separada para cada versão.</span><span class="sxs-lookup"><span data-stu-id="f2e10-235">Since Dolby MAT 2.1 is backwards compatible with previous versions of Dolby MAT, a class driver that indicates support for Dolby MAT 2.1 will typically also indicate support for Dolby MAT 2.0 and Dolby MAT 1.0, using a separate WAVEFORMATEXTENSIBLE\_IEC61937 structure for each version.</span></span>

 

## <a name="wma-pro"></a><span data-ttu-id="f2e10-236">WMA Pro</span><span class="sxs-lookup"><span data-stu-id="f2e10-236">WMA Pro</span></span>

<span data-ttu-id="f2e10-237">O conteúdo de áudio do WMA pro pode ser codificado em um dos quatro perfis listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2e10-237">WMA Pro audio content can be encoded in one of the four profiles listed in the following table.</span></span>



| <span data-ttu-id="f2e10-238">Perfil</span><span class="sxs-lookup"><span data-stu-id="f2e10-238">Profile</span></span> | <span data-ttu-id="f2e10-239">Propriedade-valor</span><span class="sxs-lookup"><span data-stu-id="f2e10-239">Property - Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="f2e10-240">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2e10-240">Description</span></span>                                                                                                                         |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e10-241">M0</span><span class="sxs-lookup"><span data-stu-id="f2e10-241">M0</span></span>      | <span data-ttu-id="f2e10-242">Taxa de bits máxima – 192000 bps</span><span class="sxs-lookup"><span data-stu-id="f2e10-242">Maximum bit rate – 192000 bps</span></span> <br/> <span data-ttu-id="f2e10-243">Taxa de amostragem máxima – 48 KHz</span><span class="sxs-lookup"><span data-stu-id="f2e10-243">Maximum sampling rate – 48 KHz</span></span> <br/> <span data-ttu-id="f2e10-244">Contagem máxima de canais – 2</span><span class="sxs-lookup"><span data-stu-id="f2e10-244">Maximum channel count – 2</span></span> <br/> <span data-ttu-id="f2e10-245">Tamanho máximo do buffer – 600 \* 1024 bits</span><span class="sxs-lookup"><span data-stu-id="f2e10-245">Maximum buffer size – 600\*1024 bits</span></span> <br/> <span data-ttu-id="f2e10-246">Máximo de amostras por quadro – 2048</span><span class="sxs-lookup"><span data-stu-id="f2e10-246">Maximum samples per frame – 2048</span></span> <br/> <span data-ttu-id="f2e10-247">Máximo de bits por quadro-655536</span><span class="sxs-lookup"><span data-stu-id="f2e10-247">Maximum bits per frame - 655536</span></span><br/>   | <span data-ttu-id="f2e10-248">Recomendado para música e streaming over-the-Air.</span><span class="sxs-lookup"><span data-stu-id="f2e10-248">Recommended for over-the-air music and streaming.</span></span><br/> <span data-ttu-id="f2e10-249">A taxa máxima de bits em um quadro de áudio é de 1536000 bps.</span><span class="sxs-lookup"><span data-stu-id="f2e10-249">Maximum bit rate in an audio frame is 1536000 bps.</span></span><br/>          |
| <span data-ttu-id="f2e10-250">M1</span><span class="sxs-lookup"><span data-stu-id="f2e10-250">M1</span></span>      | <span data-ttu-id="f2e10-251">Taxa de bits máxima – 385000 bps</span><span class="sxs-lookup"><span data-stu-id="f2e10-251">Maximum bit rate – 385000 bps</span></span> <br/> <span data-ttu-id="f2e10-252">Taxa de amostragem máxima – 48 KHz</span><span class="sxs-lookup"><span data-stu-id="f2e10-252">Maximum sampling rate – 48 KHz</span></span> <br/> <span data-ttu-id="f2e10-253">Contagem máxima de canais – 6</span><span class="sxs-lookup"><span data-stu-id="f2e10-253">Maximum channel count – 6</span></span> <br/> <span data-ttu-id="f2e10-254">Tamanho máximo do buffer – 600 \* 1024 bits</span><span class="sxs-lookup"><span data-stu-id="f2e10-254">Maximum buffer size – 600\*1024 bits</span></span> <br/> <span data-ttu-id="f2e10-255">Máximo de amostras por quadro – 4096</span><span class="sxs-lookup"><span data-stu-id="f2e10-255">Maximum samples per frame – 4096</span></span> <br/> <span data-ttu-id="f2e10-256">Máximo de bits por quadro-131072</span><span class="sxs-lookup"><span data-stu-id="f2e10-256">Maximum bits per frame - 131072</span></span><br/>   | <span data-ttu-id="f2e10-257">Recomendado para filmes de definição padrão Surround-Sound.</span><span class="sxs-lookup"><span data-stu-id="f2e10-257">Recommended for surround-sound standard definition movies.</span></span><br/> <span data-ttu-id="f2e10-258">A taxa máxima de bits em um quadro de áudio é de 1536000 bps.</span><span class="sxs-lookup"><span data-stu-id="f2e10-258">Maximum bit rate in an audio frame is 1536000 bps.</span></span><br/> |
| <span data-ttu-id="f2e10-259">M2</span><span class="sxs-lookup"><span data-stu-id="f2e10-259">M2</span></span>      | <span data-ttu-id="f2e10-260">Taxa de bits máxima – 769000 bps</span><span class="sxs-lookup"><span data-stu-id="f2e10-260">Maximum bit rate – 769000 bps</span></span> <br/> <span data-ttu-id="f2e10-261">Taxa de amostragem máxima – 96 KHz</span><span class="sxs-lookup"><span data-stu-id="f2e10-261">Maximum sampling rate – 96 KHz</span></span> <br/> <span data-ttu-id="f2e10-262">Contagem máxima de canais – 6</span><span class="sxs-lookup"><span data-stu-id="f2e10-262">Maximum channel count – 6</span></span> <br/> <span data-ttu-id="f2e10-263">Tamanho máximo do buffer – 1200 \* 1024 bits</span><span class="sxs-lookup"><span data-stu-id="f2e10-263">Maximum buffer size – 1200\*1024 bits</span></span> <br/> <span data-ttu-id="f2e10-264">Máximo de amostras por quadro – 4096</span><span class="sxs-lookup"><span data-stu-id="f2e10-264">Maximum samples per frame – 4096</span></span> <br/> <span data-ttu-id="f2e10-265">Máximo de bits por quadro-131072</span><span class="sxs-lookup"><span data-stu-id="f2e10-265">Maximum bits per frame - 131072</span></span><br/>  | <span data-ttu-id="f2e10-266">Recomendado para filmes de alta definição de som surround.</span><span class="sxs-lookup"><span data-stu-id="f2e10-266">Recommended for surround-sound high definition movies.</span></span><br/> <span data-ttu-id="f2e10-267">A taxa máxima em um quadro de áudio é de 3072000 bps.</span><span class="sxs-lookup"><span data-stu-id="f2e10-267">Maximum rate in an audio frame is 3072000 bps.</span></span><br/>         |
| <span data-ttu-id="f2e10-268">M3</span><span class="sxs-lookup"><span data-stu-id="f2e10-268">M3</span></span>      | <span data-ttu-id="f2e10-269">Taxa de bits máxima – 3 milhões bps</span><span class="sxs-lookup"><span data-stu-id="f2e10-269">Maximum bit rate – 3000000 bps</span></span> <br/> <span data-ttu-id="f2e10-270">Taxa de amostragem máxima – 96 KHz</span><span class="sxs-lookup"><span data-stu-id="f2e10-270">Maximum sampling rate – 96 KHz</span></span> <br/> <span data-ttu-id="f2e10-271">Contagem máxima de canais – 8</span><span class="sxs-lookup"><span data-stu-id="f2e10-271">Maximum channel count – 8</span></span> <br/> <span data-ttu-id="f2e10-272">Tamanho máximo do buffer – 2400 \* 1024 bits</span><span class="sxs-lookup"><span data-stu-id="f2e10-272">Maximum buffer size – 2400\*1024 bits</span></span> <br/> <span data-ttu-id="f2e10-273">Máximo de amostras por quadro – 4096</span><span class="sxs-lookup"><span data-stu-id="f2e10-273">Maximum samples per frame – 4096</span></span> <br/> <span data-ttu-id="f2e10-274">Máximo de bits por quadro-131072</span><span class="sxs-lookup"><span data-stu-id="f2e10-274">Maximum bits per frame - 131072</span></span><br/> | <span data-ttu-id="f2e10-275">Recomendado para o teatro digital.</span><span class="sxs-lookup"><span data-stu-id="f2e10-275">Recommended for digital theater.</span></span><br/> <span data-ttu-id="f2e10-276">A taxa máxima em um quadro de áudio é de 3072000 bps.</span><span class="sxs-lookup"><span data-stu-id="f2e10-276">Maximum rate in an audio frame is 3072000 bps.</span></span><br/>                               |



 

<span data-ttu-id="f2e10-277">Os perfis M0 e M1 se encaixam em um fluxo 48 KHz/16 bits/estéreo (1536000 bps) IEC 60958.</span><span class="sxs-lookup"><span data-stu-id="f2e10-277">The M0 and M1 profiles fit into a 48 KHz/16 bit/Stereo (1536000 bps) IEC 60958 stream.</span></span> <span data-ttu-id="f2e10-278">Os perfis m2 e M3 se enquadram em um fluxo 96 KHz/16 bits/estéreo (3072000 bps) IEC 60958.</span><span class="sxs-lookup"><span data-stu-id="f2e10-278">The M2 and M3 profiles fit into a 96 KHz/16 bit/Stereo (3072000 bps) IEC 60958 stream.</span></span>

<span data-ttu-id="f2e10-279">Os valores definidos por um aplicativo na estrutura WAVEFORMATEXTENSIBLE \_ IEC61937 para representar o WMA pro como um perfil m2 são mostrados no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2e10-279">The values set by an application in the WAVEFORMATEXTENSIBLE\_IEC61937 structure to represent WMA Pro as an M2 profile are shown in the following example.</span></span>


```C++
WAVEFORMATEXTENSIBLE_IEC61937 wfext;
Wfext.FormatExt.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
wfext.FormatExt.Format.nChannels = 2;             // One IEC 60958 Line.
wfext.FormatExt.Format.nSamplesPerSec = 96000;    // Link runs at 96 KHz.
wfext.FormatExt.Format.nAvgBytesPerSec = 384000;  // 96 KHz * 4.
wfext.FormatExt.Format.nBlockAlign = 4;           // 16 bits * 8 channels.
wfext.FormatExt.Format.wBitsPerSample = 16;       // Always at 16 bits over link.
wfext.FormatExt.Format.cbSize = 34;               // Indicates that Format is part of a 
                                                  // WAVEFORMATEXTENSIBLE_IEC61937 structure.
wfext.FormatExt.Samples.wValidBitsPerSample = 16;
wfext.FormatExt.dwChannelMask = KSAUDIO_SPEAKER_5POINT1;    // 5.1 Surround.
wfext.FormatExt.SubFormat = KSDATAFORMAT_SUBTYPE_IEC61937_WMA_PRO;
wfext.dwEncodedSamplesPerSec = 96000;                       // Sample rate of encoded content.
wfext.dwEncodedChannelCount = 6;                            // Encoded data contains 6 channels.
wfext.dwAverageBytesPerSec = 0;                             // Ignored for this format.
```



## <a name="related-topics"></a><span data-ttu-id="f2e10-280">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2e10-280">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2e10-281">Formatos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="f2e10-281">Device Formats</span></span>](device-formats.md)
</dt> </dl>

 

 




