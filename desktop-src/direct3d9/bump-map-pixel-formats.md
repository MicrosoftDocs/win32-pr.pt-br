---
description: Um mapa de relevo é um objeto IDirect3DTexture9 que usa um formato de pixel especializado.
ms.assetid: 7f405cb9-9512-44da-8a85-4b7d22017284
title: Formatos de pixel do mapa de relevo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21bbe4a9999d875e43d33389f86b35d22c81b3bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010257"
---
# <a name="bump-map-pixel-formats-direct3d-9"></a><span data-ttu-id="183b6-103">Formatos de pixel do mapa de relevo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="183b6-103">Bump Map Pixel Formats (Direct3D 9)</span></span>

<span data-ttu-id="183b6-104">Um mapa de relevo é um objeto [**IDirect3DTexture9**](/windows/desktop/api) que usa um formato de pixel especializado.</span><span class="sxs-lookup"><span data-stu-id="183b6-104">A bump map is an [**IDirect3DTexture9**](/windows/desktop/api) object that uses a specialized pixel format.</span></span> <span data-ttu-id="183b6-105">Em vez de armazenar componentes de cores vermelho, verde e azul, cada pixel em um mapa de relevo armazena os valores Delta para você e v (D<sub>U</sub> e d<sub>v</sub>) e, às vezes, um componente de luminância, L. Esses valores são aplicados pelo sistema, conforme descrito no tópico [fórmulas de mapeamento de relevo (Direct3D 9)](bump-mapping-formulas.md) .</span><span class="sxs-lookup"><span data-stu-id="183b6-105">Rather than storing red, green, and blue color components, each pixel in a bump map stores the delta values for u and v (D<sub>U</sub> and D<sub>V</sub>) and sometimes a luminance component, L. These values are applied by the system as described in the [Bump Mapping Formulas (Direct3D 9)](bump-mapping-formulas.md) topic.</span></span>

<span data-ttu-id="183b6-106">Você pode especificar um formato de pixel do mapa de relevo definindo o formato como um dos seguintes: D3DFMT \_ CxV8U8, D3DFMT \_ V8U8, D3DFMT \_ L6V5U5, D3DFMT \_ X8L8V8U8, D3DFMT \_ Q8W8V8U8 ou D3DFMT \_ V16U16.</span><span class="sxs-lookup"><span data-stu-id="183b6-106">You can specify a bump map pixel format by setting the format to one of the following: D3DFMT\_CxV8U8, D3DFMT\_V8U8, D3DFMT\_L6V5U5, D3DFMT\_X8L8V8U8, D3DFMT\_Q8W8V8U8, or D3DFMT\_V16U16.</span></span> <span data-ttu-id="183b6-107">Para obter descrições, consulte [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="183b6-107">For descriptions, see [D3DFORMAT](d3dformat.md).</span></span>

<span data-ttu-id="183b6-108">Os componentes D<sub>U</sub> e d<sub>V</sub> de um pixel são valores assinados que variam de-1,0 a + 1,0.</span><span class="sxs-lookup"><span data-stu-id="183b6-108">The D<sub>U</sub> and D<sub>V</sub> components of a pixel are signed values that range from - 1.0 to +1.0.</span></span> <span data-ttu-id="183b6-109">O componente de luminância, quando usado, é um valor inteiro sem sinal que varia de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="183b6-109">The luminance component, when used, is an unsigned integer value that ranges from 0 to 255.</span></span>

> [!Note]  
> <span data-ttu-id="183b6-110">Antes de escolher um formato de pixel do mapa de relevo, verifique se há suporte para o formato específico.</span><span class="sxs-lookup"><span data-stu-id="183b6-110">Before picking a bump map pixel format, check if the particular format is supported.</span></span> <span data-ttu-id="183b6-111">Para obter mais informações, consulte [usando o mapeamento de relevo (Direct3D 9)](using-bump-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="183b6-111">For more information, see [Using Bump Mapping (Direct3D 9)](using-bump-mapping.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="183b6-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="183b6-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="183b6-113">Mapeamento de relevo</span><span class="sxs-lookup"><span data-stu-id="183b6-113">Bump Mapping</span></span>](bump-mapping.md)
</dt> </dl>

 

 



