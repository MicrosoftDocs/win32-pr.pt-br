---
title: Estruturas de sombreador (gráficos do Direct3D 11)
description: As estruturas são usadas para criar e usar sombreadores.
ms.assetid: 3b8ece5c-5065-4711-b12c-06cf7ea0e1ba
keywords:
- estruturas, sombreadores do Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14739e3db38c075e19e58a90b12bbf7d06b48a4e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644172"
---
# <a name="shader-structures-direct3d-11-graphics"></a>Estruturas de sombreador (gráficos do Direct3D 11)

As estruturas são usadas para criar e usar sombreadores.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                       | Descrição                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**\_Desc de \_ instância de classe D3D11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_class_instance_desc)<br/>                | Descreve uma instância de classe HLSL.<br/>                           |
| [**\_Desc de \_ rastreamento de sombreador de computação D3D11 \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_compute_shader_trace_desc)<br/>   | Descreve uma instância de um sombreador de computação a ser rastreado.<br/>         |
| [**\_Desc de \_ rastreamento de sombreador de domínio D3D11 \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_domain_shader_trace_desc)<br/>     | Descreve uma instância de um sombreador de domínio para rastrear.<br/>          |
| [**\_Função D3D11 \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_function_desc)<br/>                             | Descreve uma função.<br/>                                       |
| [**\_Desc de \_ rastreamento de sombreador de geometria D3D11 \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_geometry_shader_trace_desc)<br/> | Descreve uma instância de um sombreador Geometry a ser rastreado.<br/>        |
| [**Desc. de \_ \_ rastreamento de sombreador D3D11 envoltória \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_hull_shader_trace_desc)<br/>         | Descreve uma instância de um sombreador envoltória para rastrear.<br/>            |
| [**\_Desc de biblioteca D3D11 \_**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_library_desc)<br/>                               | Descreve uma biblioteca do.<br/>                                        |
| [**D3D11 do \_ parâmetro \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_parameter_desc)<br/>                           | Descreve um parâmetro de função. <br/>                            |
| [**\_Desc de \_ rastreamento de sombreador de pixel D3D11 \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_pixel_shader_trace_desc)<br/>       | Descreve uma instância de um sombreador de pixel para rastreamento.<br/>           |
| [**\_Desc buffer de sombreador D3D11 \_ \_**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_buffer_desc)<br/>                  | Descreve um buffer de constante de sombreador.<br/>                         |
| [**D3D11 de \_ sombreador \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_desc)<br/>                                 | Descreve um sombreador.<br/>                                         |
| [**\_Desc de \_ entrada de SOMBREAdor D3D11 \_ \_**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_input_bind_desc)<br/>         | Descreve como um recurso de sombreador está associado a uma entrada de sombreador.<br/> |
| [**\_Desc de rastreamento do sombreador D3D11 \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_shader_trace_desc)<br/>                    | Descreve um objeto de rastreamento de sombreador.<br/>                            |
| [**D3D11 \_ sombreador \_ tipo \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_type_desc)<br/>                      | Descreve um tipo de variável de sombreador.<br/>                           |
| [**\_Variável de sombreador D3D11 \_ \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_variable_desc)<br/>              | Descreve uma variável de sombreador.<br/>                                |
| [**D3D11 \_ de \_ parâmetro de assinatura \_ desc**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)<br/>      | Descreve uma assinatura de sombreador.<br/>                               |
| [**\_Registro de rastreamento do D3D11 \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_register)<br/>                           | Descreve um registro de rastreamento.<br/>                                 |
| [**\_Estatísticas de rastreamento do D3D11 \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_stats)<br/>                                 | Especifica estatísticas sobre um rastreamento.<br/>                         |
| [**\_Etapa de rastreamento de D3D11 \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_step)<br/>                                   | Descreve uma etapa de rastreamento, que é uma instrução.<br/>            |
| [**\_Valor de rastreamento de D3D11 \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_value)<br/>                                 | Descreve um valor de rastreamento.<br/>                                    |
| [**\_Desc de \_ rastreamento de sombreador de vértice D3D11 \_ \_**](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_vertex_shader_trace_desc)<br/>     | Descreve uma instância de um sombreador de vértice a ser rastreado.<br/>          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do sombreador](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

 





