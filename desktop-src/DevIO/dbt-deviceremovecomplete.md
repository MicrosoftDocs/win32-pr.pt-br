---
description: O sistema transmite o evento de dispositivo DBT DEVICEREMOVECOMPLETE quando um dispositivo ou parte \_ da mídia foi fisicamente removido.
ms.assetid: e25d35b9-f8f1-4850-996c-e1cb393cca66
title: DBT_DEVICEREMOVECOMPLETE evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5998742d823d710bfb91cd10579a3fb1ec65bec42b615fc7fdac3ac35545b24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539186"
---
# <a name="dbt_deviceremovecomplete-event"></a>Evento DBT \_ DEVICEREMOVECOMPLETE

O sistema transmite o evento de dispositivo DBT DEVICEREMOVECOMPLETE quando um dispositivo ou parte \_ da mídia foi fisicamente removido.

Para transmitir esse evento de dispositivo, o sistema usa a mensagem [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ DEVICEREMOVECOMPLETE e *lParam* definidos conforme descrito a seguir.


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

Definido como DBT \_ DEVICEREMOVECOMPLETE

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura que identifica o dispositivo removido. A estrutura consiste em um header independente de evento, seguido por membros dependentes de evento que descrevem o dispositivo. Para usar essa estrutura, trate a estrutura como uma estrutura [**\_ \_ HDR DEV BROADCAST**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) e verifique seu membro **dbch \_ devicetype** para determinar o tipo de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar **TRUE.**

## <a name="remarks"></a>Comentários

O sistema pode transmitir uma mensagem DBT DEVICEREMOVECOMPLETE sem enviar mensagens \_ [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) e [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) correspondentes. Nesses casos, os aplicativos e drivers devem se recuperar da perda do dispositivo da melhor maneira possível.

Se a mídia estiver sendo removida, o tipo de dispositivo que chega será um volume (o membro do tipo de dispositivo **dbch \_** é DBT DEVTYP VOLUME) e a alteração afeta a mídia (o membro de sinalizadores \_ \_ **dbcv \_** é DBTF \_ MEDIA).

## <a name="examples"></a>Exemplos

Para ver um exemplo, consulte [Detecting Media Insertion or Removal](detecting-media-insertion-or-removal.md) or [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).

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

 

 




