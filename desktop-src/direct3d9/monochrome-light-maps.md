---
description: Algumas placas aceleradoras 3D mais antigas não oferecem suporte à mesclagem de textura com o valor de alfa do pixel de destino.
ms.assetid: 77d3b9fd-3232-4955-9df2-d4763d3eed6f
title: Mapas leves monocromáticos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ca63c2e7bb3ed51f1c6c5184536aa51e0a11e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105763903"
---
# <a name="monochrome-light-maps-direct3d-9"></a><span data-ttu-id="3fec1-103">Mapas leves monocromáticos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3fec1-103">Monochrome Light Maps (Direct3D 9)</span></span>

<span data-ttu-id="3fec1-104">Algumas placas aceleradoras 3D mais antigas não oferecem suporte à mesclagem de textura com o valor de alfa do pixel de destino.</span><span class="sxs-lookup"><span data-stu-id="3fec1-104">Some older 3D accelerator boards do not support texture blending using the alpha value of the destination pixel.</span></span> <span data-ttu-id="3fec1-105">Consulte [mesclagem de textura alfa (Direct3D 9)](alpha-texture-blending.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="3fec1-105">See [Alpha Texture Blending (Direct3D 9)](alpha-texture-blending.md) for more information.</span></span> <span data-ttu-id="3fec1-106">Em geral, esses adaptadores também não oferecem suporte à mistura de múltipla textura.</span><span class="sxs-lookup"><span data-stu-id="3fec1-106">These adapters also generally do not support multiple texture blending.</span></span> <span data-ttu-id="3fec1-107">Se o app for executado em um adaptador desse tipo, ele pode usar a mistura da textura de passagem múltipla para executar o mapeamento de luzes monocromáticas.</span><span class="sxs-lookup"><span data-stu-id="3fec1-107">If your application is running on an adapter such as this, it can use multipass texture blending to perform monochrome light mapping.</span></span>

<span data-ttu-id="3fec1-108">Para executar o mapeamento de luzes monocromáticas, um app armazena as informações de iluminação nos dados de alfa das texturas de mapa de luzes.</span><span class="sxs-lookup"><span data-stu-id="3fec1-108">To perform monochrome light mapping, an application stores the lighting information in the alpha data of its light map textures.</span></span> <span data-ttu-id="3fec1-109">O app usa os recursos de filtragem de textura do Direct3D para realizar um mapeamento de cada pixel na imagem do primitivo para um texel correspondente no mapa de luz.</span><span class="sxs-lookup"><span data-stu-id="3fec1-109">The application uses the texture filtering capabilities of Direct3D to perform a mapping from each pixel in the primitive's image to a corresponding texel in the light map.</span></span> <span data-ttu-id="3fec1-110">Ele define o fator de mesclagem de origem para o valor de alfa do texel correspondente.</span><span class="sxs-lookup"><span data-stu-id="3fec1-110">It sets the source blending factor to the alpha value of the corresponding texel.</span></span>

<span data-ttu-id="3fec1-111">O exemplo a seguir ilustra como um aplicativo pode usar uma textura como um mapa claro monocromático:</span><span class="sxs-lookup"><span data-stu-id="3fec1-111">The following example illustrates how an application can use a texture as a monochrome light map:</span></span>


```
// This example assumes that d3dDevice is a valid pointer to an
// IDirect3DDevice9 interface and that lptexLightMap is a valid
// pointer to a texture that contains monochrome light map data.

// Set the light map texture as the current texture.
d3dDevice->SetTexture(0, lptexLightMap);

// Set the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLOROP, D3DTOP_SELECTARG1);

// Set argument 1 to the color operation.
d3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1,
                                D3DTA_TEXTURE | D3DTA_ALPHAREPLICATE);
```



<span data-ttu-id="3fec1-112">Como os adaptadores de vídeo que não dão suporte à mesclagem alfa de destino normalmente não dão suporte a várias mesclagens de textura, este exemplo define o mapa claro como a primeira textura, que está disponível em todas as placas aceleradoras 3D.</span><span class="sxs-lookup"><span data-stu-id="3fec1-112">Because display adapters that do not support destination alpha blending usually do not support multiple texture blending, this example sets the light map as the first texture, which is available on all 3D accelerator cards.</span></span> <span data-ttu-id="3fec1-113">O código de exemplo define a operação de cor para o estágio de mesclagem da textura para misturar os dados de textura com a cor existente do primitivo.</span><span class="sxs-lookup"><span data-stu-id="3fec1-113">The sample code sets the color operation for the texture's blending stage to blend the texture data with the primitive's existing color.</span></span> <span data-ttu-id="3fec1-114">Em seguida, ele seleciona a primeira textura e a cor existente do primitivo como os dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="3fec1-114">It then selects the first texture and the primitive's existing color as the input data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fec1-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3fec1-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fec1-116">Mapeamento claro com texturas</span><span class="sxs-lookup"><span data-stu-id="3fec1-116">Light Mapping with Textures</span></span>](light-mapping-with-textures.md)
</dt> </dl>

 

 



