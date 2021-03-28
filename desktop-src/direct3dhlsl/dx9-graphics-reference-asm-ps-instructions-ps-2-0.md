---
title: Instruções de ps_2_0
description: Esta seção contém informações de referência para as instruções da versão 2 0 do sombreador de pixel \_ .
ms.assetid: 70492436-4d0d-48e6-b3d2-8934931fb5c2
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bac2a70ed0147885174c2290d5e58c92ae3347e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104988533"
---
# <a name="ps_2_0-instructions"></a>\_instruções PS 2 \_ 0

Esta seção contém informações de referência para as instruções da versão 2 0 do sombreador de pixel \_ .

Há vários tipos de instruções de sombreador de pixel, como mostrado na tabela. As colunas à direita significam o seguinte:

-   Slots de instrução-número de Slots de instrução usados por cada instrução.
-   Instalação – um sombreador de pixel deve ter uma instrução de versão e deve ser a primeira instrução.
-   Aritmética – essas instruções fornecem as operações matemáticas em um sombreador.
-   Textura-essas instruções são usadas para carregar e obter amostras de dados de textura e modificar coordenadas de textura.
-   Novas-essas instruções são novas nesta versão.

## <a name="instruction-set"></a>Conjunto de instruções



| Name                                                             | Descrição                                                                                      | Slots de instrução | Instalação | Aritmético | Textura | Novo |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|-------------------|-------|------------|---------|-----|
| [ABS-PS](abs---ps.md)                                         | Valor absoluto                                                                                   | 1                 |       | x          |         | x   |
| [Adicionar-PS](add---ps.md)                                         | Adicionar dois vetores                                                                                  | 1                 |       | x          |         |     |
| [CMP-PS](cmp---ps.md)                                         | Comparar origem com 0                                                                              | 1                 |       | x          |         |     |
| [CRS-PS](crs---ps.md)                                         | Produto cruzado                                                                                    | 2                 |       | x          |         | x   |
| [\_SampleType de DCL (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) | Declarar a dimensão de textura para uma amostra                                                      | 0                 | x     |            |         | x   |
| [DCL-(SM2, SM3-PS ASM)](dcl---ps.md)                        | Declare a associação entre registradores de saída do sombreador de vértice e registros de entrada do sombreador de pixel. | 0                 | x     |            |         | x   |
| [def-PS](def---ps.md)                                         | Definir constantes                                                                                 | 0                 | x     |            |         |     |
| [dp2add-PS](dp2add---ps.md)                                   | produto 2D dot e adicionar                                                                           | 2                 |       | x          |         | x   |
| [DP3-PS](dp3---ps.md)                                         | produto 3D dot                                                                                   | 1                 |       | x          |         |     |
| [DP4-PS](dp4---ps.md)                                         | produto do ponto de 4D                                                                                   | 1                 |       | x          |         |     |
| [exp-PS](exp---ps.md)                                         | Precisão total 2<sup>x</sup>                                                                     | 1                 |       | x          |         | x   |
| [FRC-PS](frc---ps.md)                                         | Componente fracionário                                                                             | 1                 |       | x          |         | x   |
| [log-PS](log---ps.md)                                         | ₂ de log de precisão total (x)                                                                           | 1                 |       | x          |         | x   |
| [LRP-PS](lrp---ps.md)                                         | Interpolação linear                                                                               | 2                 |       | x          |         |     |
| [M3X2-PS](m3x2---ps.md)                                       | 3x2 multiplicar                                                                                     | 2                 |       | x          |         | x   |
| [m3x3-PS](m3x3---ps.md)                                       | multiplicar a 3x3                                                                                     | 3                 |       | x          |         | x   |
| [M3x4-PS](m3x4---ps.md)                                       | 3x4 multiplicar                                                                                     | 4                 |       | x          |         | x   |
| [m4x3-PS](m4x3---ps.md)                                       | 4x3 multiplicar                                                                                     | 3                 |       | x          |         | x   |
| [m4x4-PS](m4x4---ps.md)                                       | 4x4 multiplicar                                                                                     | 4                 |       | x          |         | x   |
| [Mad-PS](mad---ps.md)                                         | Multiplicar e adicionar                                                                                 | 1                 |       | x          |         |     |
| [máximo de PS](max---ps.md)                                         | Máximo                                                                                          | 1                 |       | x          |         | x   |
| [min-PS](min---ps.md)                                         | Mínimo                                                                                          | 1                 |       | x          |         | x   |
| [MOV-PS](mov---ps.md)                                         | Mover                                                                                             | 1                 |       | x          |         |     |
| [Mul-PS](mul---ps.md)                                         | Multiplicar                                                                                         | 1                 |       | x          |         |     |
| [Nop-PS](nop---ps.md)                                         | Nenhuma operação                                                                                     | 1                 |       | x          |         |     |
| [NRM-PS](nrm---ps.md)                                         | Normaliza                                                                                        | 3                 |       | x          |         | x   |
| [pow-PS](pow---ps.md)                                         | x<sup>y</sup>                                                                                    | 3                 |       | x          |         | x   |
| [profissionais](ps---ps.md)                                                | Versão                                                                                          | 0                 | x     |            |         |     |
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

 

 




