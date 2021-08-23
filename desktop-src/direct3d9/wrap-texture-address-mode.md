---
description: O modo de endereço de textura de quebra, identificado pelo membro WRAP D3DTADDRESS do tipo enumerado D3DTEXTUREADDRESS, faz com que o Direct3D repita a textura em cada junção \_ de inteiro.
ms.assetid: fe33c484-346d-4888-ba88-b8ab00feefbb
title: Modo de endereço de textura de wrap (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 820273a68754c11f17f4f2762c7e824562b8e52bfc0b2b097c21e82789ce4168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627816"
---
# <a name="wrap-texture-address-mode-direct3d-9"></a>Modo de endereço de textura de wrap (Direct3D 9)

O modo de endereço de textura de quebra, identificado pelo membro WRAP D3DTADDRESS do tipo \_ enumerado [**D3DTEXTUREADDRESS,**](./d3dtextureaddress.md) faz com que o Direct3D repita a textura em cada junção de inteiro. Suponhamos que, por exemplo, seu aplicativo crie uma primitiva quadrada e especifique as coordenadas de textura de (0.0,0.0), (0.0,3.0), (3.0,3.0) e (3.0,0.0). Definir o modo de endereçamento de textura como D3DTADDRESS WRAP resulta na textura sendo aplicada três vezes nas instruções u e v, conforme mostrado na ilustração \_ a seguir.

![ilustração de uma textura de face encapsulada na direção u e na direção v](images/wrap.png)

Os efeitos desse modo de endereço de textura são semelhantes, mas distintos daqueles do modo espelho. Para obter mais informações, consulte [Modo de endereço de textura espelhada (Direct3D 9)](mirror-texture-address-mode.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modos de endereçamento de textura](texture-addressing-modes.md)
</dt> </dl>

 

 
