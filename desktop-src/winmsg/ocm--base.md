---
description: Usado para definir mensagens privadas para uso por classes de janela privada, geralmente no formato OCM \_ \_ base + x, em que x é um valor inteiro.
ms.assetid: b1a9c0ca-349d-49d2-9b8b-ae7d3bf94c10
title: OCM__BASE (OLECTL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0f159dc4eab2f6a240b3400354b58ab1e94e466522c9b91f34af0f0cc60eb70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118031196"
---
# <a name="ocm__base"></a>\_ \_ base OCM

Usado para definir mensagens privadas para uso por classes de janela privada, geralmente no formato **OCM \_ \_ base** + *x*, em que *x* é um valor inteiro.

``` syntax
#define WM_USER                   0x0400
#define OCM__BASE                (WM_USER+0x1c00)
```

## <a name="remarks"></a>Comentários

A seguir estão os intervalos de números de mensagem.



| Intervalo                                                 | Significado                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| 0 por meio do [**WM \_ usuário**](wm-user.md)-1<br/>   | Mensagens reservadas para uso pelo sistema.<br/>            |
| [**WM \_ USUÁRIO**](wm-user.md) por meio de 0x7FFF<br/> | Mensagens de inteiros para uso por classes de janela privada.<br/> |
| [**WM \_ APLICATIVO**](wm-app.md) por meio de 0xBFFF<br/>   | Mensagens disponíveis para uso por aplicativos.<br/>         |
| 0xC000 a 0xFFFF<br/>                      | Mensagens de cadeia de caracteres para uso por aplicativos.<br/>            |
| Maior que 0xFFFF<br/>                        | Reservado pelo sistema.<br/>                             |



 

Os números de mensagem no primeiro intervalo (0 [**por \_ usuário do WM**](wm-user.md)  1) são definidos pelo sistema. Os valores neste intervalo que não são definidos explicitamente são reservados pelo sistema.

Os números de mensagem no segundo intervalo [**( \_ usuário do WM**](wm-user.md) por meio de 0x7FFF) podem ser definidos e usados por um aplicativo para enviar mensagens dentro de uma classe de janela privada. Esses valores não podem ser usados para definir mensagens que são significativas em um aplicativo porque algumas classes de janela predefinidas já definem valores nesse intervalo. Por exemplo, classes de controle predefinidas como **Button**, **Edit**, **ListBox** e **ComboBox** podem usar esses valores. As mensagens neste intervalo não devem ser enviadas a outros aplicativos, a menos que os aplicativos tenham sido projetados para trocar mensagens e para anexar o mesmo significado aos números de mensagem.

Os números de mensagem no terceiro intervalo (0x8000 a 0xBFFF) estão disponíveis para que os aplicativos usem como mensagens privadas. As mensagens neste intervalo não entram em conflito com as mensagens do sistema.

Os números de mensagem no quarto intervalo (0xC000 a 0xFFFF) são definidos em tempo de execução quando um aplicativo chama a função [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) para recuperar um número de mensagem para uma cadeia de caracteres. Todos os aplicativos que registram a mesma cadeia de caracteres podem usar o número de mensagem associado para troca de mensagens. No entanto, o número da mensagem real não é uma constante e não pode ser considerado o mesmo entre sessões diferentes.

Os números de mensagem no quinto intervalo (maior que 0xFFFF) são reservados pelo sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>OLECTL. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[**aplicativo do WM \_**](wm-app.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Mensagens e filas de mensagens](messages-and-message-queues.md)
</dt> </dl>

 

