---
description: O sistema transmite o evento de \_ dispositivo DBT DEVICEQUERYREMOVE para solicitar permissão para remover um dispositivo ou parte da mídia.
ms.assetid: a0e9aa57-da0e-4e9c-99d0-5502040d2664
title: DBT_DEVICEQUERYREMOVE evento (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c9dbdee13318f9a664582fdba8f9e3f9bfc5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754793"
---
# <a name="dbt_devicequeryremove-event"></a>\_Evento DBT DEVICEQUERYREMOVE

O sistema transmite o evento de \_ dispositivo DBT DEVICEQUERYREMOVE para solicitar permissão para remover um dispositivo ou parte da mídia. Essa mensagem é a última chance de aplicativos e drivers se preparar para essa remoção. No entanto, qualquer aplicativo pode negar essa solicitação e cancelar a operação.

Para transmitir esse evento de dispositivo, o sistema usa a mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ DEVICEQUERYREMOVE e *lParam* definido conforme descrito a seguir.


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

Defina como DBT \_ DEVICEQUERYREMOVE.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura que identifica o dispositivo a ser removido. A estrutura consiste em um cabeçalho independente de evento, seguida por membros dependentes de evento que descrevem o dispositivo. Para usar essa estrutura, trate a estrutura como uma [**estrutura \_ \_ HDR de difusão de dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) e, em seguida, verifique seu membro **dbch \_ DeviceType** para determinar o tipo de dispositivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar **true** para conceder permissão para remover um dispositivo.

Retornar consulta de difusão \_ \_ negar para negar permissão para remover um dispositivo.

## <a name="remarks"></a>Comentários

Você deve fechar todos os identificadores para o dispositivo ou a remoção do dispositivo falhará.

## <a name="examples"></a>Exemplos

Para obter um exemplo, consulte [processando uma solicitação para remover um dispositivo](processing-a-request-to-remove-a-device.md).

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

 

 




