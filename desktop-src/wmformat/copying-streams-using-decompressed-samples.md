---
title: Copiando fluxos usando amostras descompactadas
description: Copiando fluxos usando amostras descompactadas
ms.assetid: 03ad8415-1dff-4362-94b4-7ec69c3e7888
keywords:
- SDK do Windows Media Format, copiando fluxos
- ASF (Advanced Systems Format), copiando fluxos
- ASF (formato de sistemas avançados), copiando fluxos
- fluxos, copiando usando dados descompactados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c5c0f98b02090d98814983ad518ee3cd7e5d8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105798389"
---
# <a name="copying-streams-using-decompressed-samples"></a><span data-ttu-id="f776c-107">Copiando fluxos usando amostras descompactadas</span><span class="sxs-lookup"><span data-stu-id="f776c-107">Copying Streams Using Decompressed Samples</span></span>

<span data-ttu-id="f776c-108">É altamente recomendável que você não copie fluxos de um arquivo para outro usando exemplos descompactados.</span><span class="sxs-lookup"><span data-stu-id="f776c-108">It is strongly recommended that you not copy streams from one file to another using decompressed samples.</span></span> <span data-ttu-id="f776c-109">O processo de descompactar e recompactar amostras diminuirá a qualidade da saída.</span><span class="sxs-lookup"><span data-stu-id="f776c-109">The process of decompressing and recompressing samples will degrade the quality of the output.</span></span> <span data-ttu-id="f776c-110">Se você precisar descompactar seus exemplos e, em seguida, copiá-los para outro fluxo, poderá encontrar alguma dificuldade com fluxos codificados de taxa de bits variável (VBR) com base em qualidade.</span><span class="sxs-lookup"><span data-stu-id="f776c-110">If you do need to decompress your samples and then copy them to another stream, you may encounter some difficulty with quality-based variable bit rate (VBR) encoded streams.</span></span>

<span data-ttu-id="f776c-111">Quando o codec conclui a compactação de um fluxo de VBR com base na qualidade, ele registra a taxa de bits e a janela de buffer do conteúdo resultante.</span><span class="sxs-lookup"><span data-stu-id="f776c-111">When the codec finishes compressing a quality-based VBR stream, it records the bit rate and buffer window of the resulting content.</span></span> <span data-ttu-id="f776c-112">Quando você lê um arquivo que contém um fluxo codificado com a VBR com base em qualidade, o perfil obtido do leitor notará a taxa de bits e a janela de buffer, bem como a taxa de bits máxima e a janela de buffer máximo.</span><span class="sxs-lookup"><span data-stu-id="f776c-112">When you read a file containing a stream encoded with quality-based VBR, the profile obtained from the reader will note the bit rate and buffer window as well as the maximum bit rate and maximum buffer window.</span></span> <span data-ttu-id="f776c-113">Essa configuração no perfil normalmente significa um fluxo de taxa de bits de variável restrita de taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="f776c-113">This configuration in the profile normally signifies a bit-rate constrained variable bit rate stream.</span></span> <span data-ttu-id="f776c-114">Como resultado, quando você definir o perfil no gravador, ele esperará uma passagem de pré-processamento para o fluxo, pois os fluxos de VBR com taxa de bits restritas exigem codificação de duas passagens.</span><span class="sxs-lookup"><span data-stu-id="f776c-114">As a result, when you set the profile on the writer, it will expect a preprocessing pass for the stream, because bit-rate constrained VBR streams require two-pass encoding.</span></span> <span data-ttu-id="f776c-115">Você deve tratar o fluxo como se fosse um fluxo de VBR de taxa de bits restrita e fornecer os exemplos para pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="f776c-115">You should treat the stream as if it were a bit-rate constrained VBR stream and deliver the samples for preprocessing.</span></span> <span data-ttu-id="f776c-116">Como você está usando os valores retornados após a codificação do conteúdo em um nível de qualidade específico, esses valores representam o nível de qualidade desejado.</span><span class="sxs-lookup"><span data-stu-id="f776c-116">Because you are using the values returned after encoding the content at a particular quality level, those values represent the desired quality level.</span></span> <span data-ttu-id="f776c-117">É claro que a qualidade da saída recodificada será, de certa forma, degradada, como resultado da nova codificação.</span><span class="sxs-lookup"><span data-stu-id="f776c-117">Of course, the quality of the re-encoded output will be somewhat degraded anyway, as a result of the re-encoding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f776c-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f776c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f776c-119">**Copiando dados de um arquivo para outro**</span><span class="sxs-lookup"><span data-stu-id="f776c-119">**Copying Data from One File to Another**</span></span>](copying-data-from-one-file-to-another.md)
</dt> <dt>

[<span data-ttu-id="f776c-120">**Copiando fluxos sem descompactar os dados**</span><span class="sxs-lookup"><span data-stu-id="f776c-120">**Copying Streams Without Decompressing the Data**</span></span>](copying-streams-without-decompressing-the-data.md)
</dt> </dl>

 

 




