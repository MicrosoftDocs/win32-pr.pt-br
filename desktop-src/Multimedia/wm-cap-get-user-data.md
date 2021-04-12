---
title: Mensagem de WM_CAP_GET_USER_DATA (VFW. h)
description: A mensagem de obtenção de dados do usuário do WM \_ Cap \_ \_ \_ recupera um \_ valor de dados PTR longo associado a uma janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capGetUserData.
ms.assetid: f7c121ba-44a1-4916-b602-c53d8332c2af
keywords:
- Multimídia do Windows de mensagem WM_CAP_GET_USER_DATA
topic_type:
- apiref
api_name:
- WM_CAP_GET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02951667600acba115f506a610b167b72b69ea99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499660"
---
# <a name="wm_cap_get_user_data-message"></a>\_Mensagem de \_ obtenção \_ de \_ dados do usuário do WM Cap

A mensagem de **\_ obtenção de \_ \_ \_ dados do usuário do WM Cap** recupera um valor de dados **\_ PTR longo** associado a uma janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro [**capGetUserData**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) .


```C++
WM_CAP_GET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retorna um valor salvo anteriormente usando a mensagem de [**dados do usuário do WM \_ Cap \_ \_ \_ set**](wm-cap-set-user-data.md) .

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

 

 





