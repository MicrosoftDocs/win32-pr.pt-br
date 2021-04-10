---
description: Desabilita o uso de plug-ins de câmera de pós-processamento pelo leitor de origem.
ms.assetid: 837A6BA8-9C79-4B0A-B40D-C094009BFF2C
title: Atributo MF_SOURCE_READER_DISABLE_CAMERA_PLUGINS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7c72529d1cb684c547d283ce7f9ec92782f359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171604"
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
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do leitor de origem](source-reader-attributes.md)
</dt> </dl>

 

 




