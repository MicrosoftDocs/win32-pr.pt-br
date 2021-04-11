---
description: O modo de endereço de textura de encapsulamento, identificado pelo \_ membro D3DTADDRESS Wrap do tipo enumerado D3DTEXTUREADDRESS, faz o Direct3D repetir a textura em cada junção de número inteiro.
ms.assetid: fe33c484-346d-4888-ba88-b8ab00feefbb
title: Modo de endereço de textura de encapsulamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721ace45599236022f32e6b0ec3723e346befbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163715"
---
# <a name="wrap-texture-address-mode-direct3d-9"></a><span data-ttu-id="b9563-103">Modo de endereço de textura de encapsulamento (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b9563-103">Wrap Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="b9563-104">O modo de endereço de textura de encapsulamento, identificado pelo \_ membro D3DTADDRESS Wrap do tipo enumerado [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , faz o Direct3D repetir a textura em cada junção de número inteiro.</span><span class="sxs-lookup"><span data-stu-id="b9563-104">The wrap texture address mode, identified by the D3DTADDRESS\_WRAP member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, makes Direct3D repeat the texture on every integer junction.</span></span> <span data-ttu-id="b9563-105">Suponhamos que, por exemplo, seu aplicativo crie uma primitiva quadrada e especifique as coordenadas de textura de (0.0,0.0), (0.0,3.0), (3.0,3.0) e (3.0,0.0).</span><span class="sxs-lookup"><span data-stu-id="b9563-105">Suppose, for example, your application creates a square primitive and specifies texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0).</span></span> <span data-ttu-id="b9563-106">Definir o modo de endereçamento de textura como D3DTADDRESS \_ encapsula os resultados na textura que está sendo aplicada três vezes nas direções u e v, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="b9563-106">Setting the texture addressing mode to D3DTADDRESS\_WRAP results in the texture being applied three times in both the u-and v-directions, as shown in the following illustration.</span></span>

![ilustração de uma textura de face encapsulada na direção u e na direção v](images/wrap.png)

<span data-ttu-id="b9563-108">Os efeitos desse modo de endereço de textura são semelhantes, mas distintos do modo de espelho.</span><span class="sxs-lookup"><span data-stu-id="b9563-108">The effects of this texture address mode are similar to, but distinct from, those of the mirror mode.</span></span> <span data-ttu-id="b9563-109">Para obter mais informações, consulte [modo de endereço de textura de espelho (Direct3D 9)](mirror-texture-address-mode.md).</span><span class="sxs-lookup"><span data-stu-id="b9563-109">For more information, see [Mirror Texture Address Mode (Direct3D 9)](mirror-texture-address-mode.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9563-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b9563-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9563-111">Modos de endereçamento de textura</span><span class="sxs-lookup"><span data-stu-id="b9563-111">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
