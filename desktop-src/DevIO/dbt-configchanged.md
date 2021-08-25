---
description: O sistema transmite o evento do dispositivo DBT CONFIGCHANGED para indicar que a configuração atual foi alterada, devido a um \_ encaixe ou desencaixamento. Um aplicativo ou driver que armazena dados no Registro na chave de CONFIGURAÇÃO ATUAL do HKEY \_ \_ deve atualizar os dados.
ms.assetid: e5e33970-b17e-4723-98aa-e242f90fe4e7
title: DBT_CONFIGCHANGED evento (Dbt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7e0d93b2a89793bb572a5c7563e54fa3114101443b43b8d6beac7955bdd6ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874507"
---
# <a name="dbt_configchanged-event"></a>Evento DBT \_ CONFIGCHANGED

O sistema transmite o evento do dispositivo DBT CONFIGCHANGED para indicar que a configuração atual foi alterada, devido a um \_ encaixe ou desencaixamento. Um aplicativo ou driver que armazena dados no Registro na chave de CONFIGURAÇÃO ATUAL do HKEY \_ \_ deve atualizar os dados.

Para transmitir esse evento de dispositivo, o sistema usa a mensagem [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ CONFIGCHANGED e *lParam definido* como zero.


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

Definido como DBT \_ CONFIGCHANGED.

</dd> <dt>

*lParam* 
</dt> <dd>

Definido como zero.

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

[**WM \_ DEVICECHANGE**](wm-devicechange.md)
</dt> </dl>

 

 




