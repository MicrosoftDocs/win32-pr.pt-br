---
description: Notifica um aplicativo quando um IME está prestes a mostrar uma mensagem de erro ou outras informações. O aplicativo recebe esse comando por meio da mensagem WM \_ IME \_ NOTIFY com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: b898283a-af1a-484f-bfb8-e5d5c0ac8ee1
title: IMN_GUIDELINE de notificação (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8bbcce8c1e7a04f4474d09f221ff2e2644e84b49d98edf09c1137604b71b226
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107096"
---
# <a name="imn_guideline-notification-code"></a>Código de notificação \_ de IMN GUIDELINE

Notifica um aplicativo quando um IME está prestes a mostrar uma mensagem de erro ou outras informações. O aplicativo recebe esse comando por meio da mensagem [**WM \_ IME \_ NOTIFY**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.


```C++
IMN_GUIDELINE
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

De definido como DIRETRIZ de \_ IMN.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse comando não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Um aplicativo processa esse comando chamando a [**função ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea) para recuperar a mensagem de erro ou as informações do IME.

A janela IME exibe a mensagem de erro ou a cadeia de caracteres de informações em uma janela de informações.

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

[**ImmGetGuideLine**](/windows/desktop/api/Imm/nf-imm-immgetguidelinea)
</dt> <dt>

[**NOTIFICAÇÃO \_ DO WM IME \_**](wm-ime-notify.md)
</dt> </dl>

 

 




