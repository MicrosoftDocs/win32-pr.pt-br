---
description: Transição de apaga do SMPTE
ms.assetid: 9271bd4b-57b1-4b1b-bfee-d6ae5f49a154
title: Transição de apaga do SMPTE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40db8097b61d1b750f8e17067bda08f94a54504c8e990656b7416d84a9a1c089
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050427"
---
# <a name="smpte-wipe-transition"></a>Transição de apaga do SMPTE

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A transição de apagamento SMPTE produz qualquer um dos apagamentos padrão definidos pela SMPTE (Society of Motion Picture and Television Engineers) no documento SMPTE 258M-1993, com exceção da divisão quadrária.

![transição de apagando em andamento](images/trans-wipe.png)

CLSID (ID de classe): {DE75D012-7A65-11D2-8CEA-00A0C9441E20}

Nome da variável CLSID: CLSID \_ DxtJpeg

Nome amigável: "DxtJpeg"

Propriedades



| Propriedade       | Type   | Padrão  | Descrição                                                                                                                                                                                                                                                                                                      |
|----------------|--------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BorderColor    | long   | 0x000000 | Cor da borda em torno das bordas do padrão de apagando. O valor desse atributo é um número hexadecimal com o formato 0x *RRGGBB,* em que *RR* é o valor vermelho, *GG* é o valor verde e *BB* é o valor azul. (Portanto, vermelho puro, verde e azul são 0xFF000, 0x00FF00 e 0x0000FF, respectivamente.) |
| BorderSoftness | long   | 0        | Largura da região desfocado em torno das bordas do padrão de apagando. Especifique zero para nenhuma região desfocado.                                                                                                                                                                                                              |
| BorderWidth    | long   | 0        | Largura da borda sólida ao longo das bordas do padrão de apagando. Especifique zero para nenhuma borda.                                                                                                                                                                                                                       |
| MaskName       | BSTR   | **NULL** | Se não **for NULL,** especificará o nome de um arquivo JPEG a ser usado como a máscara de apagando em vez de um apagando padrão e integrado. O arquivo deve conter um gradiente monocromático de 8 bits por pixel. O gradiente é usado como uma máscara para definir a progressão do apagamento.                                                                 |
| MaskNum        | long   | 1        | Código de apagamento SMPTE padrão especificando o estilo de apagamento a ser usado. Para ver uma lista de códigos de apagando e seus esquemas associados, consulte o documento SMPTE 258M-1993.                                                                                                                                                            |
| OffsetX        | long   | 0        | Deslocamento horizontal da origem do apagando do centro da imagem. Válido somente para valores de **MaskNum** de 101 a 131.                                                                                                                                                                                         |
| OffsetY        | long   | 0        | Deslocamento vértice da origem do apagando do centro da imagem. Válido somente para valores de **MaskNum** de 101 a 131.                                                                                                                                                                                            |
| ReplicateX     | long   | 0        | Número de vezes para replicar o padrão de apagando horizontalmente. Válido somente para valores de **MaskNum** de 101 a 131.                                                                                                                                                                                                |
| Replicatey     | long   | 0        | Número de vezes para replicar o padrão de apagando verticalmente. Válido somente para valores de **MaskNum** de 101 a 131.                                                                                                                                                                                                  |
| Scalex         | double | 1.0      | Quantidade pela qual alongar o apagaamento horizontalmente, como uma porcentagem da definição de apagaamento original. Válido somente para valores de **MaskNum** de 101 a 131.                                                                                                                                                         |
| Scaley         | double | 1.0      | Quantidade pela qual alongar o apagaamento verticalmente, como uma porcentagem da definição de apagaamento original. Válido somente para valores de **MaskNum** de 101 a 131.                                                                                                                                                           |



 

## <a name="remarks"></a>Comentários

Essa transição dá suporte aos seguintes apagadores SMPTE padrão:



| Número | Descrição                   | Número | Descrição                                 |
|--------|-------------------------------|--------|---------------------------------------------|
| 1      | Horizontal                    | 211    | Radial, esquerdo direito, superior                     |
| 2      | Vertical                      | 212    | Radial, para cima para baixo, direita                      |
| 3      | Canto superior esquerdo                    | 213    | Radial, esquerdo direito, parte superior inferior              |
| 4      | Canto superior direito                   | 214    | Radial, para cima para baixo, para a esquerda e para a direita                 |
| 5      | Inferior direito                   | 221    | Radial, superior                                 |
| 6      | Inferior esquerdo                    | 222    | Radial, direita                               |
| 7      | Quatro cantos                  | 223    | Radial, inferior                              |
| 8      | Quatro quadrados                  | 224    | Radial, esquerda                                |
| 21     | Portas de barra vertical, verticais          | 225    | Radial, no sentido horário superior, inferior no sentido horário     |
| 22     | Portas de portões, horizontal        | 226    | Radial, à esquerda no sentido horário, à direita no sentido horário     |
| 23     | Centro superior                    | 227    | Radial, no sentido horário superior, inferior no sentido anti-horário |
| 24     | Centro direito                  | 228    | Radial, à esquerda no sentido horário, à direita no sentido anti-horário |
| 25     | Centro inferior                 | 231    | Radial, divisão superior                           |
| 26     | Centro esquerdo                   | 232    | Radial, divisão direita                         |
| 41     | Diagonal, NW para ES            | 233    | Radial, divisão inferior                        |
| 42     | Diagonal, NE para SW            | 234    | Radial, divisão à esquerda                          |
| 43     | Triângulos, superior/inferior         | 235    | Divisão radial, parte superior inferior                    |
| 44     | Triângulos, esquerda/direita         | 236    | Divisão radial, esquerda direita                    |
| 45     | Faixa diagonal, SW para NE     | 241    | Radial, canto superior esquerdo                     |
| 46     | Faixa diagonal, NW para ES     | 242    | Radial, canto inferior esquerdo                  |
| 47     | Cross                         | 243    | Radial, canto inferior direito                 |
| 48     | Caixa de losango                   | 244    | Radial, canto superior direito                    |
| 61     | Borda, superior                    | 245    | Radial, superior esquerdo, inferior direito              |
| 62     | Ental, à direita                  | 246    | Radial, inferior esquerdo, superior direito              |
| 63     | Borda, parte inferior                 | 251    | Radial central, superior                          |
| 64     | Ressição, esquerda                   | 252    | Radial central, esquerda                         |
| 65     | V                             | 253    | Radial central, inferior                       |
| 66     | V, direita                      | 254    | Radial central, direita                        |
| 67     | V, invertido                   | 261    | Radial da caixa, direita                           |
| 68     | V, esquerda                       | 262    | Radial da caixa, superior                             |
| 71     | Sawtooth, esquerda                | 263    | Radial central, superior, inferior                  |
| 72     | Sawtooth, top                 | 264    | Radial central, esquerda, direita                  |
| 73     | Sawtooth, vertical            | 301    | Matriz, horizontal                          |
| 74     | Sawtooth, horizontal          | 302    | Matriz, vertical                            |
| 101    | Box                           | 303    | Matriz, diagonal, superior esquerdo                  |
| 102    | Diamond                       | 304    | Matriz, diagonal, superior direito                 |
| 103    | Triângulo, para cima                  | 305    | Matriz, diagonal, inferior direito              |
| 104    | Triângulo, direita               | 306    | Matriz, diagonal, inferior esquerdo               |
| 105    | Triângulo, parte inferior              | 310    | Matriz, no sentido horário superior esquerdo                  |
| 106    | Triângulo, à esquerda                | 311    | Matriz, no sentido horário superior direito                 |
| 107    | Seta para cima                | 312    | Matriz, no sentido horário inferior direito              |
| 108    | Seta para a cabeça, direita             | 313    | Matriz, no sentido horário inferior esquerdo               |
| 109    | Seta para cima, para baixo              | 314    | Matriz, no sentido anti-horário superior esquerdo              |
| 110    | Seta para a esquerda              | 315    | Matriz, no sentido anti-horário superior direito             |
| 111    | Todo mundo, para cima                  | 316    | Matriz, no sentido anti-horário inferior direito          |
| 112    | Washington, para baixo                | 317    | Matriz, no sentido anti-horário, inferior esquerdo           |
| 113    | Hexágono                       | 320    | Matriz, vertical superior esquerdo, superior direito        |
| 114    | Hexágono, girado              | 321    | Matriz, vertical inferior esquerdo, inferior direito  |
| 119    | Circle                        | 322    | Matriz, vertical superior esquerdo, inferior direito     |
| 120    | Oval, horizontal              | 323    | Matriz, vertical inferior esquerdo, superior direito     |
| 121    | Oval, vertical                | 324    | Matriz, canto superior esquerdo horizontal, canto inferior esquerdo    |
| 122    | Olho, horizontal               | 325    | Matriz, canto superior direito horizontal, canto inferior direito  |
| 123    | Olho, vertical                 | 326    | Matriz, superior esquerdo horizontal, inferior direito   |
| 124    | Retângulo arredondado, horizontal | 327    | Matriz, canto superior direito horizontal, canto inferior esquerdo   |
| 125    | Retângulo arredondado, vertical   | 328    | Matriz, diagonal inferior esquerda, superior direito     |
| 127    | Estrela de 4 pontos                  | 329    | Matriz, diagonal superior esquerda, inferior direita     |
| 128    | estrela de 4 pontas                  | 340    | Matriz, primeiro espiral duplo                   |
| 129    | estrela de 6 pontas                  | 341    | Matriz, espiral duplo inferior                |
| 130    | Heart                         | 342    | Matriz, espiral duplo à esquerda                  |
| 131    | Keyhole                       | 343    | Matriz, espiral duplo à direita                 |
| 201    | Radial, 12 horas            | 344    | Matriz, espiral quádruplo, parte superior inferior             |
| 202    | Radial, 3 horas             | 345    | Matriz, espiral quádruplo, esquerda para a direita             |
| 203    | Radial, 6 horas             | 350    | Cascata, esquerda                             |
| 204    | Radial, 9 horas             | 351    | Cascata, à direita                            |
| 205    | Radial, 12 + 6 horas        | 352    | Cascata, horizontal, esquerda                 |
| 206    | Radial, 3 + 9 horas         | 353    | Cascata, horizontal, direita                |
| 207    | Radial, 4 vias                 | 409    | Máscara aleatória                                 |



 

 

 



