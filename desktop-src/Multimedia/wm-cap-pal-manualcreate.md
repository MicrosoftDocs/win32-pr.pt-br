---
title: Mensagem de WM_CAP_PAL_MANUALCREATE (VFW. h)
description: A mensagem do WM \_ Cap \_ PAL \_ MANUALCREATE solicita que o driver de captura amostras de quadros de vídeo manualmente e crie uma nova paleta. Você pode enviar essa mensagem explicitamente ou usando a macro capPaletteManual.
ms.assetid: 96b6b2d6-084a-411e-8495-ea27e0c4f04f
keywords:
- Multimídia do Windows de mensagem WM_CAP_PAL_MANUALCREATE
topic_type:
- apiref
api_name:
- WM_CAP_PAL_MANUALCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dfd5b6588381ede0faaae539d3d8418b041f458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644514"
---
# <a name="wm_cap_pal_manualcreate-message"></a>\_Mensagem de \_ MANUALCREATE de PAL do WM Cap \_

A mensagem do **WM \_ Cap \_ PAL \_ MANUALCREATE** solicita que o driver de captura amostras de quadros de vídeo manualmente e crie uma nova paleta. Você pode enviar essa mensagem explicitamente ou usando a macro [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) .


```C++
WM_CAP_PAL_MANUALCREATE 
wParam = (WPARAM) (fGrab); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*
</dt> <dd>

Sinalizador de histograma da paleta. Defina esse parâmetro como **true** para cada quadro incluído na criação da paleta ideal. Depois que o último quadro tiver sido coletado, defina esse parâmetro como **false** para calcular a paleta ideal e enviá-lo para o driver de captura.

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*
</dt> <dd>

Número de cores na paleta. O valor máximo para esse parâmetro é 256. Esse valor é usado somente durante a coleta do primeiro quadro em uma sequência.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem de [**erro de retorno de chamada do WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , a função de retorno de chamada de erro será chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





