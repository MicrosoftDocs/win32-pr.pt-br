---
title: ps_2_0 instruções
description: Esta seção contém informações de referência para as instruções do sombreador de pixel versão \_ 2 0.
ms.assetid: 70492436-4d0d-48e6-b3d2-8934931fb5c2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 292263ed6331c8cc878d6dbd9cfa3e4d766c193d2242b841afb926b296675ccf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067986"
---
# <a name="ps_2_0-instructions"></a>ps \_ 2 \_ 0 Instructions

Esta seção contém informações de referência para as instruções do sombreador de pixel versão \_ 2 0.

Há vários tipos de instruções de sombreador de pixel, conforme mostrado na tabela. As colunas à direita significam o seguinte:

-   Slots de instrução – número de slots de instrução usados por cada instrução.
-   Instalação – um sombreador de pixel deve ter uma instrução de versão e deve ser a primeira instrução.
-   Aritmética – essas instruções fornecem as operações matemáticas em um sombreador.
-   Textura – essas instruções são usadas para carregar e amostrar dados de textura e modificar as coordenadas de textura.
-   Novo – essas instruções são novas para esta versão.

## <a name="instruction-set"></a>Conjunto de instruções



| Nome                                                             | Descrição                                                                                      | Slots de instrução | Instalação | Aritmético | Textura | Novo |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|-----|
| [abs - ps](abs---ps.md)                                         | Valor absoluto                                                                                   | 1                 |       | x          |         | x   |
| [add - ps](add---ps.md)                                         | Adicionar dois vetores                                                                                  | 1                 |       | x          |         |     |
| [cmp - ps](cmp---ps.md)                                         | Comparar a origem com 0                                                                              | 1                 |       | x          |         |     |
| [crs - ps](crs---ps.md)                                         | Produto cruzado                                                                                    | 2                 |       | x          |         | x   |
| [dcl \_ samplerType (sm2, sm3 – ps asm)](dcl-samplertype---ps.md) | Declarar a dimensão de textura para um exemplo                                                      | 0                 | x     |            |         | x   |
| [dcl - (sm2, sm3 - ps asm)](dcl---ps.md)                        | Declare a associação entre registros de saída do sombreador de vértice e registros de entrada do sombreador de pixel. | 0                 | x     |            |         | x   |
| [def - ps](def---ps.md)                                         | Definir constantes                                                                                 | 0                 | x     |            |         |     |
| [dp2add – ps](dp2add---ps.md)                                   | Produto de ponto 2D e adicionar                                                                           | 2                 |       | x          |         | x   |
| [dp3 – ps](dp3---ps.md)                                         | Produto de ponto 3D                                                                                   | 1                 |       | x          |         |     |
| [dp4 – ps](dp4---ps.md)                                         | Produto de ponto 4D                                                                                   | 1                 |       | x          |         |     |
| [exp - ps](exp---ps.md)                                         | Precisão completa 2<sup>x</sup>                                                                     | 1                 |       | x          |         | x   |
| [frc – ps](frc---ps.md)                                         | Componente fracionado                                                                             | 1                 |       | x          |         | x   |
| [log - ps](log---ps.md)                                         | Log de precisão completa(x)                                                                           | 1                 |       | x          |         | x   |
| [lrp – ps](lrp---ps.md)                                         | Interpolação linear                                                                               | 2                 |       | x          |         |     |
| [m3x2 – ps](m3x2---ps.md)                                       | Multiplicação de 3x2                                                                                     | 2                 |       | x          |         | x   |
| [m3x3 – ps](m3x3---ps.md)                                       | Multiplicação de 3x3                                                                                     | 3                 |       | x          |         | x   |
| [m3x4 – ps](m3x4---ps.md)                                       | Multiplicação de 3x4                                                                                     | 4                 |       | x          |         | x   |
| [m4x3 – ps](m4x3---ps.md)                                       | Multiplicação de 4x3                                                                                     | 3                 |       | x          |         | x   |
| [m4x4-PS](m4x4---ps.md)                                       | 4x4 multiplicar                                                                                     | 4                 |       | x          |         | x   |
| [Mad-PS](mad---ps.md)                                         | Multiplicar e adicionar                                                                                 | 1                 |       | x          |         |     |
| [máximo de PS](max---ps.md)                                         | Máximo                                                                                          | 1                 |       | x          |         | x   |
| [min-PS](min---ps.md)                                         | Mínimo                                                                                          | 1                 |       | x          |         | x   |
| [MOV-PS](mov---ps.md)                                         | Mover                                                                                             | 1                 |       | x          |         |     |
| [Mul-PS](mul---ps.md)                                         | Multiplicar                                                                                         | 1                 |       | x          |         |     |
| [Nop-PS](nop---ps.md)                                         | Nenhuma operação                                                                                     | 1                 |       | x          |         |     |
| [NRM-PS](nrm---ps.md)                                         | Normalizar                                                                                        | 3                 |       | x          |         | x   |
| [pow-PS](pow---ps.md)                                         | x<sup>y</sup>                                                                                    | 3                 |       | x          |         | x   |
| [ps](ps---ps.md)                                                | Versão                                                                                          | 0                 | x     |            |         |     |
| [RCP-PS](rcp---ps.md)                                         | Recíproco                                                                                       | 1                 |       | x          |         | x   |
| [RSQ-PS](rsq---ps.md)                                         | Raiz quadrada recíproca                                                                           | 1                 |       | x          |         | x   |
| [Sincos-PS](sincos---ps.md)                                   | Seno e cosseno                                                                                  | 8                 |       | x          |         | x   |
| [sub-PS](sub---ps.md)                                         | Subtrair                                                                                         | 1                 |       | x          |         |     |
| [texkill-PS](texkill---ps.md)                                 | Renderizar Kill pixel                                                                                | 1                 |       |            | x       |     |
| [texld-PS \_ 2 \_ 0 e superior](texld---ps-2-0.md)                    | Amostra de uma textura                                                                                 | 1                 |       |            | x       | x   |
| [texldb-PS](texldb---ps.md)                                   | Amostragem de textura com tendência de nível de detalhe do componente w-                                      | 1                 |       |            | x       | x   |
| [texldp-PS](texldp---ps.md)                                   | Amostragem de textura com divisão projetada pelo componente w-                                           | 1                 |       |            | x       | x   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




