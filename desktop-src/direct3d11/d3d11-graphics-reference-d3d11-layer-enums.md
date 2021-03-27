---
title: Enumerações de camada
description: Esta seção contém informações sobre as enumerações de camada.
ms.assetid: 0fd0456b-2638-4b4c-8a34-a3e104a1a034
keywords:
- enumerações, camada do Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e1cca3fa500a529930c8d0c39005697045d18b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104967242"
---
# <a name="layer-enumerations"></a>Enumerações de camada

Esta seção contém informações sobre as enumerações de camada.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Categoria de mensagem D3D11 \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_category)<br/>                             | Categorias de mensagens de depuração. Isso identificará a categoria de uma mensagem ao recuperar uma mensagem com [**ID3D11InfoQueue:: GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) e ao adicionar uma mensagem com [**ID3D11InfoQueue:: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage). Ao criar um [**filtro de fila de informações**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter), esses valores podem ser usados para permitir ou negar quaisquer categorias de mensagens a serem passadas pelos filtros de armazenamento e recuperação.<br/> |
| [**\_ID da mensagem D3D11 \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_id)<br/>                                         | Mensagens de depuração para configurar um filtro de fila de informações (consulte [**D3D11 \_ info \_ Queue \_ Filter**](/windows/desktop/api/D3D11SDKLayers/ns-d3d11sdklayers-d3d11_info_queue_filter)); Use essas mensagens para permitir ou negar as categorias de mensagens a serem passadas pelos filtros de armazenamento e recuperação. Essas IDs são usadas por métodos como [**ID3D11InfoQueue:: GetMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-getmessage) ou [**ID3D11InfoQueue:: AddMessage**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11infoqueue-addmessage). <br/>                                                             |
| [**\_Severidade da mensagem D3D11 \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_message_severity)<br/>                             | Depurar níveis de severidade de mensagem para uma fila de informações.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**\_Sinalizadores D3D11 RLDO \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_rldo_flags)<br/>                                         | Opções para a quantidade de informações a serem relatadas sobre o tempo de vida de um objeto de dispositivo.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [**\_Opções de acompanhamento do sombreador D3D11 \_ \_**](/windows/win32/api/d3d11sdklayers/ne-d3d11sdklayers-d3d11_shader_tracking_options)<br/>              | Opções que especificam como executar o rastreamento de depuração do sombreador.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**\_Tipo de \_ recurso de acompanhamento de SOMBREAdor D3D11 \_ \_**](/windows/desktop/api/D3D11SDKLayers/ne-d3d11sdklayers-d3d11_shader_tracking_resource_type)<br/> | Indica quais tipos de recursos controlar.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de camada](d3d11-graphics-reference-d3d11-layer.md)
</dt> </dl>

 

 





