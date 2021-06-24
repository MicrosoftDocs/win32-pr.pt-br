---
description: Usado para definir mensagens privadas para uso por classes de janela privada, geralmente do formato OCM \_ \_ BASE+x, em que x é um valor inteiro.
ms.assetid: b1a9c0ca-349d-49d2-9b8b-ae7d3bf94c10
title: OCM__BASE (Olectl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa3713d8a7b7447430e914e2582089244a417b1c
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2021
ms.locfileid: "112588055"
---
# <a name="ocm__base"></a>BASE DO \_ OCM \_

Usado para definir mensagens privadas para uso por classes de janela privada, geralmente do formato **OCM \_ \_ BASE** x , em +  *que x* é um valor inteiro.

``` syntax
#define WM_USER                   0x0400
#define OCM__BASE                (WM_USER+0x1c00)
```

## <a name="remarks"></a>Comentários

A seguir estão os intervalos de números de mensagem.



| Intervalo                                                 | Significado                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| 0 a [**WM \_ USER**](wm-user.md)-1<br/>   | Mensagens reservadas para uso pelo sistema.<br/>            |
| [**WM \_ USUÁRIO**](wm-user.md) por meio 0x7FFF<br/> | Mensagens de inteiro para uso por classes de janela privada.<br/> |
| [**WM \_ APLICATIVO**](wm-app.md) por meio 0xBFFF<br/>   | Mensagens disponíveis para uso por aplicativos.<br/>         |
| 0xC000 por meio 0xFFFF<br/>                      | Mensagens de cadeia de caracteres para uso por aplicativos.<br/>            |
| Maior que 0xFFFF<br/>                        | Reservado pelo sistema.<br/>                             |



 

Os números de mensagem no primeiro intervalo (0 a [**WM \_ USER**](wm-user.md)  1) são definidos pelo sistema. Os valores nesse intervalo que não são definidos explicitamente são reservados pelo sistema.

Os números de mensagem no segundo intervalo ([**WM \_ USER**](wm-user.md) 0x7FFF) podem ser definidos e usados por um aplicativo para enviar mensagens dentro de uma classe de janela privada. Esses valores não podem ser usados para definir mensagens significativas em um aplicativo porque algumas classes de janela predefinidas já definem valores nesse intervalo. Por exemplo, classes de controle predefinidas como **BUTTON,** **EDIT,** **LISTBOX** e **COMBOBOX** podem usar esses valores. As mensagens nesse intervalo não devem ser enviadas a outros aplicativos, a menos que os aplicativos tenham sido projetados para trocar mensagens e anexar o mesmo significado aos números de mensagem.

Os números de mensagem no terceiro intervalo (0x8000 até 0xBFFF) estão disponíveis para que os aplicativos usem como mensagens privadas. As mensagens nesse intervalo não estão em conflito com mensagens do sistema.

Os números de mensagem no quarto intervalo (0xC000 a 0xFFFF) são definidos em tempo de 0xFFFF quando um aplicativo chama a função [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) para recuperar um número de mensagem para uma cadeia de caracteres. Todos os aplicativos que registram a mesma cadeia de caracteres podem usar o número de mensagem associado para trocar mensagens. O número real da mensagem, no entanto, não é uma constante e não pode ser presumido como o mesmo entre sessões diferentes.

Os números de mensagem no quinto intervalo (maior que 0xFFFF) são reservados pelo sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Olectl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Registerwindowmessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**APLICATIVO \_ WM**](wm-app.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Mensagens e filas de mensagens](messages-and-message-queues.md)
</dt> </dl>

 

