---
description: Indica que o tipo de saída foi definido no mecanismo de captura em resposta a IMFCaptureSink2::SetOutputType.
ms.assetid: A48CBC82-87C2-4AED-B7E0-B7C60FCCE4CC
title: MF_CAPTURE_ENGINE_OUTPUT_MEDIA_TYPE_SET atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 138a5893d4ccdd014354e00718a98eda9ba41616c1f1507c8749c9b36dcc0c29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013406"
---
# <a name="mf_capture_engine_output_media_type_set-attribute"></a>Atributo MF \_ CAPTURE ENGINE OUTPUT MEDIA TYPE \_ \_ \_ \_ \_ SET

Indica que o tipo de saída foi definido no mecanismo de captura em resposta a [**IMFCaptureSink2::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

Você pode chamar [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus) para descobrir se a operação foi bem-sucedida ou não.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Mfcaptureengine.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFCaptureSink2::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
</dt> </dl>

 

 




