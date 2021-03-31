---
title: Taxa de bits
description: Taxa de bits
ms.assetid: 7c35a07b-03d3-42d7-aefc-8e6a0033ac48
keywords:
- SDK do Windows Media Format, taxas de bits
- ASF (Advanced Systems Format), taxas de bits
- ASF (formato de sistemas avançados), taxas de bits
- taxas de bits, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d793be8fe04746a61eea48bcf066d95d641221a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636972"
---
# <a name="bit-rate"></a><span data-ttu-id="18e97-107">Taxa de bits</span><span class="sxs-lookup"><span data-stu-id="18e97-107">Bit Rate</span></span>

<span data-ttu-id="18e97-108">Taxa de bits refere-se à quantidade de dados por segundo que é entregue de um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="18e97-108">Bit rate refers to the amount of data per second that is delivered from an ASF file.</span></span> <span data-ttu-id="18e97-109">As medições de taxa de bits são em bits por segundo (bps) ou kilobits por segundo (Kbps).</span><span class="sxs-lookup"><span data-stu-id="18e97-109">Bit rate measurements are in bits per second (bps) or kilobits per second (Kbps).</span></span> <span data-ttu-id="18e97-110">A taxa de bits geralmente é confundida com largura de banda, que é uma medida da capacidade de transferência de dados de uma rede.</span><span class="sxs-lookup"><span data-stu-id="18e97-110">Bit rate is often confused with bandwidth, which is a measurement of the data transfer capacity of a network.</span></span> <span data-ttu-id="18e97-111">A largura de banda também é medida em bps e kbps.</span><span class="sxs-lookup"><span data-stu-id="18e97-111">Bandwidth is also measured in bps and Kbps.</span></span>

<span data-ttu-id="18e97-112">O Windows Media Format SDK pode ser usado para criar aplicativos que fornecem fluxo de conteúdo baseado no Windows Media por meio de locais da Internet ou da intranet.</span><span class="sxs-lookup"><span data-stu-id="18e97-112">The Windows Media Format SDK can be used to create applications that deliver streaming Windows Media-based content from Internet or intranet locations.</span></span> <span data-ttu-id="18e97-113">Quando você está transmitindo dados por uma rede ou pela Internet, a taxa de bits é de importância vital para a experiência do usuário final.</span><span class="sxs-lookup"><span data-stu-id="18e97-113">When you are streaming data across a network or the Internet, the bit rate is of vital importance to the end-user experience.</span></span> <span data-ttu-id="18e97-114">Se a largura de banda disponível para a rede for menor que a taxa de bits do arquivo ASF, a reprodução do arquivo será interrompida de alguma forma.</span><span class="sxs-lookup"><span data-stu-id="18e97-114">If the bandwidth available to the network is less than the bit rate of the ASF file, the playback of the file will be interrupted in some way.</span></span> <span data-ttu-id="18e97-115">Normalmente, a largura de banda insuficiente fará com que os exemplos sejam ignorados ou uma pausa na reprodução enquanto mais dados são armazenados em buffer.</span><span class="sxs-lookup"><span data-stu-id="18e97-115">Usually, insufficient bandwidth will result in either samples being skipped, or a pause in playback while more data is buffered.</span></span>

<span data-ttu-id="18e97-116">Cada arquivo ASF recebe um valor de taxa de bits no momento da criação, com base no tipo e no número de fluxos incluídos no perfil usado.</span><span class="sxs-lookup"><span data-stu-id="18e97-116">Every ASF file is assigned a bit rate value at the time of creation, based upon the type and number of streams that are included in the profile used.</span></span> <span data-ttu-id="18e97-117">Os fluxos individuais têm suas próprias taxas de bits.</span><span class="sxs-lookup"><span data-stu-id="18e97-117">Individual streams have their own bit rates.</span></span> <span data-ttu-id="18e97-118">As taxas de bits podem ser constantes (os dados originais são compactados de forma a manter um fluxo constante de dados em aproximadamente a mesma taxa) ou variável (os dados originais são compactados de forma a manter a mesma qualidade em todo o tempo, mesmo que isso possa significar um fluxo de dados irregular).</span><span class="sxs-lookup"><span data-stu-id="18e97-118">Bit rates can be constant (the original data is compressed in such a way as to maintain a constant flow of data at approximately the same rate) or variable (the original data is compressed in such a way as to maintain the same quality throughout, even though this may mean uneven data flow).</span></span> <span data-ttu-id="18e97-119">Tipos de taxa de bits diferentes podem ser aplicados a fluxos diferentes no mesmo arquivo.</span><span class="sxs-lookup"><span data-stu-id="18e97-119">Different bit rate types can be applied to different streams within the same file.</span></span>

<span data-ttu-id="18e97-120">Você pode codificar o mesmo conteúdo para vários fluxos diferentes, cada um com uma taxa de bits diferente.</span><span class="sxs-lookup"><span data-stu-id="18e97-120">You can encode the same content to several different streams, each with a different bit rate.</span></span> <span data-ttu-id="18e97-121">Em seguida, você pode configurar os fluxos para que eles sejam mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="18e97-121">Then you can configure the streams so that they are mutually exclusive.</span></span> <span data-ttu-id="18e97-122">Isso permite que você crie um único arquivo que pode ser transmitido para usuários com larguras de banda diferentes.</span><span class="sxs-lookup"><span data-stu-id="18e97-122">This enables you to create a single file that can be streamed to users with different bandwidths.</span></span> <span data-ttu-id="18e97-123">Esse recurso é chamado de taxa de bits múltipla ou MBR.</span><span class="sxs-lookup"><span data-stu-id="18e97-123">This feature is called multiple bit rate, or MBR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18e97-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="18e97-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18e97-125">**Conceitos**</span><span class="sxs-lookup"><span data-stu-id="18e97-125">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="18e97-126">**Codificação de taxa de bits constante (CBR)**</span><span class="sxs-lookup"><span data-stu-id="18e97-126">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="18e97-127">**Entradas, fluxos e saídas**</span><span class="sxs-lookup"><span data-stu-id="18e97-127">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="18e97-128">**Perfis**</span><span class="sxs-lookup"><span data-stu-id="18e97-128">**Profiles**</span></span>](profiles.md)
</dt> <dt>

[<span data-ttu-id="18e97-129">**Codificação de taxa de bits variável (VBR)**</span><span class="sxs-lookup"><span data-stu-id="18e97-129">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




