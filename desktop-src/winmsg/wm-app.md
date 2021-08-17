---
description: Usado para definir mensagens privadas, geralmente do formulário WM \_ app + x, em que x é um valor inteiro.
ms.assetid: fdb549df-426f-4af5-9c17-6e8730e4abc0
title: WM_APP (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01c2f09bef9ef479cfa5bd0bb56760fd17196087992276b2caa1daf7616fea9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931816"
---
# <a name="wm_app"></a>aplicativo do WM \_

Usado para definir mensagens privadas, geralmente do formulário **WM \_ app** + *x*, em que *x* é um valor inteiro.

``` syntax
#define WM_APP                          0x8000
```

## <a name="remarks"></a>Comentários

A constante do **\_ aplicativo do WM** é usada para distinguir os valores de mensagem que estão reservados para uso pelo sistema e os valores que podem ser usados por um aplicativo para enviar mensagens dentro de uma classe de janela privada. A seguir estão os intervalos de números de mensagem disponíveis.



| Intervalo                                                 | Significado                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| 0 por meio do [**\_ usuário do WM**](wm-user.md) – 1<br/>   | Mensagens reservadas para uso pelo sistema.<br/>            |
| [**WM \_ USUÁRIO**](wm-user.md) por meio de 0x7FFF<br/> | Mensagens de inteiros para uso por classes de janela privada.<br/> |
| **WM \_ APLICATIVO** por meio de 0xBFFF<br/>                 | Mensagens disponíveis para uso por aplicativos.<br/>         |
| 0xC000 a 0xFFFF<br/>                      | Mensagens de cadeia de caracteres para uso por aplicativos.<br/>            |
| Maior que 0xFFFF<br/>                        | Reservado pelo sistema.<br/>                             |



 

Os números de mensagem no primeiro intervalo (0 [**por \_ usuário do WM**](wm-user.md) – 1) são definidos pelo sistema. Os valores neste intervalo que não são definidos explicitamente são reservados pelo sistema.

Os números de mensagem no segundo intervalo [**( \_ usuário do WM**](wm-user.md) por meio de 0x7FFF) podem ser definidos e usados por um aplicativo para enviar mensagens dentro de uma classe de janela privada. Esses valores não podem ser usados para definir mensagens que são significativas em um aplicativo porque algumas classes de janela predefinidas já definem valores nesse intervalo. Por exemplo, classes de controle predefinidas como **Button**, **Edit**, **ListBox** e **ComboBox** podem usar esses valores. As mensagens neste intervalo não devem ser enviadas a outros aplicativos, a menos que os aplicativos tenham sido projetados para trocar mensagens e para anexar o mesmo significado aos números de mensagem.

Os números de mensagem no terceiro intervalo (0x8000 a 0xBFFF) estão disponíveis para que os aplicativos usem como mensagens privadas. As mensagens neste intervalo não entram em conflito com as mensagens do sistema.

Os números de mensagem no quarto intervalo (0xC000 a 0xFFFF) são definidos em tempo de execução quando um aplicativo chama a função [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) para recuperar um número de mensagem para uma cadeia de caracteres. Todos os aplicativos que registram a mesma cadeia de caracteres podem usar o número de mensagem associado para troca de mensagens. No entanto, o número da mensagem real não é uma constante e não pode ser considerado o mesmo entre sessões diferentes.

Os números de mensagem no quinto intervalo (maior que 0xFFFF) são reservados pelo sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**usuário do WM \_**](wm-user.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Mensagens e filas de mensagens](messages-and-message-queues.md)
</dt> </dl>

 

 
