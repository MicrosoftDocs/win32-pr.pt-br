---
title: Mensagem de MCIWNDM_REALIZE (VFW. h)
description: A \_ mensagem MCIWNDM percebe que a paleta é usada atualmente pelo dispositivo MCI em uma janela MCIWnd. Essa macro é definida com a mensagem de MCIWNDM de \_ percepção. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndRealize.
ms.assetid: fe8803b5-3500-44b4-97f7-784bedf0b362
keywords:
- Multimídia do Windows de mensagem MCIWNDM_REALIZE
topic_type:
- apiref
api_name:
- MCIWNDM_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef3a803791a4f8dfe94d128d42ea06a7b28e739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918054"
---
# <a name="mciwndm_realize-message"></a>MCIWNDM \_ perceber mensagem

A mensagem **MCIWNDM \_ percebe** que a paleta é usada atualmente pelo dispositivo MCI em uma janela MCIWnd. Essa macro é definida com a mensagem de **MCIWNDM de \_ percepção** . Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) .


```C++
MCIWNDM_REALIZE 
wParam = (WPARAM) (BOOL) fBkgnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fBkgnd"></span><span id="fbkgnd"></span><span id="FBKGND"></span>*fBkgnd*
</dt> <dd>

Sinalizador de plano de fundo. Especifique **true** para este parâmetro se a janela for um aplicativo em segundo plano.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

**MCIWNDM \_ A CONCRETIZAção** usa a paleta do dispositivo MCI e chama a função [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) . Se seu aplicativo manipula explicitamente as mensagens da [**\_ paletachanged do WM**](/windows/desktop/gdi/wm-palettechanged) e do [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) , você deve usar essa mensagem em seu aplicativo em vez de usar **RealizePalette**. Se o corpo de um desses manipuladores de mensagens contiver apenas **RealizePalette**, encaminhe a mensagem para a janela MCIWnd, que irá perceber automaticamente a paleta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**paleta do WMchanged \_**](/windows/desktop/gdi/wm-palettechanged)
</dt> <dt>

[**QUERYNEWPALETTE do WM \_**](/windows/desktop/gdi/wm-querynewpalette)
</dt> </dl>

 

