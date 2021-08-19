---
title: WM_CAP_PAL_MANUALCREATE mensagem (Vfw.h)
description: A mensagem WM CAP PAL MANUALCREATE solicita que o driver de captura samplee manualmente quadros de vídeo e \_ \_ crie uma nova \_ paleta. Você pode enviar essa mensagem explicitamente ou usando a macro capPaletteManual.
ms.assetid: 96b6b2d6-084a-411e-8495-ea27e0c4f04f
keywords:
- WM_CAP_PAL_MANUALCREATE mensagem Windows Multimídia
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
ms.openlocfilehash: c8cc313cb6eae8e757d0777642bbc0ab72fe07fcfbf5b530a6479675c8ab3c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781287"
---
# <a name="wm_cap_pal_manualcreate-message"></a>WM \_ CAP \_ PAL \_ MANUALCRIAR mensagem

A **mensagem WM CAP PAL \_ \_ \_ MANUALCREATE** solicita que o driver de captura samplee manualmente quadros de vídeo e crie uma nova paleta. Você pode enviar essa mensagem explicitamente ou usando a [**macro capPaletteManual.**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual)


```C++
WM_CAP_PAL_MANUALCREATE 
wParam = (WPARAM) (fGrab); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*
</dt> <dd>

Sinalizador de histograma da paleta. De definir esse parâmetro **como TRUE** para cada quadro incluído na criação da paleta ideal. Depois que o último quadro tiver sido coletado, de definido esse parâmetro como **FALSE** para calcular a paleta ideal e enviá-lo para o driver de captura.

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*
</dt> <dd>

Número de cores na paleta. O valor máximo para esse parâmetro é 256. Esse valor é usado somente durante a coleta do primeiro quadro em uma sequência.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário.

Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR,**](wm-cap-set-callback-error.md) a função de retorno de chamada de erro será chamada.

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

 

 





