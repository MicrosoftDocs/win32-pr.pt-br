---
description: Filtro de decodificador de CC
ms.assetid: 57ef75f6-411c-4b1f-b0dc-ac293ebc0b9c
title: Filtro de decodificador de CC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93995207e4f1a397db28f743d1f972b871b0553
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919769"
---
# <a name="cc-decoder-filter"></a><span data-ttu-id="d94d6-103">Filtro de decodificador de CC</span><span class="sxs-lookup"><span data-stu-id="d94d6-103">CC Decoder Filter</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d94d6-104">Este componente foi removido do Windows Vista e de sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="d94d6-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="d94d6-105">Ele está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d94d6-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="d94d6-106">O decodificador CC VBI é um filtro de classe de fluxo do modo kernel.</span><span class="sxs-lookup"><span data-stu-id="d94d6-106">The CC VBI Decoder is a kernel-mode stream class filter.</span></span> <span data-ttu-id="d94d6-107">Ele aparece em GraphEdit na categoria "codecs de VBI de streaming WDM".</span><span class="sxs-lookup"><span data-stu-id="d94d6-107">It appears in GraphEdit under the "WDM Streaming VBI Codecs" category.</span></span> <span data-ttu-id="d94d6-108">Ele aceita exemplos de onda fornecidos por um filtro de captura e entrega dados de legendas fechadas decodificados para a [linha 21 decodificador](line-21-decoder-filter.md) e/ou para aplicativos interessados.</span><span class="sxs-lookup"><span data-stu-id="d94d6-108">It accepts sample waveforms delivered by a capture filter and delivers decoded closed-captioning data to the [Line 21 Decoder](line-21-decoder-filter.md) and/or to interested applications.</span></span>

<span data-ttu-id="d94d6-109">Esse filtro tem dois pinos de entrada, VBI e HWCC.</span><span class="sxs-lookup"><span data-stu-id="d94d6-109">This filter has two input pins, VBI and HWCC.</span></span> <span data-ttu-id="d94d6-110">O PIN do VBI é usado para dados brutos do VBI e o PIN do HWCC é usado quando a decodificação de VBI é executada no hardware pelo filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="d94d6-110">The VBI pin is used for raw VBI data, and the HWCC pin is used when the VBI decoding is performed in hardware by the capture filter.</span></span> <span data-ttu-id="d94d6-111">Quando os dados são recebidos no PIN do HWCC, o decodificador de CC opera no modo de "passagem" e envia os dados diretamente para o decodificador da linha 21 sem processá-los de forma alguma.</span><span class="sxs-lookup"><span data-stu-id="d94d6-111">When the data is received on the HWCC pin, the CC Decoder operates in "pass-through" mode, and sends the data directly to the Line 21 Decoder without processing it in any way.</span></span> <span data-ttu-id="d94d6-112">Se o filtro de captura expõe um PIN HWCC, ele deve ser conectado diretamente ao PIN correspondente no decodificador CC.</span><span class="sxs-lookup"><span data-stu-id="d94d6-112">If the capture filter exposes an HWCC pin, it must be connected directly to the corresponding pin on the CC Decoder.</span></span> <span data-ttu-id="d94d6-113">A categoria de PIN é a **\_ captura de vídeo \_ CC \_ do PINNAME**.</span><span class="sxs-lookup"><span data-stu-id="d94d6-113">The pin category is **PINNAME\_VIDEO\_CC\_CAPTURE**.</span></span>

<span data-ttu-id="d94d6-114">O decodificador CC tem até oito pinos de saída, cada um deles pode selecionar suas próprias linhas e subfluxos.</span><span class="sxs-lookup"><span data-stu-id="d94d6-114">The CC Decoder has up to eight output pins, each of which can select their own lines and substreams.</span></span> <span data-ttu-id="d94d6-115">O primeiro pino de saída é conectado ao decodificador de linha 21.</span><span class="sxs-lookup"><span data-stu-id="d94d6-115">The first output pin is connected to the Line-21 Decoder.</span></span>

<span data-ttu-id="d94d6-116">O filtro de decodificador de CC aparece na categoria de filtro "codecs de VBI de streaming WDM" (**am \_ KSCATEGORY \_ VBICODEC**).</span><span class="sxs-lookup"><span data-stu-id="d94d6-116">The CC Decoder filter appears in the "WDM Streaming VBI Codecs" filter category (**AM\_KSCATEGORY\_VBICODEC**).</span></span>

<span data-ttu-id="d94d6-117">Como esse é um filtro de modo kernel, os aplicativos não podem criá-lo diretamente usando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="d94d6-117">Because this is a kernel-mode filter, applications cannot create it directly using **CoCreateInstance**.</span></span> <span data-ttu-id="d94d6-118">Em vez disso, use o [enumerador de dispositivo do sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="d94d6-118">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="d94d6-119">Para obter mais informações, consulte [Criando filtros de Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="d94d6-119">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d94d6-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d94d6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d94d6-121">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="d94d6-121">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="d94d6-122">Exibindo legendas ocultas</span><span class="sxs-lookup"><span data-stu-id="d94d6-122">Viewing Closed Captions</span></span>](viewing-closed-captions.md)
</dt> </dl>

 

 



