---
description: Desabilita o uso de plug-ins de câmera de pós-processamento pelo leitor de origem.
ms.assetid: 837A6BA8-9C79-4B0A-B40D-C094009BFF2C
title: Atributo MF_SOURCE_READER_DISABLE_CAMERA_PLUGINS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66ae9c69d13b6af3e368b57a3f864f031d0cc7e63716d2267ae5d3869d102b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600286"
---
# <a name="mf_source_reader_disable_camera_plugins-attribute"></a>\_Leitor de origem MF \_ \_ desabilitar atributo de plug- \_ ins de câmera \_

Desabilita o uso de plug-ins de câmera de pós-processamento pelo [leitor de origem](source-reader.md).

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica quando o leitor de origem é usado com uma fonte de captura de vídeo. Se esse atributo for **true**, ele impedirá que o leitor de origem carregue quaisquer plug-ins de pós-processamento que possam ser fornecidos pela câmera. Caso contrário, por padrão, o leitor de origem os carregará.

O valor padrão desse atributo é **false**. Defina o atributo ao criar o leitor de origem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do leitor de origem](source-reader-attributes.md)
</dt> </dl>

 

 




