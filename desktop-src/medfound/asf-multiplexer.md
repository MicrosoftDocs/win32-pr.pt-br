---
description: Multiplexador ASF
ms.assetid: 007a6da5-47cf-476a-b0f7-566a68ad19ce
title: Multiplexador ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362a1e0be72e8bc516e37ec83c36446177816f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010331"
---
# <a name="asf-multiplexer"></a><span data-ttu-id="01070-103">Multiplexador ASF</span><span class="sxs-lookup"><span data-stu-id="01070-103">ASF Multiplexer</span></span>

<span data-ttu-id="01070-104">O *multiplexador* de ASF é um objeto de camada WMContainer que funciona com o [objeto de dados ASF](asf-file-structure.md) e dá a um aplicativo a capacidade de gerar pacotes de dados para um contêiner ASF.</span><span class="sxs-lookup"><span data-stu-id="01070-104">The ASF *multiplexer* is a WMContainer layer object that works with the [ASF Data Object](asf-file-structure.md) and gives an application the ability to generate data packets for an ASF container.</span></span> <span data-ttu-id="01070-105">O multiplexador aceita dados de mídia na forma de [amostras de mídia](media-samples.md) e gera amostras de mídia com base nos parâmetros de streaming e de pacote ASF definidos no [objeto de cabeçalho ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="01070-105">The multiplexer accepts media data in the form of [Media Samples](media-samples.md) and outputs media samples based on streaming and ASF packet parameters defined in the [ASF Header Object](asf-file-structure.md).</span></span> <span data-ttu-id="01070-106">Os exemplos de mídia de saída armazenam referências a um ou mais buffers de mídia que contêm dados de mídia digital em pacotes. Você pode usar esse objeto em um cenário de codificação de arquivo em que ele recebe amostras de fluxo codificadas do codificador ou para transcodificação ASF-ASF (remuxing).</span><span class="sxs-lookup"><span data-stu-id="01070-106">The output media samples hold references to one or more media buffers that contain packetized digital media data.You can use this object in a file encoding scenario where it receives encoded stream samples from the encoder or for ASF-ASF transcoding (remuxing).</span></span>

<span data-ttu-id="01070-107">O diagrama a seguir ilustra a geração de pacotes de dados ASF para um arquivo ASF usando o multiplexador.</span><span class="sxs-lookup"><span data-stu-id="01070-107">The following diagram illustrates ASF data packet generation for an ASF file using the multiplexer.</span></span>

![diagrama mostrando a geração de pacotes de dados ASF](images/bb2da6a9-5e50-4dea-9b79-ae32759ac48a.gif)

<span data-ttu-id="01070-109">Para obter informações sobre a estrutura de um arquivo ASF, consulte [estrutura de arquivo ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="01070-109">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="01070-110">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="01070-110">This section contains the following topics:</span></span>



| <span data-ttu-id="01070-111">Tópico</span><span class="sxs-lookup"><span data-stu-id="01070-111">Topic</span></span>                                                                  | <span data-ttu-id="01070-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="01070-112">Description</span></span>                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="01070-113">Criando o objeto Multiplexador</span><span class="sxs-lookup"><span data-stu-id="01070-113">Creating the Multiplexer Object</span></span>](creating-the-multiplexer-object.md) | <span data-ttu-id="01070-114">Como criar e inicializar o multiplexador.</span><span class="sxs-lookup"><span data-stu-id="01070-114">How to create and initialize the multiplexer.</span></span>                     |
| [<span data-ttu-id="01070-115">Gerando novos pacotes de dados ASF</span><span class="sxs-lookup"><span data-stu-id="01070-115">Generating New ASF Data Packets</span></span>](generating-new-asf-data-packets.md) | <span data-ttu-id="01070-116">Como gerar pacotes de dados para constituir um novo objeto de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="01070-116">How to generate data packets to constitute a new ASF Data Object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="01070-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01070-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01070-118">Componentes ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="01070-118">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="01070-119">Tutorial: copiando fluxos ASF de um arquivo para outro</span><span class="sxs-lookup"><span data-stu-id="01070-119">Tutorial: Copying ASF Streams from One File to Another</span></span>](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[<span data-ttu-id="01070-120">Tutorial: gravando um arquivo WMA usando a codificação de CBR</span><span class="sxs-lookup"><span data-stu-id="01070-120">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



