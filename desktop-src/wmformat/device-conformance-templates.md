---
title: Modelos de conformidade do dispositivo
description: Modelos de conformidade do dispositivo
ms.assetid: 5172ab39-819a-4d74-8e6e-b275b43f664c
keywords:
- SDK do Windows Media Format, modelos de conformidade do dispositivo
- codecs, modelos de conformidade do dispositivo
- modelos de conformidade do dispositivo, sobre
- modelos, modelos de conformidade do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eccb88b372f9e0eb463d88db83d70102408a7a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292771"
---
# <a name="device-conformance-templates"></a><span data-ttu-id="533be-107">Modelos de conformidade do dispositivo</span><span class="sxs-lookup"><span data-stu-id="533be-107">Device Conformance Templates</span></span>

<span data-ttu-id="533be-108">Os codecs do Windows Media 9 Series dão suporte a modelos de conformidade do dispositivo, que são definidos como intervalos de definições de configuração de fluxo e algoritmos de codec.</span><span class="sxs-lookup"><span data-stu-id="533be-108">The Windows Media 9 Series codecs support device conformance templates, which are defined ranges of stream configuration settings and codec algorithms.</span></span> <span data-ttu-id="533be-109">Cada modelo define os intervalos de valores apropriados para determinados dispositivos.</span><span class="sxs-lookup"><span data-stu-id="533be-109">Each template defines the ranges of values appropriate for certain devices.</span></span>

<span data-ttu-id="533be-110">No passado, os fabricantes de hardware que tornaram os dispositivos capazes de reproduzir arquivos ASF estavam funcionando para seus próprios padrões.</span><span class="sxs-lookup"><span data-stu-id="533be-110">In the past, the hardware manufacturers that made devices capable of playing ASF files were all working to their own standards.</span></span> <span data-ttu-id="533be-111">Isso resultou na ampla variedade de recursos em dispositivos semelhantes que continuam hoje.</span><span class="sxs-lookup"><span data-stu-id="533be-111">This resulted in the widely disparate range of capabilities on similar devices that continues today.</span></span>

<span data-ttu-id="533be-112">Com os modelos de conformidade do dispositivo, os codecs do Windows Media estabelecem um aterramento comum para dispositivos semelhantes.</span><span class="sxs-lookup"><span data-stu-id="533be-112">With device conformance templates, the Windows Media codecs establish common ground for similar devices.</span></span> <span data-ttu-id="533be-113">Os fabricantes de hardware podem declarar a quais modelos seus dispositivos estão em conformidade, permitindo que os criadores de conteúdo direcionem com mais confiança seus arquivos para a leitura de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="533be-113">Hardware manufacturers can state which templates their devices conform to, enabling content creators to more confidently target their files to reading devices.</span></span> <span data-ttu-id="533be-114">Também é mais fácil para os aplicativos de Player determinarem se um arquivo é inadequado para o dispositivo antes de tentar reproduzi-lo.</span><span class="sxs-lookup"><span data-stu-id="533be-114">It is also easier for player applications to determine whether a file is inappropriate for the device before attempting to play it.</span></span>

<span data-ttu-id="533be-115">Um modelo de conformidade do dispositivo é identificado por uma cadeia de caracteres, que é armazenada como um atributo de metadados associado ao fluxo ao qual o modelo se aplica.</span><span class="sxs-lookup"><span data-stu-id="533be-115">A device conformance template is identified by a string, which is stored as a metadata attribute associated with the stream to which the template applies.</span></span> <span data-ttu-id="533be-116">Para obter uma lista dos modelos e suas cadeias de caracteres e parâmetros, consulte [parâmetros de modelo de conformidade do dispositivo](device-conformance-template-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="533be-116">For a list of the templates and their strings and parameters, see [Device Conformance Template Parameters](device-conformance-template-parameters.md).</span></span>

<span data-ttu-id="533be-117">Os modelos de conformidade do dispositivo têm suporte para todos os codecs do Windows Media 9 Series e posteriores, exceto o codec de tela do Windows Media Video 9 e o codec Windows Media Audio 9 Lossless.</span><span class="sxs-lookup"><span data-stu-id="533be-117">Device conformance templates are supported for all of the Windows Media 9 Series and later codecs except the Windows Media Video 9 Screen codec and the Windows Media Audio 9 Lossless codec.</span></span>

## <a name="related-topics"></a><span data-ttu-id="533be-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="533be-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="533be-119">**Recursos do codec**</span><span class="sxs-lookup"><span data-stu-id="533be-119">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="533be-120">**Trabalhando com modelos de conformidade do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="533be-120">**Working with Device Conformance Templates**</span></span>](working-with-device-conformance-templates.md)
</dt> </dl>

 

 




