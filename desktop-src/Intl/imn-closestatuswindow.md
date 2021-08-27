---
description: Notifica um aplicativo quando um IME está prestes a fechar a janela de status. O aplicativo recebe esse comando por meio da mensagem WM \_ IME \_ NOTIFY com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: d59fdf76-50e7-4a59-b1bd-a12cdb0026f6
title: IMN_CLOSESTATUSWINDOW de notificação (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a56093e5dac9c5b9b236c6819a627c1d8c1fc05aa8350824577f29f64c007e71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107156"
---
# <a name="imn_closestatuswindow-notification-code"></a>Código de notificação IMN \_ CLOSESTATUSWINDOW

Notifica um aplicativo quando um IME está prestes a fechar a janela de status. O aplicativo recebe esse comando por meio da mensagem [**WM \_ IME \_ NOTIFY**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.


```C++
IMN_CLOSESTATUSWINDOW
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

De definido como IMN \_ CLOSESTATUSWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse comando não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Um aplicativo deverá processar esse comando se ele exibir a janela de status para o IME.

A janela IME fecha a janela de status quando processa esse comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>Imm.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de Métodos de Entrada](input-method-manager.md)
</dt> <dt>

[Comandos do Gerenciador de Métodos de Entrada](input-method-manager-commands.md)
</dt> <dt>

[**NOTIFICAÇÃO \_ DO WM IME \_**](wm-ime-notify.md)
</dt> </dl>

 

 




