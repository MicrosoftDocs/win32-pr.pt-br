---
title: Trabalhando com saídas
description: Trabalhando com saídas
ms.assetid: e2e14e88-dddc-496d-8087-1455da0821e3
keywords:
- SDK do Windows Media Format, trabalhando com saídas
- ASF (Advanced Systems Format), trabalhando com saídas
- ASF (formato de sistemas avançados), trabalhando com saídas
- ASF (Advanced Systems Format), formatos e números de saída
- ASF (formato de sistemas avançados), números e formatos de saída
- formatos e números de saída, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d089a645838a295e07eb740927d75238473cc4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640135"
---
# <a name="working-with-outputs"></a><span data-ttu-id="fa226-109">Trabalhando com saídas</span><span class="sxs-lookup"><span data-stu-id="fa226-109">Working with Outputs</span></span>

<span data-ttu-id="fa226-110">Como padrão, cada exemplo que você recebe de um objeto leitor é associado a um número de saída.</span><span class="sxs-lookup"><span data-stu-id="fa226-110">As a default, every sample you receive from either reader object is associated with an output number.</span></span> <span data-ttu-id="fa226-111">Cada número de saída corresponde a um fluxo no arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="fa226-111">Each output number corresponds to a stream in the ASF file.</span></span> <span data-ttu-id="fa226-112">O leitor atribui números de saída aos fluxos no arquivo quando o arquivo é aberto.</span><span class="sxs-lookup"><span data-stu-id="fa226-112">The reader assigns output numbers to the streams in the file when the file is opened.</span></span> <span data-ttu-id="fa226-113">Normalmente, há uma saída para cada fluxo em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="fa226-113">Normally there is one output for each stream in a file.</span></span> <span data-ttu-id="fa226-114">No entanto, se o arquivo usar a exclusão mútua, cada grupo de fluxos mutuamente exclusivos será atribuído a um único número de saída.</span><span class="sxs-lookup"><span data-stu-id="fa226-114">If the file uses mutual exclusion, however, each group of mutually exclusive streams is assigned a single output number.</span></span> <span data-ttu-id="fa226-115">O fluxo que corresponde ao número de saída dos fluxos mutuamente exclusivos é determinado pelo leitor, no caso de arquivos de taxa de bits múltipla (MBR) ou por seu aplicativo, se você estiver usando a seleção de fluxo manual.</span><span class="sxs-lookup"><span data-stu-id="fa226-115">The stream that corresponds to the output number of the mutually exclusive streams is determined either by the reader, in the case of multiple bit rate (MBR) files, or by your application, if you are using manual stream selection.</span></span>

<span data-ttu-id="fa226-116">Como o nome de conexão definido no perfil não é persistido no arquivo, o leitor cria um nome de conexão padrão para cada saída que é simplesmente uma representação de cadeia de caracteres do número de saída, por exemplo "1", "2", "3" e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="fa226-116">Because the connection name set in the profile is not persisted in the file, the reader creates a default connection name for each output that is simply a string representation of the output number, for example "1", "2", "3" and so on.</span></span> <span data-ttu-id="fa226-117">Os nomes de conexão habilitam aplicativos e o próprio leitor, para correlacionar saídas a fluxos.</span><span class="sxs-lookup"><span data-stu-id="fa226-117">The connection names enable applications, and the reader itself, to correlate outputs to streams.</span></span> <span data-ttu-id="fa226-118">Em um arquivo de taxa de vários bits, vários fluxos compartilham um nome de conexão.</span><span class="sxs-lookup"><span data-stu-id="fa226-118">In a multiple bit rate file, several streams share a connection name.</span></span> <span data-ttu-id="fa226-119">Isso não importa com o leitor, porque as propriedades de saída para cada fluxo de MBR são idênticas.</span><span class="sxs-lookup"><span data-stu-id="fa226-119">This does not matter to the reader, because the output properties for each MBR stream are identical.</span></span>

<span data-ttu-id="fa226-120">Cada saída tem um ou mais formatos de saída com suporte.</span><span class="sxs-lookup"><span data-stu-id="fa226-120">Each output has one or more supported output formats.</span></span> <span data-ttu-id="fa226-121">Um formato de saída é o formato que os exemplos não compactados fornecidos pelo leitor usam.</span><span class="sxs-lookup"><span data-stu-id="fa226-121">An output format is the format that the uncompressed samples delivered by the reader use.</span></span> <span data-ttu-id="fa226-122">Quando o leitor abre um arquivo, ele define o formato de cada saída para o padrão para o subtipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="fa226-122">When the reader opens a file, it sets the format of each output to the default for the media subtype.</span></span> <span data-ttu-id="fa226-123">O número e o tipo de formatos de saída com suporte são determinados pelo codec que descompacta os dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="fa226-123">The number and type of output formats supported is determined by the codec that decompresses the media data.</span></span>

<span data-ttu-id="fa226-124">Os tópicos a seguir explicam como trabalhar com saídas:</span><span class="sxs-lookup"><span data-stu-id="fa226-124">The following topics explain how to work with outputs:</span></span>

-   [<span data-ttu-id="fa226-125">Para identificar os números de saída</span><span class="sxs-lookup"><span data-stu-id="fa226-125">To Identify Output Numbers</span></span>](to-identify-output-numbers.md)
-   [<span data-ttu-id="fa226-126">Atribuindo formatos de saída</span><span class="sxs-lookup"><span data-stu-id="fa226-126">Assigning Output Formats</span></span>](assigning-output-formats.md)

## <a name="related-topics"></a><span data-ttu-id="fa226-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa226-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa226-128">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="fa226-128">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="fa226-129">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="fa226-129">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="fa226-130">**Lendo arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="fa226-130">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




