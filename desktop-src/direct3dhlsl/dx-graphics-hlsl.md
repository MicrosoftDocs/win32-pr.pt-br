---
title: HLSL (linguagem do sombreador de alto nível)
description: HLSL é a linguagem de sombreador de alto nível C como a que você usa com sombreadores programáveis no DirectX.
ms.assetid: 09cdd8d6-0cf5-4f7e-b480-f748d2fa9ca9
ms.topic: article
ms.date: 01/11/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.custom: contperf-fy21q3
ms.openlocfilehash: c0876cda302d4c6215b640c210e880795273cd6c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104968273"
---
# <a name="high-level-shader-language-hlsl"></a>HLSL (linguagem do sombreador de alto nível)

HLSL é a linguagem de sombreador de alto nível C como a que você usa com sombreadores programáveis no DirectX.

Por exemplo, você pode usar HLSL para escrever um [sombreador de vértice](../direct3d11/vertex-shader-stage.md)ou um [sombreador de pixel](../direct3d11/pixel-shader-stage.md)e usar esses sombreadores na implementação do renderizador em seu aplicativo [Direct3D](../direct3d12/directx-12-programming-guide.md) .

Ou você pode usar HLSL para escrever um sombreador de computação, talvez para implementar uma simulação física. No entanto, se, por exemplo, você estiver inclinado a escrever seu próprio operador de convolução (para o processamento de imagens) como HLSL em um sombreador de computação, você obterá um melhor desempenho nesse cenário se usar o [Direct Machine Learning (DirectML)](../direct3d12/dml.md) em vez disso.

O HLSL foi criado (começando com o DirectX 9) para configurar o [pipeline](../direct3d11/overviews-direct3d-11-graphics-pipeline.md)3D programável. Você pode programar todo o pipeline com instruções de HLSL.

## <a name="where-to-go-next"></a>Onde ir em seguida

* [Guia de programação para HLSL](./dx-graphics-hlsl-pguide.md)
* [Referência para HLSL](./dx-graphics-hlsl-reference.md)

### <a name="programming-guide-for-hlsl"></a>Guia de programação para HLSL

Para obter uma introdução conceitual ao HLSL, consulte o [Guia de programação para HLSL](./dx-graphics-hlsl-pguide.md).

O guia de programação aborda os diferentes tipos de estágios de sombreador e como criar, compilar, otimizar, associar e vincular sombreadores.

Lá você também encontrará visões gerais de, e notas de versão sobre, as gerações sucessivas da versão do modelo do sombreador que foram lançadas, voltando até o modelo de sombreador HLSL 5.

### <a name="reference-for-hlsl"></a>Referência para HLSL

Para obter a documentação de referência do HLSL, consulte a [referência para HLSL](./dx-graphics-hlsl-reference.md).

A seção de referência tem uma lista completa da sintaxe de linguagem e das funções intrínsecas criadas no HLSL para simplificar os requisitos de codificação.

Além disso, você encontrará uma discussão sobre os modelos de sombreador versus perfis, e o conteúdo de referência do modelo de sombreamento indo até o modelo de sombreador HLSL 1. Também há conteúdo abrangendo instruções de assembly, a ferramenta D3DCompiler e informações sobre os erros e avisos que um sombreador pode retornar.