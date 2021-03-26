---
title: Máscara de gravação do registro de destino
description: Uma máscara de gravação controla quais componentes de um registro de destino são gravados depois que uma instrução é concluída.
ms.assetid: 376a28c8-8a88-4807-a8ab-f59448d965e8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f649770b84174dbb716967e9d941034c3966f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916641"
---
# <a name="destination-register-write-mask"></a>Máscara de gravação do registro de destino

Uma máscara de gravação controla quais componentes de um registro de destino são gravados depois que uma instrução é concluída. Uma máscara de gravação de saída é permitida, desde que os componentes estejam na ordem de. RGBA ou. xyzw. Ou seja,. RBA e. XW são máscaras válidas. Os registros de textura têm um conjunto de regras e os registros que não são de textura têm outro conjunto de regras.

## <a name="syntax"></a>Syntax



| DST. writemask |
|---------------|



 

onde

-   o DST é um registro de destino.
-   writemask é uma sequência de máscaras de um dos conjuntos: (x, y, z, w) ou (vermelho, verde, azul, alfa).

## <a name="remarks"></a>Comentários

As seguintes máscaras de gravação de destino estão disponíveis.



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| . xyzw (padrão)       | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| . xyz                  | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| . w                    | x    | x    | x    | x    | x    | x    | x     | x    | x     |
| máscara arbitrária        |      |      |      | x    | x    | x    | x     | x    | x     |



 

A máscara arbitrária permite que qualquer conjunto de canais seja combinado para produzir uma máscara. Os canais devem estar listados na ordem r, g, b, a-por exemplo, Register. RBA, que atualiza os canais vermelho, azul e alfa do destino. A máscara arbitrária está disponível na versão 1 \_ 4 ou superior.

Se nenhuma máscara de gravação de destino for especificada, a máscara de gravação de destino padronizará para o caso RGBA. Em outras palavras, todos os canais no registro de destino são atualizados.

Para as versões de 1 \_ a 1 \_ 3, a instrução aritmética de DP3 [DP3-PS](dp3---ps.md) pode usar apenas as máscaras de gravação de saída. RGB ou. RGBA.

As máscaras de gravação de registro de destino têm suporte apenas para operações aritméticas. Eles não podem ser usados em instruções de endereçamento de textura, com exceção das instruções da versão 1 \_ 4, [texcrd-PS](texcrd---ps.md) e [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md).

O padrão é gravar todos os quatro canais de cor.


```
// All four color channels can be written by explicitly listing them.
mul r0.rgba, t0, v0

// Or, the default mask can be used to write all four channels.
mul r0, t0, v0
```



A máscara de gravação alfa também é conhecida como a máscara de gravação escalar, porque ela usa o pipeline escalar.


```
add r0.a, t1, v1
```



Portanto, essa instrução coloca efetivamente a soma do componente alfa do T1 e o componente alfa de v1 em r0. a.

A máscara de gravação de cor é usada para controlar a gravação nos canais de cores.


```
// The color write mask is also referred to as the vector write mask, 
//   because it uses the vector pipeline.
mul r0.rgb, t0, v0
```



Para a versão 1 \_ 4, as máscaras de gravação de destino podem ser usadas em qualquer combinação, desde que as máscaras sejam ordenadas como r, g, b, a.


```
// This example updates the red, blue, and alpha channels.
mov r0.rba, r1
```



Uma instrução coemitida permite que duas instruções potencialmente diferentes sejam emitidas simultaneamente. Isso é feito executando as instruções no pipeline alfa e no pipeline RGB.


```
  mul r0.rgb, t0, v0
+ add r1.a,   t1, c1
```



A vantagem de emparelhar instruções dessa forma é que ela permite que operações diferentes sejam executadas no pipeline de vetor e escalar em paralelo.

Esses registros de saída do sombreador de vértice são restritos às seguintes máscaras de gravação:



| Tipo de registro | Máscara de gravação necessária                                              |
|---------------|------------------------------------------------------------------|
| oFog          | nenhuma máscara de gravação explícita é permitida neste registro escalar        |
| oPts          | nenhuma máscara de gravação explícita é permitida neste registro escalar        |
| oPos          | . xyzw (que é o padrão)                                      |
| To\#          | máscara combinada:. x \| . XY \| . xyz \| . xyzw (que é o padrão) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modificadores de registro do sombreador de pixel](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




