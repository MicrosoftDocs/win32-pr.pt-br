---
title: ps_3_0 instruções
description: Esta seção contém informações de referência para as instruções do sombreador de pixel versão \_ 3 0.
ms.assetid: 36972b9b-a4e7-45b4-83f5-959e75d270de
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e44d13bfc726830a8c3fb770b34d5563fde2684f5c8bdf3fea54dec2312af4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982856"
---
# <a name="ps_3_0-instructions"></a>Instruções ps \_ 3 \_ 0

Esta seção contém informações de referência para as instruções do sombreador de pixel versão \_ 3 0.

Há vários tipos de instruções de sombreador de pixel, conforme mostrado na tabela. As colunas à direita significam o seguinte:

-   Slots de instrução – número de slots de instrução usados por cada instrução.
-   Instalação – um sombreador de pixel deve ter uma instrução de versão e deve ser a primeira instrução.
-   Aritmética – essas instruções fornecem as operações matemáticas em um sombreador.
-   Textura – essas instruções são usadas para carregar e amostrar dados de textura e modificar as coordenadas de textura.
-   Flow controle – essas instruções fornecem controle de fluxo estático e dinâmico para a execução de instruções.
-   Novo – essas instruções são novas para esta versão.

## <a name="instruction-set"></a>Conjunto de instruções



| Nome                                                             | Descrição                                                                          | Slots de instrução | Instalação | Aritmético | Textura | Controle de fluxo | Novo |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------|-------|------------|---------|--------------|-----|
| [abs - ps](abs---ps.md)                                         | Valor absoluto                                                                       | 1                 |       | x          |         |              |     |
| [add - ps](add---ps.md)                                         | Adicionar dois vetores                                                                      | 1                 |       | x          |         |              |     |
| [break - ps](break---ps.md)                                     | Sair de um loop... endloop ou rep... bloco endrep                                  | 1                 |       |            |         | x            |     |
| [break \_ comp - ps](break-comp---ps.md)                          | Sair condicionalmente de um loop... endloop ou rep... bloco endrep, com uma comparação | 3                 |       |            |         | x            |     |
| [breakp – ps](break-p---ps.md)                                  | sair de um loop... endloop ou rep... bloco endrep, com base em um predicado            | 3                 |       |            |         | x            |     |
| [call - ps](call---ps.md)                                       | Chamar uma sub-rotina                                                                    | 2                 |       |            |         | x            |     |
| [callnz bool - ps](callnz-bool---ps.md)                         | Chamar uma sub-rotina se um registro booliana não for zero                                  | 3                 |       |            |         | x            |     |
| [callnz pred – ps](callnz-pred---ps.md)                         | Chamar uma sub-rotina se um registro de predicado não for zero                                | 3                 |       |            |         | x            |     |
| [cmp - ps](cmp---ps.md)                                         | Comparar a origem com 0                                                                  | 1                 |       | x          |         |              |     |
| [crs - ps](crs---ps.md)                                         | Produto cruzado                                                                        | 2                 |       | x          |         |              |     |
| [dcl \_ samplerType (sm2, sm3 – ps asm)](dcl-samplertype---ps.md) | Declarar a dimensão de textura para um exemplo                                          | 0                 | x     |            |         |              |     |
| [\_semântica dcl (sm3 – ps asm)](dcl-usage---ps.md)              | Declarar registros de entrada e saída                                                   | 0                 | x     |            |         |              | x   |
| [def - ps](def---ps.md)                                         | Definir constantes                                                                     | 0                 | x     |            |         |              |     |
| [defb – ps](defb---ps.md)                                       | Definir uma constante booliana                                                            | 0                 | x     |            |         |              |     |
| [defi – ps](defi---ps.md)                                       | Definir uma constante de inteiro                                                           | 0                 | x     |            |         |              |     |
| [dp2add – ps](dp2add---ps.md)                                   | Produto de ponto 2D e adicionar                                                               | 2                 |       | x          |         |              |     |
| [dp3 – ps](dp3---ps.md)                                         | Produto de ponto 3D                                                                       | 1                 |       | x          |         |              |     |
| [dp4 – ps](dp4---ps.md)                                         | Produto de ponto 4D                                                                       | 1                 |       | x          |         |              |     |
| [dsx – ps](dsx---ps.md)                                         | Taxa de alteração na direção x                                                    | 2                 |       | x          |         |              |     |
| [dsy - ps](dsy---ps.md)                                         | Taxa de alteração na direção y                                                    | 2                 |       | x          |         |              |     |
| [else - ps](else---ps.md)                                       | Iniciar um bloco else                                                                  | 1                 |       |            |         | x            |     |
| [endif - ps](endif---ps.md)                                     | Encerrar um se... bloco else                                                               | 1                 |       |            |         | x            |     |
| [endloop – ps](endloop---ps.md)                                 | Encerrar um loop                                                                           | 2                 |       |            |         | x            | x   |
| [endrep – ps](endrep---ps.md)                                   | Fim de um bloco de repetição                                                                | 2                 |       |            |         | x            |     |
| [exp - ps](exp---ps.md)                                         | Precisão completa 2<sup>x</sup>                                                         | 1                 |       | x          |         |              |     |
| [frc – ps](frc---ps.md)                                         | Componente fracionado                                                                 | 1                 |       | x          |         |              |     |
| [se bool - ps](if-bool---ps.md)                                 | Iniciar um bloco if                                                                    | 3                 |       |            |         | x            |     |
| [if \_ comp - ps](if-comp---ps.md)                                | Iniciar um bloco if com uma comparação                                                  | 3                 |       |            |         | x            |     |
| [if pred – ps](if-pred---ps.md)                                 | Iniciar um bloco if com predication                                                   | 3                 |       |            |         | x            |     |
| [label - ps](label---ps.md)                                     | Rótulo                                                                                | 0                 |       |            |         | x            |     |
| [log - ps](log---ps.md)                                         | Log de precisão completa(x)                                                               | 1                 |       | x          |         |              |     |
| [loop - ps](loop---ps.md)                                       | Loop                                                                                 | 3                 |       |            |         | x            | x   |
| [lrp – ps](lrp---ps.md)                                         | Interpolação linear                                                                   | 2                 |       | x          |         |              |     |
| [m3x2 – ps](m3x2---ps.md)                                       | Multiplicação de 3x2                                                                         | 2                 |       | x          |         |              |     |
| [m3x3 – ps](m3x3---ps.md)                                       | Multiplicação de 3x3                                                                         | 3                 |       | x          |         |              |     |
| [m3x4 – ps](m3x4---ps.md)                                       | Multiplicação de 3x4                                                                         | 4                 |       | x          |         |              |     |
| [m4x3 – ps](m4x3---ps.md)                                       | Multiplicação de 4x3                                                                         | 3                 |       | x          |         |              |     |
| [m4x4 – ps](m4x4---ps.md)                                       | Multiplicação de 4x4                                                                         | 4                 |       | x          |         |              |     |
| [mad - ps](mad---ps.md)                                         | Multiplicar e adicionar                                                                     | 1                 |       | x          |         |              |     |
| [max - ps](max---ps.md)                                         | Máximo                                                                              | 1                 |       | x          |         |              |     |
| [min - ps](min---ps.md)                                         | Mínimo                                                                              | 1                 |       | x          |         |              |     |
| [mov - ps](mov---ps.md)                                         | Mover                                                                                 | 1                 |       | x          |         |              |     |
| [mul - ps](mul---ps.md)                                         | Multiplicar                                                                             | 1                 |       | x          |         |              |     |
| [nop – ps](nop---ps.md)                                         | Nenhuma operação                                                                         | 1                 |       | x          |         |              |     |
| [NRM-PS](nrm---ps.md)                                         | Normalizar                                                                            | 3                 |       | x          |         |              |     |
| [pow-PS](pow---ps.md)                                         | x<sup>y</sup>                                                                        | 3                 |       | x          |         |              |     |
| [ps](ps---ps.md)                                                | Versão                                                                              | 0                 | x     |            |         |              |     |
| [RCP-PS](rcp---ps.md)                                         | Recíproco                                                                           | 1                 |       | x          |         |              |     |
| [Rep-PS](rep---ps.md)                                         | Repetir                                                                               | 3                 |       |            |         | x            |     |
| [RET-PS](ret---ps.md)                                         | Fim de uma sub-rotina                                                                  | 1                 |       |            |         | x            |     |
| [RSQ-PS](rsq---ps.md)                                         | Raiz quadrada recíproca                                                               | 1                 |       | x          |         |              |     |
| [comp de setp \_](setp-comp---ps.md)                                 | Definir o registro de predicado                                                           | 1                 |       |            |         | x            |     |
| [Sincos-PS](sincos---ps.md)                                   | Seno e cosseno                                                                      | 8                 |       | x          |         |              |     |
| [sub-PS](sub---ps.md)                                         | Subtrair                                                                             | 1                 |       | x          |         |              |     |
| [texkill-PS](texkill---ps.md)                                 | Renderizar Kill pixel                                                                    | 2                 |       |            | x       |              |     |
| [texld-PS \_ 2 \_ 0 e superior](texld---ps-2-0.md)                    | Amostra de uma textura                                                                     | Veja a observação 1        |       |            | x       |              |     |
| [texldb-PS](texldb---ps.md)                                   | Amostragem de textura com tendência de nível de detalhe do componente w-                          | 6                 |       |            | x       |              |     |
| [texldl-PS](texldl---ps.md)                                   | Amostragem de textura com nível de detalhe do componente w-                               | Confira a observação 2        |       |            | x       |              | x   |
| [texldd-PS](texldd---ps.md)                                   | Amostragem de textura com gradientes fornecidos pelo usuário                                        | 3                 |       |            | x       |              |     |
| [texldp-PS](texldp---ps.md)                                   | Amostragem de textura com divisão projetada pelo componente w-                               | Veja a observação 3        |       |            | x       |              |     |



 

Observações:

1.  Se a textura for um mapa de cubo, slots = 4; caso contrário, Slots = 1.
2.  Se a textura for um mapa de cubo, Slots = 5; caso contrário, slots = 2.
3.  Se a textura for um mapa de cubo, slots = 4; caso contrário, Slots = 3.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




