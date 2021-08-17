---
description: Notifica um aplicativo quando o IME precisa alterar a estrutura RECONVERTSTRING. O aplicativo recebe esse comando por meio da mensagem SOLICITAÇÃO do WM \_ IME \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 035a7072-d292-4883-bc3e-d1e9ed64d9ec
title: IMR_CONFIRMRECONVERTSTRING de notificação (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a0fd1c38c7552d09489c51b9acc897f679aa3a218e86bbba222225fcff57e90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948793"
---
# <a name="imr_confirmreconvertstring-notification-code"></a>Código de \_ notificação IMR CONFIRMRECONVERTSTRING

Notifica um aplicativo quando o IME precisa alterar a [**estrutura RECONVERTSTRING.**](/windows/win32/api/imm/ns-imm-reconvertstring) O aplicativo recebe esse comando por meio da mensagem [**SOLICITAÇÃO do WM \_ IME \_**](wm-ime-request.md) com configurações de parâmetro, conforme mostrado abaixo.


```C++
LRESULT IMR_CONFIRMRECONVERTSTRING
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

De definido como IMR \_ CONFIRMRECONVERTSTRING.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Ponteiro para uma [**estrutura RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) do IME. Para obter mais informações, consulte a seção Comentários.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará um valor diferente de zero se o aplicativo aceitar a estrutura [**RECONVERTSTRING alterada.**](/windows/win32/api/imm/ns-imm-reconvertstring) Caso contrário, o comando retornará 0 e o IME usará a estrutura **RECONVERTSTRING** original.

## <a name="remarks"></a>Comentários

O aplicativo preenche a estrutura [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) ao receber o comando [IMR \_ RECONVERTSTRING.](imr-reconvertstring.md)

Depois que o aplicativo tiver tratado [IMR \_ RECONVERTSTRING](imr-reconvertstring.md), o IME poderá ou não ajustar a [**estrutura RECONVERTSTRING.**](/windows/win32/api/imm/ns-imm-reconvertstring) O IME envia a SOLICITAÇÃO do WM IME com \_ \_ **IMR \_ CONFIRMRECONVERTSTRING** para confirmar as alterações na **estrutura RECONVERTSTRING.** Se o aplicativo retornar **TRUE** para **IMR \_ CONFIRMRECONVERTSTRING**, o IME gerará uma nova cadeia de caracteres de composição com base na estrutura **RECONVERTSTRING** para o comando **IMR \_ CONFIRMRECONVERTSTRING.** Se o aplicativo retornar **FALSE** para **IMR \_ CONFIRMRECONVERTSTRING**, o IME gerará uma nova cadeia de caracteres de composição com base na estrutura **RECONVERTSTRING** original especificada pelo aplicativo no comando IMR \_ RECONVERTSTRING.

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

[IMR \_ RECONVERTSTRING](imr-reconvertstring.md)
</dt> <dt>

[**Reconvertstring**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**SOLICITAÇÃO \_ DO WM IME \_**](wm-ime-request.md)
</dt> </dl>

 

 




