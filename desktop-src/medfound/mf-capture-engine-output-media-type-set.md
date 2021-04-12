---
description: 'Indica que o tipo de saída foi definido no mecanismo de captura em resposta a IMFCaptureSink2:: SetOutputType.'
ms.assetid: A48CBC82-87C2-4AED-B7E0-B7C60FCCE4CC
title: Atributo MF_CAPTURE_ENGINE_OUTPUT_MEDIA_TYPE_SET (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5819de6a07f3b6a339400d65ff9260c33b14c592
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297978"
---
# <a name="mf_capture_engine_output_media_type_set-attribute"></a>\_Atributo de \_ \_ conjunto de \_ tipos de mídia de saída do \_ mecanismo de captura \_ MF

Indica que o tipo de saída foi definido no mecanismo de captura em resposta a [**IMFCaptureSink2:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

Você pode chamar [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus) para descobrir se a operação foi bem-sucedida ou não.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Mfcaptureengine. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFCaptureSink2:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
</dt> </dl>

 

 




