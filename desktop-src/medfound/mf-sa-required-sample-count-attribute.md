---
description: Indica o número de buffers descompactados que o sink de mídia EVR (renderização de vídeo aprimorado) requer para desintercalar.
ms.assetid: b62bff64-153f-4028-a546-250419dc4152
title: MF_SA_REQUIRED_SAMPLE_COUNT atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2db64ae093228cc50695fed3ac5e39a8c44987b54d72d6e1295ccae2b6a95f42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118059407"
---
# <a name="mf_sa_required_sample_count-attribute"></a>Atributo MF \_ SA \_ REQUIRED \_ SAMPLE \_ COUNT

Indica o número de buffers descompactados que o sink de mídia EVR (renderização de vídeo aprimorado) requer para desintercalar.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse é um atributo de nível de fluxo. Para obter o atributo do EVR, faça o seguinte:

1.  Chame [**IMFMediaSink::GetStreamSinkByIndex para**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) obter o sink de fluxo.
2.  Consulte o sink de fluxo para a interface [**IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
3.  Chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Internamente, o mixer fornece esse atributo para o EVR. Para obter o atributo do mixer, chame [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho do Vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP do Server 2008 Desktop \|\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> </dl>

 

 




