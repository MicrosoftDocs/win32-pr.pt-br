---
description: Reprodução de fluxos de áudio do karaokê
ms.assetid: 1a8d0f42-35b8-4743-9ae7-619b99936f76
title: Reprodução de fluxos de áudio do karaokê
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907bfa3e359915cf537de75cdc739630fe607d97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105759493"
---
# <a name="playing-karaoke-audio-streams"></a><span data-ttu-id="aff5a-103">Reprodução de fluxos de áudio do karaokê</span><span class="sxs-lookup"><span data-stu-id="aff5a-103">Playing Karaoke Audio Streams</span></span>

<span data-ttu-id="aff5a-104">O navegador de DVD pode reproduzir discos DVD-Video com fluxos de áudio do karaokê, mas a reprodução do karaokê também requer um decodificador que dá suporte à mixagem de karaokê multicanal.</span><span class="sxs-lookup"><span data-stu-id="aff5a-104">The DVD Navigator can play DVD-Video discs with karaoke audio streams, but karaoke playback also requires a decoder that supports multichannel karaoke mixing.</span></span> <span data-ttu-id="aff5a-105">Especificamente, o decodificador deve dar suporte ao [**conjunto de propriedades do DVD karaokê**](dvd-karaoke-property-set.md) (am \_ Property \_ DVDKARAOKE).</span><span class="sxs-lookup"><span data-stu-id="aff5a-105">Specifically, the decoder must support the [**DVD Karaoke Property Set**](dvd-karaoke-property-set.md) (AM\_PROPERTY\_DVDKARAOKE).</span></span>

<span data-ttu-id="aff5a-106">Os discos do karaokê são um tipo de disco DVD-Video e têm a mesma estrutura de navegação.</span><span class="sxs-lookup"><span data-stu-id="aff5a-106">Karaoke discs are a type of DVD-Video disc and have the same navigation structure.</span></span> <span data-ttu-id="aff5a-107">As músicas geralmente são formatadas como títulos, e os títulos podem ser agrupados em conjuntos de títulos com base no desempenho, no estilo musical ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="aff5a-107">Songs are generally formatted as titles, and titles can be grouped into title sets based on performer, musical style, or other criteria.</span></span> <span data-ttu-id="aff5a-108">A principal diferença entre o karaokê e outros tipos de DVD-Videos é o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="aff5a-108">The main difference between karaoke and other types of DVD-Videos is the audio stream.</span></span> <span data-ttu-id="aff5a-109">Todos os discos do karaokê contêm áudio multicanal, geralmente Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="aff5a-109">Karaoke discs all contain multichannel audio, usually Dolby AC-3.</span></span> <span data-ttu-id="aff5a-110">Os canais 0 e 1 sempre contêm a música instrumenta de plano de fundo, enquanto os canais de 2 a 5 podem conter qualquer combinação de vozes de guia, Melodies de guia e efeitos sonoros.</span><span class="sxs-lookup"><span data-stu-id="aff5a-110">Channels 0 and 1 always contain the background instrumental music, while channels 2 through 5 can each contain any combination of guide vocals, guide melodies, and sound effects.</span></span> <span data-ttu-id="aff5a-111">Um aplicativo de karaokê pode controlar o volume e o alto-falante de destino para cada canal auxiliar.</span><span class="sxs-lookup"><span data-stu-id="aff5a-111">A karaoke application can control the volume and destination speaker for each auxiliary channel.</span></span>

<span data-ttu-id="aff5a-112">Quando o navegador de DVD detecta o conteúdo do karaokê em um disco e entra no modo do karaokê, ele informa ao decodificador que, em seguida, deve ativar mudo dos três canais superiores (os canais auxiliares) até que qualquer um deles seja explicitamente ativado por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aff5a-112">When the DVD Navigator detects karaoke content on a disc and goes into karaoke mode, it informs the decoder, which then should mute the upper three channels (the auxiliary channels) until any or all of them are explicitly turned on by an application.</span></span> <span data-ttu-id="aff5a-113">As tarefas básicas de um aplicativo do karaokê são:</span><span class="sxs-lookup"><span data-stu-id="aff5a-113">The basic tasks of a karaoke application are to:</span></span>

1.  <span data-ttu-id="aff5a-114">Determine o número de canais auxiliares e seu conteúdo usando métodos [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) .</span><span class="sxs-lookup"><span data-stu-id="aff5a-114">Determine the number of auxiliary channels and their contents using [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods.</span></span>
2.  <span data-ttu-id="aff5a-115">Forneça uma interface do usuário que exibe o conteúdo do canal e permite que os usuários ativem ou desativem qualquer canal auxiliar a qualquer momento, usando [**IDvdControl2:: SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode).</span><span class="sxs-lookup"><span data-stu-id="aff5a-115">Provide a user interface that displays the channel contents and enables users to turn any auxiliary channel on or off at any time, using [**IDvdControl2::SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode).</span></span>

<span data-ttu-id="aff5a-116">Essas etapas são ilustradas no aplicativo de exemplo de DVD em DVDCore. cpp no método **Getaudioattributes** .</span><span class="sxs-lookup"><span data-stu-id="aff5a-116">These steps are illustrated in the DVD Sample application in DVDCore.cpp in the **GetAudioAttributes** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aff5a-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aff5a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aff5a-118">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="aff5a-118">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



