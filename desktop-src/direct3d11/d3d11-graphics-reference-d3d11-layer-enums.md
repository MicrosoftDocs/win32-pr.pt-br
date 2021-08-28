---
title: Enumerações de camada
description: Esta seção contém informações sobre as enumerações de camada.
ms.assetid: 0fd0456b-2638-4b4c-8a34-a3e104a1a034
keywords:
- enumerações, Camada Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af59a6ac6fae73cafdbee3f0d93d019d7a8ee0b472cd979e2ddcaeade387ef4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460886"
---
# <a name="layer-enumerations"></a>Enumerações de camada

Esta seção contém informações sobre as enumerações de camada.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CATEGORIA DE MENSAGEM D3D11 \_ \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_category)<br/>                             | Categorias de mensagens de depuração. Isso identificará a categoria de uma mensagem ao recuperar uma mensagem com [**ID3D11InfoQueue::GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) e ao adicionar uma mensagem com [**ID3D11InfoQueue::AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage). Ao criar um [**filtro de fila**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)de informações , esses valores podem ser usados para permitir ou negar qualquer categoria de mensagens para passar pelos filtros de armazenamento e recuperação.<br/> |
| [**ID DA MENSAGEM D3D11 \_ \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_id)<br/>                                         | Depurar mensagens para configurar um filtro de fila de informações (consulte [**D3D11 \_ INFO \_ QUEUE \_ FILTER**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); use essas mensagens para permitir ou negar categorias de mensagem para passar pelos filtros de armazenamento e recuperação. Essas IDs são usadas por métodos como [**ID3D11InfoQueue::GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) ou [**ID3D11InfoQueue::AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage). <br/>                                                             |
| [**SEVERIDADE DA MENSAGEM D3D11 \_ \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_severity)<br/>                             | Depurar níveis de severidade da mensagem para uma fila de informações.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**SINALIZADORES RLDO D3D11 \_ \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_rldo_flags)<br/>                                         | Opções para a quantidade de informações a relatar sobre o tempo de vida de um objeto de dispositivo.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [**OPÇÕES DE ACOMPANHAMENTO DO SOMBREADOR D3D11 \_ \_ \_**](/windows/win32/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_options)<br/>              | Opções que especificam como executar o acompanhamento de depuração do sombreador.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**TIPO DE RECURSO DE ACOMPANHAMENTO DO SOMBREADOR D3D11 \_ \_ \_ \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_shader_tracking_resource_type)<br/> | Indica quais tipos de recursos acompanhar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de camada](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





