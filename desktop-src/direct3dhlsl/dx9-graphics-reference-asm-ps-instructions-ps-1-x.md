---
title: Instruções ps_1_1, ps_1_2, ps_1_3, ps_1_4
description: Esta seção contém informações de referência para as instruções da versão 1 X do sombreador de pixel \_ .
ms.assetid: cb496887-6755-4f29-b465-a36548b88722
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cc624c3f3b64d41f428f68fcf2643f4600dcdec1
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129894"
---
# <a name="ps_1_1-ps_1_2-ps_1_3-ps_1_4-instructions"></a>PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4 instruções

Esta seção contém informações de referência para as instruções da versão 1 X do sombreador de pixels \_ .

Há vários tipos de instruções de sombreador de pixel, conforme mostrado na tabela a seguir.

## <a name="instruction-set"></a>Conjunto de instruções



| Versão                                    | Descrição                                                                   | Slots de instrução | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 |
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

 

 




