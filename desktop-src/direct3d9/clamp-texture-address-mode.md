---
description: O modo de endereço de textura fixe, identificado pelo \_ membro D3DTADDRESS fixe do tipo enumerado D3DTEXTUREADDRESS, faz com que o Direct3D refixe suas coordenadas de textura para o \[ intervalo 0,0, 1,0 \] .
ms.assetid: 8efed38d-4c9f-4a8d-9d1b-af1c8df9292a
title: Modo de endereço de textura fixe (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153ed1f044bacaec6b87420eb7df22a2557349a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764216"
---
# <a name="clamp-texture-address-mode-direct3d-9"></a><span data-ttu-id="f7d50-103">Modo de endereço de textura fixe (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f7d50-103">Clamp Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="f7d50-104">O modo de endereço de textura fixe, identificado pelo \_ membro D3DTADDRESS fixe do tipo enumerado [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , faz com que o Direct3D refixe suas coordenadas de textura para o \[ intervalo 0,0, 1,0 \] .</span><span class="sxs-lookup"><span data-stu-id="f7d50-104">The clamp texture address mode, identified by the D3DTADDRESS\_CLAMP member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to clamp your texture coordinates to the \[0.0, 1.0\] range.</span></span> <span data-ttu-id="f7d50-105">Ou seja, ele aplica a textura uma vez e, em seguida, mancha a cor dos pixels da borda.</span><span class="sxs-lookup"><span data-stu-id="f7d50-105">That is, it applies the texture once, then smears the color of edge pixels.</span></span> <span data-ttu-id="f7d50-106">Por exemplo, suponha que seu aplicativo crie um primitivo quadrado e atribua coordenadas de textura (0,0, 0,0), (0,0, 3,0), (3.0, 3.0) e (3.0, 0,0) aos vértices do primitivo.</span><span class="sxs-lookup"><span data-stu-id="f7d50-106">For example, suppose that your application creates a square primitive and assigns texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0) to the primitive's vertices.</span></span> <span data-ttu-id="f7d50-107">Definir o modo de endereçamento de textura como D3DTADDRESS \_ fixe resulta na aplicação da textura.</span><span class="sxs-lookup"><span data-stu-id="f7d50-107">Setting the texture addressing mode to D3DTADDRESS\_CLAMP results in the texture being applied once.</span></span> <span data-ttu-id="f7d50-108">As cores dos pixels na parte superior das colunas e no final das linhas são estendidas até a parte superior e à direita da primitiva respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f7d50-108">The pixel colors at the top of the columns and the end of the rows are extended to the top and right of the primitive respectively.</span></span>

<span data-ttu-id="f7d50-109">A ilustração a seguir mostra uma textura ancorada.</span><span class="sxs-lookup"><span data-stu-id="f7d50-109">The following illustration shows a clamped texture.</span></span>

![ilustração de uma textura e uma textura ancorada](images/clamp.png)

## <a name="related-topics"></a><span data-ttu-id="f7d50-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7d50-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7d50-112">Modos de endereçamento de textura</span><span class="sxs-lookup"><span data-stu-id="f7d50-112">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
