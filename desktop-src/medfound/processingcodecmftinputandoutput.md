---
description: Entrada e saída de MFT do codec de processamento
ms.assetid: 2d012508-de13-411f-9102-22e47faddffd
title: Entrada e saída de MFT do codec de processamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af3a16fa1855574f1b7618bc0d41bf85c15412f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164894"
---
# <a name="processing-codec-mft-input-and-output"></a><span data-ttu-id="62977-103">Entrada e saída de MFT do codec de processamento</span><span class="sxs-lookup"><span data-stu-id="62977-103">Processing Codec MFT Input and Output</span></span>

<span data-ttu-id="62977-104">Quando você tiver configurado o tipo de entrada e o tipo de saída para um MFT, você poderá começar a processar exemplos de dados.</span><span class="sxs-lookup"><span data-stu-id="62977-104">When you have configured the input type and output type for an MFT, you can begin processing data samples.</span></span> <span data-ttu-id="62977-105">Você passa amostras para o MFT para processamento usando o método [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e, em seguida, recupera o exemplo processado chamando [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span><span class="sxs-lookup"><span data-stu-id="62977-105">You pass samples to the MFT for processing by using the [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method, and then retrieve the processed sample by calling [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="62977-106">Você deve definir carimbos e durações de tempo precisos para todos os exemplos de entrada passados.</span><span class="sxs-lookup"><span data-stu-id="62977-106">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="62977-107">Os carimbos de data/hora não são estritamente necessários, mas ajudam a manter a sincronização de áudio/vídeo.</span><span class="sxs-lookup"><span data-stu-id="62977-107">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="62977-108">Se você não tiver carimbos de data/hora para suas amostras, é melhor deixá-las fora do que usar valores incertos.</span><span class="sxs-lookup"><span data-stu-id="62977-108">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62977-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="62977-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62977-110">Trabalhando com codec MFTs</span><span class="sxs-lookup"><span data-stu-id="62977-110">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



