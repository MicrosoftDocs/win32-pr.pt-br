---
description: Tipo de formato VideoInfo2
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: Tipo de formato VideoInfo2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b0f435e0e2a1b5b1d948c42a881f19300a9c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789823"
---
# <a name="videoinfo2-format-type"></a><span data-ttu-id="3e552-103">Tipo de formato VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="3e552-103">VideoInfo2 Format Type</span></span>

<span data-ttu-id="3e552-104">O tipo de mídia preferencial de um PIN de visualização pode ser um tipo com um formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="3e552-104">A preview pin's preferred media type might be a type with a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format.</span></span> <span data-ttu-id="3e552-105">Essa estrutura de formato dá suporte a recursos especiais, como taxas de proporção de vídeo e imagem entrelaçadas.</span><span class="sxs-lookup"><span data-stu-id="3e552-105">This format structure supports special features such as interlaced video and picture aspect ratios.</span></span>

<span data-ttu-id="3e552-106">O VMR-7 e o VMR-9 dão suporte ao [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) diretamente.</span><span class="sxs-lookup"><span data-stu-id="3e552-106">The VMR-7 and the VMR-9 both support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) directly.</span></span> <span data-ttu-id="3e552-107">Quando você conectar o VMR ao decodificador, ele negociará o melhor formato.</span><span class="sxs-lookup"><span data-stu-id="3e552-107">When you connect the VMR to the decoder, they will negotiate the best format.</span></span> <span data-ttu-id="3e552-108">No entanto, o filtro de processamento de vídeo mais antigo não oferece suporte a **VIDEOINFOHEADER2**.</span><span class="sxs-lookup"><span data-stu-id="3e552-108">The older Video Renderer filter, however, does not support **VIDEOINFOHEADER2**.</span></span> <span data-ttu-id="3e552-109">Para usar os tipos de formato **VIDEOINFOHEADER2** com o filtro de processador de vídeo, você deve inserir o filtro de [mixer de sobreposição](overlay-mixer-filter.md) no grafo.</span><span class="sxs-lookup"><span data-stu-id="3e552-109">To use **VIDEOINFOHEADER2** format types with the Video Renderer filter, you must insert the [Overlay Mixer](overlay-mixer-filter.md) filter into the graph.</span></span>

1.  <span data-ttu-id="3e552-110">Enumere os tipos de mídia preferenciais no pino de saída do filtro de decodificador, usando o método [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="3e552-110">Enumerate the preferred media types on the decoder filter's output pin, using the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>
2.  <span data-ttu-id="3e552-111">Verifique o primeiro tipo de mídia na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="3e552-111">Check the first media type in the enumeration sequence.</span></span>
3.  <span data-ttu-id="3e552-112">Se o tipo de formato for **Format \_ VideoInfo2**, conecte o pino de saída ao mixer de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="3e552-112">If the format type is **FORMAT\_VideoInfo2**, connect the output pin to the Overlay Mixer.</span></span> <span data-ttu-id="3e552-113">Em seguida, conecte o mixer de sobreposição ao processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3e552-113">Then connect the Overlay Mixer to the video renderer.</span></span> <span data-ttu-id="3e552-114">(Consulte [Pins de porta de vídeo](video-port-pins.md).)</span><span class="sxs-lookup"><span data-stu-id="3e552-114">(See [Video Port Pins](video-port-pins.md).)</span></span>

<span data-ttu-id="3e552-115">Se você não se preocupa com esses recursos, não precisa usar o mixer de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="3e552-115">If you do not care about these features, you do not have to use the Overlay Mixer.</span></span> <span data-ttu-id="3e552-116">Conecte o decodificador diretamente ao processador de vídeo e ele se conectará com um formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="3e552-116">Connect the decoder directly to the Video Renderer, and it will connect with a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e552-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e552-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e552-118">Tópicos de captura avançada</span><span class="sxs-lookup"><span data-stu-id="3e552-118">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="3e552-119">Usando o mixer de sobreposição na captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="3e552-119">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



