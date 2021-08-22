---
description: O modo de endereço de textura de cor da borda, identificado pelo \_ membro de borda D3DTADDRESS do tipo enumerado D3DTEXTUREADDRESS, faz com que o Direct3D use uma cor arbitrária, conhecida como a cor da borda, para qualquer coordenada de textura fora do intervalo de 0,0 até 1,0, inclusive.
ms.assetid: 689dbda1-0692-411d-9727-2fdf1df960ec
title: Modo de endereço de textura de cor da borda (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e0685359227f80a847174157117e90116cffe8e61a48e172451a83aa8ec5fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496307"
---
# <a name="border-color-texture-address-mode-direct3d-9"></a>Modo de endereço de textura de cor da borda (Direct3D 9)

O modo de endereço de textura de cor da borda, identificado pelo \_ membro de borda D3DTADDRESS do tipo enumerado [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , faz com que o Direct3D use uma cor arbitrária, conhecida como a cor da borda, para qualquer coordenada de textura fora do intervalo de 0,0 até 1,0, inclusive.

Na ilustração a seguir, o aplicativo especifica que a textura deve ser aplicada à primitiva usando uma borda vermelha.

![ilustração de uma textura e uma textura com uma borda vermelha](images/border.png)

Os aplicativos definem a cor da borda chamando [**IDirect3DDevice9:: Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate). Defina o primeiro parâmetro para a chamada para o identificador de estágio de textura desejado, o segundo parâmetro para o \_ valor de estado de estágio de BORDERCOLOR D3DSAMP e o terceiro parâmetro para a nova cor de borda RGBA.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modos de endereçamento de textura](texture-addressing-modes.md)
</dt> </dl>

 

 
