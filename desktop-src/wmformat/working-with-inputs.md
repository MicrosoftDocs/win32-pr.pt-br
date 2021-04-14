---
title: Trabalhando com entradas
description: Trabalhando com entradas
ms.assetid: 72daa7ca-4264-46bf-91ac-8b95fdbfd41c
keywords:
- SDK do Windows Media Format, trabalhando com entradas
- ASF (Advanced Systems Format), trabalhando com entradas
- ASF (formato de sistemas avançados), trabalhando com entradas
- perfis, trabalhando com entradas
- fluxos, trabalhando com entradas
- codecs, trabalhando com entradas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7016b5304b0d77e130b68d9a9feef15ffe54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453564"
---
# <a name="working-with-inputs"></a><span data-ttu-id="417d2-109">Trabalhando com entradas</span><span class="sxs-lookup"><span data-stu-id="417d2-109">Working with Inputs</span></span>

<span data-ttu-id="417d2-110">Assim como a configuração de fluxo adequada no perfil é necessária para obter o codec para compactar um fluxo, você também deve garantir que o tipo de mídia descompactada que você passa para o gravador seja descrito com precisão.</span><span class="sxs-lookup"><span data-stu-id="417d2-110">Just as the proper stream configuration in the profile is required to get the codec to compress a stream, you must also ensure that the type of uncompressed media you pass to the writer is accurately described.</span></span> <span data-ttu-id="417d2-111">Cada codec do Windows Media tem um tipo de entrada padrão associado, mas há suporte para vários tipos de entrada.</span><span class="sxs-lookup"><span data-stu-id="417d2-111">Every Windows Media codec has an associated default input type, but several input types are supported.</span></span> <span data-ttu-id="417d2-112">Você pode examinar as entradas com suporte e selecionar aquela que corresponde aos seus dados.</span><span class="sxs-lookup"><span data-stu-id="417d2-112">You can examine the supported inputs and select the one that matches your data.</span></span> <span data-ttu-id="417d2-113">O processo de trabalho com entradas é resumido nas seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="417d2-113">The process of working with inputs is summarized in the following steps:</span></span>

1.  <span data-ttu-id="417d2-114">Quando você carrega um perfil para o gravador usar, o objeto do gravador atribui um número de entrada para cada conexão no perfil.</span><span class="sxs-lookup"><span data-stu-id="417d2-114">When you load a profile for the writer to use, the writer object assigns an input number for each connection in the profile.</span></span> <span data-ttu-id="417d2-115">Para obter mais informações sobre como carregar perfis para o gravador, consulte [para usar perfis com o gravador](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="417d2-115">For more information about loading profiles for the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span> <span data-ttu-id="417d2-116">A menos que você esteja usando a exclusão mútua por taxa de bits, há uma conexão para cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="417d2-116">Unless you are using mutual exclusion by bit rate, there is one connection for each stream.</span></span> <span data-ttu-id="417d2-117">Os fluxos mutuamente exclusivos por taxa de bits compartilham uma única conexão.</span><span class="sxs-lookup"><span data-stu-id="417d2-117">Streams that are mutually exclusive by bit rate share a single connection.</span></span>
2.  <span data-ttu-id="417d2-118">Seu aplicativo deve identificar os números de entrada para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="417d2-118">Your application should identify the input numbers for the file.</span></span> <span data-ttu-id="417d2-119">Para obter mais informações sobre como identificar números de entrada, consulte [para identificar entradas por número](to-identify-inputs-by-number.md).</span><span class="sxs-lookup"><span data-stu-id="417d2-119">For more information about identifying input numbers, see [To Identify Inputs By Number](to-identify-inputs-by-number.md).</span></span>
3.  <span data-ttu-id="417d2-120">Para cada entrada, você deve garantir que o formato de entrada corresponda aos seus dados.</span><span class="sxs-lookup"><span data-stu-id="417d2-120">For each input, you should ensure that the input format matches your data.</span></span> <span data-ttu-id="417d2-121">Você pode enumerar os formatos de entrada com suporte no SDK.</span><span class="sxs-lookup"><span data-stu-id="417d2-121">You can enumerate the input formats supported by the SDK.</span></span> <span data-ttu-id="417d2-122">Para obter mais informações, consulte [para enumerar formatos de entrada](to-enumerate-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="417d2-122">For more information, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span> <span data-ttu-id="417d2-123">Você não pode enumerar os formatos de entrada de fluxos arbitrários ou fluxos que já estão compactados.</span><span class="sxs-lookup"><span data-stu-id="417d2-123">You cannot enumerate the input formats of arbitrary streams or streams that are already compressed.</span></span> <span data-ttu-id="417d2-124">Para obter mais informações sobre esses casos especiais, consulte [entradas de fluxo arbitrárias e precompactadas](arbitrary-and-precompressed-stream-inputs.md).</span><span class="sxs-lookup"><span data-stu-id="417d2-124">For more information about these special cases, see [Arbitrary and Precompressed Stream Inputs](arbitrary-and-precompressed-stream-inputs.md).</span></span>
4.  <span data-ttu-id="417d2-125">Atribua o formato de entrada correto para cada conexão.</span><span class="sxs-lookup"><span data-stu-id="417d2-125">Assign the correct input format for each connection.</span></span> <span data-ttu-id="417d2-126">Para obter mais informações, consulte [atribuindo formatos de entrada](assigning-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="417d2-126">For more information, see [Assigning Input Formats](assigning-input-formats.md).</span></span>
5.  <span data-ttu-id="417d2-127">Alguns recursos de codec e gravador são configurados no momento da codificação em vez de no perfil.</span><span class="sxs-lookup"><span data-stu-id="417d2-127">Some codec and writer features are configured at encoding time instead of in the profile.</span></span> <span data-ttu-id="417d2-128">Para configurar esses recursos, você deve usar as configurações de entrada.</span><span class="sxs-lookup"><span data-stu-id="417d2-128">To configure these features, you must use input settings.</span></span> <span data-ttu-id="417d2-129">Para obter mais informações, consulte [para definir as configurações de entrada](to-set-input-settings.md).</span><span class="sxs-lookup"><span data-stu-id="417d2-129">For more information, see [To Set Input Settings](to-set-input-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="417d2-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="417d2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="417d2-131">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="417d2-131">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




