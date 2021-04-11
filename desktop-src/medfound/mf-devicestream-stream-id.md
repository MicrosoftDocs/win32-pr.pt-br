---
description: Especifica o identificador de streaming de kernel (KS) para um fluxo em um dispositivo de captura de vídeo.
ms.assetid: 03C48CBA-FAD0-4127-89E5-3F1874BF32DB
title: Atributo MF_DEVICESTREAM_STREAM_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f7143487af1125da9334fc39c152aee9363b97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010721"
---
# <a name="mf_devicestream_stream_id-attribute"></a>\_Atributo de \_ ID de fluxo MF DEVICESTREAM \_

Especifica o identificador de streaming de kernel (KS) para um fluxo em um dispositivo de captura de vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Para obter esse atributo, faça o seguinte:

1.  Consulte a origem da mídia para a interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .
2.  Chame [**IMFMediaSourceEx:: Getstreamattributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para o fluxo.
3.  Chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obter o atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




