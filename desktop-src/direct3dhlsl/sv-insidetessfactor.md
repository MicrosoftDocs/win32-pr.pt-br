---
title: SV_InsideTessFactor
description: Define o valor de mosaico dentro de uma superfície de patch.
ms.assetid: f0762aca-d84d-44c0-a163-9737ef92c1e5
keywords:
- SV_InsideTessFactor HLSL
topic_type:
- apiref
api_name:
- SV_InsideTessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a05cabbb9410136d2bd82ee272ad92ff1b1f430
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104967065"
---
# <a name="sv_insidetessfactor"></a>\_INSIDETESSFACTOR VA

Define o valor de mosaico dentro de uma superfície de patch.

## <a name="type"></a>Tipo



|            |                |
|------------|----------------|
| Tipo       | Topologia de entrada |
| float \[ 2\] | patch quádruplo     |
| FLOAT      | Tri patch      |
| unused     | isoline        |



 

Fatores de mosaico devem ser declarados como matriz; Eles não podem ser empacotados em um único vetor.

## <a name="remarks"></a>Comentários

Esse valor deve ser definido durante a função constante patch do sombreador envoltória.

Valor de saída necessário para o sombreador envoltória se estiver usando patches Quad ou tri. Esse valor é uma entrada necessária para o sombreador de domínio para que o hardware corresponda às assinaturas por meio de Tessellator.

Essa função tem suporte nos seguintes tipos de sombreadores:



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Semântica](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




