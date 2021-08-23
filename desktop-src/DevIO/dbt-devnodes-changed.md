---
description: O sistema transmite o evento de dispositivo DBT DEVNODES CHANGED quando um dispositivo foi \_ adicionado ou removido do \_ sistema. Os aplicativos que mantêm listas de dispositivos no sistema devem atualizar suas listas.
ms.assetid: 62acc633-7dad-4792-a5a2-1f95356479d1
title: DBT_DEVNODES_CHANGED evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00d43873241c3f72336dd996fb9fa3486229d9ffcf522923d68ab606313afb7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539156"
---
# <a name="dbt_devnodes_changed-event"></a>Evento DBT \_ DEVNODES \_ CHANGED

O sistema transmite o evento de dispositivo DBT DEVNODES CHANGED quando um dispositivo foi \_ adicionado ou removido do \_ sistema. Os aplicativos que mantêm listas de dispositivos no sistema devem atualizar suas listas.

Para transmitir esse evento de dispositivo, o sistema usa a mensagem [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ DEVNODES CHANGED e \_ *lParam definido* como zero.


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Um identificador para uma janela.

</dd> <dt>

*Umsg* 
</dt> <dd>

O [**\_ identificador de mensagem WM DEVICECHANGE.**](wm-devicechange.md)

</dd> <dt>

*wParam* 
</dt> <dd>

De definido como DBT \_ DEVNODES \_ CHANGED.

</dd> <dt>

*lParam* 
</dt> <dd>

Definido como zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar **TRUE.**

## <a name="remarks"></a>Comentários

Não há informações adicionais sobre qual dispositivo foi adicionado ou removido do sistema. Os aplicativos que exigem mais informações devem se registrar para notificação de dispositivo usando [**a função RegisterDeviceNotification.**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2003<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Dbt.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de dispositivo](device-events.md)
</dt> <dt>

[Gerenciamento de Dispositivos eventos](device-management-events.md)
</dt> <dt>

[**HDR \_ DE \_ DIFUSÃO DE DESENVOLVIMENTO**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




