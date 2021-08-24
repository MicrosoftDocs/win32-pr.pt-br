---
description: Uma mensagem enviada a todas as janelas de nível superior quando a função SystemParametersInfo altera uma configuração de todo o sistema ou quando as configurações de política foram alteradas.
ms.assetid: 77174e06-a25b-440a-9e9c-4fd5979c433c
title: WM_SETTINGCHANGE mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302f156da905263ed7f3d1d331d4dbb25af5b3e81d9df6136281c7dbc7b3914c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710036"
---
# <a name="wm_settingchange-message"></a>Mensagem WM \_ SETTINGCHANGE

Uma mensagem enviada a todas as janelas de nível superior quando a função [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) altera uma configuração de todo o sistema ou quando as configurações de política foram alteradas.

Os aplicativos **devem enviar WM \_ SETTINGCHANGE** para todas as janelas de nível superior quando fizerem alterações nos parâmetros do sistema. (Essa mensagem não pode ser enviada diretamente para uma janela.) Para enviar a **mensagem WM \_ SETTINGCHANGE** para todas as janelas de nível superior, use a função [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) com o parâmetro *hwnd* definido como **HWND \_ BROADCAST.**

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_WININICHANGE                 0x001A
#define WM_SETTINGCHANGE                WM_WININICHANGE
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Quando o sistema envia essa mensagem como resultado de uma chamada [**SystemParametersInfo,**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) o parâmetro *wParam* é o valor do parâmetro *uiAction* passado para a **função SystemParametersInfo.** Para ver uma lista de valores, consulte **SystemParametersInfo**.

Quando o sistema envia essa mensagem como resultado de uma alteração nas configurações de política, esse parâmetro indica o tipo de política que foi aplicada. Esse valor será 1 se a política de computador tiver sido aplicada ou zero se a política de usuário tiver sido aplicada.

Quando o sistema envia essa mensagem como resultado de uma alteração nas configurações de localidade, esse parâmetro é zero.

Quando um aplicativo envia essa mensagem, esse parâmetro deve ser **NULL.**

</dd> <dt>

*lParam* 
</dt> <dd>

Quando o sistema envia essa mensagem como resultado de uma chamada [**SystemParametersInfo,**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) *lParam* é um ponteiro para uma cadeia de caracteres que indica a área que contém o parâmetro do sistema que foi alterado. Esse parâmetro geralmente não indica qual parâmetro do sistema específico foi alterado. (Observe que alguns aplicativos enviam essa mensagem com *lParam definido* como **NULL**.) Em geral, ao receber essa mensagem, você deve verificar e recarregar as configurações de parâmetro do sistema usadas pelo aplicativo.

Essa cadeia de caracteres pode ser o nome de uma chave do Registro ou o nome de uma seção no Win.ini arquivo. Quando a cadeia de caracteres é um nome do Registro, ela normalmente indica apenas o nó folha no Registro, não o caminho completo.

Quando o sistema envia essa mensagem como resultado de uma alteração nas configurações de política, esse parâmetro aponta para a cadeia de caracteres "Política".

Quando o sistema envia essa mensagem como resultado de uma alteração nas configurações de localidade, esse parâmetro aponta para a cadeia de caracteres "intl".

Para efetuar uma alteração nas variáveis de ambiente do sistema ou do usuário, broadcast esta mensagem com *lParam definido* como a cadeia de caracteres "Ambiente".

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Se você processar essa mensagem, retorne zero.

## <a name="remarks"></a>Comentários

O *parâmetro lParam* indica qual métrica do sistema foi alterada, por exemplo, "ConvertibleSlateMode" se o indicador CONVERTIBLESLATEMODE foi alternado ou "SystemDockMode" se o indicador DOCKED foi alternado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de política](/previous-versions/windows/desktop/Policy/policy-events)
</dt> <dt>

[**Sendmessagetimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)
</dt> <dt>

[**Systemparametersinfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
