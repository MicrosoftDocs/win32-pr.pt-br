---
title: Guia de programação para HLSL
description: Os dados entram no pipeline de gráficos como um fluxo de primitivos e são processados pelos estágios do sombreador.
ms.assetid: 4894e085-30e7-4cc5-8ae6-a84b601e4ce3
ms.topic: article
ms.date: 02/21/2019
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cd242efaaf3cdb44f424a603f2fc522dda540ec8
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/12/2021
ms.locfileid: "104968256"
---
# <a name="programming-guide-for-hlsl"></a>Guia de programação para HLSL

Os dados entram no pipeline de gráficos como um fluxo de primitivos e são processados pelos estágios do sombreador. Os estágios de sombreador reais dependem da versão do Direct3D, mas, certamente, incluem os estágios de vértice, pixel e Geometry. Outros estágios incluem o envoltória e os sombreadores de domínio para mosaico e o sombreador de computação. Esses estágios são totalmente programáveis usando a[HLSL](dx-graphics-hlsl-reference.md)(linguagem de sombreamento de alto nível).

Os sombreadores HLSL podem ser compilados em tempo de autor ou em tempo de execução e definidos no tempo de execução no estágio de pipeline apropriado. Os sombreadores do Direct3D 9 podem ser criados usando o [modelo do sombreador 1](dx-graphics-hlsl-sm1.md), o [modelo do sombreador 2](dx-graphics-hlsl-sm2.md) e o [modelo do sombreador 3](dx-graphics-hlsl-sm3.md); Os sombreadores do Direct3D 10 só podem ser criados no [modelo do sombreador 4](dx-graphics-hlsl-sm4.md). Os sombreadores do Direct3D 11 podem ser criados no [Shader Model 5](d3d11-graphics-reference-sm5.md). O Direct3D 11,3 e o Direct3D 12 podem ser criados no [Shader model 5,1](shader-model-5-1.md), e o Direct3D 12 também pode ser projetado no [Shader Model 6](shader-model-6-0.md).

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [Usando vinculação de sombreador](using-shader-linking.md) | Mostramos como criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução. |
| [Escrevendo sombreadores HLSL no Direct3D 9](dx-graphics-hlsl-writing-shaders-9.md) | |
| [Usando sombreadores no Direct3D 9](dx-graphics-hlsl-using-shaders-9.md) | |
| [Usando sombreadores no Direct3D 10](dx-graphics-hlsl-using-shaders-10.md) | |
| [Otimizando sombreadores HLSL](dx-graphics-hlsl-optimize.md) | |
| [Depurando sombreadores no Visual Studio](dx-graphics-hlsl-debug-visual-studio.md) | A ferramenta mais recente para depuração de sombreadores agora é fornecida como um recurso no Microsoft Visual Studio, chamado depurador de gráficos do Visual Studio.  |
| [Compilar um sombreador](dx-graphics-hlsl-part1.md) | Agora, vamos examinar várias maneiras de compilar o código do sombreador e as convenções de extensões de arquivo para o código do sombreador. |
| [Especificando destinos do compilador](specifying-compiler-targets.md) | Aqui, listamos os destinos de vários perfis que as funções **D3DCompile \** _ e o compilador HLSL suportam. |
| [Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place](dx-graphics-hlsl-unpacking-packing-dxgi-format.md) | |
| [Usando precisão mínima de HLSL](using-hlsl-minimum-precision.md) | A partir do Windows 8, os drivers gráficos podem implementar os [tipos de dados escalares HLSL](dx-graphics-hlsl-scalar.md) mínimos de precisão usando qualquer precisão maior ou igual à precisão de bit especificada.  |
| [Modelo de sombreador HLSL 5](overviews-direct3d-11-hlsl.md) | |
| [Modelo de sombreador HLSL 5,1](hlsl-shader-model-5-1-features-for-direct3d-12.md) | Esta seção descreve os recursos do Shader Model 5,1, pois eles se aplicam na prática ao D3D12 e ao D3D 11.3. Todos os hardwares do DirectX 12 dão suporte ao modelo de sombreador 5,1. |
| [Modelo de sombreador HLSL 6,0](hlsl-shader-model-6-0-features-for-direct3d-12.md) | Descreve os intrínsecores de operação de onda adicionados ao modelo de sombreador HLSL 6,0. |
| [Modelo de sombreador HLSL 6,4](hlsl-shader-model-6-4-features-for-direct3d-12.md) | Descreve os intrínsecos do Machine Learning adicionados ao modelo de sombreador HLSL 6,4. |

## <a name="related-topics"></a>Tópicos relacionados

_ [HLSL](dx-graphics-hlsl.md)
* [Referência para HLSL](dx-graphics-hlsl-reference.md)
