---
description: O sistema transmite o evento de dispositivo DBT \_ DEVICETYPESPECIFIC quando ocorre um evento específico do dispositivo.
ms.assetid: 5d68e29d-b4d7-46f4-a35e-1db286e944ca
title: DBT_DEVICETYPESPECIFIC evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd8fb403568cef55741a8c206929d9105284f5191c547500fd79ff39f6b01f1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109026"
---
# <a name="dbt_devicetypespecific-event"></a>Evento DBT \_ DEVICETYPESPECIFIC

O sistema transmite o evento de dispositivo DBT \_ DEVICETYPESPECIFIC quando ocorre um evento específico do dispositivo.

Para transmitir esse evento de dispositivo, o sistema usa a mensagem [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ DEVICETYPESPECIFIC e *lParam* definidos conforme descrito a seguir.


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

Definido como DBT \_ DEVICETYPESPECIFIC.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura que identifica o dispositivo. A estrutura consiste em um header independente de evento, seguido por membros dependentes de evento que descrevem o dispositivo. Para usar essa estrutura, trate a estrutura como uma estrutura [**\_ \_ HDR DEV BROADCAST**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) e verifique seu membro **dbch \_ devicetype** para determinar o tipo de dispositivo.

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

[**HDR \_ DE \_ DIFUSÃO DE DESENVOLVIMENTO**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




