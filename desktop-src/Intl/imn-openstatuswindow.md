---
description: Notifica um aplicativo quando um IME está prestes a criar a janela de status. O aplicativo recebe esse comando por meio da mensagem WM \_ IME \_ NOTIFY com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: bbd85c72-aa78-4e1d-8a7a-490650b2d782
title: IMN_OPENSTATUSWINDOW de notificação (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1726ca2433f450f92ddf7da4752b1a53b23e4176b8f0c6f14d03f6fa279f9daa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107106"
---
# <a name="imn_openstatuswindow-notification-code"></a>Código de notificação IMN \_ OPENSTATUSWINDOW

Notifica um aplicativo quando um IME está prestes a criar a janela de status. O aplicativo recebe esse comando por meio da mensagem [**WM \_ IME \_ NOTIFY**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.


```C++
IMN_OPENSTATUSWINDOW
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

De definido como IMN \_ OPENSTATUSWINDOW.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse comando não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Um aplicativo processa esse comando para exibir a janela de status para o IME por si só.

A janela IME cria uma janela de status quando processa esse comando e define as cadeias de caracteres a exibir na janela no contexto de entrada. Os aplicativos podem obter informações sobre a janela de status usando a [**função ImmGetConversionStatus.**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)

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

[**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus)
</dt> <dt>

[**NOTIFICAÇÃO \_ DO WM IME \_**](wm-ime-notify.md)
</dt> </dl>

 

 




