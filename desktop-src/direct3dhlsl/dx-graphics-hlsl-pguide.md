---
title: Guia de programação para HLSL
description: Os dados entram no pipeline gráfico como um fluxo de primitivos e são processados pelos estágios do sombreador.
ms.assetid: 4894e085-30e7-4cc5-8ae6-a84b601e4ce3
ms.topic: article
ms.date: 02/21/2019
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca0b1f93b3c5f56cd7a074571ec6657cedc924688606e3612a66ef0f9e40d51e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726065"
---
# <a name="programming-guide-for-hlsl"></a>Guia de programação para HLSL

Os dados entram no pipeline gráfico como um fluxo de primitivos e são processados pelos estágios do sombreador. Os estágios reais do sombreador dependem da versão do Direct3D, mas certamente incluem os estágios de vértice, pixel e geometria. Outros estágios incluem o chassi e sombreadores de domínio para mosaico e o sombreador de computação. Esses estágios são completamente programáveis usando a[HLSL (Linguagem](dx-graphics-hlsl-reference.md)de Sombreamento de Alto Nível).

Os sombreadores HLSL podem ser compilados em tempo de autor ou em runtime e definidos em runtime no estágio de pipeline apropriado. Os sombreadores direct3D 9 podem ser projetados usando o modelo de sombreador [1,](dx-graphics-hlsl-sm1.md)o modelo de sombreador [2](dx-graphics-hlsl-sm2.md) e o modelo [de sombreador 3](dx-graphics-hlsl-sm3.md); Os sombreadores do Direct3D 10 só podem ser projetados no [modelo de sombreador 4.](dx-graphics-hlsl-sm4.md) Os sombreadores do Direct3D 11 podem ser projetados no [modelo de sombreador 5.](d3d11-graphics-reference-sm5.md) O Direct3D 11.3 e o Direct3D 12 podem ser projetados no modelo de sombreador [5.1](shader-model-5-1.md)e o Direct3D 12 também pode ser projetado no modelo de sombreador [6.](shader-model-6-0.md)

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [Usando a vinculação do sombreador](using-shader-linking.md) | Mostramos como criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de executar. |
| [Escrevendo sombreadores HLSL no Direct3D 9](dx-graphics-hlsl-writing-shaders-9.md) | |
| [Usando sombreadores no Direct3D 9](dx-graphics-hlsl-using-shaders-9.md) | |
| [Usando sombreadores no Direct3D 10](dx-graphics-hlsl-using-shaders-10.md) | |
| [Otimizando sombreadores HLSL](dx-graphics-hlsl-optimize.md) | |
| [Depurando sombreadores no Visual Studio](dx-graphics-hlsl-debug-visual-studio.md) | A ferramenta mais recente para depurar sombreadores agora é Microsoft Visual Studio, chamada Visual Studio Depurador de Gráficos.  |
| [Compilar um sombreador](dx-graphics-hlsl-part1.md) | Agora, vamos ver várias maneiras de compilar seu código de sombreador e convenções para extensões de arquivo para código de sombreador. |
| [Especificando destinos do compilador](specifying-compiler-targets.md) | Aqui, listamos os destinos para vários perfis que as funções **D3DCompile \*** e o compilador HLSL suportam. |
| [Desempacotar e empacotar formato DXGI \_ para In-Place edição de imagem](dx-graphics-hlsl-unpacking-packing-dxgi-format.md) | |
| [Usando precisão mínima de HLSL](using-hlsl-minimum-precision.md) | Começando com Windows 8, os drivers gráficos podem implementar tipos de dados escalares [HLSL](dx-graphics-hlsl-scalar.md) de precisão mínima usando qualquer precisão maior ou igual à precisão de bit especificada.  |
| [Modelo 5 do sombreador HLSL](overviews-direct3d-11-hlsl.md) | |
| [Modelo 5.1 do sombreador HLSL](hlsl-shader-model-5-1-features-for-direct3d-12.md) | Esta seção descreve os recursos do Modelo de Sombreador 5.1, pois eles se aplicam na prática a D3D12 e D3D11.3. Todo o hardware do DirectX 12 dá suporte ao Modelo de Sombreador 5.1. |
| [Modelo 6.0 do Sombreador HLSL](hlsl-shader-model-6-0-features-for-direct3d-12.md) | Descreve os intrínsecos de operação de onda adicionados ao Modelo de Sombreador HLSL 6.0. |
| [Modelo 6.4 do sombreador HLSL](hlsl-shader-model-6-4-features-for-direct3d-12.md) | Descreve os intrínsecos de aprendizado de máquina adicionados ao Modelo de Sombreador HLSL 6.4. |

## <a name="related-topics"></a>Tópicos relacionados

* [Hlsl](dx-graphics-hlsl.md)
* [Referência para HLSL](dx-graphics-hlsl-reference.md)
