---
title: Trabalhando com índices
description: Trabalhando com índices
ms.assetid: 7daa4b29-0597-462d-ad65-135d0ef7362d
keywords:
- SDK do Windows Media Format, índices
- ASF (Advanced Systems Format), índices
- ASF (formato de sistemas avançados), índices
- índices, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34057046223daf2e16950e0e38b1b0db5df32c4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822442"
---
# <a name="working-with-indexes"></a><span data-ttu-id="2d273-107">Trabalhando com índices</span><span class="sxs-lookup"><span data-stu-id="2d273-107">Working with Indexes</span></span>

<span data-ttu-id="2d273-108">O SDK do Windows Media Format dá suporte à busca e ao seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="2d273-108">The Windows Media Format SDK supports seeking and striding through content.</span></span> <span data-ttu-id="2d273-109">A busca permite que você especifique um local na linha do tempo do arquivo para começar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="2d273-109">Seeking enables you to specify a place on the file's timeline to begin playback.</span></span> <span data-ttu-id="2d273-110">A habilitação permite que você encaminhe e retroceda rapidamente a saída de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="2d273-110">Striding enables you to fast-forward and rewind the output of a file.</span></span> <span data-ttu-id="2d273-111">Os arquivos devem ser indexados para aproveitar esses recursos.</span><span class="sxs-lookup"><span data-stu-id="2d273-111">Files must be indexed to take advantage of these features.</span></span> <span data-ttu-id="2d273-112">Um índice é uma série de valores que representam as posições no arquivo (horas de apresentação, números de quadro ou códigos de tempo SMTP) com deslocamentos correspondentes na seção de dados do arquivo para cada.</span><span class="sxs-lookup"><span data-stu-id="2d273-112">An index is a series of values representing positions in the file (either presentation times, frame numbers, or SMTPE time codes) with corresponding offsets into the data section of the file for each.</span></span> <span data-ttu-id="2d273-113">A indexação é mais importante para fluxos de vídeo, pois o tempo de apresentação de fluxo de áudio pode ser facilmente estimado.</span><span class="sxs-lookup"><span data-stu-id="2d273-113">Indexing is most important for video streams, as audio stream presentation time can be easily estimated.</span></span> <span data-ttu-id="2d273-114">No entanto, alguns fluxos de áudio também podem exigir índices.</span><span class="sxs-lookup"><span data-stu-id="2d273-114">However, some audio streams may require indexes as well.</span></span> <span data-ttu-id="2d273-115">Por padrão, o gravador irá indexar todos os novos arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="2d273-115">By default, the writer will index every new ASF file.</span></span> <span data-ttu-id="2d273-116">Se forem feitas alterações no conteúdo de um arquivo, você deverá atualizar o índice por conta própria usando o objeto indexador.</span><span class="sxs-lookup"><span data-stu-id="2d273-116">If changes are made to the content of a file, you must refresh the index yourself using the indexer object.</span></span>

<span data-ttu-id="2d273-117">O indexador dá suporte à indexação temporal e com base em quadros, bem como à indexação com base em códigos de tempo SMPTE (se houver).</span><span class="sxs-lookup"><span data-stu-id="2d273-117">The indexer supports both temporal and frame-based indexing as well as indexing based on SMPTE time codes (if present).</span></span> <span data-ttu-id="2d273-118">O gravador criará um índice temporal por padrão para cada novo fluxo de vídeo codificado em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="2d273-118">The writer will create a temporal index by default for every new video stream encoded to a file.</span></span> <span data-ttu-id="2d273-119">Você deve configurar e chamar explicitamente o indexador para criar um índice de código de tempo baseado em quadro ou SMPTE.</span><span class="sxs-lookup"><span data-stu-id="2d273-119">You must explicitly configure and call the indexer to create a frame-based or SMPTE time code index.</span></span>

<span data-ttu-id="2d273-120">Quando são feitas alterações no conteúdo de um arquivo ASF, ele deve ser indexado novamente.</span><span class="sxs-lookup"><span data-stu-id="2d273-120">When changes are made to the content of an ASF file, it must be indexed again.</span></span>

<span data-ttu-id="2d273-121">As seções a seguir apresentam o código de exemplo para executar tarefas comuns de indexação.</span><span class="sxs-lookup"><span data-stu-id="2d273-121">The following sections present example code for performing common indexing tasks.</span></span>

-   [<span data-ttu-id="2d273-122">Para desabilitar a indexação automática</span><span class="sxs-lookup"><span data-stu-id="2d273-122">To Disable Automatic Indexing</span></span>](to-disable-automatic-indexing.md)
-   [<span data-ttu-id="2d273-123">Para configurar o indexador</span><span class="sxs-lookup"><span data-stu-id="2d273-123">To Configure the Indexer</span></span>](to-configure-the-indexer.md)
-   [<span data-ttu-id="2d273-124">Para indexar um arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="2d273-124">To Index an ASF File</span></span>](to-index-an-asf-file.md)
-   [<span data-ttu-id="2d273-125">Para interromper a indexação em andamento</span><span class="sxs-lookup"><span data-stu-id="2d273-125">To Stop Indexing in Progress</span></span>](to-stop-indexing-in-progress.md)

<span data-ttu-id="2d273-126">Além disso, o aplicativo de exemplo DSCopy ilustra o uso do indexador.</span><span class="sxs-lookup"><span data-stu-id="2d273-126">In addition, the DSCopy sample application illustrates the use of the indexer.</span></span> <span data-ttu-id="2d273-127">Para obter mais informações, consulte [aplicativos de exemplo](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="2d273-127">For more information, see [Sample Applications](sample-applications.md).</span></span>

 

 




