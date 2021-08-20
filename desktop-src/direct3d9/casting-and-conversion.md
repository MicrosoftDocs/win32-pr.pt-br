---
description: Ao transferir valores entre o aplicativo host e um parâmetro de efeito, os dados são gravados como esperado quando o tipo de dados de origem (no aplicativo host) corresponde ao tipo de dados de destino (no parâmetro de efeito).
ms.assetid: 4f3ef14a-7d67-45fe-9282-541221815d1f
title: Elenco e conversão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ca806caba09796acc4d0f966926edb9b6a37cf0ab2d40656e7d99f92d5b46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097121"
---
# <a name="casting-and-conversion"></a>Elenco e conversão

Ao transferir valores entre o aplicativo host e um parâmetro de efeito, os dados são gravados como esperado quando o tipo de dados de origem (no aplicativo host) corresponde ao tipo de dados de destino (no parâmetro de efeito). Quando os tipos de dados forem diferentes, a conversão ocorrerá, pois os dados de origem serão reorganizados para se ajustarem ao destino.

DXSAS define as regras de conversão de tipo a seguir. Esses são um superconjunto das regras de conversão de tipo de efeito (. FX) e HLSL. DXSAS também define alguns [modificadores de valor de parâmetro](#parameter-value-modifiers) que podem afetar o valor que está sendo transferido do aplicativo host para um parâmetro associado.

## <a name="type-casting"></a>Conversão de tipo

A tabela a seguir lista a conversão que ocorrerá quando um tipo de dados for transferido para outro tipo de dados:



| Tipo de Fonte                                  | Tipo de Destino                             | Comportamento                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FLOAT                                        | INT                                          | Arredondar para zero.                                                                                                                                                                                                                                                                                                                                                                                      |
| float, int                                   | bool                                         | Valores que não são iguais a 0-baseados em uma comparação não-igual a para 0 (int) ou 0,0 (float)-são considerados como true, caso contrário, o valor é considerado como false.                                                                                                                                                                                                                                         |
| INT                                          | FLOAT                                        |                                                                                                                                                                                                                                                                                                                                                                                                          |
| bool                                         | int, float                                   | False é convertido em zero. True é convertido em um.                                                                                                                                                                                                                                                                                                                                                     |
| texture1D, texture2D, texture3D, textureCUBE | textura                                      | A textura de destino é tratada como o tipo de textura de origem.                                                                                                                                                                                                                                                                                                                                               |
| string                                       | texture1D, texture2D, texture3D, textureCUBE | O valor da cadeia de caracteres é tratado como um endereço de recurso e resolvido da mesma maneira que a [anotação de inicialização do parâmetro](parameter-initialization-annotation.md). Se o endereço do recurso não puder ser resolvido, a conversão será inválida e os aplicativos host deverão retornar um erro. Se o recurso for resolvido corretamente, o tipo da expressão será tratado como o mesmo tipo do recurso resolvido. |



 

## <a name="class-casting"></a>Conversão de classe

Além das regras de conversão de tipo descritas acima, DXSAS define o conjunto de regras de conversão necessárias para converter entre tipos de classe. As matrizes de coluna (N x 1), matrizes de linha (1 x N) e estruturas numéricas são tratadas como vetores.

Os parâmetros de matriz de efeito e as variáveis de matriz HLSL podem definir se o valor é uma matriz de linha principal ou de coluna principal; no entanto, as APIs do DirectX sempre tratam [**D3DMATRIX**](d3dmatrix.md) e [**D3DXMATRIX**](d3dxmatrix.md) como linha-principal.



| Classe de origem | Classe de destino | Comportamento                                                                                                                                                                                                                                                                                                                                        |
|--------------|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Escalar       | Escalar            | Aplicar conversão de tipo.                                                                                                                                                                                                                                                                                                                             |
| Escalar       | Vetor            | Replique o valor de origem escalar em todos os componentes do vetor de destino depois de aplicar a conversão de tipo e o comportamento do Conversion descrito em conversão de tipo.                                                                                                                                                                             |
| Escalar       | Matriz            | Replique o valor de origem escalar em todos os componentes da matriz de destino depois de aplicar a conversão de tipo e o comportamento do Conversion descrito em conversão de tipo.                                                                                                                                                                             |
| Escalar       | Objeto            | Conversão inválida. Os aplicativos host devem retornar um erro.                                                                                                                                                                                                                                                                                           |
| Escalar       | Estrutura         | Válido somente se a estrutura de destino contiver apenas elementos numéricos. Se for válido, replique o valor de origem escalar em todos os componentes da estrutura de destino depois de aplicar a conversão de tipo e o comportamento de validação descritos em conversão de tipo.                                                                                        |
| Vetor       | Escalar            | O escalar de destino recebe o valor do primeiro componente do vetor de origem depois de aplicar a conversão de tipo e o comportamento de conversão descrito em [conversão de tipo](#type-casting).                                                                                                                                                       |
| Vetor       | Vetor            | Conversão inválida se o vetor de destino tiver mais componentes do que o vetor de origem. O vetor de destino recebe os valores mais à esquerda do vetor de origem depois de aplicar a conversão de tipo e o comportamento de converter descrito em [conversão de tipo](#type-casting). Os componentes restantes mais à direita do vetor de origem são perdidos.             |
| Vetor       | Matriz            | Conversão inválida, a menos que o vetor de origem tenha o mesmo número de componentes que a matriz de destino. Se a conversão for válida, o comportamento da conversão de vetor para vetor será aplicado.                                                                                                                                                             |
| Vetor       | Objeto            | Conversão inválida. Os aplicativos host devem retornar um erro.                                                                                                                                                                                                                                                                                           |
| Vetor       | Estrutura         | Válido somente se a estrutura de destino tiver apenas elementos numéricos e não contiver mais elementos do que o vetor de origem tiver componentes. Os elementos da estrutura de destino recebem os componentes mais à esquerda do vetor de origem depois de aplicar a conversão de tipo e o comportamento de converter descrito em [conversão de tipo](#type-casting).      |
| Matriz       | Escalar            | O escalar de destino recebe o valor do valor superior esquerdo da matriz de origem depois de aplicar a conversão de tipo e o comportamento de converter descrito em [conversão de tipo](#type-casting).                                                                                                                                                 |
| Matriz       | Vetor            | Conversão inválida, a menos que a matriz de origem tenha o mesmo número de componentes que o vetor de destino. Se a conversão for válida, o comportamento da conversão vetorial para vetor acima será aplicado.                                                                                                                                                       |
| Matriz       | Matriz            | Conversão inválida se a matriz de destino tiver mais componentes do que a matriz de origem. A matriz de destino recebe os valores na extremidade superior esquerda da matriz de origem depois de aplicar a conversão de tipo e o comportamento do Conversion descrito em [conversão de tipo](#type-casting). Os componentes restantes na parte inferior direita da matriz de origem são perdidos. |
| Matriz       | Objeto            | Conversão inválida. Os aplicativos host devem retornar um erro.                                                                                                                                                                                                                                                                                           |
| Matriz       | Estrutura         | O tamanho da estrutura deve ser igual ao tamanho da matriz e todos os componentes da estrutura devem ser numéricos.                                                                                                                                                                                                                          |
| Objeto       | Escalar            | Conversão inválida. Os aplicativos host devem retornar um erro.                                                                                                                                                                                                                                                                                           |
| Objeto       | Vetor            | Conversão inválida. Os aplicativos host devem retornar um erro.                                                                                                                                                                                                                                                                                           |
| Objeto       | Matriz            | Conversão inválida. Os aplicativos host devem retornar um erro.                                                                                                                                                                                                                                                                                           |
| Objeto       | Objeto            | Válido se os tipos dos objetos forem idênticos e de acordo com o comportamento definido na [conversão de tipo](#type-casting).                                                                                                                                                                                                                   |
| Estrutura    | Escalar            | Válido se a estrutura de origem contiver pelo menos um membro numérico. O escalar de destino recebe o valor do primeiro membro numérico da estrutura de origem depois de aplicar a conversão de tipo e o comportamento de converter descrito em [conversão de tipo](#type-casting).                                                                                |
| Estrutura    | Vetor            | A estrutura de origem deve ter pelo menos o tamanho do vetor. Os primeiros componentes devem ser numéricos até o tamanho do vetor de destino.                                                                                                                                                                                                    |
| Estrutura    | Matriz            | A estrutura de origem deve ter pelo menos o tamanho do vetor. Os primeiros componentes devem ser numéricos até o tamanho do vetor de destino.                                                                                                                                                                                                    |
| Estrutura    | Estrutura         | A estrutura de destino não deve ser maior que a estrutura de origem. Uma conversão válida deve existir entre todos os respectivos componentes de origem e de destino.                                                                                                                                                                                       |



 

## <a name="parameter-value-modifiers"></a>Modificadores de valor de parâmetro

As anotações de modificador de parâmetro adicionam informações adicionais a um parâmetro para que os dados do parâmetro possam ser interpretados corretamente. Por exemplo, um vetor pode precisar ser expresso com dados normalizados ou um comprimento pode ser medido em polegadas. As anotações de modificador de valor de parâmetro expressam essas informações adicionais para que os aplicativos host possam transformar valores corretamente quando os dados são transferidos para um parâmetro de efeito.

Estes são os modificadores de parâmetro:



| Anotações de modificador de valor de parâmetro | Descrição                                    |
|--------------------------------------|------------------------------------------------|
| [SasNormalize](#sasnormalize)        | Especifique se um vetor é normalizado ou não. |
| [SasUnits](#sasunits)                | Especifique as unidades de medida para um parâmetro.  |



 

### <a name="sasnormalize"></a>SasNormalize

A anotação SasNormalize denota que o parâmetro associado deve ser um valor normalizado sempre que é atribuído. Esta anotação afeta apenas os parâmetros float2, float3 e FLOAT4.


```
string SasNormalize = "Value";
```



em que o valor é true ou false.

Veja um exemplo:


```
float3 UpNormal
<
  bool SasNormalize = "True";
>;
```



### <a name="sasunits"></a>SasUnits

Os dados do parâmetro de efeito estão nas seguintes unidades:


```
string SasUnits = "Value";
```



em que value é um dos seguintes:



| Tipo de Medida     | Valor        | Descrição                    |
|----------------------|--------------|--------------------------------|
| Nenhuma unidade             | cadeia de caracteres vazia | Nenhuma unidade                       |
| Distância             | MM           | Milímetros                    |
|                      | cm           | Centímetros                    |
|                      | m            | Medidores                         |
|                      | km           | quilômetros                     |
| Ângulo                | rad          | Radians                        |
| Tempo                 | ms           | Milissegundos                   |
|                      | seção          | Segundos                        |
|                      | min          | minutos                        |
|                      | h           | Horas                          |
| Velocidade linear      | mm/s       | Milímetros por segundo         |
|                      | cm/s       | Centímetros por segundo         |
|                      | m/s        | Metros por segundo              |
|                      | m/hr         | Metros por hora                |
|                      | km/hora        | Quilômetros por hora            |
| Aceleração linear  | mm/s ²      | Milímetros por segundo ao quadrado |
|                      | cm/s ²      | Centímetros por segundo ao quadrado |
|                      | m/s ²       | Metros por segundo ao quadrado      |
|                      | m/hr ²        | Medidores por hora ao quadrado        |
|                      | km/hr ²       | Quilômetros por hora ao quadrado    |
| Angular Velocidade     | Rad/s      | Radianos por segundo             |
| Angular Aceleração | Rad/s ²     | Radianos por segundo ao quadrado     |
| Área                 | mm;          | Milímetros quadrados            |
|                      | cm;          | Centímetros quadrados            |
|                      | M ²           | Metros quadrados                 |
|                      | Km ²          | Quilômetros quadrados             |
| Volume               | mm;          | Milímetros em cubo              |
|                      | Cm ³          | Centímetros em cubos              |
|                      | M ³           | Medidores em cubos                   |
|                      | km;          | Quilômetros em cubos               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de semântica e anotações padrão do DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



