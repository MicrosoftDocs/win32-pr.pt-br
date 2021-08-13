---
title: Registros de saída
description: Registros de saída
ms.assetid: 44148185-1051-44b9-afde-a2ecd76c829f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3cfa17c09315f4cdca98f5c5fc10f7ab15541eb8b774835963b06169c4afe225
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457766"
---
# <a name="output-registers"></a>Registros de saída

-   Registro de cor do vértice
-   Registro de neblina
-   Registro de posição \_
-   \_Registro de tamanho do ponto \_
-   \_Registro de coordenadas de textura \_

Os nomes de registro são precedidos por uma letra minúscula o, indicando que os registros de saída são somente gravação.

## <a name="vertex-color-register---od0-od1"></a>Registro de cor do vértice-oD0, oD1

oD0 é o registro de cores difusas. oD1 é o registro de cor especular. O valor de oD0 é interpolado e gravado no registro de cor de entrada 0 (V0) do sombreador de pixel. O valor de oD1 é interpolado e gravado no registro de cor de entrada 1 (v1) do sombreador de pixel. Para obter mais informações sobre registros de cores do sombreador de pixel, consulte registros.



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro de cor do vértice  | x    | x    | x     | x    |      |       |



 

## <a name="fog-register---ofog"></a>Registro de neblina-oFog

O valor de neblina de saída é registrado. O valor é o fator de neblina a ser interpolado e, em seguida, roteado para a tabela de neblina. Somente o componente x escalar da neblina é usado. Os valores são clamped entre zero e um antes de passar para o rasterizador.



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro de neblina           | x    | x    | x     | x    |      |       |



 

## <a name="position-register---opos"></a>Registro de posição – oPos

A posição de saída registra. O valor é a posição no espaço de recorte homogêneo. Esse valor deve ser gravado pelo sombreador de vértice.



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro de posição      | x    | x    | x     | x    |      |       |



 

## <a name="point-size-register---opts"></a>Registro de tamanho de ponto – opta

O tamanho do ponto de saída é registrado. Somente o componente x escalar do tamanho do ponto é usado.



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro de tamanho do ponto    | x    | x    | x     | x    |      |       |



 

## <a name="texture-coordinate-register---ot0-to-ot7"></a>Registro de coordenadas de textura-oT0 para oT7

As coordenadas de textura de saída são registradas. Especificamente, essas são uma matriz de registros de dados de saída que são iterados e usados como coordenadas de textura pelos estágios de amostragem de texturas que encaminham dados para o sombreador de pixel.



| Versões do sombreador de vértice      | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------------|------|------|-------|------|------|-------|
| Registro de coordenadas de textura | x    | x    | x     | x    |      |       |



 

Ao gravar em um registro de coordenadas de textura, é recomendável passar apenas o número de valores de ponto flutuante como a dimensão do mapa de textura correspondente. Controle os valores passados com um modificador. Por exemplo, use. XY para um mapa de textura 2D.

Quando a projeção de textura está habilitada para um estágio de textura, todos os quatro valores de ponto flutuante devem ser gravados no registro de textura correspondente.

Qualquer um dos \* sinalizadores de transformação de textura D3DTTFF deve ser zero quando o pipeline programável está sendo usado.

### <a name="texture-coordinate-range"></a>Intervalo de coordenadas de textura

Dados de vértice de objeto fornecem coordenadas de textura de entrada. Os objetos que não usavam texturas com ladrilhos normalmente têm coordenadas de textura no intervalo de \[ 0, 1 \] . Os objetos que usam texturas de lado, como o terreno, normalmente têm coordenadas de textura que variam de \[ -?, +? \] onde? pode ser um número de ponto flutuante grande.

A interpolação da coordenada de textura é executada em dados de vértice para rasterização. Durante a rasterização, as coordenadas de textura são interpoladas entre vértices de objeto, modificadas por quebra de textura e dimensionadas pelo tamanho da textura (também levando em conta o modo de endereço de textura) para produzir um índice inteiro. O índice é usado para executar uma análise de textura. MaxTextureRepeat pode ser usado para determinar quantas vezes uma textura pode ser lado a lado.

Se as coordenadas de textura são lidas diretamente em um sombreador de pixel (usando o texcoord ou o texcrd), o intervalo de coordenadas de textura depende da instrução e da versão do sombreador de pixel.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




