---
description: Define um quadro de coordenadas ou &\# 0034; quadro de referência. &\# 0034; O modelo de quadro está aberto e pode conter qualquer objeto. As funções de carregamento de malha D3DX reconhecem instâncias de modelo de malha, FrameTransformMatrix e quadro como objetos filho ao carregar uma instância de frame.
ms.assetid: vs|directx_sdk|~\frame.htm
title: Quadro (gráficos do Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81cc9d02b1bcbc21cc299739d93272afcf110c92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825606"
---
# <a name="frame-direct3d-9-graphics"></a>Quadro (gráficos do Direct3D 9)

Define um quadro de coordenadas ou "quadro de referência". O modelo de quadro está aberto e pode conter qualquer objeto. As funções de carregamento de malha D3DX reconhecem instâncias de modelo de [**malha**](mesh.md), [**FrameTransformMatrix**](frametransformmatrix.md)e **quadro** como objetos filho ao carregar uma instância de **frame** .

``` syntax
template Frame
{
    < 3D82AB46-62DA-11CF-AB39-0020AF71E433 >
    [...]           
} 
```

O modelo de quadro reconhece o **quadro** filho e os nós de [**malha**](mesh.md) dentro de um quadro e pode reconhecer modelos definidos pelo usuário por meio de uma função de retorno de chamada.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Modelos](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



