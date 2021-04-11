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
# <a name="wrap-texture-address-mode-direct3d-9"></a>Modo de endereço de textura de encapsulamento (Direct3D 9)

O modo de endereço de textura de encapsulamento, identificado pelo \_ membro D3DTADDRESS Wrap do tipo enumerado [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , faz o Direct3D repetir a textura em cada junção de número inteiro. Suponhamos que, por exemplo, seu aplicativo crie uma primitiva quadrada e especifique as coordenadas de textura de (0.0,0.0), (0.0,3.0), (3.0,3.0) e (3.0,0.0). Definir o modo de endereçamento de textura como D3DTADDRESS \_ encapsula os resultados na textura que está sendo aplicada três vezes nas direções u e v, conforme mostrado na ilustração a seguir.

![ilustração de uma textura de face encapsulada na direção u e na direção v](images/wrap.png)

Os efeitos desse modo de endereço de textura são semelhantes, mas distintos do modo de espelho. Para obter mais informações, consulte [modo de endereço de textura de espelho (Direct3D 9)](mirror-texture-address-mode.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modos de endereçamento de textura](texture-addressing-modes.md)
</dt> </dl>

 

 
