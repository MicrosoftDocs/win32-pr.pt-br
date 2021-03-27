---
title: Modelo de sombreador HLSL 5
description: Modelo de sombreador HLSL 5
ms.assetid: 072c1ff2-ca1b-427c-9969-aa24ebb4ee38
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b33b0e2f009b796eb0b8828cc195fb9543ba2b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823835"
---
# <a name="hlsl-shader-model-5"></a>Modelo de sombreador HLSL 5

Esta seção contém material de visão geral para a linguagem High-Level Shader, especificamente os novos recursos no Shader Model 5 introduzidos no Microsoft Direct3D 11.

## <a name="in-this-section"></a>Nesta seção



| Item                                                                                                                                                                                                               | Descrição                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Vinculação dinâmica](overviews-direct3d-11-hlsl-dynamic-linking.md)<br/>                                 | A vinculação dinâmica permite que o tempo de execução tome uma decisão no tempo de empate (em vez de em tempo de compilação) sobre qual caminho de código deve ser executado. Isso reduz o problema de proliferação de sombreador causado por sombreadores com assinaturas de entrada quase idênticas.<br/>                                                                                                                         |
| <span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Recursos do sombreador de geometria](overviews-direct3d-11-hlsl-gs-features.md)<br/> | Novos recursos de sombreador de geometria, incluindo: instanciação, que fornece um aumento de desempenho quando a ordem de primitivos no fluxo não importa, e fluxos de saída de vários pontos, para que um sombreador possa gerar vértices em mais de um fluxo.<br/>                                                                                                                |
| <span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Mosaico](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)<br/>                                        | O tempo de execução do Direct3D 11 dá suporte a três novos estágios que implementam mosaico, que converte as superfícies de subdivisão de detalhe baixo em primitivos de detalhes mais altos na GPU. O bloco de mosaico organiza (ou decompõe) as superfícies de ordem superior em estruturas adequadas para renderização. Os três estágios de mosaico são envoltória-Shader, Tessellator e estágios de sombreador de domínio.<br/> |



 

Além disso, a seção de referência aborda muitos novos elementos de API para o modelo de sombreador 5, incluindo: [atributos](d3d11-graphics-reference-sm5-attributes.md), [funções intrínsecas](d3d11-graphics-reference-sm5-intrinsics.md), [objetos e métodos do sombreador 5 e](d3d11-graphics-reference-sm5-objects.md) [valores do sistema](d3d11-graphics-reference-sm5-system-values.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

