---
title: Matrizes (RPC) (TFS)
description: As categorias de matriz de chamada de procedimento remoto (RPC) incluem tamanho fixo, compatível, variável, variável e complexa.
ms.assetid: 7144ec87-90f2-463a-80e4-28cb4771325f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6271f6a459ebfb96cc5c4d55153bb4c77b013a50925d9c3a4ba9dd81b0f6fbdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073486"
---
# <a name="arrays-rpc"></a>Matrizes (RPC)

Várias categorias de matriz foram definidas com base em suas características de desempenho, principalmente se a matriz pode ser copiada em bloco.

Para algumas categorias, como uma matriz de tamanho fixo, existem dois tipos de descritores de matriz; Eles são indicados por um em correção no nome do token FC à esquerda.



| Formatar caractere | Descrição                                                           |
|------------------|-----------------------------------------------------------------------|
| SM               | O tamanho total do tipo pode ser representado em um int sem sinal de 16 bits.    |
| LG               | O tamanho total do tipo precisa de um longo de 32 bits sem sinal para ser representado. |



 

Campos comuns a matrizes:

-   \_Tamanho total

    Tamanho total da matriz na memória, em bytes. Isso é o mesmo que o tamanho da conexão após o alinhamento. O tamanho total é calculado para categorias para as quais o problema de preenchimento não existe e o tamanho é o tamanho real da matriz.

-   tamanho do elemento \_

    Tamanho total na memória de um único elemento da matriz, incluindo o preenchimento (isso pode acontecer apenas para matrizes complexas).

-   Descrição do elemento \_

    Descrição do tipo de elemento da matriz.

-   layout do ponteiro \_

    Consulte o tópico [layout do ponteiro](pointer-layout-tfs.md) para obter mais informações.

## <a name="fixed-sized-arrays"></a>Matrizes de tamanho fixo

Uma cadeia de formato de matriz de tamanho fixo é gerada para matrizes que têm um tamanho conhecido e, portanto, podem ser copiadas em bloco para o buffer de marshaling. Os dois formatos de descritor de matriz fixos são os seguintes.

``` syntax
FC_SMFARRAY alignment<1> 
total_size<2> 
[pointer_layout<>]  
element_description<> 
FC_END
```

e

``` syntax
FC_LGFARRAY alignment<1> 
total_size<4> 
[pointer_layout<>] 
element_description<> 
FC_END
```

## <a name="conformant-array"></a>Matriz de conformidade

Uma matriz compatível pode ser copiada em bloco depois que o tamanho da matriz é conhecido.

``` syntax
FC_CARRAY alignment<1>
element_size<2> 
conformance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END
```

A descrição de conformidade \_<> é um descritor de correlação e tem 4 ou 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado.

## <a name="conformant-varying-array"></a>Matriz de variação em conformidade

Uma matriz de variação em conformidade também pode ser copiada em bloco.

``` syntax
FC_CVARRAY alignment<1> 
element_size<2> 
conformance_description<> 
variance_description<>  
[pointer_layout<>] 
element_description<> 
FC_END
```

A descrição de conformidade \_<> e a descrição da variância \_<> é um descritor de correlação e tem 4 ou 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado.

## <a name="varying-array"></a>Matriz variável

As matrizes variantes têm duas possibilidades, dependendo do tamanho da matriz.

``` syntax
FC_SMVARRAY alignment<1>
total_size<2>  
number_elements<2> 
element_size<2> 
variance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END

FC_LGVARRAY alignment<1>
total_size<4>  
number_elements<4> 
element_size<2> 
variance_description<4>
[pointer_layout<>] 
element_description<> 
FC_END
```

A descrição da variância \_<> é um descritor de correlação e tem 4 ou 6 bytes, dependendo do [**/robust**](/windows/desktop/Midl/-robust) que está sendo usado.

Para matrizes variáveis inseridas dentro de uma estrutura, o campo deslocamento<2> da \_ Descrição da variância<> é um deslocamento relativo da posição da matriz variável na estrutura até a variação que descreve o campo. Normalmente, o deslocamento é relativo ao início da estrutura.

## <a name="complex-arrays"></a>Matrizes complexas

Uma matriz complexa é qualquer matriz com um elemento que impede que ele seja copiado em bloco e, dessa forma, uma ação adicional precisa ser executada. Esses elementos tornam uma matriz complexa:

-   tipos simples: ENUM16, \_ \_ INT3264 (somente em plataformas de 64 bits), um integral com \[ [ **intervalo**](/windows/desktop/Midl/range)\]
-   ponteiros de referência e de interface (todos os ponteiros em plataformas de 64 bits)
-   uniões
-   estruturas complexas (consulte o tópico de descrição de estrutura complexa para obter uma lista completa de motivos para uma estrutura ser complexa)
-   elementos definidos com \[ [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) \] , \[ [**\_ Marshal do usuário**](/windows/desktop/Midl/user-marshal)\]
-   Todas as matrizes multidimensionais com pelo menos uma dimensão de conformidade e/ou variável são complexas, independentemente do tipo de elemento subjacente.

A descrição complexa da matriz é a seguinte:

``` syntax
FC_BOGUS_ARRAY alignment<1> 
number_of_elements<2> 
conformance_description<> 
variance_description<> 
element_description<> 
FC_END
```

O número \_ de \_ elementos<2> campo será zero se a matriz for compatível.

A descrição de conformidade \_<> e a descrição da variância \_<> é um descritor de correlação e tem 4 ou 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado. Se a matriz tiver conformidade e/ou variação, a descrição de conformidade \_<> e/ou a descrição da variação \_<> campo (s) terá descrições válidas, caso contrário, os quatro primeiros bytes do descritor de correlação serão definidos como 0xFFFFFFFF. Os sinalizadores, quando presentes, são definidos como zero.

 

 
