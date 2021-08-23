---
title: Modelo de sombreador 5
description: Esta seção contém as páginas de referência para o HLSL Shader Model 5.
ms.assetid: ec646940-8901-45c5-a44c-434c8acae2aa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a252c8ad3cc12c443506fbcc3802d9f1f7c15cfbe8cc62d937fcb9ca8723a8da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119371456"
---
# <a name="shader-model-5"></a>Modelo de sombreador 5

Esta seção contém as páginas de referência para o HLSL Shader Model 5.

O Shader Model 5 é um superconjunto dos recursos no [Shader Model 4](dx-graphics-hlsl-sm4.md). Ele foi projetado usando um núcleo de sombreador comum que fornece um conjunto comum de recursos para todos os sombreadores programáveis, que só podem ser programados usando HLSL.



| Recurso                   | Funcionalidade                                                                                                                                             |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Conjunto de instruções           | [**Funções intrínsecas HLSL**](dx-graphics-hlsl-intrinsic-functions.md)                                                                               |
| Sombreador máximo do vértice         | Nenhuma restrição                                                                                                                                         |
| Sombreador máximo de pixel          | Nenhuma restrição                                                                                                                                         |
| Novos perfis de sombreador adicionados | cs \_ 4 \_ 0, GS \_ 4 \_ 0 \* , PS \_ 4 \_ 0 \* , vs \_ 4 \_ 0 \* , cs \_ 4 \_ 1, GS \_ 4 \_ 1 \* , PS \_ 4 \_ 1 \* , vs \_ 4 \_ 1 \* , cs \_ 5 0, DS 5 0, GS 5 0, HS 5 0, \_ \_ \_ \_ \_ \_ \_ PS \_ 5 \_ 0, vs \_ 5 \_ 0 |



 

\* -GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 e vs \_ 4 \_ 1 foram introduzidos no modelo do sombreador 4,0, no entanto, o DirectX 11 adiciona suporte para [buffers estruturados](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) e buffers de endereço de bytes para o modelo do sombreador 4 em execução no hardware do DirectX 10.

O Shader Model 5 apresenta o [sombreador de computação](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) que fornece computação de uso geral de alta velocidade.

Uma lista mais completa dos recursos do Shader Model 5 está incluída na listagem dos [recursos do Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features).

A seção de [assembly do Shader Model 5](shader-model-5-assembly--directx-hlsl-.md) descreve as instruções do assembly com suporte no modelo do sombreador 5.

## <a name="in-this-section"></a>Nesta seção



| Item                                                                                                                                                                                                                                                        | Descrição                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Atributos do Shader Model 5](d3d11-graphics-reference-sm5-attributes.md)<br/>                                     | Páginas de referência para atributos do Shader Model 5.<br/>          |
| <span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Funções intrínsecas do modelo de sombreador 5](d3d11-graphics-reference-sm5-intrinsics.md)<br/> | Páginas de referência para funções intrínsecas do modelo de sombreador 5.<br/> |
| <span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Objetos do Shader Model 5](d3d11-graphics-reference-sm5-objects.md)<br/>                                                    | Páginas de referência para objetos e métodos do Shader Model 5.<br/> |
| <span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Valores de sistema do Shader Model 5](d3d11-graphics-reference-sm5-system-values.md)<br/>                      | Páginas de referência para valores de sistema do Shader Model 5.<br/>       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelos de sombreador vs. perfis de sombreador](dx-graphics-hlsl-models.md)
</dt> </dl>

 

