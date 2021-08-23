---
description: O sistema transmite o evento de \_ dispositivo DBT DEVICEQUERYREMOVEFAILED quando uma solicitação para remover um dispositivo ou parte da mídia foi cancelada.
ms.assetid: a24916a9-b67a-4622-b9f3-4b4f26bf4d6b
title: DBT_DEVICEQUERYREMOVEFAILED evento (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 605c2689d7d986b4e85fda6d8ce5f24fa6483641de46a6a84f3e4e96ba473897
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076300"
---
# <a name="dbt_devicequeryremovefailed-event"></a>\_Evento DBT DEVICEQUERYREMOVEFAILED

O sistema transmite o evento de \_ dispositivo DBT DEVICEQUERYREMOVEFAILED quando uma solicitação para remover um dispositivo ou parte da mídia foi cancelada.

Para transmitir esse evento de dispositivo, o sistema usa a mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ DEVICEQUERYREMOVEFAILED e *lParam* definido conforme descrito a seguir.


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

Defina como DBT \_ DEVICEQUERYREMOVEFAILED.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura que identifica o dispositivo. A estrutura consiste em um cabeçalho independente de evento, seguida por membros dependentes de evento que descrevem o dispositivo. Para usar essa estrutura, trate a estrutura como uma [**estrutura \_ \_ HDR de difusão de dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) e, em seguida, verifique seu membro **dbch \_ DeviceType** para determinar o tipo de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar **true**.

## <a name="examples"></a>Exemplos

Para obter um exemplo, consulte [processando uma solicitação para remover um dispositivo](processing-a-request-to-remove-a-device.md).

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

[**\_cabeçalho de difusão de dev \_**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**DEVICECHANGE do WM \_**](wm-devicechange.md)
</dt> </dl>

 

 




