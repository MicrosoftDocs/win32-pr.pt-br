---
title: Mensagem de WM_MOUSEACTIVATE (WinUser. h)
description: Enviado quando o cursor está em uma janela inativa e o usuário pressiona um botão do mouse. A janela pai receberá essa mensagem somente se a janela filho a passar para a função DefWindowProc.
ms.assetid: 335c0819-a655-4dd1-9511-1f148b87271c
keywords:
- Entrada de mouse e teclado de mensagem WM_MOUSEACTIVATE
topic_type:
- apiref
api_name:
- WM_MOUSEACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba74141f8d519541d1e63327179fff2f27ad403
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085424"
---
# <a name="wm_mouseactivate-message"></a>Mensagem do WM \_ MOUSEACTIVATE

Enviado quando o cursor está em uma janela inativa e o usuário pressiona um botão do mouse. A janela pai receberá essa mensagem somente se a janela filho a passar para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_MOUSEACTIVATE                0x0021
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela pai de nível superior da janela que está sendo ativada.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior Especifica o valor de teste de clique retornado pela função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como resultado do processamento da mensagem [**\_ NCHITTEST do WM**](wm-nchittest.md) . Para obter uma lista de valores de teste de clique, consulte **WM \_ NCHITTEST**.

A palavra de ordem superior especifica o identificador da mensagem do mouse gerada quando o usuário pressionou um botão do mouse. A mensagem do mouse é descartada ou postada na janela, dependendo do valor de retorno.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno especifica se a janela deve ser ativada e se o identificador da mensagem do mouse deve ser Descartado. Deve ser um dos valores a seguir.



| Código/valor de retorno                                                                                                                                          | Descrição                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**Ma \_ ATIVAR**</dt> <dt>1</dt> </dl>         | Ativa a janela e não descarta a mensagem do mouse.<br/>         |
| <dl> <dt>**Ma \_ ACTIVATEANDEAT**</dt> <dt>2</dt> </dl>   | Ativa a janela e descarta a mensagem do mouse.<br/>                 |
| <dl> <dt>**Ma \_ Noativar**</dt> <dt>3</dt> </dl>       | Não ativa a janela e não descarta a mensagem do mouse.<br/> |
| <dl> <dt>**Ma \_ NOACTIVATEANDEAT**</dt> <dt>4</dt> </dl> | Não ativa a janela, mas descarta a mensagem do mouse.<br/>         |



 

## <a name="remarks"></a>Comentários

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) passa a mensagem para a janela pai de uma janela filho antes de qualquer processamento ocorrer. A janela pai determina se a janela filho deve ser ativada. Se ele ativar a janela filho, a janela pai deverá retornar **ma \_ noactivate** ou **ma \_ NOACTIVATEANDEAT** para impedir que o sistema processe a mensagem ainda mais.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**NCHITTEST do WM \_**](wm-nchittest.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada do mouse](mouse-input.md)
</dt> </dl>

 

