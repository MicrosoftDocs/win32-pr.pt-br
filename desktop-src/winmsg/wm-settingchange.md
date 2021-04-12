---
description: Uma mensagem que é enviada para todas as janelas de nível superior quando a função SystemParametersInfo altera uma configuração de todo o sistema ou quando as configurações de política são alteradas.
ms.assetid: 77174e06-a25b-440a-9e9c-4fd5979c433c
title: Mensagem de WM_SETTINGCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c3d1360b5e4cc5de2dbd23b09b8f2ad034948f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171699"
---
# <a name="wm_settingchange-message"></a>Mensagem do WM \_ SETTINGCHANGE

Uma mensagem que é enviada para todas as janelas de nível superior quando a função [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) altera uma configuração de todo o sistema ou quando as configurações de política são alteradas.

Os aplicativos devem enviar o **WM \_ SETTINGCHANGE** para todas as janelas de nível superior quando fizerem alterações nos parâmetros do sistema. (Esta mensagem não pode ser enviada diretamente a uma janela.) Para enviar a mensagem do **WM \_ SETTINGCHANGE** para todas as janelas de nível superior, use a função [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) com o parâmetro *HWND* definido como a **\_ difusão HWND**.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_WININICHANGE                 0x001A
#define WM_SETTINGCHANGE                WM_WININICHANGE
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Quando o sistema envia essa mensagem como resultado de uma chamada [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) , o parâmetro *wParam* é o valor do parâmetro *UiAction* passado para a função **SystemParametersInfo** . Para obter uma lista de valores, consulte **SystemParametersInfo**.

Quando o sistema envia essa mensagem como resultado de uma alteração nas configurações de política, esse parâmetro indica o tipo de política que foi aplicada. Esse valor será 1 se a política do computador tiver sido aplicada ou zero se a política do usuário tiver sido aplicada.

Quando o sistema envia essa mensagem como resultado de uma alteração nas configurações de localidade, esse parâmetro é zero.

Quando um aplicativo envia essa mensagem, esse parâmetro deve ser **nulo**.

</dd> <dt>

*lParam* 
</dt> <dd>

Quando o sistema envia essa mensagem como resultado de uma chamada [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) , *lParam* é um ponteiro para uma cadeia de caracteres que indica a área que contém o parâmetro do sistema que foi alterado. Esse parâmetro geralmente não indica qual parâmetro de sistema específico foi alterado. (Observe que alguns aplicativos enviam essa mensagem com *lParam* definido como **NULL**.) Em geral, ao receber essa mensagem, você deve verificar e recarregar as configurações de parâmetro do sistema que são usadas pelo seu aplicativo.

Essa cadeia de caracteres pode ser o nome de uma chave do registro ou o nome de uma seção no arquivo Win.ini. Quando a cadeia de caracteres é um nome de registro, ela normalmente indica apenas o nó folha no registro, não o caminho completo.

Quando o sistema envia essa mensagem como resultado de uma alteração nas configurações de política, esse parâmetro aponta para a cadeia de caracteres "Policy".

Quando o sistema envia essa mensagem como resultado de uma alteração nas configurações de localidade, esse parâmetro aponta para a cadeia de caracteres "intl".

Para afetar uma alteração nas variáveis de ambiente do sistema ou do usuário, transmita essa mensagem com *lParam* definido para a cadeia de caracteres "Environment".

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Se você processar essa mensagem, retornará zero.

## <a name="remarks"></a>Comentários

O parâmetro *lParam* indica qual métrica do sistema foi alterada, por exemplo, "ConvertibleSlateMode" se o indicador ConvertibleSlateMode foi alternado ou "SystemDockMode" se o indicador encaixado foi alternado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de política](/previous-versions/windows/desktop/Policy/policy-events)
</dt> <dt>

[**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
