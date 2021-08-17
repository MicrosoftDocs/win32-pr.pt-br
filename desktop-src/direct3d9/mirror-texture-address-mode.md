---
description: O modo de endereço de textura de espelho, identificado pelo \_ membro D3DTADDRESS mirror do tipo enumerado D3DTEXTUREADDRESS, faz com que o Direct3D espelhe a textura a cada limite inteiro.
ms.assetid: 816efd4d-94b3-4b6c-9fc9-218cc2207b97
title: Modo de endereço de textura de espelho (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ef8731c060e95c470bbf8d34222b9ee66e7f9da2c7a6f03a09c2989986ca3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728358"
---
# <a name="mirror-texture-address-mode-direct3d-9"></a>Modo de endereço de textura de espelho (Direct3D 9)

O modo de endereço de textura de espelho, identificado pelo \_ membro D3DTADDRESS mirror do tipo enumerado [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , faz com que o Direct3D espelhe a textura a cada limite inteiro. Suponhamos que, por exemplo, seu aplicativo crie uma primitiva quadrada e especifique as coordenadas de textura de (0.0,0.0), (0.0,3.0), (3.0,3.0) e (3.0,0.0). Definir o modo de endereçamento de textura como D3DTADDRESS \_ Mirror faz com que a textura seja aplicada três vezes nas direções u e v. As linhas e colunas alternadas em que ele é aplicado são uma imagem espelhada da linha ou coluna anterior, conforme mostrado na ilustração a seguir.

![ilustração de imagens espelhadas em uma grade 3x3](images/mirror.png)

Os efeitos desse modo de endereço de textura são semelhantes, mas distintos do modo de encapsulamento. Para obter mais informações, consulte [encapsular o modo de endereço de textura (Direct3D 9)](wrap-texture-address-mode.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modos de endereçamento de textura](texture-addressing-modes.md)
</dt> </dl>

 

 
