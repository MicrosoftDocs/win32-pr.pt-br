---
title: ps_1_1, ps_1_2, ps_1_3, ps_1_4 instruções
description: Esta seção contém informações de referência para instruções do sombreador de pixel versão 1 \_ X.
ms.assetid: cb496887-6755-4f29-b465-a36548b88722
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 217e207d2f60d39979c7117cb48e0cb033fd98c6fbfb419642ff43e59759d510
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119730"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4-instructions"></a>ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ 1 \_ 4 Instruções

Esta seção contém informações de referência para as instruções do sombreador de pixel versão 1 \_ X.

Há vários tipos de instruções de sombreador de pixel, conforme mostrado na tabela a seguir.

## <a name="instruction-set"></a>Conjunto de instruções



| Versão                                    | Descrição                                                                   | Slots de instrução | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
|--------------------------------------------|-------------------------------------------------------------------------------|-------------------|------|------|------|------|
| [ps](ps---ps.md)                          | Número de versão                                                                | 0                 | x    | x    | x    | x    |
| Instruções constantes                      |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [def - ps](def---ps.md)                   | Definir constantes                                                              | 0                 | x    | x    | x    | x    |
| Instruções de fase                         |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [phase - ps](phase---ps.md)               | Transição entre a fase 1 e a fase 2                                        | 0                 |      |      |      | x    |
| Instruções aritméticas                    |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [add - ps](add---ps.md)                   | Adicionar dois vetores                                                               | 1                 | x    | x    | x    | x    |
| [bem - ps](bem---ps.md)                   | Aplicar uma transformação de mapa de ambiente de aumento falso                                   | 2                 |      |      |      | x    |
| [cmp - ps](cmp---ps.md)                   | Comparar a origem com 0                                                           | 1º                |      | x    | x    | x    |
| [cnd - ps](cnd---ps.md)                   | Comparar a origem com 0,5                                                         | 1                 | x    | x    | x    | x    |
| [dp3 – ps](dp3---ps.md)                   | Produto de ponto de três componentes                                                   | 1                 | x    | x    | x    | x    |
| [dp4 – ps](dp4---ps.md)                   | Produto de ponto de quatro componentes                                                    | 1º                |      | x    | x    | x    |
| [lrp – ps](lrp---ps.md)                   | Interpolação linear                                                            | 1                 | x    | x    | x    | x    |
| [mad - ps](mad---ps.md)                   | Multiplicar e adicionar                                                              | 1                 | x    | x    | x    | x    |
| [mov - ps](mov---ps.md)                   | Mover                                                                          | 1                 | x    | x    | x    | x    |
| [mul - ps](mul---ps.md)                   | Multiplicar                                                                      | 1                 | x    | x    | x    | x    |
| [nop – ps](nop---ps.md)                   | Nenhuma operação                                                                  | 0                 | x    | x    | x    | x    |
| [sub - ps](sub---ps.md)                   | Subtrair                                                                      | 1                 | x    | x    | x    | x    |
| Instruções de textura                       |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [tex - ps](tex---ps.md)                   | Amostra de uma textura                                                              | 1                 | x    | x    | x    |      |
| [texbem – ps](texbem---ps.md)             | Aplicar uma transformação de mapa de ambiente de aumento falso                                   | 1                 | x    | x    | x    |      |
| [texbeml – ps](texbeml---ps.md)           | Aplicar uma transformação de mapa de ambiente de aumento falso com correção de luminância         | 1+1;              | x    | x    | x    |      |
| [texcoord – ps](texcoord---ps.md)         | Interpretar dados de coordenadas de textura como dados de cor                               | 1                 | x    | x    | x    |      |
| [texcrd - ps](texcrd---ps.md)             | Copiar dados de coordenadas de textura como dados de cor                                    | 1                 |      |      |      | x    |
| [texdepth – ps](texdepth---ps.md)         | Calcular valores de profundidade                                                        | 1                 |      |      |      | x    |
| [texdp3 – ps](texdp3---ps.md)             | Produto de ponto de três componentes entre os dados de textura e as coordenadas de textura  | 1                 |      | x    | x    |      |
| [texdp3tex – ps](texdp3tex---ps.md)       | Produto de ponto de três componentes e lookup de textura 1D                             | 1                 |      | x    | x    |      |
| [texkill – ps](texkill---ps.md)           | Cancela a renderização de pixels com base em uma comparação                             | 1                 | x    | x    | x    | x    |
| [texld - ps \_ 1 \_ 4](texld---ps-1-4.md)     | Amostra de uma textura                                                              | 1                 |      |      |      | x    |
| [texm3x2depth – ps](texm3x2depth---ps.md) | Calcular valores de profundidade por pixel                                              | 1                 |      |      | x    |      |
| [texm3x2pad – ps](texm3x2pad---ps.md)     | Multiplicação da matriz da primeira linha de uma multiplicação de matriz de duas linhas                        | 1                 | x    | x    | x    |      |
| [texm3x2tex – ps](texm3x2tex---ps.md)     | Multiplicação da matriz de linha final de uma multiplicação de matriz de duas linhas                        | 1                 | x    | x    | x    |      |
| [texm3x3 – ps](texm3x3---ps.md)           | multiplicar matriz de 3x3                                                           | 1                 |      | x    | x    |      |
| [texm3x3pad-PS](texm3x3pad---ps.md)     | A primeira ou a segunda linha multiplicar uma multiplicação de uma matriz de três linhas                   | 1                 | x    | x    | x    |      |
| [texm3x3spec-PS](texm3x3spec---ps.md)   | Multiplicação da linha final de uma matriz de três linhas                             | 1                 | x    | x    | x    |      |
| [texm3x3tex-PS](texm3x3tex---ps.md)     | Pesquisa de textura usando uma matriz 3x3 multiplique                                   | 1                 | x    | x    | x    |      |
| [texm3x3vspec-PS](texm3x3vspec---ps.md) | Pesquisa de textura usando uma matriz 3x3 multiplique, com vetor de raio não constante | 1                 | x    | x    | x    |      |
| [texreg2ar-PS](texreg2ar---ps.md)       | Amostra de uma textura usando os componentes alfa e vermelho                           | 1                 | x    | x    | x    |      |
| [texreg2gb-PS](texreg2gb---ps.md)       | Amostra de uma textura usando os componentes verde e azul                          | 1                 | x    | x    | x    |      |
| [texreg2rgb-PS](texreg2rgb---ps.md)     | Exemplo de textura usando os componentes vermelho, verde e azul                     | 1                 |      | x    | x    |      |



 

1.  1 slot no PS \_ 1 \_ 4; 2 slots no PS \_ 1 \_ 2 e PS \_ 1 \_ 3
2.  1 + 1 = 1 instrução aritmética + 1 instrução de textura

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




