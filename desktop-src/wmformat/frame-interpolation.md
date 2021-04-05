---
title: Interpolação de quadros
description: Interpolação de quadros
ms.assetid: 74dbe855-361c-42ba-b21b-322ccd1c91d0
keywords:
- SDK do Windows Media Format, interpolação de quadros
- codecs, interpolação de quadros
- interpolação de quadros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c62f95322920576eec0f10f3e4d61a279fdc4cf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007114"
---
# <a name="frame-interpolation"></a><span data-ttu-id="2d796-106">Interpolação de quadros</span><span class="sxs-lookup"><span data-stu-id="2d796-106">Frame Interpolation</span></span>

<span data-ttu-id="2d796-107">A interpolação de quadros é o processo de criação de quadros de vídeo intermediários com base nos dados em dois quadros consecutivos de vídeo codificado.</span><span class="sxs-lookup"><span data-stu-id="2d796-107">Frame interpolation is the process of creating intermediate video frames based on the data in two consecutive frames of encoded video.</span></span> <span data-ttu-id="2d796-108">Na verdade, a interpolação de quadros aumenta a [*taxa de quadros*](wmformat-glossary.md) do vídeo codificado no momento da decodificação.</span><span class="sxs-lookup"><span data-stu-id="2d796-108">In effect, frame interpolation increases the [*frame rate*](wmformat-glossary.md) of encoded video at the time of decoding.</span></span> <span data-ttu-id="2d796-109">Você pode usar a interpolação de quadro para melhorar a suavidade de reprodução de fluxos de vídeo com taxas de quadros baixas.</span><span class="sxs-lookup"><span data-stu-id="2d796-109">You can use frame interpolation to improve the smoothness of playback for video streams with low frame rates.</span></span>

<span data-ttu-id="2d796-110">Como esse é um recurso de decodificação, ele não envolve nenhuma opção de codificação especial e não adiciona sobrecarga ao conteúdo.</span><span class="sxs-lookup"><span data-stu-id="2d796-110">Because this is a decoding feature, it does not involve any special encoding options and adds no overhead to the content.</span></span> <span data-ttu-id="2d796-111">A interpolação do quadro é especificada como uma configuração de saída no objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="2d796-111">Frame interpolation is specified as an output setting in the reader object.</span></span>

<span data-ttu-id="2d796-112">Somente o codec do Windows Media Video 9 dá suporte à interpolação de quadros.</span><span class="sxs-lookup"><span data-stu-id="2d796-112">Only the Windows Media Video 9 codec supports frame interpolation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d796-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d796-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d796-114">**Recursos do codec**</span><span class="sxs-lookup"><span data-stu-id="2d796-114">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="2d796-115">**IWMReaderAdvanced2::SetOutputSetting**</span><span class="sxs-lookup"><span data-stu-id="2d796-115">**IWMReaderAdvanced2::SetOutputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[<span data-ttu-id="2d796-116">**Configurações de saída**</span><span class="sxs-lookup"><span data-stu-id="2d796-116">**Output Settings**</span></span>](output-settings.md)
</dt> </dl>

 

 




