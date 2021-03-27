---
title: Registro de coordenadas de textura (referência de HLSL VS)
description: Este registro de saída do sombreador de vértice contém coordenadas de textura por vértice.
ms.assetid: d42c8e4c-8227-4fe8-9432-90c592011024
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad3937b8f0b3f7acd6313774f6de7cde133e69c5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084846"
---
# <a name="texture-coordinate-register-hlsl-vs-reference"></a>Registro de coordenadas de textura (referência de HLSL VS)

Este registro de saída do sombreador de vértice contém coordenadas de textura por vértice.

Um registro consiste em propriedades que determinam se o registro se comporta.



| Propriedade        | Descrição   |
|-----------------|---------------|
| Name            | oT0 - oT7     |
| Contagem           | Oito vetores |
| Permissões de e/s | Somente gravação    |



 

Os registros de coordenadas de textura de saída são uma matriz de registros de dados de saída. Os dados de registro são iterados e usados como coordenadas de textura pelos estágios de amostragem de textura para fornecer dados ao sombreador de pixel.

Ao gravar em um registro de coordenadas de textura, é recomendável que você passe apenas o número de valores de ponto flutuante como a dimensão do mapa de textura correspondente. Controle os valores que são passados com um modificador. Por exemplo, use. XY para um mapa de textura 2D.

Os sinalizadores de pipeline de vértice de função fixa, [**D3DTEXTURETRANSFORMFLAGS**](/windows/desktop/direct3d9/d3dtexturetransformflags) (D3DTTFF \_ COUNT1, D3DTTFF \_ COUNT2, D3DTTFF \_ COUNT3, D3DTTFF \_ COUNT4), devem ser definidos como zero se você estiver usando um sombreador de vértice programável.

Dados de vértice de objeto fornecem coordenadas de textura de entrada. Os objetos que não usam texturas com ladrilhos normalmente têm coordenadas de textura no intervalo de \[ 0, 1 \] . Os objetos que usam texturas de lado, como o terreno, normalmente têm coordenadas de textura que variam de \[ -n, + n, \] em que n pode ser qualquer número de ponto flutuante.

A interpolação de coordenadas de textura é executada em dados de vértice para rasterização. Durante a rasterização, as coordenadas de textura são interpoladas entre os vértices do objeto, modificadas pelo encapsulamento de textura e dimensionadas pelo tamanho da textura (também levando em conta os modos de endereçamento de textura) para produzir um índice de número inteiro. Em seguida, o índice é usado para executar uma pesquisa de textura. Use o valor MaxTextureRepeat em [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) para determinar o número de vezes que uma textura pode ser colocada ao lado.

## <a name="example"></a>Exemplo

Declare o registro de coordenadas de textura.


```
dcl_texcoord v7
```



Copie as coordenadas de textura por vértice para o registro de saída.


```
mov oT0, v7
```





| Versões do sombreador de vértice      | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------------|------|------|-------|------|------|-------|
| Registro de coordenadas de textura | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 