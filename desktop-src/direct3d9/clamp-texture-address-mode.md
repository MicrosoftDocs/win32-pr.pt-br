---
description: O modo de endereço de textura fixe, identificado pelo \_ membro D3DTADDRESS fixe do tipo enumerado D3DTEXTUREADDRESS, faz com que o Direct3D refixe suas coordenadas de textura para o \[ intervalo 0,0, 1,0 \] .
ms.assetid: 8efed38d-4c9f-4a8d-9d1b-af1c8df9292a
title: Modo de endereço de textura fixe (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0602b66c28dfbd48cc7ac3504ff643cd0ffe31769ee8edbeede5b4b870914289
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751347"
---
# <a name="clamp-texture-address-mode-direct3d-9"></a>Modo de endereço de textura fixe (Direct3D 9)

O modo de endereço de textura fixe, identificado pelo \_ membro D3DTADDRESS fixe do tipo enumerado [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , faz com que o Direct3D refixe suas coordenadas de textura para o \[ intervalo 0,0, 1,0 \] . Ou seja, ele aplica a textura uma vez e, em seguida, mancha a cor dos pixels da borda. Por exemplo, suponha que seu aplicativo crie um primitivo quadrado e atribua coordenadas de textura (0,0, 0,0), (0,0, 3,0), (3.0, 3.0) e (3.0, 0,0) aos vértices do primitivo. Definir o modo de endereçamento de textura como D3DTADDRESS \_ fixe resulta na aplicação da textura. As cores dos pixels na parte superior das colunas e no final das linhas são estendidas até a parte superior e à direita da primitiva respectivamente.

A ilustração a seguir mostra uma textura ancorada.

![ilustração de uma textura e uma textura ancorada](images/clamp.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modos de endereçamento de textura](texture-addressing-modes.md)
</dt> </dl>

 

 
