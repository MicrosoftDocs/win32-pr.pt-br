---
description: Identifica o componente que gerou um evento de captura.
ms.assetid: DCCF3054-AF14-44C7-84C0-B03E35B5D90A
title: MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88efff7cea540c1fae2c14d44dd7676c4f523b562a66a4c4f4bc4dffea59d5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474464"
---
# <a name="mf_capture_engine_event_generator_guid-attribute"></a>Atributo GUID DO GERADOR DE EVENTOS DO MECANISMO DE CAPTURA \_ \_ \_ \_ \_ DE MF

Identifica o componente que gerou um evento de captura.

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

Esse atributo aparece em alguns eventos do mecanismo de captura. Para obter esse atributo, chame [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) no objeto de evento. O objeto de evento é passado para o aplicativo por meio do [**método IMFCaptureEngineOnEventCallback::OnEvent.**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent)

O valor é um identificador de interface para o componente que gerou o evento. Por exemplo, o valor **\_ IID IMFCapturePreviewSink** indica o sink de visualização ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)). Nem todo evento de captura contém esse atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                   |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                         |
| Cabeçalho<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do Mecanismo de Captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




