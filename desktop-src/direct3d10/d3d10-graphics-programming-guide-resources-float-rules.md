---
description: O Direct3D 10 dá suporte a várias representações de ponto flutuante diferentes. Todos os cálculos de ponto flutuante funcionam em um subconjunto definido do comportamento de ponto flutuante de precisão única de IEEE 754 32 bits.
ms.assetid: 57221d13-8993-4db3-b1a0-88bdcf6f0167
title: Regras de ponto de FFloating (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6909d037b11f9098bb3e0dbad0f1846b79b513e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784561"
---
# <a name="floating-point-rules-direct3d-10"></a>Regras de ponto flutuante (Direct3D 10)

O Direct3D 10 dá suporte a várias representações de ponto flutuante diferentes. Todos os cálculos de ponto flutuante funcionam em um subconjunto definido do comportamento de ponto flutuante de precisão única de IEEE 754 32 bits.

-   [Regras de Floating-Point de 32 bits](#32-bit-floating-point-rules)
    -   [Regras do IEEE-754 respeitadas](#honored-ieee-754-rules)
    -   [Desvios ou requisitos adicionais das regras IEEE-754](#deviations-or-additional-requirements-from-ieee-754-rules)
-   [Regras de Floating-Point de 16 bits](#16-bit-floating-point-rules)
-   [Regras de Floating-Point de 11 e 10 bits](#11-bit-and-10-bit-floating-point-rules)
-   [Tópicos relacionados](#related-topics)

## <a name="32-bit-floating-point-rules"></a>Regras de Floating-Point de 32 bits

Existem dois conjuntos de regras: aquele em conformidade com IEEE-754, e aquele que desvia do padrão.

### <a name="honored-ieee-754-rules"></a>Regras do IEEE-754 respeitadas

Algumas dessas regras são uma única opção onde a IEEE-754 oferece opções.

-   Divisão por 0 produz + /-INF, exceto 0/0, o que resulta em NaN.
-   o log de (+/-) 0 produz -INF. o log de um valor negativo (diferente de -0) produz NaN.
-   A raiz quadrada recíproca (rsq) ou raiz quadrada (sqrt) de um número negativo produz NaN. A exceção é - 0; sqrt(-0) produz - 0 e rsq(-0) produz -INF.
-   INF - INF = NaN
-   (+/-)INF / (+/-)INF = NaN
-   (+/-) INF \* 0 = Nan
-   Qualquer valor NaN (qualquer OP) = NaN
-   As comparações EQ, GT, GE, LT e LE, quando um ou ambos operandos for NaN retornará **FALSE**.
-   As comparações ignoram o sinal de 0 (sendo assim, +0 igual -0).
-   A comparação NE, quando um ou ambos operandos for NaN retornará **TRUE**.
-   As comparações de qualquer valor não NaN com +/-INF retornam o resultado correto.

### <a name="deviations-or-additional-requirements-from-ieee-754-rules"></a>Desvios ou requisitos adicionais das regras IEEE-754

-   O IEEE-754 exibe que as operações de ponto flutuante produzam um resultado que seja o valor representável mais próximo a um resultado infinitamente preciso, conhecido como valor arredondado para o número par mais próximo. No entanto, o Direct3D 10 define um requisito mais flexível: as operações de ponto flutuante de 32 bits produzem um resultado que está dentro de uma unidade-último local (1 ULP) do resultado infinitamente preciso. Isso significa que, por exemplo, o hardware tem permissão de truncar resultados em 32 bits, em vez de executar o arredondamento para o número par mais próximo, uma vez que isso resultaria em um erro de no máximo 1 ULP.
-   Não há nenhum suporte para exceções de ponto flutuante, bits de status ou interrupções.
-   Denorms são liberadas para zero com sinal preservado na entrada e saída de qualquer operação matemática de ponto flutuante. São feitas exceções para qualquer operação de movimentação de dados e e/s que não manipula os dados.
-   Os Estados que contêm valores de ponto flutuante, como visor MinDepth/MaxDepth, valores de BorderColor, etc., podem ser fornecidos como valores não normativos e podem ou não ser liberados antes de serem usados pelo hardware.
-   As operações de mínimo ou máximo liberam denorms para a comparação, mas o resultado pode ou não ser um denorm liberado.
-   A entrada NaN para uma operação sempre produz NaN na saída, no entanto, o padrão de bit exato do NaN não é necessário para permanecer o mesmo (a menos que a operação seja uma instrução de movimentação bruta, o que não altera dados.)
-   As operações min ou Max para as quais apenas um operando é NaN retornam o outro operando como resultado (ao contrário das regras de comparação acima). Essa é uma nova regra IEEE (IEEE 754R), necessária no Direct3D 10.
-   Outra nova regra IEEE 754R é que min (-0, + 0) = = min (+ 0,-0) = =-0 e Max (-0, + 0) = = Max (+ 0,-0) = = + 0, que respeitam o sinal, em contraste com as regras de comparação para zero assinado (declarado acima). O Direct3D 10 recomenda o comportamento do IEEE 754R aqui, mas não será imposto; é permitido que o resultado da comparação de zeros seja dependente da ordem dos parâmetros, usando uma comparação que ignora os sinais.
-   x \* 1.0 f sempre resulta em x (exceto descarregamento desnormal).
-   x/1.0f sempre resulta em x (exceto denorm liberados).
-   x +/- 0.0f sempre resulta em x (exceto denorm liberados). Mas -0 + 0 = +0.
-   As operações fundidas (como mad, dp3) produzem resultados que não são menos precisos do que a pior ordem serial possível da avaliação da expansão não fundida da operação. Observe que a definição da pior ordenação possível, para fins de tolerância, não é uma definição fixa para uma determinada operação com fusível; depende dos valores específicos das entradas. As etapas individuais na expansão não-fundida são cada uma delas permitida 1 tolerância de ULP (ou para quaisquer instruções que o Direct3D 10 chama com uma tolerância mais inlax do que 1 ULP, a tolerância mais incerto é permitida).
-   As operações fundidas cumprem as mesmas regras NaN que as operações não fundidas.
-   Multiplicar e dividir cada operação no nível de precisão de ponto flutuante de 32 bits (precisão para 1 ULP).

## <a name="16-bit-floating-point-rules"></a>Regras de Floating-Point de 16 bits

O Direct3D 10 também dá suporte a representações de 16 bits de números de ponto flutuante.

Formato:

-   Sinal de 1 bit (s) na posição MSB bit
-   5 bits de expoente ajustado (e)
-   10 bits de fração (f), com um bit oculto adicional

Um valor de float16 (v) segue as seguintes regras:

-   Se e == 31 e f != 0, então v é NaN independente de s
-   se e = = 31 e f = = 0, então v = (-1) s \* Infinity (infinito assinado)
-   se e estiver entre 0 e 31, v = (-1) s \* 2 (e-15) \* (1. f)
-   se e = = 0 e f! = 0, v = (-1) s \* 2 (e-14) \* (0. f) (números desnormalizados)
-   se e = = 0 e f = = 0, então v = (-1) s \* 0 (assinado zero)

as regras de ponto flutuante de 32 bits também contêm números de ponto flutuante de 16 bits, ajustadas para o layout de bit descrito acima. Algumas exceções:

-   Precisão: as operações não fundidas em números de ponto flutuante de 16 bits produzem um resultado que é o valor representável mais próximo de um resultado infinitamente preciso (arredondado para o número par mais próximo, de acordo com IEEE-754, aplicado aos valores de 16 bits). As regras de ponto flutuante de 32 bits aderem à tolerância de 1 ULP, as regras de ponto flutuante de 16 bits aderem a 0,5 ULP para as operações não fundidas e 0,6 ULP para operações fundidas.
-   Os números de ponto flutuante de 16 bits preservam denorms.

## <a name="11-bit-and-10-bit-floating-point-rules"></a>Regras de Floating-Point de 11 e 10 bits

O Direct3D 10 também dá suporte a formatos de ponto flutuante de 11 e 10 bits.

Formato:

-   Nenhum bit de sinal
-   5 bits de expoente ajustado (e)
-   6 bits de fração (f) para um formato de 11 bits, 5 bits de fração (f) para um formato de 10 bits, com um bit oculto adicional em ambos os casos.

Um valor de float11/float10 (v) segue as regras a seguir:

-   se e == 31 and f != 0, então v é NaN
-   se e == 31 e f == 0, então v = +infinito
-   se e estiver entre 0 e 31, v = 2 (e-15) \* (1. f)
-   se e = = 0 e f! = 0, v = \* 2 (e-14) \* (0. f) (números desnormalizados)
-   se e == 0 e f == 0, então v = 0 (zero)

as regras de ponto flutuante de 32 bits também contêm números de ponto flutuante de 11 e 10 bits, ajustados para o layout de bit descrito acima. As exceções incluem:

-   Precisão: as regras de ponto flutuante de 32 bits aderem a 0,5 ULP.
-   Os números de ponto flutuante de 10/11 bits preservam denorms.
-   Qualquer operação que resultaria em um número menor que zero é clamped para zero.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



