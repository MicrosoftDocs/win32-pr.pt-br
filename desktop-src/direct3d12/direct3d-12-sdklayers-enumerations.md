---
title: Enumerações da camada de depuração
description: As enumerações a seguir são declaradas em d3d12sdklayers. h.
ms.assetid: 6E76C857-128E-4F0E-9711-72C4CF6C835C
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746c0def35c8eb282264cb4ab0b40eb5c08f0f9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105748106"
---
# <a name="debug-layer-enumerations"></a>Enumerações da camada de depuração

As enumerações a seguir são declaradas em d3d12sdklayers. h.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Tipo de \_ parâmetro de lista de comandos de depuração D3D12 \_ \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_command_list_parameter_type)<br/>                                 | Indica o tipo de parâmetro de depuração usado por [**ID3D12DebugCommandList1:: SetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-setdebugparameter) e [**ID3D12DebugCommandList1:: GetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-getdebugparameter).<br/>                                                                                                                                                                                                      |
| [**\_Tipo de \_ parâmetro de dispositivo de depuração D3D12 \_ \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_device_parameter_type)<br/>                                              | Especifica o tipo de dados da memória apontada pelo parâmetro *pData* de [**ID3D12DebugDevice1:: SetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter) e [**ID3D12DebugDevice1:: GetDebugParameter**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-getdebugparameter).<br/>                                                                                                                                                                                        |
| [**\_Recurso de depuração D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_feature)<br/>                                                                            | Sinalizadores para recursos opcionais da camada de depuração D3D12.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**\_Sinalizadores de \_ validação baseados em GPU \_ D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_flags)<br/>                                                | Descreve o nível de validação baseada em GPU a ser executada no tempo de execução.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**\_Sinalizadores de \_ \_ criação de \_ estado do pipeline de validação baseada \_ \_ em \_ GPU D3D12**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_pipeline_state_create_flags)<br/> | Especifica como a validação de GPU-Based trata os Estados de pipeline corrigidos durante [**ID3D12Device:: CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) e [**ID3D12Device:: CreateComputePipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate).<br/>                                                                                                                                                                             |
| [**\_Modo de \_ \_ patch do \_ sombreador de validação baseado \_ em GPU D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode)<br/>                      | Especifica o tipo de aplicação de patch de sombreador usado pela validação de GPU-Based no nível do dispositivo ou da lista de comandos.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**\_Categoria de mensagem D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_category)<br/>                                                                      | Especifica categorias de mensagens de depuração. Isso identificará a categoria de uma mensagem ao recuperar uma mensagem com [**ID3D12InfoQueue:: GetMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage) e ao adicionar uma mensagem com [**ID3D12InfoQueue:: AddMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage). Ao criar um filtro de fila de informações, esses valores podem ser usados para permitir ou negar quaisquer categorias de mensagens a serem passadas pelos filtros de armazenamento e recuperação. <br/> |
| [**\_ID da mensagem D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_id)<br/>                                                                                  | Especifica as IDs de mensagem de depuração para configurar um filtro de fila de informações (consulte [**D3D12 \_ info \_ Queue \_ Filter**](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter)); Use essas mensagens para permitir ou negar as categorias de mensagens a serem passadas pelos filtros de armazenamento e recuperação. Essas IDs são usadas por métodos como [**ID3D12InfoQueue:: GetMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-getmessage) ou [**ID3D12InfoQueue:: AddMessage**](/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12infoqueue-addmessage). <br/>                        |
| [**\_Severidade da mensagem D3D12 \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_message_severity)<br/>                                                                      | Depurar níveis de severidade de mensagem para uma fila de informações.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| [**\_Sinalizadores D3D12 RLDO \_**](/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_rldo_flags)<br/>                                                                                  | Especifica as opções para a quantidade de informações a serem relatadas sobre o tempo de vida de um objeto de dispositivo ativo. <br/>                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configuração do ambiente programação do Direct3D 12](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Referência da camada de depuração](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Referência do Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 





