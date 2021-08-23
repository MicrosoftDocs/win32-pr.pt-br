---
title: Mensagem de WM_CAP_PAL_PASTE (VFW. h)
description: A mensagem do WM \_ Cap \_ PAL \_ Paste copia a paleta da área de transferência e a transmite para um driver de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capPalettePaste.
ms.assetid: d49c7fd9-be40-4a07-8339-b85f7c4c331e
keywords:
- mensagem de WM_CAP_PAL_PASTE Windows multimídia
topic_type:
- apiref
api_name:
- WM_CAP_PAL_PASTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7bedb760a444abe9b0667592855d701dc24a02b8ee57ea15ab30912a5e216d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686826"
---
# <a name="wm_cap_pal_paste-message"></a>\_Mensagem de \_ colagem da PAL do WM Cap \_

A mensagem do **WM \_ Cap \_ PAL \_ Paste** copia a paleta da área de transferência e a transmite para um driver de captura. Você pode enviar essa mensagem explicitamente ou usando a macro [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) .


```C++
WM_CAP_PAL_PASTE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem de [**erro de retorno de chamada do WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , a função de retorno de chamada de erro será chamada.

## <a name="remarks"></a>Comentários

Um driver de captura usa uma paleta quando exigido pelo formato de vídeo digitalizado especificado.

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

 

 





