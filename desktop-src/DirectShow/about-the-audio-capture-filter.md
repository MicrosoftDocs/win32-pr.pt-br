---
description: Sobre o filtro de captura de áudio
ms.assetid: ff345670-5a75-40d3-a228-8bc22aa76708
title: Sobre o filtro de captura de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5e28bef37ca52f0a33fc95b6d2a387cbbe2fb3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087859"
---
# <a name="about-the-audio-capture-filter"></a><span data-ttu-id="506c2-103">Sobre o filtro de captura de áudio</span><span class="sxs-lookup"><span data-stu-id="506c2-103">About the Audio Capture Filter</span></span>

<span data-ttu-id="506c2-104">O DirectShow habilita a captura de entradas analógicas em uma placa de som por meio do [filtro de captura de áudio](audio-capture-filter.md).</span><span class="sxs-lookup"><span data-stu-id="506c2-104">DirectShow enables capture from the analog inputs on a sound card through the [Audio Capture Filter](audio-capture-filter.md).</span></span> <span data-ttu-id="506c2-105">Esse filtro usa as APIs do wavee *xxx* para controlar qualquer dispositivo cujo driver dê suporte a essas APIs.</span><span class="sxs-lookup"><span data-stu-id="506c2-105">This filter uses the waveIn *XXX* APIs to control any device whose driver supports these APIs.</span></span> <span data-ttu-id="506c2-106">Cada cartão no sistema é representado por uma instância separada do filtro.</span><span class="sxs-lookup"><span data-stu-id="506c2-106">Each card on the system is represented by a separate instance of the filter.</span></span>

<span data-ttu-id="506c2-107">O filtro de captura de áudio expõe cada entrada no cartão, como o microfone ou a entrada MIDI, como um pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="506c2-107">The Audio Capture filter exposes each input on the card, such as the microphone or the MIDI input, as an input pin.</span></span> <span data-ttu-id="506c2-108">Os Pins de entrada representam o que o driver expõe como linhas de origem de áudio.</span><span class="sxs-lookup"><span data-stu-id="506c2-108">The input pins represent what the driver exposes as audio source lines.</span></span> <span data-ttu-id="506c2-109">No entanto, nenhum dado passa por esses Pins de entrada e eles não se conectam a outros filtros do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="506c2-109">No data travels through these input pins, however, and they do not connect to other DirectShow filters.</span></span> <span data-ttu-id="506c2-110">Eles simplesmente fornecem uma maneira para um aplicativo controlar as entradas.</span><span class="sxs-lookup"><span data-stu-id="506c2-110">They simply provide a way for an application to control the inputs.</span></span> <span data-ttu-id="506c2-111">O aplicativo pode usar um PIN de entrada para habilitar ou desabilitar a entrada, ou para definir propriedades de combinação como equalização Bass, equalização de agudo, panorâmica e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="506c2-111">The application can use an input pin to enable or disable the input, or to set mixing properties such as bass equalization, treble equalization, pan, and so forth.</span></span> <span data-ttu-id="506c2-112">A quantidade de controle disponível depende do driver.</span><span class="sxs-lookup"><span data-stu-id="506c2-112">The amount of control that is available depends on the driver.</span></span> <span data-ttu-id="506c2-113">Para compreender e explorar totalmente os recursos de uma placa de som específica, você precisará da documentação do fabricante do cartão.</span><span class="sxs-lookup"><span data-stu-id="506c2-113">To fully understand and exploit the capabilities of a particular sound card, you will need the documentation from the card's manufacturer.</span></span>

> [!Note]  
> <span data-ttu-id="506c2-114">Você pode capturar da entrada de CD-Audio, mas esse fluxo de áudio já passou pelo conversor digital para analógico, portanto, haverá uma perda de qualidade de som do CD original.</span><span class="sxs-lookup"><span data-stu-id="506c2-114">You can capture from the CD-Audio input, but this audio stream has already gone through the digital-to-analog converter, so there will be a loss of sound quality from the original CD.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="506c2-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="506c2-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="506c2-116">Captura de áudio</span><span class="sxs-lookup"><span data-stu-id="506c2-116">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



