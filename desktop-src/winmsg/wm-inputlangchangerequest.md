---
description: Postado na janela com o foco quando o usuário escolhe um novo idioma de entrada, seja com a tecla de atalho (especificada no aplicativo do painel de controle teclado) ou do indicador na barra de tarefas do sistema.
ms.assetid: db38c31c-6ae4-4401-82b8-7fd220c1678c
title: Mensagem de WM_INPUTLANGCHANGEREQUEST (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df361c479978083c29281764e65c48b131c22b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761178"
---
# <a name="wm_inputlangchangerequest-message"></a>Mensagem do WM \_ INPUTLANGCHANGEREQUEST

Postado na janela com o foco quando o usuário escolhe um novo idioma de entrada, seja com a tecla de atalho (especificada no aplicativo do painel de controle teclado) ou do indicador na barra de tarefas do sistema. Um aplicativo pode aceitar a alteração passando a mensagem para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ou rejeitar a alteração (e impedir que ela aconteça) retornando imediatamente.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_INPUTLANGCHANGEREQUEST       0x0050
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A nova localidade de entrada. Esse parâmetro pode ser uma combinação dos sinalizadores a seguir.



| Valor                                                                                                                                                                                                                                                            | Significado                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INPUTLANGCHANGE_BACKWARD"></span><span id="inputlangchange_backward"></span><dl> <dt>**INPUTLANGCHANGE \_**</dt> <dt>0x0004</dt> retroativa </dl>       | Uma tecla de acesso foi usada para escolher a localidade de entrada anterior na lista instalada de localidades de entrada. Esse sinalizador não pode ser usado com o \_ sinalizador de encaminhamento INPUTLANGCHANGE.<br/> |
| <span id="INPUTLANGCHANGE_FORWARD"></span><span id="inputlangchange_forward"></span><dl> <dt>**INPUTLANGCHANGE \_ Encaminhar**</dt> <dt>0x0002</dt> </dl>          | Uma tecla de acesso foi usada para escolher a próxima localidade de entrada na lista instalada de localidades de entrada. Esse sinalizador não pode ser usado com o \_ sinalizador de retrocesso INPUTLANGCHANGE.<br/>    |
| <span id="INPUTLANGCHANGE_SYSCHARSET"></span><span id="inputlangchange_syscharset"></span><dl> <dt>**INPUTLANGCHANGE \_ SYSCHARSET**</dt> <dt>0x0001</dt> </dl> | O layout de teclado da nova localidade de entrada pode ser usado com o conjunto de caracteres do sistema.<br/>                                                                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

O identificador de localidade de entrada. Para obter mais informações, consulte [idiomas, localidades e layouts de teclado](../inputdev/about-keyboard-input.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Essa mensagem é postada, não enviada, para o aplicativo, portanto, o valor de retorno é ignorado. Para aceitar a alteração, o aplicativo deve passar a mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Para rejeitar a alteração, o aplicativo deve retornar zero sem chamar **DefWindowProc**.

## <a name="remarks"></a>Comentários

Quando a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) recebe a **mensagem \_ INPUTLANGCHANGEREQUEST do WM** , ela ativa a nova localidade de entrada e notifica o aplicativo sobre a alteração enviando a mensagem [**\_ INPUTLANGCHANGE do WM**](wm-inputlangchange.md) .

O indicador de idioma estará presente na barra de tarefas somente se você tiver instalado mais de um layout de teclado e se tiver habilitado o indicador usando o aplicativo painel de controle do teclado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**INPUTLANGCHANGE do WM \_**](wm-inputlangchange.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
