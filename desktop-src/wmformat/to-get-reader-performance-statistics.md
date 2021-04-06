---
title: Para obter estatísticas de desempenho do leitor
description: Para obter estatísticas de desempenho do leitor
ms.assetid: 996abfe6-1444-48ab-8c34-ba923c4cd511
keywords:
- ASF (Advanced Systems Format), estatísticas de desempenho de leitor
- ASF (formato de sistemas avançados), estatísticas de desempenho de leitor
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- Formato de sistema avançado (ASF), estatísticas de desempenho
- ASF (formato de sistemas avançados), estatísticas de desempenho
- leitores assíncronos, estatísticas de desempenho
- desempenho, estatísticas de leitor
- desempenho, leitores assíncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5484b211f2c2d1e9ad4cf9aac3773c7946757c2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103823562"
---
# <a name="to-get-reader-performance-statistics"></a><span data-ttu-id="b51b9-112">Para obter estatísticas de desempenho do leitor</span><span class="sxs-lookup"><span data-stu-id="b51b9-112">To Get Reader Performance Statistics</span></span>

<span data-ttu-id="b51b9-113">Ao ler arquivos localmente com o leitor assíncrono, não é necessário verificar o desempenho das operações de leitura.</span><span class="sxs-lookup"><span data-stu-id="b51b9-113">When reading files locally with the asynchronous reader, it is not necessary to check the performance of reading operations.</span></span> <span data-ttu-id="b51b9-114">No entanto, se seu aplicativo estiver lendo de uma fonte de streaming, as estatísticas de desempenho poderão ser muito importantes.</span><span class="sxs-lookup"><span data-stu-id="b51b9-114">If your application is reading from a streaming source however, performance statistics can be very important.</span></span> <span data-ttu-id="b51b9-115">Seu aplicativo pode responder às alterações no desempenho de reprodução para garantir a melhor experiência possível do usuário final.</span><span class="sxs-lookup"><span data-stu-id="b51b9-115">Your application can respond to changes in playback performance to ensure the best possible end-user experience.</span></span>

<span data-ttu-id="b51b9-116">As informações de desempenho que você pode recuperar do leitor incluem as seguintes estatísticas:</span><span class="sxs-lookup"><span data-stu-id="b51b9-116">The performance information you can retrieve from the reader includes the following statistics:</span></span>

-   <span data-ttu-id="b51b9-117">A largura de banda atual da conexão.</span><span class="sxs-lookup"><span data-stu-id="b51b9-117">The current bandwidth of the connection.</span></span>
-   <span data-ttu-id="b51b9-118">O número de pacotes recebidos do servidor.</span><span class="sxs-lookup"><span data-stu-id="b51b9-118">The number of packets received from the server.</span></span>
-   <span data-ttu-id="b51b9-119">O número de pacotes perdidos que foram recuperados.</span><span class="sxs-lookup"><span data-stu-id="b51b9-119">The number of lost packets that were recovered.</span></span>
-   <span data-ttu-id="b51b9-120">O número de pacotes perdidos que não foram recuperados.</span><span class="sxs-lookup"><span data-stu-id="b51b9-120">The number of lost packets that were not recovered.</span></span>
-   <span data-ttu-id="b51b9-121">A porcentagem do número total de pacotes enviados que foram recebidos.</span><span class="sxs-lookup"><span data-stu-id="b51b9-121">The percentage of the total number of packets sent that have been received.</span></span>

<span data-ttu-id="b51b9-122">Para obter estatísticas de desempenho do leitor, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="b51b9-122">To get reader performance statistics, perform the following steps.</span></span>

1.  <span data-ttu-id="b51b9-123">Antes de iniciar a reprodução, crie uma estrutura de [**\_ \_ estatísticas do WM Reader**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) .</span><span class="sxs-lookup"><span data-stu-id="b51b9-123">Before starting playback, create a [**WM\_READER\_STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics) structure.</span></span> <span data-ttu-id="b51b9-124">Você deve definir o membro **cbSize** como sizeof (estatísticas do WM \_ Reader \_ ).</span><span class="sxs-lookup"><span data-stu-id="b51b9-124">You must set the **cbSize** member to sizeof(WM\_READER\_STATISTICS).</span></span>
2.  <span data-ttu-id="b51b9-125">Obtenha um ponteiro para a interface [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) do objeto leitor chamando **IWMReader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="b51b9-125">Obtain a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
3.  <span data-ttu-id="b51b9-126">Durante a reprodução, faça chamadas para [**IWMReaderAdvanced:: Getstatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) com frequência para monitorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="b51b9-126">During playback, make calls to [**IWMReaderAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics) frequently to monitor performance.</span></span> <span data-ttu-id="b51b9-127">Passe sua estrutura de **\_ \_ estatísticas do WM Reader** com cada chamada e examine os membros apropriados.</span><span class="sxs-lookup"><span data-stu-id="b51b9-127">Pass your **WM\_READER\_STATISTICS** structure with each call and examine the appropriate members.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b51b9-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b51b9-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b51b9-129">**Lendo arquivos com o leitor assíncrono**</span><span class="sxs-lookup"><span data-stu-id="b51b9-129">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




