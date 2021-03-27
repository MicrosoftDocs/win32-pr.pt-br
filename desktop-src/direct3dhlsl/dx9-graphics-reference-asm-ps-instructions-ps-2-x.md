---
title: Instruções de ps_2_x
description: Esta seção contém informações de referência para as instruções da versão 2 x do sombreador de pixels \_ .
ms.assetid: a9b5f9dd-1139-4f80-ada6-e2fc0fb7effe
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 047067d26f9b85ef981a007059d9f2e87ae28ce3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967202"
---
# <a name="ps_2_x-instructions"></a>Instruções do PS \_ 2 \_ x

Esta seção contém informações de referência para as instruções da versão 2 x do sombreador de pixels \_ .

Há vários tipos de instruções de sombreador de pixel, como mostrado na tabela. As colunas à direita significam o seguinte:

-   Slots de instrução-número de Slots de instrução usados por cada instrução.
-   Instalação – um sombreador de pixel deve ter uma instrução de versão e deve ser a primeira instrução.
-   Aritmética – essas instruções fornecem as operações matemáticas em um sombreador.
-   Textura-essas instruções são usadas para carregar e obter amostras de dados de textura e modificar coordenadas de textura.
-   Controle de fluxo-essas instruções fornecem controle de fluxo estático e dinâmico para a execução de instruções.
-   Novas-essas instruções são novas nesta versão.

## <a name="instruction-set"></a>Conjunto de instruções



| Name                                                             | Descrição                                                                                      | Slots de instrução | Instalação | Aritmético | Textura | Controle de fluxo | Novo |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|--------------|-----|
| [ABS-PS](abs---ps.md)                                         | Valor absoluto                                                                                   | 1                 |       | x          |         |              |     |
| [Adicionar-PS](add---ps.md)                                         | Adicionar dois vetores                                                                                  | 1                 |       | x          |         |              |     |
| [-PS de interrupção](break---ps.md)                                     | Interromper um representante... bloco endrep                                                                | 1                 |       |            |         | x            | x   |
| [interromper \_ comp-PS](break-comp---ps.md)                          | Interromper condicionalmente um representante... bloco endrep, com uma comparação                               | 3                 |       |            |         | x            | x   |
| [breakp-PS](break-p---ps.md)                                  | Interromper um representante... bloco endrep, com base em um predicado                                          | 3                 |       |            |         | x            | x   |
| [Call-PS](call---ps.md)                                       | Chamar uma sub-rotina                                                                                | 2                 |       |            |         | x            | x   |
| [callnz bool-PS](callnz-bool---ps.md)                         | Chamar uma sub-rotina se um registro booliano não for zero                                              | 3                 |       |            |         | x            | x   |
| [callnz Pred-PS](callnz-pred---ps.md)                         | Chamar uma sub-rotina se um registro de predicado não for zero                                            | 3                 |       |            |         | x            | x   |
| [CMP-PS](cmp---ps.md)                                         | Comparar origem com 0                                                                              | 1                 |       | x          |         |              |     |
| [CRS-PS](crs---ps.md)                                         | Produto cruzado                                                                                    | 2                 |       | x          |         |              |     |
| [\_SampleType de DCL (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) | Declarar a dimensão de textura para uma amostra                                                      | 0                 | x     |            |         |              |     |
| [DCL-(SM2, SM3-PS ASM)](dcl---ps.md)                        | Declare a associação entre registradores de saída do sombreador de vértice e registros de entrada do sombreador de pixel. | 0                 | x     |            |         |              |     |
| [def-PS](def---ps.md)                                         | Definir constantes                                                                                 | 0                 | x     |            |         |              |     |
| [DEFB-PS](defb---ps.md)                                       | Definir uma constante booliana                                                                        | 0                 | x     |            |         |              | x   |
| [defi-PS](defi---ps.md)                                       | Definir uma constante de inteiro                                                                       | 0                 | x     |            |         |              | x   |
| [dp2add-PS](dp2add---ps.md)                                   | produto 2D dot e adicionar                                                                           | 2                 |       | x          |         |              |     |
| [DP3-PS](dp3---ps.md)                                         | produto 3D dot                                                                                   | 1                 |       | x          |         |              |     |
| [DP4-PS](dp4---ps.md)                                         | produto do ponto de 4D                                                                                   | 1                 |       | x          |         |              |     |
| [DSX-PS](dsx---ps.md)                                         | Taxa de alteração na direção de x                                                                | 2                 |       | x          |         |              | x   |
| [DSY-PS](dsy---ps.md)                                         | Taxa de alteração na direção y                                                                | 2                 |       | x          |         |              | x   |
| [else-PS](else---ps.md)                                       | Iniciar um bloco else                                                                              | 1                 |       |            |         | x            | x   |
| [endif-PS](endif---ps.md)                                     | Terminar um if... bloco else                                                                           | 1                 |       |            |         | x            | x   |
| [endrep-PS](endrep---ps.md)                                   | Fim de um bloco de repetição                                                                            | 2                 |       |            |         | x            | x   |
| [exp-PS](exp---ps.md)                                         | Precisão total 2<sup>x</sup>                                                                     | 1                 |       | x          |         |              |     |
| [FRC-PS](frc---ps.md)                                         | Componente fracionário                                                                             | 1                 |       | x          |         |              |     |
| [se bool-PS](if-bool---ps.md)                                 | Iniciar um bloco If                                                                                | 3                 |       |            |         | x            | x   |
| [Se \_ comp-PS](if-comp---ps.md)                                | Iniciar um bloco If com uma comparação                                                              | 3                 |       |            |         | x            | x   |
| [se Pred-PS](if-pred---ps.md)                                 | Iniciar um bloco If com predicação                                                               | 3                 |       |            |         | x            | x   |
| [rótulo-PS](label---ps.md)                                     | Label                                                                                            | 0                 |       |            |         | x            | x   |
| [log-PS](log---ps.md)                                         | ₂ de log de precisão total (x)                                                                           | 1                 |       | x          |         |              |     |
| [LRP-PS](lrp---ps.md)                                         | Interpolação linear                                                                               | 2                 |       | x          |         |              |     |
| [M3X2-PS](m3x2---ps.md)                                       | 3x2 multiplicar                                                                                     | 2                 |       | x          |         |              |     |
| [m3x3-PS](m3x3---ps.md)                                       | multiplicar a 3x3                                                                                     | 3                 |       | x          |         |              |     |
| [M3x4-PS](m3x4---ps.md)                                       | 3x4 multiplicar                                                                                     | 4                 |       | x          |         |              |     |
| [m4x3-PS](m4x3---ps.md)                                       | 4x3 multiplicar                                                                                     | 3                 |       | x          |         |              |     |
| [m4x4-PS](m4x4---ps.md)                                       | 4x4 multiplicar                                                                                     | 4                 |       | x          |         |              |     |
| [Mad-PS](mad---ps.md)                                         | Multiplicar e adicionar                                                                                 | 1                 |       | x          |         |              |     |
| [máximo de PS](max---ps.md)                                         | Máximo                                                                                          | 1                 |       | x          |         |              |     |
| [min-PS](min---ps.md)                                         | Mínimo                                                                                          | 1                 |       | x          |         |              |     |
| [MOV-PS](mov---ps.md)                                         | Mover                                                                                             | 1                 |       | x          |         |              |     |
| [Mul-PS](mul---ps.md)                                         | Multiplicar                                                                                         | 1                 |       | x          |         |              |     |
| [Nop-PS](nop---ps.md)                                         | Nenhuma operação                                                                                     | 1                 |       | x          |         |              |     |
| [NRM-PS](nrm---ps.md)                                         | Normaliza                                                                                        | 3                 |       | x          |         |              |     |
| [pow-PS](pow---ps.md)                                         | x<sup>y</sup>                                                                                    | 3                 |       | x          |         |              |     |
| [profissionais](ps---ps.md)                                                | Versão                                                                                          | 0                 | x     |            |         |              |     |
| [RCP-PS](rcp---ps.md)                                         | Recíproco                                                                                       | 1                 |       | x          |         |              |     |
| [Rep-PS](rep---ps.md)                                         | Repetir                                                                                           | 3                 |       |            |         | x            | x   |
| [RET-PS](ret---ps.md)                                         | Fim de uma sub-rotina                                                                              | 1                 |       |            |         | x            | x   |
| [RSQ-PS](rsq---ps.md)                                         | Raiz quadrada recíproca                                                                           | 1                 |       | x          |         |              |     |
| [comp de setp \_](setp-comp---ps.md)                                 | Definir o registro de predicado                                                                       | 1                 |       |            |         | x            | x   |
| [Sincos-PS](sincos---ps.md)                                   | Seno e cosseno                                                                                  | 8                 |       | x          |         |              |     |
| [sub-PS](sub---ps.md)                                         | Subtrair                                                                                         | 1                 |       | x          |         |              |     |
| [texkill-PS](texkill---ps.md)                                 | Renderizar Kill pixel                                                                                | Veja a observação 1        |       |            | x       |              |     |
| [texld-PS \_ 2 \_ 0 e superior](texld---ps-2-0.md)                    | Amostra de uma textura                                                                                 | Confira a observação 2        |       |            | x       |              |     |
| [texldb-PS](texldb---ps.md)                                   | Amostragem de textura com tendência de nível de detalhe do componente w-                                      | Veja a observação 3        |       |            | x       |              |     |
| [texldd-PS](texldd---ps.md)                                   | Amostragem de textura com gradientes fornecidos pelo usuário                                                    | 3                 |       |            | x       |              | x   |
| [texldp-PS](texldp---ps.md)                                   | Amostragem de textura com divisão projetada pelo componente w-                                           | Veja a observação 4        |       |            | x       |              |     |



 

Observações:

1.  Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) for definido, slots = 2; caso contrário, Slots = 1.
2.  Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) for definido e a textura for um mapa de cubo, slots = 4; caso contrário, slot = 1.
3.  Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) for definido, slots = 6; caso contrário, Slots = 1.
4.  Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) não for definido, Slots = 1; caso contrário:
    -   Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) for definido e a textura for um mapa de cubo, slots = 4.
    -   Se [**D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) for definido e a textura não for um mapa de cubo, Slots = 3.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 