---
description: O sistema transmite o evento de \_ dispositivo DBT DEVNODES \_ alterado quando um dispositivo foi adicionado ou removido do sistema. Os aplicativos que mantêm listas de dispositivos no sistema devem atualizar suas listas.
ms.assetid: 62acc633-7dad-4792-a5a2-1f95356479d1
title: DBT_DEVNODES_CHANGED evento (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1450e9a87d541e5df3d9a9286e48601697e6aaae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089201"
---
# <a name="dbt_devnodes_changed-event"></a>Evento de alteração de DBT \_ DEVNODES \_

O sistema transmite o evento de \_ dispositivo DBT DEVNODES \_ alterado quando um dispositivo foi adicionado ou removido do sistema. Os aplicativos que mantêm listas de dispositivos no sistema devem atualizar suas listas.

Para transmitir esse evento de dispositivo, o sistema usa a mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ DEVNODES \_ alterado e *lParam* definido como zero.


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

Definido como DBT \_ DEVNODES \_ foi alterado.

</dd> <dt>

*lParam* 
</dt> <dd>

Definido como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar **true**.

## <a name="remarks"></a>Comentários

Não há informações adicionais sobre qual dispositivo foi adicionado ou removido do sistema. Os aplicativos que exigem mais informações devem se registrar para a notificação do dispositivo usando a função [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2003<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>DBT. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de dispositivo](device-events.md)
</dt> <dt>

[Eventos de gerenciamento de dispositivo](device-management-events.md)
</dt> <dt>

[**\_cabeçalho de difusão de dev \_**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**DEVICECHANGE do WM \_**](wm-devicechange.md)
</dt> </dl>

 

 




