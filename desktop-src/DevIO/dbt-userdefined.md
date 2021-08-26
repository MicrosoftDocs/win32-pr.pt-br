---
description: O \_ evento de dispositivo DBT USERdefined identifica um evento definido pelo usuário.
ms.assetid: b42feda9-5fe7-4e54-aad9-28c61d2f29b6
title: DBT_USERDEFINED evento (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49eca726ea9c4336a36f30872ad068e45062a67189192154374d5d5b21e578ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103866"
---
# <a name="dbt_userdefined-event"></a>\_Evento DBT USERdefined

O \_ evento de dispositivo DBT USERdefined identifica um evento definido pelo usuário.

Para transmitir esse evento de dispositivo, chame a função [**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) com a mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) . Defina *wParam* como DBT UserDefined \_ e defina *lParam* conforme descrito a seguir.


```C++
LRESULT CALLBACK WindowProc( HWND   hwnd,     // handle to window
                             UINT   uMsg,     // WM_DEVICECHANGE
                             WPARAM wParam,   // DBT_USERDEFINED
                             LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* 
</dt> <dd>

Um identificador para uma janela.

</dd> <dt>

*uMsg* 
</dt> <dd>

O identificador de mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) .

</dd> <dt>

*wParam* 
</dt> <dd>

Defina como DBT \_ USERdefined.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**\_ \_ \_ userdefineda de difusão de desenvolvimento**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) que descreve a difusão definida pelo usuário em andamento. O membro **dbud \_ szName** contém o nome da mensagem definida pelo usuário, seguido por qualquer dado definido pelo usuário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2003<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>DBT. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de dispositivo](device-events.md)
</dt> <dt>

[Eventos de gerenciamento de dispositivo](device-management-events.md)
</dt> <dt>

[**\_UserDefined de difusão de DEV \_ \_**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)
</dt> <dt>

[**DEVICECHANGE do WM \_**](wm-devicechange.md)
</dt> <dt>

[**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)
</dt> </dl>

 

