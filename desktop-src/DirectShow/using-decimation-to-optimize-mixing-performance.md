---
description: Usando o Decimation para otimizar o desempenho de mixagem
ms.assetid: 94d4ce86-9d60-4fd4-ab01-851dc073680b
title: Usando o Decimation para otimizar o desempenho de mixagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e9e4ddfe3bbba3eb5eeab91b7cf0e8b9cbfa03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829059"
---
# <a name="using-decimation-to-optimize-mixing-performance"></a><span data-ttu-id="d17c0-103">Usando o Decimation para otimizar o desempenho de mixagem</span><span class="sxs-lookup"><span data-stu-id="d17c0-103">Using Decimation to Optimize Mixing Performance</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d17c0-104">A otimização descrita nesta seção é altamente dependente do hardware subjacente.</span><span class="sxs-lookup"><span data-stu-id="d17c0-104">The optimization described in this section is highly dependent on the underlying hardware.</span></span> <span data-ttu-id="d17c0-105">A menos que você possa garantir que tipo de hardware de gráficos será usado com o aplicativo, pode degradar seriamente a aparência da imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d17c0-105">Unless you can guarantee what type of graphics hardware will be used with the application, it may seriously degrade the appearance of the video image.</span></span>

 

<span data-ttu-id="d17c0-106">A HDTV requer muita capacidade de processamento, que em sistemas mais novos é fornecida principalmente pela placa gráfica.</span><span class="sxs-lookup"><span data-stu-id="d17c0-106">HDTV requires a lot of processing power, which on newer systems is provided mostly by the graphics card.</span></span> <span data-ttu-id="d17c0-107">Mas mesmo se a placa gráfica e o decodificador puderem dar suporte a resoluções de 1920 x 1080, talvez o usuário nem sempre tenha seu monitor definido para essa resolução.</span><span class="sxs-lookup"><span data-stu-id="d17c0-107">But even if the graphics card and the decoder can support resolutions of 1920x1080, the user may not always have their monitor set to this resolution.</span></span> <span data-ttu-id="d17c0-108">Nesse caso, o chip de gráficos é necessário para criar uma imagem 1920 x 1080 e, em seguida, reduzir a resolução antes de enviá-la para o buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="d17c0-108">In this case, the graphics chip is required to create a 1920 x 1080 image, and then reduce the resolution before sending it to the frame buffer.</span></span>

<span data-ttu-id="d17c0-109">Como esse é um desperdício de poder de processamento, o VMR fornece uma maneira de DECIMATE (reduzir) a imagem no momento em que ela está sendo processada na superfície do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="d17c0-109">Since this is a waste of processing power, the VMR provides a way to decimate (reduce) the image at the time it is being rendered onto the DirectDraw surface.</span></span> <span data-ttu-id="d17c0-110">Isso elimina a cópia de memória extra necessária se a imagem tiver que ser redimensionada depois de ser renderizada.</span><span class="sxs-lookup"><span data-stu-id="d17c0-110">This eliminates the extra memory copy required if the image has to be resized after it has been rendered.</span></span>

<span data-ttu-id="d17c0-111">**VMR-7:** Para habilitar Decimation, chame [**IVMRMixerControl:: SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) com o \_ sinalizador MixerPref DecimateOutput.</span><span class="sxs-lookup"><span data-stu-id="d17c0-111">**VMR-7:** To enable decimation, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) with the MixerPref\_DecimateOutput flag.</span></span>

<span data-ttu-id="d17c0-112">**VMR-9:** Para habilitar Decimation, chame [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) com o \_ sinalizador MixerPref9 DecimateOutput.</span><span class="sxs-lookup"><span data-stu-id="d17c0-112">**VMR-9:** To enable decimation, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_DecimateOutput flag.</span></span>

<span data-ttu-id="d17c0-113">O método **SetMixingPrefs** deve ser chamado antes da conexão do VMR.</span><span class="sxs-lookup"><span data-stu-id="d17c0-113">The **SetMixingPrefs** method must be called before the VMR is connected.</span></span> <span data-ttu-id="d17c0-114">Os sinalizadores de preferência de combinação não podem ser alterados após a execução do grafo.</span><span class="sxs-lookup"><span data-stu-id="d17c0-114">The mixing preference flags cannot be changed once the graph is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d17c0-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d17c0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d17c0-116">Usando o modo de mixagem do VMR</span><span class="sxs-lookup"><span data-stu-id="d17c0-116">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



