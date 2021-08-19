---
description: Notifica um aplicativo quando a fonte do contexto de entrada é atualizada. O aplicativo recebe esse comando por meio da \_ mensagem de notificação do IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 946bee83-91af-4647-9b22-96d42466352c
title: IMN_SETCOMPOSITIONFONT código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a5ec4fd5ba8237a1fbba9be3878037c37dc74c2e07f29026ca89ead91512f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949186"
---
# <a name="imn_setcompositionfont-notification-code"></a>Código de notificação do IMN \_ SETCOMPOSITIONFONT

Notifica um aplicativo quando a fonte do contexto de entrada é atualizada. O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ notificação do IME do WM**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.


```C++
IMN_SETCOMPOSITIONFONT
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Defina como IMN \_ SETCOMPOSITIONFONT.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Este comando não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

O aplicativo pode obter informações sobre a fonte usando a função [**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta) . A janela do IME subseqüentemente usa a fonte para desenhar a cadeia de caracteres de composição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>Imm. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos do Gerenciador de métodos de entrada](input-method-manager-commands.md)
</dt> <dt>

[**ImmGetCompositionFont**](/windows/desktop/api/Imm/nf-imm-immgetcompositionfonta)
</dt> <dt>

[**\_notificação do IME do WM \_**](wm-ime-notify.md)
</dt> </dl>

 

 




