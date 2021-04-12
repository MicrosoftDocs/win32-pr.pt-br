---
description: O sistema transmite o evento de \_ dispositivo DBT QUERYCHANGECONFIG para solicitar permissão para alterar a configuração atual (Dock ou desencaixar). Qualquer aplicativo pode negar essa solicitação e cancelar a alteração.
ms.assetid: 2e452ea7-e2bf-4500-952a-ee7d891533a0
title: DBT_QUERYCHANGECONFIG evento (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48367da1788ae2985b21fad6e960153008e9ffd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500950"
---
# <a name="dbt_querychangeconfig-event"></a>\_Evento DBT QUERYCHANGECONFIG

O sistema transmite o evento de \_ dispositivo DBT QUERYCHANGECONFIG para solicitar permissão para alterar a configuração atual (Dock ou desencaixar). Qualquer aplicativo pode negar essa solicitação e cancelar a alteração.

Para transmitir esse evento de dispositivo, o sistema usa a mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ QUERYCHANGECONFIG e *lParam* definido como zero.


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

Defina como DBT \_ QUERYCHANGECONFIG.

</dd> <dt>

*lParam* 
</dt> <dd>

Definido como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorne **true** para conceder permissão para alterar a configuração.

Retornar consulta de difusão \_ \_ negar para negar permissão para alterar a configuração.

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

[**DEVICECHANGE do WM \_**](wm-devicechange.md)
</dt> </dl>

 

 




