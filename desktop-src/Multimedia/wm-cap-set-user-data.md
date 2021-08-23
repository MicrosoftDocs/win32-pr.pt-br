---
title: Mensagem de WM_CAP_SET_USER_DATA (VFW. h)
description: A Cap do WM \_ \_ definir a \_ \_ mensagem de dados do usuário associa um \_ valor de dados PTR longo a uma janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capSetUserData.
ms.assetid: 067502e3-f009-4cf2-b612-4a0b64624416
keywords:
- mensagem de WM_CAP_SET_USER_DATA Windows multimídia
topic_type:
- apiref
api_name:
- WM_CAP_SET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5b4a192b774572ea374b08d4a4128389281e44ee00614806841b0b007d978b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803546"
---
# <a name="wm_cap_set_user_data-message"></a>\_Mensagem de \_ \_ dados do usuário Set Cap do WM \_

A **Cap do WM definir a mensagem de \_ \_ \_ \_ dados do usuário** associa um valor de dados **\_ PTR longo** a uma janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetUserData**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) .


```C++
WM_CAP_SET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = (LPARAM)lUser; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*
</dt> <dd>

Valor de dados a ser associado a uma janela de captura.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** se a captura de streaming estiver em andamento.

## <a name="remarks"></a>Comentários

Normalmente, essa mensagem é usada para apontar para um bloco de dados associado a uma janela de captura.

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

 

 





