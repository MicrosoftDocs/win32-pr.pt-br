---
description: O sistema transmite o evento de \_ dispositivo DBT DEVICEREMOVECOMPLETE quando um dispositivo ou uma parte da mídia foi fisicamente removida.
ms.assetid: e25d35b9-f8f1-4850-996c-e1cb393cca66
title: DBT_DEVICEREMOVECOMPLETE evento (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c899d8cee4a0be34829ba0a8edbaf27be71f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749063"
---
# <a name="dbt_deviceremovecomplete-event"></a>\_Evento DBT DEVICEREMOVECOMPLETE

O sistema transmite o evento de \_ dispositivo DBT DEVICEREMOVECOMPLETE quando um dispositivo ou uma parte da mídia foi fisicamente removida.

Para transmitir esse evento de dispositivo, o sistema usa a mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ DEVICEREMOVECOMPLETE e *lParam* definido conforme descrito a seguir.


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

Definir como DBT \_ DEVICEREMOVECOMPLETE

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura que identifica o dispositivo removido. A estrutura consiste em um cabeçalho independente de evento, seguida por membros dependentes de evento que descrevem o dispositivo. Para usar essa estrutura, trate a estrutura como uma [**estrutura \_ \_ HDR de difusão de dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) e, em seguida, verifique seu membro **dbch \_ DeviceType** para determinar o tipo de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar **true**.

## <a name="remarks"></a>Comentários

O sistema pode difundir uma \_ mensagem DBT DEVICEREMOVECOMPLETE sem enviar as mensagens [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) e [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) correspondentes. Nesses casos, os aplicativos e os drivers devem se recuperar da perda do dispositivo da melhor maneira possível.

Se a mídia estiver sendo removida, o tipo de dispositivo que chega é um volume (o membro **dbch \_ DeviceType** é DBT \_ DEVTYP \_ volume) e a alteração afeta a mídia (o membro **\_ sinalizadores dbcv** é a \_ mídia DBTF).

## <a name="examples"></a>Exemplos

Para obter um exemplo, consulte [detectando a inserção ou remoção de mídia](detecting-media-insertion-or-removal.md) ou [processando uma solicitação para remover um dispositivo](processing-a-request-to-remove-a-device.md).

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

 

 




