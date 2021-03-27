---
title: Enumerações de recursos (gráficos do Direct3D 11)
description: As enumerações são usadas para especificar informações sobre como os recursos são criados e acessados durante a renderização.
ms.assetid: b547819b-7006-40b5-84a4-adf198048051
keywords:
- enumerações, recurso do Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6124fcbc93cb0069152dd20d3b4b3bf0f4be60d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104967250"
---
# <a name="resource-enumerations-direct3d-11-graphics"></a>Enumerações de recursos (gráficos do Direct3D 11)

As enumerações são usadas para especificar informações sobre como os recursos são criados e acessados durante a renderização.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                               | Descrição                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Sinalizador de associação de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)<br/>                                                             | Identifica como associar um recurso ao pipeline.<br/>                                                                                                                                 |
| [**\_ \_ Sinalizador SRV D3D11 \_ BUFFEREX**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bufferex_srv_flag)<br/>                                            | Identifica como exibir um recurso de buffer.<br/>                                                                                                                                          |
| [**\_Sinalizador de \_ UAV do buffer D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_buffer_uav_flag)<br/>                                                | Identifica as opções de exibição de acesso não ordenado para um recurso de buffer.<br/>                                                                                                                    |
| [**Sinalizador de D3D11 \_ verificar níveis de qualidade de \_ multiamostra \_ \_ \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag)<br/> | Identifica como verificar os níveis de qualidade de multiamostras.<br/>                                                                                                                                |
| [**\_Sinalizador de \_ acesso de CPU D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)<br/>                                                | Especifica os tipos de acesso de CPU permitidos para um recurso.<br/>                                                                                                                          |
| [**\_Dimensão DSV \_ D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_dimension)<br/>                                                     | Especifica como acessar um recurso usado em uma exibição de estêncil de profundidade.<br/>                                                                                                                   |
| [**\_Sinalizador DSV de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_flag)<br/>                                                               | Opções de exibição de estêncil de profundidade.<br/>                                                                                                                                                        |
| [**\_Mapa D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)<br/>                                                                          | Identifica um recurso a ser acessado para leitura e gravação pela CPU. Os aplicativos podem combinar um ou mais desses sinalizadores.<br/>                                                      |
| [**\_Sinalizador de mapa de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map_flag)<br/>                                                               | Especifica como a CPU deve responder quando um aplicativo chama o método [**ID3D11DeviceContext:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) em um recurso que está sendo usado pela GPU.<br/> |
| [**\_Dimensão de recurso D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)<br/>                                           | Identifica o tipo de recurso que está sendo usado.<br/>                                                                                                                                        |
| [**\_ \_ Sinalizador diverso de recurso D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)<br/>                                          | Identifica opções para recursos.<br/>                                                                                                                                                  |
| [**\_Dimensão D3D11 RTV \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_rtv_dimension)<br/>                                                     | Esses sinalizadores identificam o tipo de recurso que será exibido como um destino de renderização.<br/>                                                                                                  |
| [**\_Dimensão SRV do D3D11 \_**](/previous-versions/windows/desktop/legacy/ff476217(v=vs.85))<br/>                                                     | Esses sinalizadores identificam o tipo de recurso que será exibido como um recurso de sombreador.<br/>                                                                                                |
| [**D3D11 \_ \_ níveis de qualidade multiamostrais padrão \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_standard_multisample_quality_levels)<br/>       | Especifica um tipo de padrão de várias amostras.<br/>                                                                                                                                             |
| [**\_Layout de textura D3D11 \_**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout)<br/>                                                   | Especifica opções de layout de textura.<br/>                                                                                                                                                  |
| [**\_Sinalizador de \_ cópia do bloco D3D11 \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag)<br/>                                                 | Identifica como copiar um bloco.<br/>                                                                                                                                                     |
| [**\_Sinalizador de \_ mapeamento de bloco D3D11 \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_mapping_flag)<br/>                                           | Identifica como executar uma operação de mapeamento de bloco.<br/>                                                                                                                                |
| [**\_Sinalizador de \_ intervalo de blocos do D3D11 \_**](/windows/desktop/api/d3d11_2/ne-d3d11_2-d3d11_tile_range_flag)<br/>                                                | Especifica um intervalo de mapeamentos de bloco a ser usado com [**ID3D11DeviceContext2:: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles).<br/>                                                      |
| [**\_Dimensão D3D11 UAV \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_uav_dimension)<br/>                                                     | Opções de exibição de acesso não ordenado.<br/>                                                                                                                                                     |
| [**Uso de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)<br/>                                                                      | Identifica o uso de recursos esperado durante a renderização. O uso reflete diretamente se um recurso pode ser acessado pela CPU e/ou pela GPU (unidade de processamento gráfico).<br/>              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de recurso](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

