---
title: Diferença de registro de origem
description: Subtraia 0,5 de todos os componentes.
ms.assetid: 6e1e96b0-e265-4b43-a9cb-8435e1fe891c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5c564dad0d4caf859ae00155dfd9619d90276cf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916643"
---
# <a name="source-register-bias"></a>Diferença de registro de origem

Subtraia 0,5 de todos os componentes.

## <a name="registers"></a>Registros

Registro de origem. Para obter mais informações sobre tipos de registro, consulte [PS \_ 1 1 PS 1 2 PS 1 3 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).

## <a name="remarks"></a>Comentários

O conteúdo do registro não é alterado. O modificador é aplicado somente aos dados lidos do registro. A tendência é aplicada a todos os quatro canais de cores (RGBA) da seguinte maneira:


```
output = (input - 0.5)
```



O efeito é modificar os dados que estavam no intervalo de 0 a 1 para que estejam no intervalo de-0,5 a 0,5. A aplicação de ajustes aos dados fora desse intervalo pode produzir resultados indefinidos.

> [!Note]  
> Esse modificador é mutuamente exclusivo com o [registro de origem inverter](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)e, portanto, não pode ser aplicado ao mesmo registro.

 

Este modificador é para uso com as instruções aritméticas.

## <a name="example"></a>Exemplo

Este exemplo executa a mesma operação que D3DTOP \_ ADDsigned no DirectX 6,0 e 7,0 várias sintaxes de textura.


```
add r0, r0, t0_bias; Shift down by 0.5.
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modificadores de registro de origem do sombreador de pixel](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




