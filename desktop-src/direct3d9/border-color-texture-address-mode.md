---
description: O modo de endereço de textura de cor da borda, identificado pelo \_ membro de borda D3DTADDRESS do tipo enumerado D3DTEXTUREADDRESS, faz com que o Direct3D use uma cor arbitrária, conhecida como a cor da borda, para qualquer coordenada de textura fora do intervalo de 0,0 até 1,0, inclusive.
ms.assetid: 689dbda1-0692-411d-9727-2fdf1df960ec
title: Modo de endereço de textura de cor da borda (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b42b18d88f3b9305d0602e43a9528357a9397d6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370474"
---
# <a name="border-color-texture-address-mode-direct3d-9"></a><span data-ttu-id="9300a-103">Modo de endereço de textura de cor da borda (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9300a-103">Border Color Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="9300a-104">O modo de endereço de textura de cor da borda, identificado pelo \_ membro de borda D3DTADDRESS do tipo enumerado [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , faz com que o Direct3D use uma cor arbitrária, conhecida como a cor da borda, para qualquer coordenada de textura fora do intervalo de 0,0 até 1,0, inclusive.</span><span class="sxs-lookup"><span data-stu-id="9300a-104">The border color texture address mode, identified by the D3DTADDRESS\_BORDER member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to use an arbitrary color, known as the border color, for any texture coordinates outside the range of 0.0 through 1.0, inclusive.</span></span>

<span data-ttu-id="9300a-105">Na ilustração a seguir, o aplicativo especifica que a textura deve ser aplicada à primitiva usando uma borda vermelha.</span><span class="sxs-lookup"><span data-stu-id="9300a-105">In the following illustration, the application specifies that the texture be applied to the primitive using a red border.</span></span>

![ilustração de uma textura e uma textura com uma borda vermelha](images/border.png)

<span data-ttu-id="9300a-107">Os aplicativos definem a cor da borda chamando [**IDirect3DDevice9:: Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="9300a-107">Applications set the border color by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).</span></span> <span data-ttu-id="9300a-108">Defina o primeiro parâmetro para a chamada para o identificador de estágio de textura desejado, o segundo parâmetro para o \_ valor de estado de estágio de BORDERCOLOR D3DSAMP e o terceiro parâmetro para a nova cor de borda RGBA.</span><span class="sxs-lookup"><span data-stu-id="9300a-108">Set the first parameter for the call to the desired texture stage identifier, the second parameter to the D3DSAMP\_BORDERCOLOR stage state value, and the third parameter to the new RGBA border color.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9300a-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9300a-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9300a-110">Modos de endereçamento de textura</span><span class="sxs-lookup"><span data-stu-id="9300a-110">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
