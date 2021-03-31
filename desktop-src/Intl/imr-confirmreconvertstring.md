---
description: Notifica um aplicativo quando o IME precisa alterar a estrutura reconverterstring. O aplicativo recebe esse comando por meio da \_ mensagem de solicitação IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 035a7072-d292-4883-bc3e-d1e9ed64d9ec
title: IMR_CONFIRMRECONVERTSTRING código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c500a155be14f447bb07ad506e12d5bece66e225
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662153"
---
# <a name="imr_confirmreconvertstring-notification-code"></a>Código de notificação do IMR \_ CONFIRMRECONVERTSTRING

Notifica um aplicativo quando o IME precisa alterar a estrutura [**REconverterstring**](/windows/win32/api/imm/ns-imm-reconvertstring) . O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ solicitação IME do WM**](wm-ime-request.md) com configurações de parâmetro, conforme mostrado abaixo.


```C++
LRESULT IMR_CONFIRMRECONVERTSTRING
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Defina como IMR \_ CONFIRMRECONVERTSTRING.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Ponteiro para uma estrutura [**REconverterstring**](/windows/win32/api/imm/ns-imm-reconvertstring) do IME. Para obter mais informações, consulte a seção Comentários.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um valor diferente de zero se o aplicativo aceita a estrutura [**REconverterstring**](/windows/win32/api/imm/ns-imm-reconvertstring) alterada. Caso contrário, o comando retornará 0 e o IME usará a estrutura **REconverterstring** original.

## <a name="remarks"></a>Comentários

O aplicativo preenche a estrutura [**REconverterstring**](/windows/win32/api/imm/ns-imm-reconvertstring) após receber o comando [IMR \_ reconverterstring](imr-reconvertstring.md) .

Depois que o aplicativo tratou de [IMR \_ reconverterstring](imr-reconvertstring.md), o IME pode ou não ajustar a estrutura [**reconverterstring**](/windows/win32/api/imm/ns-imm-reconvertstring) . O IME envia a \_ solicitação de IME do WM \_ com o **IMR \_ CONFIRMRECONVERTSTRING** para confirmar as alterações na estrutura **reconverterstring** . Se o aplicativo retornar **true** para **IMR \_ CONFIRMRECONVERTSTRING**, o IME gerará uma nova cadeia de caracteres de composição com base na estrutura **reconverterstring** para o comando **IMR \_ CONFIRMRECONVERTSTRING** . Se o aplicativo retornar **false** para **IMR \_ CONFIRMRECONVERTSTRING**, o IME gerará uma nova cadeia de caracteres de composição com base na estrutura **reconverterstring** original especificada pelo aplicativo no \_ comando IMR reconverterstring.

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

[Reconverter de IMR \_](imr-reconvertstring.md)
</dt> <dt>

[**Reconverterstring**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**\_solicitação do IME do WM \_**](wm-ime-request.md)
</dt> </dl>

 

 




