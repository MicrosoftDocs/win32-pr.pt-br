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
# <a name="border-color-texture-address-mode-direct3d-9"></a>Modo de endereço de textura de cor da borda (Direct3D 9)

O modo de endereço de textura de cor da borda, identificado pelo \_ membro de borda D3DTADDRESS do tipo enumerado [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , faz com que o Direct3D use uma cor arbitrária, conhecida como a cor da borda, para qualquer coordenada de textura fora do intervalo de 0,0 até 1,0, inclusive.

Na ilustração a seguir, o aplicativo especifica que a textura deve ser aplicada à primitiva usando uma borda vermelha.

![ilustração de uma textura e uma textura com uma borda vermelha](images/border.png)

Os aplicativos definem a cor da borda chamando [**IDirect3DDevice9:: Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate). Defina o primeiro parâmetro para a chamada para o identificador de estágio de textura desejado, o segundo parâmetro para o \_ valor de estado de estágio de BORDERCOLOR D3DSAMP e o terceiro parâmetro para a nova cor de borda RGBA.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modos de endereçamento de textura](texture-addressing-modes.md)
</dt> </dl>

 

 
