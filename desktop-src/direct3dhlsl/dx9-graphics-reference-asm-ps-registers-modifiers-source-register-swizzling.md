---
title: Swizzling de registro de origem (referência do HLSL PS)
description: Swizzling refere-se à capacidade de copiar qualquer componente de registro de origem para qualquer componente de registro temporário. Swizzling não afeta os dados de registro de origem. Antes de uma instrução ser executada, os dados em um registro de origem são copiados para um registro temporário.
ms.assetid: 27aee6a8-5185-4236-b3e4-44addf230c34
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ffc655129740f112a3ade9eb40c0bbe29dfc1fb
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104293610"
---
# <a name="source-register-swizzling-hlsl-ps-reference"></a>Swizzling de registro de origem (referência do HLSL PS)

Swizzling refere-se à capacidade de copiar qualquer componente de registro de origem para qualquer componente de registro temporário. Swizzling não afeta os dados de registro de origem. Antes de uma instrução ser executada, os dados em um registro de origem são copiados para um registro temporário.

## <a name="source-swizzling"></a>Swizzling de origem

O swizzle de origem permite que o componente individual de um registro de origem assuma o valor de qualquer um dos quatro componentes do mesmo registro de origem antes que o registro seja lido para computação.

Por exemplo, o swizzle. zxxy significa:

-   o componente. x assumirá o valor do componente. z
-   o componente. y assumirá o valor do componente. x
-   o componente. z assumirá o valor do componente. x
-   o componente. w assumirá o valor do componente. y

Os componentes podem aparecer em qualquer ordem. Se menos de quatro componentes forem especificados, o último componente será repetido. Por exemplo:


```
.xy  = .xyyy
.wzx = .wzxx
.z   = .zzzz
```



Se nenhum componente for especificado, nenhum swizzling será aplicado.

Algumas instruções têm restrições para swizzle de origem. Elas são listadas nas páginas de referência de instrução respeitadas.



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| . x                    |      |      |      | x    | x    | x    | x     | x    | x     |
| . y                    |      |      |      | x    | x    | x    | x     | x    | x     |
| . z                    | w.x.y.\*  | w.x.y.\*  | x\*  | x    | x    | x    | x     | x    | x     |
| . w                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| . xyzw (padrão)       | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| .yzxw                 |      |      |      |      | x    | x    | x     | x    | x     |
| .zxyw                 |      |      |      |      | x    | x    | x     | x    | x     |
| .wzyx                 |      |      |      |      | x    | x    | x     | x    | x     |
| swizzle arbitrário     |      |      |      |      |      | x    | x     | x    | x     |



 

\* Disponível somente se a máscara de gravação de destino for. w (. a).

## <a name="arbitrary-swizzle"></a>Swizzle arbitrário

Swizzles pode ser aplicado a registros de origem em uma ordem arbitrária; ou seja, qualquer registro de origem pode usar qualquer máscara de componente, em qualquer ordem.

## <a name="replicate-swizzle"></a>Replicar swizzle

Replicate swizzle copia um componente para outro. Isso é, exatamente um dos componentes. x,. y,. z,. w swizzle (ou o. r,. g,. b,. equivalentes) deve ser especificado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modificadores de registro de origem do sombreador de pixel](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> <dt>

[PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 PS 1 \_ \_ \_ \_ 3 \_ \_ PS \_ 1 \_ 4 registros](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[\_registros PS 2 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[\_registros PS 2 \_ x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[\_registros PS 3 \_ 0](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




