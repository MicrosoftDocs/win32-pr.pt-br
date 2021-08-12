---
title: WM_CAP_GET_VIDEOFORMAT mensagem (Vfw.h)
description: A mensagem WM CAP GET VIDEOFORMAT recupera uma cópia do formato de vídeo em uso ou o tamanho \_ necessário para o formato de \_ \_ vídeo. Você pode enviar essa mensagem explicitamente ou usando as macros capGetVideoFormat e capGetVideoFormatSize.
ms.assetid: ac72dfdb-fe1a-4007-bdce-41e5e67d076a
keywords:
- WM_CAP_GET_VIDEOFORMAT mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- WM_CAP_GET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afae3ea79b29cad6a758272f8f3952fdfb830a2b3d6d60f9fc5b4ca5042179fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622615"
---
# <a name="wm_cap_get_videoformat-message"></a>Mensagem WM \_ CAP \_ GET \_ VIDEOFORMAT

A **mensagem WM CAP GET \_ \_ \_ VIDEOFORMAT** recupera uma cópia do formato de vídeo em uso ou o tamanho necessário para o formato de vídeo. Você pode enviar essa mensagem explicitamente ou usando as macros [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) e [**capGetVideoFormatSize.**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize)


```C++
WM_CAP_GET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*Wsize*
</dt> <dd>

Tamanho, em bytes, da estrutura referenciada por **s**.

</dd> <dt>

<span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*
</dt> <dd>

Ponteiro para uma [**estrutura BITMAPINFO.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) Você também pode especificar **NULL** para recuperar o número de bytes necessários.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará o tamanho, em bytes, do formato de vídeo ou zero se a janela de captura não estiver conectada a um driver de captura. Para formatos de vídeo que exigem uma paleta, a paleta atual também é retornada.

## <a name="remarks"></a>Comentários

Como os formatos de vídeo compactados variam de acordo com os requisitos de tamanho, os aplicativos devem primeiro recuperar o tamanho, depois alocar memória e, por fim, solicitar os dados de formato de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

