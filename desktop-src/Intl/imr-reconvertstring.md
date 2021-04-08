---
description: Notifica um aplicativo quando um IME selecionado precisa de uma cadeia de caracteres para a reconversão. O aplicativo recebe esse comando por meio da \_ mensagem de solicitação IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 82ef20b5-bdfa-4bde-abb4-3d14ae35c116
title: IMR_RECONVERTSTRING código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbb1caeedb729b176f116a15e64879d79d519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828271"
---
# <a name="imr_reconvertstring-notification-code"></a>\_Código de notificação de REconversão de IMR

Notifica um aplicativo quando um IME selecionado precisa de uma cadeia de caracteres para a reconversão. O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ solicitação IME do WM**](wm-ime-request.md) com configurações de parâmetro, conforme mostrado abaixo.


```C++
LRESULT IMR_RECONVERTSTRING
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Defina como \_ Reconverter de IMR.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Ponteiro para um buffer que contém a estrutura de [**REconverterstring**](/windows/win32/api/imm/ns-imm-reconvertstring) e cadeias de caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna a estrutura da cadeia de caracteres de reconversão atual. Se *lParam* for definido como **NULL**, o aplicativo retornará o tamanho do buffer necessário para manter a estrutura. O comando retornará 0 se não tiver sucesso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>IMM. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos do Gerenciador de métodos de entrada](input-method-manager-commands.md)
</dt> <dt>

[**Reconverterstring**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**\_solicitação do IME do WM \_**](wm-ime-request.md)
</dt> </dl>

 

 




