---
description: Controle de fluxo
ms.assetid: b529b38c-a25c-42dd-aee1-5d263c94202d
title: Controle de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41cee586737e131d4a32508b9ba6dd9ef1bd3b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829067"
---
# <a name="stream-control"></a><span data-ttu-id="f3bfc-103">Controle de fluxo</span><span class="sxs-lookup"><span data-stu-id="f3bfc-103">Stream Control</span></span>

<span data-ttu-id="f3bfc-104">A interface [**IVMRVideoStreamControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol) no PIN de entrada do VMR permite que os aplicativos e filtros upstream controlem o comportamento do componente do mixer, incluindo a ordem Z e o estado ativo dos fluxos de entrada do VMR.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-104">The [**IVMRVideoStreamControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol) interface on the VMR's input pin(s) enables applications and upstream filters to control the behavior of the mixer component, including the Z-order and the active state of the VMR's input streams.</span></span> <span data-ttu-id="f3bfc-105">Embora essa interface seja exposta nos Pins, ela opera no componente mixer do VMR, portanto, ela só estará disponível quando o mixer for carregado, que é quando o VMR está processando vários fluxos de entrada.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-105">Although this interface is exposed on the pins, it operates on the VMR's mixer component, so it is only available when the mixer is loaded, which is when the VMR is processing multiple input streams.</span></span> <span data-ttu-id="f3bfc-106">Os filtros upstream usam os métodos [**SetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey) e [**GetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey) para controlar a chave de cor de origem.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-106">Upstream filters use the [**SetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey) and [**GetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey) methods to control the source color key.</span></span> <span data-ttu-id="f3bfc-107">Esses métodos permitem efeitos como a sobreposição de animação em vídeo.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-107">These methods enable effects such as the overlay of animation over video.</span></span> <span data-ttu-id="f3bfc-108">Basta definir a chave de cor como a cor do plano de fundo do fluxo de animação e o VMR vai misturar esse fluxo com outro fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-108">Simply set the color key to the animation stream's background color, and the VMR will mix that stream with another video stream.</span></span> <span data-ttu-id="f3bfc-109">Os aplicativos devem tomar cuidado para não alterar a chave de cores para algum valor que seja diferente do valor que está sendo usado por um filtro upstream, como um decodificador.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-109">Applications should take care not to change the color key to some value that is different than the value being used by an upstream filter, such as a decoder.</span></span>

<span data-ttu-id="f3bfc-110">Os filtros usam os métodos [**GetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate) e [**SetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate) para informar ao mixer se os dados de entrada devem ser esperados de um PIN especificado.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-110">Filters use the [**GetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate) and [**SetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate) methods to tell the mixer whether to expect input data from a specified pin.</span></span> <span data-ttu-id="f3bfc-111">Por exemplo, o decodificador Line21 usa esses métodos para ativar o PIN de entrada do VMR para dados do Line21 somente quando esses dados estão presentes no fluxo.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-111">For example, the Line21 Decoder uses these methods to activate the VMR's input pin for Line21 data only when that data is present in the stream.</span></span> <span data-ttu-id="f3bfc-112">Definir um PIN como um estado inativo instrui o mixer a não aguardar dados de um PIN especificado antes de compor a imagem.</span><span class="sxs-lookup"><span data-stu-id="f3bfc-112">Setting a pin to an inactive state instructs the mixer not to wait for data from a specified pin before compositing the image.</span></span>

 

 



