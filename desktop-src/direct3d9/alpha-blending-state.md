---
description: O valor alfa de uma cor controla sua transparência. Habilitar a mesclagem alfa permite que cores, materiais e texturas em uma superfície sejam mescladas com transparência em outra superfície.
ms.assetid: e8e925d5-262d-45c0-be9f-21c9a103d7b7
title: Estado de mistura alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884ecad07fb9aefba08a0abbab92969937ec6361
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370452"
---
# <a name="alpha-blending-state-direct3d-9"></a><span data-ttu-id="23711-104">Estado de mistura alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="23711-104">Alpha Blending State (Direct3D 9)</span></span>

<span data-ttu-id="23711-105">O valor alfa de uma cor controla sua transparência.</span><span class="sxs-lookup"><span data-stu-id="23711-105">The alpha value of a color controls its transparency.</span></span> <span data-ttu-id="23711-106">Habilitar a mesclagem alfa permite que cores, materiais e texturas em uma superfície sejam mescladas com transparência em outra superfície.</span><span class="sxs-lookup"><span data-stu-id="23711-106">Enabling alpha blending allows colors, materials, and textures on a surface to be blended with transparency onto another surface.</span></span>

<span data-ttu-id="23711-107">Para obter mais informações, consulte [mesclagem de textura alfa (Direct3D 9)](alpha-texture-blending.md) e [mesclagem de textura (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="23711-107">For more information, see [Alpha Texture Blending (Direct3D 9)](alpha-texture-blending.md) and [Texture Blending (Direct3D 9)](texture-blending.md).</span></span>

<span data-ttu-id="23711-108">Os aplicativos escritos em C++ usam o estado de renderização [**D3DRS \_ ALPHABLENDENABLE**](./d3drenderstatetype.md) para habilitar a mesclagem de transparência alfa.</span><span class="sxs-lookup"><span data-stu-id="23711-108">Applications written in C++ use the [**D3DRS\_ALPHABLENDENABLE**](./d3drenderstatetype.md) render state to enable alpha transparency blending.</span></span> <span data-ttu-id="23711-109">A API do Direct3D permite muitos tipos de mistura alfa.</span><span class="sxs-lookup"><span data-stu-id="23711-109">The Direct3D API allows many types of alpha blending.</span></span> <span data-ttu-id="23711-110">No entanto, é importante observar que o hardware 3D do usuário pode não dar suporte a todos os Estados de mesclagem permitidos pelo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="23711-110">However, it is important to note the user's 3D hardware might not support all the blending states allowed by Direct3D.</span></span>

<span data-ttu-id="23711-111">O tipo de mistura alfa que é feito depende dos Estados de renderização [**D3DRS \_ SRCBLEND**](./d3drenderstatetype.md) e **D3DRS \_ DESTBLEND** .</span><span class="sxs-lookup"><span data-stu-id="23711-111">The type of alpha blending that is done depends on the [**D3DRS\_SRCBLEND**](./d3drenderstatetype.md) And **D3DRS\_DESTBLEND** render states.</span></span> <span data-ttu-id="23711-112">Os Estados de mesclagem de origem e destino são usados em pares.</span><span class="sxs-lookup"><span data-stu-id="23711-112">Source and destination blend states are used in pairs.</span></span> <span data-ttu-id="23711-113">O exemplo de código a seguir demonstra como o estado de mesclagem de origem é definido como D3DBLEND \_ SRCCOLOR e o estado de mesclagem de destino é definido como D3DBLEND \_ INVSRCCOLOR.</span><span class="sxs-lookup"><span data-stu-id="23711-113">The following code example demonstrates how the source blend state is set to D3DBLEND\_SRCCOLOR and the destination blend state is set to D3DBLEND\_INVSRCCOLOR.</span></span>


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the source blend state.
d3dDevice->SetRenderState(D3DRS_SRCBLEND, D3DBLEND_SRCCOLOR);

// Set the destination blend state.

d3dDevice->SetRenderState(D3DRS_DESTBLEND, D3DBLEND_INVSRCCOLOR);
```



<span data-ttu-id="23711-114">Alterar os Estados de mesclagem de origem e destino pode dar a aparência dos objetos emissiva em uma atmosfera de Foggy ou poeira.</span><span class="sxs-lookup"><span data-stu-id="23711-114">Altering the source and destination blend states can give the appearance of emissive objects in a foggy or dusty atmosphere.</span></span> <span data-ttu-id="23711-115">Por exemplo, se seu aplicativo modela chamas, força campos, emissões de plasma ou objetos de radiante da mesma forma em um ambiente Foggy, defina os Estados de mesclagem de origem e destino como D3DBLEND \_ um.</span><span class="sxs-lookup"><span data-stu-id="23711-115">For instance, if your application models flames, force fields, plasma beams, or similarly radiant objects in a foggy environment, set the source and destination blend states to D3DBLEND\_ONE.</span></span>

<span data-ttu-id="23711-116">Outra aplicação da mistura alfa é controlar a iluminação em uma cena 3D, também chamada de mapeamento leve.</span><span class="sxs-lookup"><span data-stu-id="23711-116">Another application of alpha blending is to control the lighting in a 3D scene, also called light mapping.</span></span> <span data-ttu-id="23711-117">Definir o estado de mesclagem de origem como D3DBLEND \_ zero e o estado de mesclagem de destino como D3DBLEND \_ SRCALPHA escurece uma cena de acordo com as informações de alfa de origem.</span><span class="sxs-lookup"><span data-stu-id="23711-117">Setting the source blend state to D3DBLEND\_ZERO and the destination blend state to D3DBLEND\_SRCALPHA darkens a scene according to the source alpha information.</span></span> <span data-ttu-id="23711-118">O primitivo de origem é usado como um mapa claro que dimensiona o conteúdo do buffer de quadro para escurecer quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="23711-118">The source primitive is used as a light map that scales the contents of the frame buffer to darken it when appropriate.</span></span> <span data-ttu-id="23711-119">Isso produz o mapeamento de luz monocromática.</span><span class="sxs-lookup"><span data-stu-id="23711-119">This produces monochrome light mapping.</span></span>

<span data-ttu-id="23711-120">Você pode obter o mapeamento de luz de cor definindo o estado de mesclagem alfa de origem como D3DBLEND \_ zero e o estado de mesclagem de destino como D3DBLEND \_ SRCCOLOR.</span><span class="sxs-lookup"><span data-stu-id="23711-120">You can achieve color light mapping by setting the source alpha blending state to D3DBLEND\_ZERO and the destination blend state to D3DBLEND\_SRCCOLOR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23711-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="23711-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23711-122">Processar Estados</span><span class="sxs-lookup"><span data-stu-id="23711-122">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
