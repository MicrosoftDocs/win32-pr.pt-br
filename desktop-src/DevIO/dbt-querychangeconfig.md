---
description: O sistema transmite o evento de dispositivo DBT QUERYCHANGECONFIG para solicitar permissão para alterar a configuração atual \_ (encaixar ou desencaixar). Qualquer aplicativo pode negar essa solicitação e cancelar a alteração.
ms.assetid: 2e452ea7-e2bf-4500-952a-ee7d891533a0
title: DBT_QUERYCHANGECONFIG evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e9c222fdc29f635263b45b5fd7e54ee229a33d7dee1ff31cd1e3072bfe6e84f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318416"
---
# <a name="dbt_querychangeconfig-event"></a>Evento DBT \_ QUERYCHANGECONFIG

O sistema transmite o evento de dispositivo DBT QUERYCHANGECONFIG para solicitar permissão para alterar a configuração atual \_ (encaixar ou desencaixar). Qualquer aplicativo pode negar essa solicitação e cancelar a alteração.

Para transmitir esse evento de dispositivo, o sistema usa a mensagem [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ QUERYCHANGECONFIG e *lParam definido* como zero.


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

Definido como DBT \_ QUERYCHANGECONFIG.

</dd> <dt>

*lParam* 
</dt> <dd>

Definido como zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar **TRUE** para conceder permissão para alterar a configuração.

Retornar BROADCAST \_ QUERY \_ DENY para negar a permissão para alterar a configuração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2003<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>Dbt.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de dispositivo](device-events.md)
</dt> <dt>

[Gerenciamento de Dispositivos eventos](device-management-events.md)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




