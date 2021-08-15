---
title: Enumerações de recursos (elementos gráficos direct3D 11)
description: Enumerações são usadas para especificar informações sobre como os recursos são criados e acessados durante a renderização.
ms.assetid: b547819b-7006-40b5-84a4-adf198048051
keywords:
- enumerações, Recurso Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6965eabfdb66c5459da799830cba9e87312566910e0dea84d400cb39b39127e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126060"
---
# <a name="resource-enumerations-direct3d-11-graphics"></a>Enumerações de recursos (elementos gráficos direct3D 11)

Enumerações são usadas para especificar informações sobre como os recursos são criados e acessados durante a renderização.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                               | Descrição                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SINALIZADOR DE VINCULAÇÃO D3D11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)<br/>                                                             | Identifica como vincular um recurso ao pipeline.<br/>                                                                                                                                 |
| [**SINALIZADOR SRV D3D11 \_ BUFFEREX \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bufferex_srv_flag)<br/>                                            | Identifica como exibir um recurso de buffer.<br/>                                                                                                                                          |
| [**SINALIZADOR UAV DO BUFFER D3D11 \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_buffer_uav_flag)<br/>                                                | Identifica opções de exibição de acesso não organizado para um recurso de buffer.<br/>                                                                                                                    |
| [**D3D11 VERIFICAR SINALIZADOR DE NÍVEIS DE QUALIDADE \_ \_ MULTISAMPLE \_ \_ \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag)<br/> | Identifica como verificar níveis de qualidade de vários exemplos.<br/>                                                                                                                                |
| [**SINALIZADOR DE ACESSO À CPU D3D11 \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)<br/>                                                | Especifica os tipos de acesso à CPU permitidos para um recurso.<br/>                                                                                                                          |
| [**DIMENSÃO D3D11 \_ DSV \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_dimension)<br/>                                                     | Especifica como acessar um recurso usado em uma exibição de estêncil de profundidade.<br/>                                                                                                                   |
| [**SINALIZADOR D3D11 \_ DSV \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_flag)<br/>                                                               | Opções de exibição de estêncil de profundidade.<br/>                                                                                                                                                        |
| [**D3D11 \_ MAP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)<br/>                                                                          | Identifica um recurso a ser acessado para leitura e escrita pela CPU. Os aplicativos podem combinar um ou mais desses sinalizadores.<br/>                                                      |
| [**SINALIZADOR DE MAPA D3D11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map_flag)<br/>                                                               | Especifica como a CPU deve responder quando um aplicativo chama o método [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) em um recurso que está sendo usado pela GPU.<br/> |
| [**DIMENSÃO DE RECURSOS D3D11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)<br/>                                           | Identifica o tipo de recurso que está sendo usado.<br/>                                                                                                                                        |
| [**SINALIZADOR MISC DO RECURSO D3D11 \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)<br/>                                          | Identifica opções para recursos.<br/>                                                                                                                                                  |
| [**DIMENSÃO D3D11 \_ RTV \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_rtv_dimension)<br/>                                                     | Esses sinalizadores identificam o tipo de recurso que será exibido como um destino de renderização.<br/>                                                                                                  |
| [**DIMENSÃO SRV D3D11 \_ \_**](/previous-versions/windows/desktop/legacy/ff476217(v=vs.85))<br/>                                                     | Esses sinalizadores identificam o tipo de recurso que será exibido como um recurso de sombreador.<br/>                                                                                                |
| [**NÍVEIS DE QUALIDADE \_ \_ MULTISAMPLE PADRÃO \_ D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_standard_multisample_quality_levels)<br/>       | Especifica um tipo de padrão de várias amostras.<br/>                                                                                                                                             |
| [**LAYOUT DE TEXTURA D3D11 \_ \_**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout)<br/>                                                   | Especifica opções de layout de textura.<br/>                                                                                                                                                  |
| [**SINALIZADOR DE CÓPIA DE TILE D3D11 \_ \_ \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag)<br/>                                                 | Identifica como copiar umile.<br/>                                                                                                                                                     |
| [**SINALIZADOR DE MAPEAMENTO DE TILE D3D11 \_ \_ \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_mapping_flag)<br/>                                           | Identifica como executar uma operação de mapeamento deile.<br/>                                                                                                                                |
| [**SINALIZADOR DE INTERVALO DE TILE D3D11 \_ \_ \_**](/windows/desktop/api/d3d11_2/ne-d3d11_2-d3d11_tile_range_flag)<br/>                                                | Especifica um intervalo de mapeamentos de tile a ser usado com [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles).<br/>                                                      |
| [**DIMENSÃO UAV D3D11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_uav_dimension)<br/>                                                     | Opções de exibição de acesso não organizado.<br/>                                                                                                                                                     |
| [**USO DE D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)<br/>                                                                      | Identifica o uso esperado de recursos durante a renderização. O uso reflete diretamente se um recurso é acessível pela CPU e/ou pela GPU (unidade de processamento gráfico).<br/>              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de recursos](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

