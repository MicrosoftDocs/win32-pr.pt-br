---
description: O modo de endereço de textura de espelho, identificado pelo \_ membro D3DTADDRESS mirror do tipo enumerado D3DTEXTUREADDRESS, faz com que o Direct3D espelhe a textura a cada limite inteiro.
ms.assetid: 816efd4d-94b3-4b6c-9fc9-218cc2207b97
title: Modo de endereço de textura de espelho (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 471ad8b715d9375947162c66474687b9d6376bec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370159"
---
# <a name="mirror-texture-address-mode-direct3d-9"></a><span data-ttu-id="6e547-103">Modo de endereço de textura de espelho (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6e547-103">Mirror Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="6e547-104">O modo de endereço de textura de espelho, identificado pelo \_ membro D3DTADDRESS mirror do tipo enumerado [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , faz com que o Direct3D espelhe a textura a cada limite inteiro.</span><span class="sxs-lookup"><span data-stu-id="6e547-104">The mirror texture address mode, identified by the D3DTADDRESS\_MIRROR member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to mirror the texture at every integer boundary.</span></span> <span data-ttu-id="6e547-105">Suponhamos que, por exemplo, seu aplicativo crie uma primitiva quadrada e especifique as coordenadas de textura de (0.0,0.0), (0.0,3.0), (3.0,3.0) e (3.0,0.0).</span><span class="sxs-lookup"><span data-stu-id="6e547-105">Suppose, for example, your application creates a square primitive and specifies texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0).</span></span> <span data-ttu-id="6e547-106">Definir o modo de endereçamento de textura como D3DTADDRESS \_ Mirror faz com que a textura seja aplicada três vezes nas direções u e v.</span><span class="sxs-lookup"><span data-stu-id="6e547-106">Setting the texture addressing mode to D3DTADDRESS\_MIRROR results in the texture being applied three times in both the u- and v-directions.</span></span> <span data-ttu-id="6e547-107">As linhas e colunas alternadas em que ele é aplicado são uma imagem espelhada da linha ou coluna anterior, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="6e547-107">Every other row and column that it is applied to is a mirror image of the preceding row or column, as shown in the following illustration.</span></span>

![ilustração de imagens espelhadas em uma grade 3x3](images/mirror.png)

<span data-ttu-id="6e547-109">Os efeitos desse modo de endereço de textura são semelhantes, mas distintos do modo de encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="6e547-109">The effects of this texture address mode are similar to, but distinct from, those of the wrap mode.</span></span> <span data-ttu-id="6e547-110">Para obter mais informações, consulte [encapsular o modo de endereço de textura (Direct3D 9)](wrap-texture-address-mode.md).</span><span class="sxs-lookup"><span data-stu-id="6e547-110">For more information, see [Wrap Texture Address Mode (Direct3D 9)](wrap-texture-address-mode.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e547-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6e547-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e547-112">Modos de endereçamento de textura</span><span class="sxs-lookup"><span data-stu-id="6e547-112">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
