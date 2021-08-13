---
title: Estruturas de sombreador (elementos gráficos direct3D 11)
description: Estruturas são usadas para criar e usar sombreadores.
ms.assetid: 3b8ece5c-5065-4711-b12c-06cf7ea0e1ba
keywords:
- estruturas, sombreadores direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f5f5c346e4f46b1ca108200a88ae8b2ad3540585fd1a4bfc73b1dafe2b2b16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408186"
---
# <a name="shader-structures-direct3d-11-graphics"></a>Estruturas de sombreador (elementos gráficos direct3D 11)

Estruturas são usadas para criar e usar sombreadores.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                       | Descrição                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**DESC DA INSTÂNCIA \_ DE \_ CLASSE D3D11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_class_instance_desc)<br/>                | Descreve uma instância de classe HLSL.<br/>                           |
| [**D3D11 \_ DESC DE \_ RASTREAMENTO DO SOMBREADOR DE \_ \_ COMPUTAÇÃO**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_compute_shader_trace_desc)<br/>   | Descreve uma instância de um sombreador de computação a ser rastreada.<br/>         |
| [**D3D11 \_ \_ DESC DE RASTREAMENTO DO SOMBREADOR \_ \_ DE DOMÍNIO**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_domain_shader_trace_desc)<br/>     | Descreve uma instância de um sombreador de domínio a ser rastreado.<br/>          |
| [**D3D11 \_ FUNCTION \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_function_desc)<br/>                             | Descreve uma função.<br/>                                       |
| [**D3D11 \_ DESC DE \_ RASTREAMENTO DO SOMBREADOR \_ \_ GEOMETRY**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_geometry_shader_trace_desc)<br/> | Descreve uma instância de um sombreador de geometria a ser rastreada.<br/>        |
| [**D3D11 \_ DESC DE RASTREAMENTO \_ DO \_ SOMBREADOR DE CHASSI \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_hull_shader_trace_desc)<br/>         | Descreve uma instância de um sombreador de chassi a ser rastreado.<br/>            |
| [**D3D11 \_ LIBRARY \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_library_desc)<br/>                               | Descreve uma biblioteca.<br/>                                        |
| [**DESC DE PARÂMETRO D3D11 \_ \_**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_parameter_desc)<br/>                           | Descreve um parâmetro de função. <br/>                            |
| [**DESC DE RASTREAMENTO DO \_ \_ SOMBREADOR \_ \_ DE PIXEL D3D11**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_pixel_shader_trace_desc)<br/>       | Descreve uma instância de um sombreador de pixel a ser rastreado.<br/>           |
| [**DESC DO BUFFER DO \_ \_ SOMBREADOR D3D11 \_**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_buffer_desc)<br/>                  | Descreve um buffer constante do sombreador.<br/>                         |
| [**DESC DO SOMBREADOR D3D11 \_ \_**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_desc)<br/>                                 | Descreve um sombreador.<br/>                                         |
| [**D3D11 \_ DESC \_ DE BIND DE BIND \_ DO \_ SOMBREADOR**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_input_bind_desc)<br/>         | Descreve como um recurso de sombreador é vinculado a uma entrada de sombreador.<br/> |
| [**DESC DE RASTREAMENTO DO SOMBREADOR D3D11 \_ \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_shader_trace_desc)<br/>                    | Descreve um objeto de rastreamento de sombreador.<br/>                            |
| [**DESC DO TIPO DE SOMBREADOR D3D11 \_ \_ \_**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_type_desc)<br/>                      | Descreve um tipo de variável de sombreador.<br/>                           |
| [**DESC DA VARIÁVEL \_ DE SOMBREADOR D3D11 \_ \_**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_variable_desc)<br/>              | Descreve uma variável de sombreador.<br/>                                |
| [**D3D11 \_ \_ DESC DE PARÂMETRO DE \_ ASSINATURA**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)<br/>      | Descreve uma assinatura de sombreador.<br/>                               |
| [**REGISTRO DE RASTREAMENTO D3D11 \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_register)<br/>                           | Descreve um registro de rastreamento.<br/>                                 |
| [**ESTATÍSTICAS DE RASTREAMENTO D3D11 \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_stats)<br/>                                 | Especifica estatísticas sobre um rastreamento.<br/>                         |
| [**ETAPA DE RASTREAMENTO D3D11 \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_step)<br/>                                   | Descreve uma etapa de rastreamento, que é uma instrução.<br/>            |
| [**VALOR DE RASTREAMENTO D3D11 \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_value)<br/>                                 | Descreve um valor de rastreamento.<br/>                                    |
| [**D3D11 DESC DE RASTREAMENTO DO \_ \_ SOMBREADOR \_ DE \_ VÉRTICE**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_vertex_shader_trace_desc)<br/>     | Descreve uma instância de um sombreador de vértice a ser rastreada.<br/>          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do sombreador](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

 





