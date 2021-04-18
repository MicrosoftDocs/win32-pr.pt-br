---
description: Identifica o componente que gerou um evento de captura.
ms.assetid: DCCF3054-AF14-44C7-84C0-B03E35B5D90A
title: Atributo MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9a5068db357523a626404910fb7d752ea0b621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760602"
---
# <a name="mf_capture_engine_event_generator_guid-attribute"></a>\_Atributo de \_ \_ GUID do gerador de eventos do mecanismo de \_ captura MF \_

Identifica o componente que gerou um evento de captura.

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

Esse atributo aparece em alguns eventos do mecanismo de captura. Para obter esse atributo, chame [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) no objeto de evento. O objeto de evento é passado para o aplicativo por meio do método [**IMFCaptureEngineOnEventCallback:: OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) .

O valor é um identificador de interface para o componente que gerou o evento. Por exemplo, o valor **IID \_ IMFCapturePreviewSink** indica o coletor de visualização ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)). Nem todo evento de captura contém esse atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do mecanismo de captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




