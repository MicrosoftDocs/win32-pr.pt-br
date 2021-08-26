---
title: Modelo 5 do sombreador HLSL
description: Modelo 5 do sombreador HLSL
ms.assetid: 072c1ff2-ca1b-427c-9969-aa24ebb4ee38
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 537b2460b73f30397561dea37bcb3711b64a935c43d45662428585a47d6f6574
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095346"
---
# <a name="hlsl-shader-model-5"></a>Modelo 5 do sombreador HLSL

Esta seção contém o material de visão geral para a linguagem High-Level sombreador, especificamente os novos recursos no modelo de sombreador 5 introduzidos no Microsoft Direct3D 11.

## <a name="in-this-section"></a>Nesta seção



| Item                                                                                                                                                                                                               | Descrição                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Vinculação dinâmica](overviews-direct3d-11-hlsl-dynamic-linking.md)<br/>                                 | A vinculação dinâmica permite que o runtime faça uma decisão em tempo de desenho (em vez de em tempo de compilação) sobre qual caminho de código deve ser executado. Isso reduz o problema de proliferação do sombreador causado por sombreadores com assinaturas de entrada quase idênticas.<br/>                                                                                                                         |
| <span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Recursos de sombreador de geometria](overviews-direct3d-11-hlsl-gs-features.md)<br/> | Novos recursos de sombreador de geometria, incluindo: instanciamento, que fornece um aumento de desempenho quando a ordem dos primitivos no fluxo não importa e fluxos de saída de vários pontos para que um sombreador possa saída de vértices em mais de um fluxo.<br/>                                                                                                                |
| <span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Mosaico](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)<br/>                                        | O runtime do Direct3D 11 dá suporte a três novos estágios que implementam o mosaico, que converte superfícies de subdivisão de baixo detalhe em primitivos de detalhes mais altos na GPU. O bloco de mosaico organiza (ou decompõe) as superfícies de ordem superior em estruturas adequadas para renderização. Os três estágios de mosaico são estágios de sombreador de chassi, mosaico e sombreador de domínio.<br/> |



 

Além disso, a seção de referência aborda muitos novos elementos de API para o modelo de sombreador 5, [incluindo:](d3d11-graphics-reference-sm5-attributes.md)atributos [,](d3d11-graphics-reference-sm5-intrinsics.md)funções intrínsecas , objetos e métodos do modelo de [sombreador 5](d3d11-graphics-reference-sm5-objects.md)e valores [do sistema](d3d11-graphics-reference-sm5-system-values.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

