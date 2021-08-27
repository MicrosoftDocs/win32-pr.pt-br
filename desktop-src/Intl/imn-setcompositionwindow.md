---
description: Notifica um aplicativo quando o estilo ou a posição da janela de composição é atualizado. O aplicativo recebe esse comando por meio da mensagem WM \_ IME \_ NOTIFY com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 07a9f0f6-587e-47c6-8f18-b48bdab0a541
title: IMN_SETCOMPOSITIONWINDOW de notificação (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fed8e69c03250166e155b07d34a2ce19b5d5fd9336af6cf82133c258c2b88d46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107046"
---
# <a name="imn_setcompositionwindow-notification-code"></a>Código de notificação \_ IMN SETCOMPOSITIONWINDOW

Notifica um aplicativo quando o estilo ou a posição da janela de composição é atualizado. O aplicativo recebe esse comando por meio da mensagem [**WM \_ IME \_ NOTIFY**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.


```C++
IMN_SETCOMPOSITIONWINDOW
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

De definido como IMN \_ SETCOMPOSITIONWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse comando não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

O aplicativo pode obter informações sobre o formulário de composição usando o comando [**\_ GETCOMPOSITIONWINDOW do IMC.**](imc-getcompositionwindow.md)

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

[**IMC \_ GETCOMPOSITIONWINDOW**](imc-getcompositionwindow.md)
</dt> <dt>

[**NOTIFICAÇÃO \_ DO WM IME \_**](wm-ime-notify.md)
</dt> </dl>

 

 




