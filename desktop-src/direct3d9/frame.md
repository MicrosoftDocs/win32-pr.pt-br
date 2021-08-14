---
description: Define um quadro de coordenadas ou &\# 0034;frame of reference.&\# 0034; O modelo Frame está aberto e pode conter qualquer objeto. As funções de carregamento de malha D3DX reconhecem instâncias de modelo De malha, FrameTransformMatrix e Frame como objetos filho ao carregar uma instância frame.
ms.assetid: vs|directx_sdk|~\frame.htm
title: Quadro (elementos gráficos do Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff77cc6f4618b3ded3afc9453c12a96b115ec4bfe0f90cb83a92826378212c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523029"
---
# <a name="frame-direct3d-9-graphics"></a>Quadro (elementos gráficos do Direct3D 9)

Define um quadro de coordenadas ou "quadro de referência". O modelo Frame está aberto e pode conter qualquer objeto. As funções de carregamento de malha D3DX reconhecem as instâncias de modelo [**Malha**](mesh.md), [**FrameTransformMatrix**](frametransformmatrix.md)e **Frame** como objetos filho ao carregar uma **instância frame.**

``` syntax
template Frame
{
    < 3D82AB46-62DA-11CF-AB39-0020AF71E433 >
    [...]           
} 
```

O modelo de quadro reconhece nós **filho frame** e [**Mesh**](mesh.md) dentro de um quadro e pode reconhecer modelos definidos pelo usuário por meio de uma função de retorno de chamada.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



