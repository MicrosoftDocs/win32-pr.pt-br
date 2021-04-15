---
description: Configurações do decodificador para Windows Media Center Edition
ms.assetid: 019b063f-f215-44d8-a916-3125bee6af93
title: Configurações do decodificador para Windows Media Center Edition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f66b5107fa0316f6ce2547e1f5f066165ed598
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105747576"
---
# <a name="decoder-settings-for-windows-media-center-edition"></a><span data-ttu-id="97a50-103">Configurações do decodificador para Windows Media Center Edition</span><span class="sxs-lookup"><span data-stu-id="97a50-103">Decoder Settings for Windows Media Center Edition</span></span>

<span data-ttu-id="97a50-104">O Windows XP Media Center Edition 2005 e posterior usa a interface [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) para configurar o filtro de decodificador de áudio para reprodução de televisão e DVD.</span><span class="sxs-lookup"><span data-stu-id="97a50-104">Windows XP Media Center Edition 2005 and later uses the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface to configure the audio decoder filter for television and DVD playback.</span></span> <span data-ttu-id="97a50-105">Há suporte para as seguintes propriedades.</span><span class="sxs-lookup"><span data-stu-id="97a50-105">The following properties are supported.</span></span>



| <span data-ttu-id="97a50-106">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="97a50-106">Property GUID</span></span>                   | <span data-ttu-id="97a50-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="97a50-107">Description</span></span>                                      |
|---------------------------------|--------------------------------------------------|
| <span data-ttu-id="97a50-108">\_formato de \_ saída de áudio CODECAPI \_</span><span class="sxs-lookup"><span data-stu-id="97a50-108">CODECAPI\_AUDIO\_OUTPUT\_FORMAT</span></span> | <span data-ttu-id="97a50-109">Configura o formato de saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="97a50-109">Configures the audio output format.</span></span> <span data-ttu-id="97a50-110">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="97a50-110">See Remarks.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="97a50-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="97a50-111">Remarks</span></span>

<span data-ttu-id="97a50-112">O valor da propriedade de \_ formato de saída de áudio CODECAPI \_ \_ é uma representação de cadeia de caracteres de um GUID, armazenado como um valor **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="97a50-112">The value of the CODECAPI\_AUDIO\_OUTPUT\_FORMAT property is a string representation of a GUID, stored as a **BSTR** value.</span></span> <span data-ttu-id="97a50-113">Os GUIDs a seguir são definidos.</span><span class="sxs-lookup"><span data-stu-id="97a50-113">The following GUIDs are defined.</span></span>



| <span data-ttu-id="97a50-114">GUID</span><span class="sxs-lookup"><span data-stu-id="97a50-114">GUID</span></span>                                                        | <span data-ttu-id="97a50-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="97a50-115">Description</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97a50-116">\_formato de saída de áudio CODECAPI \_ \_ \_ \_ MATRIXENCODED estéreo PCM \_</span><span class="sxs-lookup"><span data-stu-id="97a50-116">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_STEREO\_MATRIXENCODED</span></span> | <span data-ttu-id="97a50-117">O filtro de áudio de software deve executar a decodificação de software e a saída de um fluxo de áudio estéreo, com a matriz de áudio multicanal codificada para os dois canais.</span><span class="sxs-lookup"><span data-stu-id="97a50-117">The software audio filter should perform software decoding and output a stereo audio stream, with the multichannel audio matrix encoded to the two channels.</span></span>                                                   |
| <span data-ttu-id="97a50-118">\_formato de saída de áudio CODECAPI \_ \_ \_ \_ estéreo PCM</span><span class="sxs-lookup"><span data-stu-id="97a50-118">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_STEREO</span></span>                | <span data-ttu-id="97a50-119">O filtro de áudio de software deve executar a decodificação de software e gerar um fluxo de áudio estéreo.</span><span class="sxs-lookup"><span data-stu-id="97a50-119">The software audio filter should perform software decoding and output a stereo audio stream.</span></span>                                                                                                                   |
| <span data-ttu-id="97a50-120">\_ \_ \_ PCM SPDIF de formato de saída \_ de áudio CODECAPI \_</span><span class="sxs-lookup"><span data-stu-id="97a50-120">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_SPDIF\_PCM</span></span>                 | <span data-ttu-id="97a50-121">O filtro de áudio de software deve executar a decodificação de áudio de software, mesmo que a saída física do PC possa ser uma interface digital, como S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="97a50-121">The software audio filter should perform software audio decoding, even though the physical output from the PC may be a digital interface, such as S/PDIF.</span></span>                                                      |
| <span data-ttu-id="97a50-122">\_formato de saída de áudio CODECAPI \_ \_ \_ SPDIF \_ fragmentado</span><span class="sxs-lookup"><span data-stu-id="97a50-122">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_SPDIF\_BITSTREAM</span></span>           | <span data-ttu-id="97a50-123">O filtro de áudio de software não deve executar a decodificação de áudio de software, mas deve passar o fragmentado de áudio digital bruto para processamento externo por um dispositivo conectado com um link de áudio digital, como S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="97a50-123">The software audio filter should not perform software audio decoding, but should pass the raw digital audio bitstream for external processing by a device connected with a digital audio link, such as S/PDIF.</span></span> |
| <span data-ttu-id="97a50-124">\_fone de \_ \_ \_ ouvido PCM do formato de saída de áudio CODECAPI \_</span><span class="sxs-lookup"><span data-stu-id="97a50-124">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_HEADPHONES</span></span>            | <span data-ttu-id="97a50-125">O filtro de áudio de software deve executar a decodificação de áudio de software e deve aplicar o processamento proprietário para otimizar para fones de ouvido.</span><span class="sxs-lookup"><span data-stu-id="97a50-125">The software audio filter should perform software audio decoding and should apply proprietary processing to optimize for headphones.</span></span> <span data-ttu-id="97a50-126">O suporte para essa configuração é opcional.</span><span class="sxs-lookup"><span data-stu-id="97a50-126">Support for this setting is optional.</span></span>                                     |



 

> [!Note]  
> <span data-ttu-id="97a50-127">A interface **ICodecAPI** armazena propriedades de codec como pares de chave/valor, onde a chave é um GUID e o valor é um tipo de **variante** .</span><span class="sxs-lookup"><span data-stu-id="97a50-127">The **ICodecAPI** interface stores codec properties as key/value pairs, where the key is a GUID and the value is a **VARIANT** type.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="97a50-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="97a50-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97a50-129">Codificador e desenvolvimento de decodificador</span><span class="sxs-lookup"><span data-stu-id="97a50-129">Encoder and Decoder Development</span></span>](encoder-and-decoder-development.md)
</dt> </dl>

 

 



