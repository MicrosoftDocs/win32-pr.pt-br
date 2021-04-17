---
title: Mensagem de WM_CAP_PAL_AUTOCREATE (VFW. h)
description: A \_ mensagem de \_ criação automática de PAL Cap do WM \_ solicita que os quadros de vídeo de exemplo do driver de captura e criem automaticamente uma nova paleta. Você pode enviar essa mensagem explicitamente ou usando a macro capPaletteAuto.
ms.assetid: b94d245d-adf4-4fe0-b053-87109ef5fd2f
keywords:
- Multimídia do Windows de mensagem WM_CAP_PAL_AUTOCREATE
topic_type:
- apiref
api_name:
- WM_CAP_PAL_AUTOCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba70de46167121aa9a83959c6d9e202039f65cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754631"
---
# <a name="wm_cap_pal_autocreate-message"></a>Mensagem de criação de email do WM \_ Cap \_ PAL \_

A mensagem de criação automática de **\_ \_ PAL \_ Cap do WM** solicita que os quadros de vídeo de exemplo do driver de captura e criem automaticamente uma nova paleta. Você pode enviar essa mensagem explicitamente ou usando a macro [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) .


```C++
WM_CAP_PAL_AUTOCREATE 
wParam = (WPARAM) (iFrames); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*
</dt> <dd>

Número de quadros a serem amostrados.

</dd> <dt>

<span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*
</dt> <dd>

Número de cores na paleta. O valor máximo para esse parâmetro é 256.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem de [**erro de retorno de chamada do WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , a função de retorno de chamada de erro será chamada.

## <a name="remarks"></a>Comentários

A sequência de vídeo de amostra deve incluir todas as cores que você deseja na paleta. Para obter a melhor paleta, talvez seja necessário obter uma amostra da sequência inteira em vez de uma parte dela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





