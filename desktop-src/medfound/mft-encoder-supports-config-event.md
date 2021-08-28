---
description: Especifica que o codificador MFT dá suporte ao recebimento de eventos MEEncodingParameter durante o streaming.
ms.assetid: 8DE04537-641C-4154-9C7F-A7D025CA4C39
title: Atributo MFT_ENCODER_SUPPORTS_CONFIG_EVENT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a528da44d59077c8445616f8fe344cba5497ced8b33be75e33be71bf9b5d76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113036"
---
# <a name="mft_encoder_supports_config_event-attribute"></a>O \_ codificador MFT \_ dá suporte ao \_ \_ atributo de evento config

Especifica que o codificador MFT dá suporte ao recebimento de eventos [MEEncodingParameter](meencodingparameters.md) durante o streaming.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Enviado pelo codificador MFT por meio de [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Aplicativos de aplicativos UWP da área de trabalho R2 \|\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Mftransform. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFTransform::P rocessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
</dt> </dl>

 

 




