---
description: Identificador para a janela de recorte de vídeo.
ms.assetid: 883bc7cf-f52f-4cb5-a942-b42b429b17a9
title: Atributo MF_ACTIVATE_VIDEO_WINDOW (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a23253c0cd1e4ae90659838acbb58056f770419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789922"
---
# <a name="mf_activate_video_window-attribute"></a>\_Atributo da \_ janela ativar vídeo do MF \_

Identificador para a janela de recorte de vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT64**

Tratar como **DWORD \_ PTR** (**hWnd**).

## <a name="remarks"></a>Comentários

Esse atributo se aplica ao objeto de ativação para o processador de vídeo avançado (EVR). O valor é definido automaticamente quando você chama [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) para criar o objeto de ativação EVR.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos avançados de processador de vídeo](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[Objetos de ativação](activation-objects.md)
</dt> </dl>

 

 




