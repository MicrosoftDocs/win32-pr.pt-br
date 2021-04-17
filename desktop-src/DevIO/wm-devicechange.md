---
description: Notifica um aplicativo sobre uma alteração na configuração de hardware de um dispositivo ou computador.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: Mensagem de WM_DEVICECHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f631d75f89f306adc0594a3df6c63d63753e163
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370405"
---
# <a name="wm_devicechange-message"></a>Mensagem do WM \_ DEVICECHANGE

Notifica um aplicativo sobre uma alteração na configuração de hardware de um dispositivo ou computador.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* 
</dt> <dd>

Um identificador para a janela.

</dd> <dt>

*uMsg* 
</dt> <dd>

O **identificador \_ DEVICECHANGE do WM** .

</dd> <dt>

*wParam* 
</dt> <dd>

O evento que ocorreu. Esse parâmetro pode ser um dos seguintes valores do arquivo de cabeçalho DBT. h.



| Valor                                                                                                                                                                                                                                                                                                  | Significado                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span><dl> <dt>**[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</dt> <dt>0x0019</dt> </dl>             | Uma solicitação para alterar a configuração atual (Dock ou Dock) foi cancelada.<br/>                                           |
| <span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span><dl> <dt>**[DBT \_ CONFIGchanged](dbt-configchanged.md)**</dt> <dt>0x0018</dt> </dl>                                         | A configuração atual foi alterada devido a um encaixe ou desencaixe.<br/>                                                             |
| <span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span><dl> <dt>**[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</dt> <dt>0x8006</dt> </dl>                                                 | Ocorreu um evento personalizado.<br/>                                                                                                |
| <span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span><dl> <dt>**[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)**</dt> <dt>0x8000</dt> </dl>                                         | Um dispositivo ou parte da mídia foi inserido e agora está disponível.<br/>                                                          |
| <span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span><dl> <dt>**[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</dt> <dt>0x8001</dt> </dl>                         | A permissão é solicitada para remover um dispositivo ou parte da mídia. Qualquer aplicativo pode negar essa solicitação e cancelar a remoção.<br/> |
| <span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span><dl> <dt>**[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</dt> <dt>0x8002</dt> </dl> | Uma solicitação para remover um dispositivo ou parte da mídia foi cancelada.<br/>                                                           |
| <span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span><dl> <dt>**[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</dt> <dt>0x8004</dt> </dl>             | Um dispositivo ou parte da mídia foi removida.<br/>                                                                                |
| <span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span><dl> <dt>**[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</dt> <dt>0x8003</dt> </dl>                 | Um dispositivo ou parte da mídia está prestes a ser removida. Não pode ser negado.<br/>                                                        |
| <span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span><dl> <dt>**[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</dt> <dt>0x8005</dt> </dl>                     | Ocorreu um evento específico do dispositivo.<br/>                                                                                       |
| <span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span><dl> <dt>**[DBT \_ DEVNODES \_ alterou](dbt-devnodes-changed.md)**</dt> <dt>0x0007</dt> </dl>                            | Um dispositivo foi adicionado ou removido do sistema.<br/>                                                                      |
| <span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span><dl> <dt>**[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</dt> <dt>0x0017</dt> </dl>                         | A permissão é solicitada para alterar a configuração atual (Dock ou desencaixar).<br/>                                               |
| <span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span><dl> <dt>**[DBT \_ 0xFFFF definido pelo UserDefined](dbt-userdefined.md)**</dt> <dt></dt> </dl>                                                 | O significado dessa mensagem é definido pelo usuário.<br/>                                                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura que contém dados específicos do evento. Seu formato depende do valor do parâmetro *wParam* . Para obter mais informações, consulte a documentação de cada evento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar **true** para conceder a solicitação.

Retornar **consulta de difusão \_ \_ negar** para negar a solicitação.

## <a name="remarks"></a>Comentários

Para dispositivos que oferecem recursos controlávels por software, como ejeção e bloqueio, o sistema normalmente envia uma mensagem [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) para permitir que aplicativos e drivers de dispositivo terminem o uso do dispositivo normalmente. Se o sistema forçar a remoção de um dispositivo, ele não poderá enviar uma mensagem [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) antes de fazer isso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP<br/>                                                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2003<br/>                                                                                    |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h ou DBT. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)
</dt> <dt>

[DBT \_ ConfigChanged](dbt-configchanged.md)
</dt> <dt>

[DBT \_ CUSTOMEVENT](dbt-customevent.md)
</dt> <dt>

[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)
</dt> <dt>

[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)
</dt> <dt>

[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)
</dt> <dt>

[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)
</dt> <dt>

[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)
</dt> <dt>

[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)
</dt> <dt>

[DBT \_ DEVNODES \_ alterado](dbt-devnodes-changed.md)
</dt> <dt>

[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)
</dt> <dt>

[DBT \_ USERdefined](dbt-userdefined.md)
</dt> </dl>

 

