---
description: Localizando tipos de saída do codificador de áudio
ms.assetid: cd47d45b-ea47-4dec-867e-d51145d7f084
title: Localizando tipos de saída do codificador de áudio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5389274cca1178ebc0ae03e21f7a804f73a5db48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771600"
---
# <a name="finding-audio-encoder-output-types-microsoft-media-foundation"></a><span data-ttu-id="30746-103">Localizando tipos de saída do codificador de áudio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="30746-103">Finding Audio Encoder Output Types (Microsoft Media Foundation)</span></span>

<span data-ttu-id="30746-104">Como você deve usar um formato de saída do codificador de áudio que é enumerado pelo codificador de áudio, você precisa ter uma maneira de encontrar o formato mais adequado às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="30746-104">Because you must use an audio encoder output format that is enumerated by the audio encoder, you need to have a way of finding the format that is most suited to your needs.</span></span> <span data-ttu-id="30746-105">O número de canais, bits por amostra e a taxa de amostragem da saída que você escolher devem corresponder aos valores do conteúdo compactado.</span><span class="sxs-lookup"><span data-stu-id="30746-105">The number of channels, bits per sample, and sample rate of the output that you choose must match the values for the content that you compress.</span></span> <span data-ttu-id="30746-106">No entanto, o codificador pode dar suporte a vários tipos dentro dessas restrições.</span><span class="sxs-lookup"><span data-stu-id="30746-106">However, the encoder may support several types within these constraints.</span></span>

<span data-ttu-id="30746-107">O fator de decisão para escolher um tipo é a taxa de bits do fluxo codificado; você deseja encontrar um tipo de mídia que corresponde à sua entrada e tem uma taxa de bits mais próxima possível de um valor de destino.</span><span class="sxs-lookup"><span data-stu-id="30746-107">The deciding factor for choosing a type is the bit rate of the encoded stream; you want to find a media type that matches your input and has a bit rate that is as close as possible to a target value.</span></span> <span data-ttu-id="30746-108">Se você estiver enumerando tipos de saída de VBR de um passo, será o valor de qualidade que decidirá o tipo usado.</span><span class="sxs-lookup"><span data-stu-id="30746-108">If you are enumerating one-pass VBR output types, it is the quality value that will decide the type you use.</span></span> <span data-ttu-id="30746-109">Para obter mais informações sobre valores de qualidade em tipos de saída enumerados, consulte [enumerando tipos de áudio para modos de codificação específicos](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="30746-109">For more information about quality values in enumerated output types, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

> [!Note]  
>    <span data-ttu-id="30746-110">O codificador de áudio enumera alguns tipos que são duplicatas de outros tipos de quase todas as formas.</span><span class="sxs-lookup"><span data-stu-id="30746-110">The audio encoder enumerates some types that are duplicates of other types in almost all ways.</span></span> <span data-ttu-id="30746-111">Essas duplicatas existem para formatos em que o número de pacotes por segundo não atende aos requisitos de armazenamento em arquivos ASF quando sincronizado com vídeo.</span><span class="sxs-lookup"><span data-stu-id="30746-111">These duplicates exist for formats where the number of packets per second does not meet the requirements for storage in ASF files when synchronized with video.</span></span> <span data-ttu-id="30746-112">Áudio sincronizado com vídeo em um arquivo ASF deve ter 3 ou mais pacotes por segundo para taxas de bits inferiores a 32000 e 5 ou mais pacotes por segundo para taxas de bits maiores ou iguais a 32000.</span><span class="sxs-lookup"><span data-stu-id="30746-112">Audio synchronized with video in an ASF file must have 3 or more packets per second for bit rates less than 32000, and 5 or more packets per second for bit rates greater than or equal to 32000.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="30746-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="30746-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30746-114">Configurando codificação de áudio</span><span class="sxs-lookup"><span data-stu-id="30746-114">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> <dt>

[<span data-ttu-id="30746-115">Enumerando tipos de áudio para modos de codificação específicos</span><span class="sxs-lookup"><span data-stu-id="30746-115">Enumerating Audio Types for Specific Encoding Modes</span></span>](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> </dl>

 

 



