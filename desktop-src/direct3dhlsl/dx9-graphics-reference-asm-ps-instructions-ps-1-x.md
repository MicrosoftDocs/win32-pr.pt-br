---
title: Instruções ps_1_1, ps_1_2, ps_1_3, ps_1_4
description: Esta seção contém informações de referência para as instruções da versão 1 X do sombreador de pixels \_ .
ms.assetid: cb496887-6755-4f29-b465-a36548b88722
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2c3fa8e76e1075da321a60d05504dff074dbfcfe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160504"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4-instructions"></a>PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4 instruções

Esta seção contém informações de referência para as instruções da versão 1 X do sombreador de pixels \_ .

Há vários tipos de instruções de sombreador de pixel, conforme mostrado na tabela a seguir.

## <a name="instruction-set"></a>Conjunto de instruções



| Versão                                    |                                                                               | Slots de instrução | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
|--------------------------------------------|-------------------------------------------------------------------------------|-------------------|------|------|------|------|
| [profissionais](ps---ps.md)                          | Número de versão                                                                | 0                 | x    | x    | x    | x    |
| Instruções constantes                      |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [def-PS](def---ps.md)                   | Definir constantes                                                              | 0                 | x    | x    | x    | x    |
| Instruções da fase                         |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [fase-PS](phase---ps.md)               | Transição entre a fase 1 e a fase 2                                        | 0                 |      |      |      | x    |
| Instruções aritméticas                    |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [Adicionar-PS](add---ps.md)                   | Adicionar dois vetores                                                               | 1                 | x    | x    | x    | x    |
| [Bem-PS](bem---ps.md)                   | Aplicar um ambiente de relevo falso – transformação de mapa                                   | 2                 |      |      |      | x    |
| [CMP-PS](cmp---ps.md)                   | Comparar origem com 0                                                           | 1 ¹                |      | x    | x    | x    |
| [CND-PS](cnd---ps.md)                   | Comparar origem com 0,5                                                         | 1                 | x    | x    | x    | x    |
| [DP3-PS](dp3---ps.md)                   | Produto de três componentes do ponto                                                   | 1                 | x    | x    | x    | x    |
| [DP4-PS](dp4---ps.md)                   | Produto de quatro componentes do ponto                                                    | 1 ¹                |      | x    | x    | x    |
| [LRP-PS](lrp---ps.md)                   | Interpolação linear                                                            | 1                 | x    | x    | x    | x    |
| [Mad-PS](mad---ps.md)                   | Multiplicar e adicionar                                                              | 1                 | x    | x    | x    | x    |
| [MOV-PS](mov---ps.md)                   | Mover                                                                          | 1                 | x    | x    | x    | x    |
| [Mul-PS](mul---ps.md)                   | Multiplicar                                                                      | 1                 | x    | x    | x    | x    |
| [Nop-PS](nop---ps.md)                   | Nenhuma operação                                                                  | 0                 | x    | x    | x    | x    |
| [sub-PS](sub---ps.md)                   | Subtrair                                                                      | 1                 | x    | x    | x    | x    |
| Instruções de textura                       |                                                                               |                   | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
| [Tex-PS](tex---ps.md)                   | Amostra de uma textura                                                              | 1                 | x    | x    | x    |      |
| [texbem-PS](texbem---ps.md)             | Aplicar um ambiente de relevo falso – transformação de mapa                                   | 1                 | x    | x    | x    |      |
| [texbeml-PS](texbeml---ps.md)           | Aplicar um ambiente de relevo falso – mapear transformação com correção de luminância         | 1 +1 ²              | x    | x    | x    |      |
| [texcoord-PS](texcoord---ps.md)         | Interpretar dados de coordenadas de textura como dados de cores                               | 1                 | x    | x    | x    |      |
| [texcrd-PS](texcrd---ps.md)             | Copiar dados de coordenadas de textura como dados de cores                                    | 1                 |      |      |      | x    |
| [texdepth-PS](texdepth---ps.md)         | Calcular valores de profundidade                                                        | 1                 |      |      |      | x    |
| [texdp3-PS](texdp3---ps.md)             | Produto de três componentes do ponto entre os dados de textura e as coordenadas de textura  | 1                 |      | x    | x    |      |
| [texdp3tex-PS](texdp3tex---ps.md)       | Produtos de ponto de três componentes e pesquisa de textura 1D                             | 1                 |      | x    | x    |      |
| [texkill-PS](texkill---ps.md)           | Cancela a renderização de pixels com base em uma comparação                             | 1                 | x    | x    | x    | x    |
| [texld-PS \_ 1 \_ 4](texld---ps-1-4.md)     | Amostra de uma textura                                                              | 1                 |      |      |      | x    |
| [texm3x2depth-PS](texm3x2depth---ps.md) | Calcular valores de profundidade por pixel                                              | 1                 |      |      | x    |      |
| [texm3x2pad-PS](texm3x2pad---ps.md)     | Multiplicação da primeira matriz de linhas de uma matriz de duas linhas                        | 1                 | x    | x    | x    |      |
| [texm3x2tex-PS](texm3x2tex---ps.md)     | Última matriz de linha de multiplicação de uma multiplicação de matriz de duas linhas                        | 1                 | x    | x    | x    |      |
| [texm3x3-PS](texm3x3---ps.md)           | multiplicar matriz de 3x3                                                           | 1                 |      | x    | x    |      |
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

 

 




