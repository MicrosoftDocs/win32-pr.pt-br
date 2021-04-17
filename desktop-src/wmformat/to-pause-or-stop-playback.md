---
title: Para pausar ou parar a reprodução
description: Para pausar ou parar a reprodução
ms.assetid: 8e43ea80-36c7-4530-8ed3-dfdb64a3a2e3
keywords:
- ASF (Advanced Systems Format), pausando a reprodução
- ASF (formato de sistemas avançados), pausando a reprodução
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- ASF (Advanced Systems Format), parando a reprodução
- ASF (formato de sistemas avançados), parando a reprodução
- ASF (Advanced Systems Format), reprodução Pausando ou parando
- ASF (formato de sistemas avançados), pausando ou parando reprodução
- leitores assíncronos, pausando a reprodução
- leitores assíncronos, parando a reprodução
- leitores assíncronos, pausando ou parando a reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728ce4c58f9198f605764d0f19d0d5f55c7f6c6b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104498980"
---
# <a name="to-pause-or-stop-playback"></a><span data-ttu-id="fd153-114">Para pausar ou parar a reprodução</span><span class="sxs-lookup"><span data-stu-id="fd153-114">To Pause or Stop Playback</span></span>

<span data-ttu-id="fd153-115">Quando você chama [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) para começar a reproduzir um arquivo, o leitor assíncrono continuará a ser processado em seus próprios threads separados até que o final do arquivo seja atingido.</span><span class="sxs-lookup"><span data-stu-id="fd153-115">When you call [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) to begin playing a file, the asynchronous reader will continue processing in its own separate threads until the end of the file is reached.</span></span> <span data-ttu-id="fd153-116">Você pode pausar ou parar a entrega de amostras usando os métodos [**IWMReader::P ause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) ou [**IWMReader:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fd153-116">You can pause or stop the delivery of samples using the [**IWMReader::Pause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) or [**IWMReader::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) methods respectively.</span></span>

## <a name="pausing"></a><span data-ttu-id="fd153-117">Pausando</span><span class="sxs-lookup"><span data-stu-id="fd153-117">Pausing</span></span>

<span data-ttu-id="fd153-118">Quando você chama **IWMReader::P ause** para pausar a reprodução de um arquivo, o leitor controla a posição atual no arquivo.</span><span class="sxs-lookup"><span data-stu-id="fd153-118">When you call **IWMReader::Pause** to pause playback of a file, the reader keeps track of the current position in the file.</span></span> <span data-ttu-id="fd153-119">Para retomar a reprodução após a pausa, chame [**IWMReader:: resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume).</span><span class="sxs-lookup"><span data-stu-id="fd153-119">To resume playing after pausing, call [**IWMReader::Resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume).</span></span> <span data-ttu-id="fd153-120">A reprodução será retomada do ponto em que está em pausa.</span><span class="sxs-lookup"><span data-stu-id="fd153-120">Playback will resume from the point at which it paused.</span></span>

## <a name="stopping"></a><span data-ttu-id="fd153-121">Parando</span><span class="sxs-lookup"><span data-stu-id="fd153-121">Stopping</span></span>

<span data-ttu-id="fd153-122">Quando você chama **IWMReader:: Stop** para interromper a reprodução de um arquivo, o leitor não controla nenhuma informação sobre o progresso da reprodução.</span><span class="sxs-lookup"><span data-stu-id="fd153-122">When you call **IWMReader::Stop** to halt playback of a file, the reader does not keep track of any information about the progress of playback.</span></span> <span data-ttu-id="fd153-123">Para usar **parar** e depois retornar ao ponto de interrupção, você deve salvar o tempo de apresentação do último exemplo entregue e usá-lo em sua chamada para **IWMReader:: Start**.</span><span class="sxs-lookup"><span data-stu-id="fd153-123">To use **Stop** and later return to the stopping point you must save the presentation time of the last sample delivered and use it in your call to **IWMReader::Start**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd153-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd153-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd153-125">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="fd153-125">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="fd153-126">**Lendo arquivos com o leitor assíncrono**</span><span class="sxs-lookup"><span data-stu-id="fd153-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




