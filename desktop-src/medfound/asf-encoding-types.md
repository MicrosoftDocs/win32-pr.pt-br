---
description: Tipos de codificação ASF
ms.assetid: ffa99c6b-3b62-4068-96d5-ad57c340d088
title: Tipos de codificação ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6187f4bbf49eafaf50a46a8af92b71b4e72885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089800"
---
# <a name="asf-encoding-types"></a><span data-ttu-id="1081c-103">Tipos de codificação ASF</span><span class="sxs-lookup"><span data-stu-id="1081c-103">ASF Encoding Types</span></span>

<span data-ttu-id="1081c-104">Todos os métodos de codificação se concentram no buffer usado pelo codificador para gerenciar dados de entrada não compactados.</span><span class="sxs-lookup"><span data-stu-id="1081c-104">The encoding methods all focus on the buffer used by the encoder to manage uncompressed input data.</span></span> <span data-ttu-id="1081c-105">Esse buffer é definido pela taxa de bits do fluxo, em bits por segundo, e pela janela de buffer, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="1081c-105">This buffer is defined by the bit rate of the stream, in bits per second, and the buffer window, in milliseconds.</span></span> <span data-ttu-id="1081c-106">Ao codificar para arquivos ASF, os codificadores de mídia do Windows obedecem às restrições do buffer.</span><span class="sxs-lookup"><span data-stu-id="1081c-106">When encoding to ASF files, the Windows Media encoders abide by the constraints of the buffer.</span></span> <span data-ttu-id="1081c-107">Para obter mais informações sobre a janela de buffer, consulte [o modelo de buffer de buckets vazados](the-leaky-bucket-buffer-model.md).</span><span class="sxs-lookup"><span data-stu-id="1081c-107">For more information about the buffer window, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span> <span data-ttu-id="1081c-108">Saber como e quando usar cada método pode ajudá-lo a criar conteúdo compactado de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="1081c-108">Knowing how and when to use each method can help you create high-quality compressed content.</span></span> <span data-ttu-id="1081c-109">A tabela a seguir contém links para tópicos sobre cada um dos métodos de codificação disponíveis que um aplicativo pode usar para codificar dados de mídia para o ASF.</span><span class="sxs-lookup"><span data-stu-id="1081c-109">The following table contains links to topics about each of the available encoding methods that an application can use to encode media data to ASF.</span></span>



| <span data-ttu-id="1081c-110">Método de codificação</span><span class="sxs-lookup"><span data-stu-id="1081c-110">Encoding method</span></span>                                                                                      | <span data-ttu-id="1081c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="1081c-111">Description</span></span>                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1081c-112">Codificação de taxa de bits constante</span><span class="sxs-lookup"><span data-stu-id="1081c-112">Constant Bit Rate Encoding</span></span>](constant-bit-rate-encoding.md)                                         | <span data-ttu-id="1081c-113">O codificador compacta os dados a uma taxa de bits especificada.</span><span class="sxs-lookup"><span data-stu-id="1081c-113">The encoder compresses data to a specified bit rate.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="1081c-114">Codificação de taxa de bits variável baseada em qualidade</span><span class="sxs-lookup"><span data-stu-id="1081c-114">Quality-Based Variable Bit Rate Encoding</span></span>](quality-based-variable-bit-rate--vbr--encoding.md)       | <span data-ttu-id="1081c-115">O codificador compacta os dados a um valor de qualidade específico para que a qualidade da mídia codificada seja consistente durante sua duração, independentemente dos requisitos de buffer do fluxo resultante.</span><span class="sxs-lookup"><span data-stu-id="1081c-115">The encoder compresses data to a particular quality value so that the quality of the encoded media is consistent throughout its duration, regardless of the buffer requirements of the resulting stream.</span></span> |
| [<span data-ttu-id="1081c-116">Codificação de taxa de bits variável irrestrita</span><span class="sxs-lookup"><span data-stu-id="1081c-116">Unconstrained Variable Bit Rate Encoding</span></span>](unconstrained-variable-bit-rate--vbr--encoding.md)       | <span data-ttu-id="1081c-117">O codificador compacta os dados à qualidade mais alta possível, mantendo uma taxa de bits especificada.</span><span class="sxs-lookup"><span data-stu-id="1081c-117">The encoder compresses data to the highest possible quality while maintaining a specified bit rate.</span></span> <span data-ttu-id="1081c-118">Esse modo também é chamado de codificação de taxa de bits variável (VBR) de 2 passagens.</span><span class="sxs-lookup"><span data-stu-id="1081c-118">This mode is also called 2-pass variable bit rate (VBR) encoding.</span></span>                                    |
| [<span data-ttu-id="1081c-119">Codificação de taxa de bits de variável com restrição de pico</span><span class="sxs-lookup"><span data-stu-id="1081c-119">Peak-Constrained Variable Bit Rate Encoding</span></span>](peak-constrained-variable-bit-rate--vbr--encoding.md) | <span data-ttu-id="1081c-120">O codificador compacta os dados a uma taxa de bits especificada enquanto mantém os valores de buffer na janela e na taxa de bits do buffer máximo especificados.</span><span class="sxs-lookup"><span data-stu-id="1081c-120">The encoder compresses data to a specified bit rate while keeping the buffer values under the specified maximum buffer window and bit rate.</span></span> <span data-ttu-id="1081c-121">Esse modo também é chamado de taxa de bits de pico de 2 passagens.</span><span class="sxs-lookup"><span data-stu-id="1081c-121">This mode is also called 2-pass peak VBR.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="1081c-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1081c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1081c-123">Suporte a ASF no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1081c-123">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="1081c-124">Codificadores de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="1081c-124">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



