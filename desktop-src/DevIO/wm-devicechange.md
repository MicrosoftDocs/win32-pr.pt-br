---
description: Notifica um aplicativo sobre uma alteração na configuração de hardware de um dispositivo ou computador.
ms.assetid: b64a3983-ee75-4199-9778-1e5b7cec59e4
title: Mensagem de WM_DEVICECHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cc45d7a7978d5501e51cc1355c43afcf12b956
ms.sourcegitcommit: 8c1942ac6731488abbeae46a7dbe3da166fee2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2021
ms.locfileid: "107581498"
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

| Valor | Significado |
|-------|---------|
| **[DBT \_ DEVNODES \_ alterado](dbt-devnodes-changed.md)**</br>0x0007 | Um dispositivo foi adicionado ou removido do sistema. |
| **[DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md)**</br>0x0017 | A permissão é solicitada para alterar a configuração atual (Dock ou desencaixar). |
| **[DBT \_ ConfigChanged](dbt-configchanged.md)**</br>0x0018 | A configuração atual foi alterada devido a um encaixe ou desencaixe. |
| **[DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md)**</br>0x0019 | Uma solicitação para alterar a configuração atual (Dock ou Dock) foi cancelada. |
| **[DBT \_ DEVICEARRIVAL](dbt-devicearrival.md)**</br>0x8000 | Um dispositivo ou parte da mídia foi inserido e agora está disponível. |
| **[DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md)**</br>0x8001 | A permissão é solicitada para remover um dispositivo ou parte da mídia. Qualquer aplicativo pode negar essa solicitação e cancelar a remoção. |
| **[DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md)**</br>0x8002 | Uma solicitação para remover um dispositivo ou parte da mídia foi cancelada. |
| **[DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md)**</br>0x8003 | Um dispositivo ou parte da mídia está prestes a ser removida. Não pode ser negado. |
| **[DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md)**</br>0x8004 | Um dispositivo ou parte da mídia foi removida. |
| **[DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md)**</br>0x8005 | Ocorreu um evento específico do dispositivo. |
| **[DBT \_ CUSTOMEVENT](dbt-customevent.md)**</br>0x8006 | Ocorreu um evento personalizado. |
| **[DBT \_ USERdefined](dbt-userdefined.md)**</br>0xFFFF | O significado dessa mensagem é definido pelo usuário. |

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
| Cliente mínimo com suporte | Windows XP |
| Servidor mínimo com suporte | Windows Server 2003|
| parâmetro | <dl> <dt>WinUser. h (incluir Windows. h ou DBT. h)</dt> </dl> |

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
