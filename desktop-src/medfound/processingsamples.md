---
description: Processando entrada e saída do codec DMO
ms.assetid: fab6244e-a20e-4395-a82c-0905e3225516
title: Processando entrada e saída do codec DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c6781d877f4c863161537fcc5b6a746691cfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296531"
---
# <a name="processing-codec-dmo-input-and-output"></a><span data-ttu-id="af47b-103">Processando entrada e saída do codec DMO</span><span class="sxs-lookup"><span data-stu-id="af47b-103">Processing Codec DMO Input and Output</span></span>

<span data-ttu-id="af47b-104">Quando você tiver configurado o tipo de entrada e o tipo de saída para um DMO, poderá começar a processar os exemplos de dados.</span><span class="sxs-lookup"><span data-stu-id="af47b-104">When you have configured the input type and output type for a DMO, you can begin processing data samples.</span></span> <span data-ttu-id="af47b-105">Você passa amostras para o DMO para processamento usando o método **IMediaObject::P rocessinput** e, em seguida, recupera o exemplo processado chamando **IMediaObject::P rocessoutput**.</span><span class="sxs-lookup"><span data-stu-id="af47b-105">You pass samples to the DMO for processing using the **IMediaObject::ProcessInput** method, and then retrieve the processed sample by calling **IMediaObject::ProcessOutput**.</span></span> <span data-ttu-id="af47b-106">Você deve definir carimbos e durações de tempo precisos para todos os exemplos de entrada passados.</span><span class="sxs-lookup"><span data-stu-id="af47b-106">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="af47b-107">Os carimbos de data/hora não são estritamente necessários, mas ajudam a manter a sincronização de áudio/vídeo.</span><span class="sxs-lookup"><span data-stu-id="af47b-107">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="af47b-108">Se você não tiver carimbos de data/hora para suas amostras, é melhor deixá-las fora do que usar valores incertos.</span><span class="sxs-lookup"><span data-stu-id="af47b-108">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af47b-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="af47b-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af47b-110">Trabalhando com codec DMOs</span><span class="sxs-lookup"><span data-stu-id="af47b-110">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 



