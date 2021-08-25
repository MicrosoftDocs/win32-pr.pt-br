---
description: O sistema transmite o evento do dispositivo DBT CONFIGCHANGECANCELED quando uma solicitação para alterar a configuração atual (encaixe ou \_ desencaixamento) foi cancelada.
ms.assetid: b4b1455c-9a04-4fa0-a3fa-ed991f278c0c
title: DBT_CONFIGCHANGECANCELED evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 624144ccd5a87d983d453c8d6a3c0667376c2a1b9340bba83f229a29882bffe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874536"
---
# <a name="dbt_configchangecanceled-event"></a>Evento DBT \_ CONFIGCHANGECANCELED

O sistema transmite o evento do dispositivo DBT CONFIGCHANGECANCELED quando uma solicitação para alterar a configuração atual (encaixe ou \_ desencaixamento) foi cancelada.

Para transmitir esse evento de dispositivo, o sistema usa a mensagem [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ CONFIGCHANGECANCELED e *lParam definido* como zero.


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

Definido como DBT \_ CONFIGCHANGECANCELED.

</dd> <dt>

*lParam* 
</dt> <dd>

Definido como zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar **TRUE.**

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

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




