---
description: Notifica um aplicativo de uma alteração na configuração de hardware de um dispositivo ou computador.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: Mensagem WM_DEVICECHANGE (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b32936d36e01a34acc9ace512703db7584768e8b51a9fe06a791b2a285ee2add
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017794"
---
# <a name="wm_devicechange-message"></a>Mensagem WM \_ DEVICECHANGE

Notifica um aplicativo de uma alteração na configuração de hardware de um dispositivo ou computador.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

```C++
LRESULT CALLBACK WindowProc(HWND   hwnd,     // handle to window
                            UINT   uMsg,     // WM_DEVICECHANGE
                            WPARAM wParam,   // device-change event
                            LPARAM lParam ); // event-specific data
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Um alça para a janela.

</dd> <dt>

*Umsg* 
</dt> <dd>

O **\_ identificador WM DEVICECHANGE.**

</dd> <dt>

*wParam* 
</dt> <dd>

O evento que ocorreu. Esse parâmetro pode ser um dos valores a seguir do arquivo de header Dbt.h.

| Valor | Significado |
|-------|---------|
| **[DBT \_ DEVNODES \_ ALTERADOS](dbt-devnodes-changed.md)**</br>0x0007 | Um dispositivo foi adicionado ou removido do sistema. |
| **[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</br>0x0017 | É solicitada permissão para alterar a configuração atual (encaixe ou desencaixamento). |
| **[DBT \_ CONFIGCHANGED](dbt-configchanged.md)**</br>0x0018 | A configuração atual foi alterada devido a um encaixe ou desencaixamento. |
| **[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</br>0x0019 | Uma solicitação para alterar a configuração atual (encaixe ou desencaixamento) foi cancelada. |
| **[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)**</br>0x8000 | Um dispositivo ou parte da mídia foi inserido e agora está disponível. |
| **[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</br>0x8001 | É solicitada permissão para remover um dispositivo ou parte da mídia. Qualquer aplicativo pode negar essa solicitação e cancelar a remoção. |
| **[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</br>0x8002 | Uma solicitação para remover um dispositivo ou parte da mídia foi cancelada. |
| **[DISPOSITIVO \_ DBTREMOVEPENDING](dbt-deviceremovepending.md)**</br>0x8003 | Um dispositivo ou parte da mídia está prestes a ser removido. Não pode ser negado. |
| **[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</br>0x8004 | Um dispositivo ou parte da mídia foi removido. |
| **[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</br>0x8005 | Ocorreu um evento específico do dispositivo. |
| **[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</br>0x8006 | Ocorreu um evento personalizado. |
| **[DBT \_ USERDEFINED](dbt-userdefined.md)**</br>0xFFFF | O significado dessa mensagem é definido pelo usuário. |

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura que contém dados específicos do evento. Seu formato depende do valor do *parâmetro wParam.* Para obter mais informações, consulte a documentação de cada evento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar **TRUE** para conceder a solicitação.

Retornar **BROADCAST \_ QUERY \_ DENY** para negar a solicitação.

## <a name="remarks"></a>Comentários

Para dispositivos que oferecem recursos controláveis por software, como ejeção e bloqueio, o sistema normalmente envia uma mensagem [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) para permitir que aplicativos e drivers de dispositivo terminem o uso do dispositivo normalmente. Se o sistema remover forçosamente um dispositivo, ele poderá não enviar uma mensagem [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) antes de fazer isso.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte | Windows XP |
| Servidor mínimo com suporte | Windows Server 2003|
| Cabeçalho | <dl> <dt>Winuser.h (inclua Windows.h ou Dbt.h)</dt> </dl> |

## <a name="see-also"></a>Confira também

<dl> <dt>

[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)
</dt> <dt>

[DBT \_ CONFIGCHANGED](dbt-configchanged.md)
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

[DISPOSITIVO \_ DBTREMOVEPENDING](dbt-deviceremovepending.md)
</dt> <dt>

[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)
</dt> <dt>

[DBT \_ DEVNODES \_ ALTERADOS](dbt-devnodes-changed.md)
</dt> <dt>

[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)
</dt> <dt>

[DBT \_ USERDEFINED](dbt-userdefined.md)
</dt> </dl>
