---
description: O atributo stretchmode especifica como alongar uma imagem que não corresponde às dimensões de saída.
ms.assetid: 9a26bb8b-2b1c-424a-ae30-e175c60c76a1
title: Atributo stretchmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a629a34dc1875a7f1d3669e32c53d0e8d3d29c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829372"
---
# <a name="stretchmode-attribute"></a><span data-ttu-id="d7475-103">Atributo stretchmode</span><span class="sxs-lookup"><span data-stu-id="d7475-103">stretchmode Attribute</span></span>

> [!Note]  
> <span data-ttu-id="d7475-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="d7475-104">\[Deprecated.</span></span> <span data-ttu-id="d7475-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d7475-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d7475-106">O `stretchmode` atributo especifica como alongar uma imagem que não corresponde às dimensões de saída.</span><span class="sxs-lookup"><span data-stu-id="d7475-106">The `stretchmode` attribute specifies how to stretch an image that does not match the output dimensions.</span></span>

## <a name="possible-values"></a><span data-ttu-id="d7475-107">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="d7475-107">Possible Values</span></span>

<span data-ttu-id="d7475-108">Deve ter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d7475-108">Must have one of the following values.</span></span>

-   <span data-ttu-id="d7475-109">"Stretch": a imagem é ampliada para se ajustar ao tamanho do quadro de saída sem preservar a taxa de proporção.</span><span class="sxs-lookup"><span data-stu-id="d7475-109">"stretch": The image is stretched to fit the output frame size without preserving aspect ratio.</span></span> <span data-ttu-id="d7475-110">(Padrão)</span><span class="sxs-lookup"><span data-stu-id="d7475-110">(Default)</span></span>
-   <span data-ttu-id="d7475-111">"cortar": a imagem é cortada para se ajustar ao tamanho do quadro de saída.</span><span class="sxs-lookup"><span data-stu-id="d7475-111">"crop": The image is cropped to fit the output frame size.</span></span>
-   <span data-ttu-id="d7475-112">"preserveaspectratio": a taxa de proporção original é preservada, com uma Letterbox preta ao longo da dimensão mais curta.</span><span class="sxs-lookup"><span data-stu-id="d7475-112">"preserveaspectratio": The original aspect ratio is preserved, with a black letterbox along the shorter dimension.</span></span>
-   <span data-ttu-id="d7475-113">"preserveaspectrationoletterbox": a imagem é redimensionada para preencher o quadro de destino inteiro, preservando a taxa de proporção.</span><span class="sxs-lookup"><span data-stu-id="d7475-113">"preserveaspectrationoletterbox": The image is resized to fill the entire target frame while preserving the aspect ratio.</span></span>

## <a name="applies-to"></a><span data-ttu-id="d7475-114">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="d7475-114">Applies To</span></span>

[<span data-ttu-id="d7475-115">**clip**</span><span class="sxs-lookup"><span data-stu-id="d7475-115">**clip**</span></span>](clip-element.md)

## <a name="see-also"></a><span data-ttu-id="d7475-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7475-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7475-117">Atributos XTL</span><span class="sxs-lookup"><span data-stu-id="d7475-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="d7475-118">**IAMTimelineSrc:: setalongamode**</span><span class="sxs-lookup"><span data-stu-id="d7475-118">**IAMTimelineSrc::SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 



