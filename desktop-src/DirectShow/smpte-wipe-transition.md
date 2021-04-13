---
description: Transição de apagamento SMPTE
ms.assetid: 9271bd4b-57b1-4b1b-bfee-d6ae5f49a154
title: Transição de apagamento SMPTE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47de62c450ff0d75f72e5fac466801991b987834
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500465"
---
# <a name="smpte-wipe-transition"></a>Transição de apagamento SMPTE

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A transição de apagamento SMPTE produz qualquer um dos apagamentos padrão definidos pela sociedade de imagem e engenheiros de televisão (SMPTE) no documento SMPTE 258M-1993, com exceção da divisão quádrupla.

![transição de apagamento em andamento](images/trans-wipe.png)

ID de classe (CLSID): {DE75D012-7A65-11D2-8CEA-00A0C9441E20}

Nome da variável CLSID: CLSID \_ DxtJpeg

Nome amigável: "DxtJpeg"

Propriedades



| Propriedade       | Type   | Padrão  | Descrição                                                                                                                                                                                                                                                                                                      |
|----------------|--------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BorderColor    | long   | 0x000000 | Cor da borda ao contrário das bordas do padrão de apagamento. O valor desse atributo é um número hexadecimal com o formato 0x *RRGGBB*, em que *RR* é o valor vermelho, *gg* é o valor verde e *BB* é o valor azul. (Portanto, vermelho puro, verde e azul são 0xFF000, 0x00FF00 e 0x0000FF, respectivamente.) |
| BorderSoftness | long   | 0        | Largura da região borrada ao contrário das bordas do padrão de apagamento. Especifique zero para nenhuma região borrada.                                                                                                                                                                                                              |
| BorderWidth    | long   | 0        | Largura da borda sólida ao longo das bordas do padrão de apagamento. Especifique zero para nenhuma borda.                                                                                                                                                                                                                       |
| Maskname       | BSTR   | **NULL** | Se não for **NULL**, especifica o nome de um arquivo JPEG a ser usado como a máscara de apagamento em vez de um apagamento interno padrão. O arquivo deve conter um gradiente monocromático de 8 bits por pixel. O gradiente é usado como uma máscara para definir a progressão do apagamento.                                                                 |
| MaskNum        | long   | 1        | Código de apagamento Standard SMPTE que especifica o estilo de apagamento a ser usado. Para obter uma lista de códigos de apagamento e seus esquemáticos associados, consulte o documento SMPTE 258M-1993.                                                                                                                                                            |
| OffsetX        | long   | 0        | Deslocamento horizontal da origem do apagamento a partir do centro da imagem. Válido somente para os valores de **MaskNum** de 101 a 131.                                                                                                                                                                                         |
| OffsetY        | long   | 0        | Verical o deslocamento da origem do apagamento do centro da imagem. Válido somente para os valores de **MaskNum** de 101 a 131.                                                                                                                                                                                            |
| ReplicateX     | long   | 0        | Número de vezes para replicar o padrão de apagamento horizontalmente. Válido somente para os valores de **MaskNum** de 101 a 131.                                                                                                                                                                                                |
| Complicação     | long   | 0        | Número de vezes para replicar o padrão de apagamento verticalmente. Válido somente para os valores de **MaskNum** de 101 a 131.                                                                                                                                                                                                  |
| ScaleX         | double | 1.0      | Valor pelo qual estender o apagamento horizontalmente, como uma porcentagem da definição de apagamento original. Válido somente para os valores de **MaskNum** de 101 a 131.                                                                                                                                                         |
| ScaleY         | double | 1.0      | Valor pelo qual estender o apagamento verticalmente, como uma porcentagem da definição de apagamento original. Válido somente para os valores de **MaskNum** de 101 a 131.                                                                                                                                                           |



 

## <a name="remarks"></a>Comentários

Essa transição dá suporte aos seguintes apagamentos padrão do SMPTE:



| Número | Descrição                   | Número | Descrição                                 |
|--------|-------------------------------|--------|---------------------------------------------|
| 1      | Horizontal                    | 211    | Radial, esquerda para a direita, superior                     |
| 2      | Vertical                      | 212    | Radial, para cima para baixo, para a direita                      |
| 3      | Superior esquerdo                    | 213    | Radial, da esquerda para a direita, de cima para baixo              |
| 4      | Superior direito                   | 214    | Radial, para cima para baixo, da esquerda para a direita                 |
| 5      | Inferior direito                   | 221    | Radial, superior                                 |
| 6      | Inferior esquerdo                    | 222    | Radial, direita                               |
| 7      | Quatro cantos                  | 223    | Radial, inferior                              |
| 8      | Quatro quadrados                  | 224    | Radial, esquerda                                |
| 21     | Portas Barn, vertical          | 225    | Radial, sentido horário superior, sentido horário inferior     |
| 22     | Portas Barn, horizontal        | 226    | Radial, esquerda e direita, sentido horário direito     |
| 23     | Superior central                    | 227    | Radial, no sentido horário superior, no sentido inferior |
| 24     | Centro direito                  | 228    | Radial, à esquerda no sentido horário, à direita |
| 25     | Inferior central                 | 231    | Radial, divisão superior                           |
| 26     | Centro esquerdo                   | 232    | Radial, divisão à direita                         |
| 41     | Diagonal, NW para SE            | 233    | Radial, divisão inferior                        |
| 42     | Diagonal, NE a SW            | 234    | Radial, divisão à esquerda                          |
| 43     | Triângulos, superior/inferior         | 235    | Radial, divisão de cima para baixo                    |
| 44     | Triângulos, esquerda/direita         | 236    | Radial, divisão da esquerda para a direita                    |
| 45     | Faixa diagonal, SW para NE     | 241    | Radial, canto superior esquerdo                     |
| 46     | Faixa diagonal, NW para SE     | 242    | Radial, canto inferior esquerdo                  |
| 47     | Cross                         | 243    | Radial, canto inferior direito                 |
| 48     | Caixa de losango                   | 244    | Radial, canto superior direito                    |
| 61     | Fatia, superior                    | 245    | Radial, superior esquerda, inferior direita              |
| 62     | Fatiar, direita                  | 246    | Radial, inferior esquerda, superior direita              |
| 63     | Fatia, inferior                 | 251    | Centro-radial, superior                          |
| 64     | Fatiar à esquerda                   | 252    | Centro-radial, esquerda                         |
| 65     | V                             | 253    | Centro-radial, inferior                       |
| 66     | V, direita                      | 254    | Centro-radial, direita                        |
| 67     | V, invertido                   | 261    | Box radial, direita                           |
| 68     | V, esquerda                       | 262    | Box radial, superior                             |
| 71     | Sawtooth, esquerda                | 263    | Central radial, superior, inferior                  |
| 72     | Sawtooth, superior                 | 264    | Central radial, esquerda, direita                  |
| 73     | Sawtooth, vertical            | 301    | Matriz, horizontal                          |
| 74     | Sawtooth, horizontal          | 302    | Matriz, vertical                            |
| 101    | Box                           | 303    | Matriz, diagonal, superior esquerda                  |
| 102    | Diamond                       | 304    | Matriz, diagonal, superior direita                 |
| 103    | Triângulo, para cima                  | 305    | Matriz, diagonal, inferior direita              |
| 104    | Triângulo, à direita               | 306    | Matriz, diagonal, inferior esquerda               |
| 105    | Triângulo, inferior              | 310    | Matriz, sentido horário superior esquerda                  |
| 106    | Triângulo, esquerda                | 311    | Matriz, sentido horário superior direito                 |
| 107    | Cabeçalho da seta, para cima                | 312    | Matriz, sentido horário inferior direita              |
| 108    | Cabeçalho da seta, à direita             | 313    | Matriz, sentido horário inferior esquerda               |
| 109    | Cabeçalho da seta, para baixo              | 314    | Matriz, sentido anti-horário superior esquerda              |
| 110    | Cabeçalho da seta, esquerda              | 315    | Matriz, no sentido anti-horário superior direita             |
| 111    | Pentágono, para cima                  | 316    | Matriz, no sentido horário inferior direita          |
| 112    | Pentágono, para baixo                | 317    | Matriz, no sentido horário inferior esquerda           |
| 113    | Hexágono                       | 320    | Matriz, vertical superior esquerda, superior direita        |
| 114    | Hexágono, girado              | 321    | Matriz, vertical inferior esquerda, inferior direita  |
| 119    | Circle                        | 322    | Matriz, vertical superior esquerda, inferior direita     |
| 120    | Oval, horizontal              | 323    | Matriz, vertical inferior esquerda, superior direita     |
| 121    | Oval, vertical                | 324    | Matriz, horizontal superior esquerda, inferior esquerda    |
| 122    | Olho, horizontal               | 325    | Matriz, horizontal superior direita, inferior direita  |
| 123    | Olho, vertical                 | 326    | Matriz, horizontal superior esquerda, inferior direita   |
| 124    | Retângulo arredondado, horizontal | 327    | Matriz, horizontal superior direita, inferior esquerda   |
| 125    | Retângulo arredondado, vertical   | 328    | Matriz, diagonal inferior esquerda, superior direita     |
| 127    | estrela de 4 pontas                  | 329    | Matriz, diagonal superior esquerda, inferior direita     |
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



 

 

 



