---
title: Mensagem de WM_ENTERIDLE (WinUser. h)
description: Enviado para a janela do proprietário de uma caixa de diálogo modal ou um menu que está entrando em um estado ocioso. Uma caixa de diálogo modal ou um menu entra em estado ocioso quando nenhuma mensagem está aguardando em sua fila depois de ter processado uma ou mais mensagens anteriores.
ms.assetid: 11b1f942-185f-4de4-90a2-e2934bb1394f
keywords:
- Caixas de diálogo de WM_ENTERIDLE mensagem
topic_type:
- apiref
api_name:
- WM_ENTERIDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f99b3150a0dbc1a81b78498c8e295fbf2397c22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369805"
---
# <a name="wm_enteridle-message"></a>Mensagem do WM \_ ENTERIDLE

Enviado para a janela do proprietário de uma caixa de diálogo modal ou um menu que está entrando em um estado ocioso. Uma caixa de diálogo modal ou um menu entra em estado ocioso quando nenhuma mensagem está aguardando em sua fila depois de ter processado uma ou mais mensagens anteriores.


```C++
#define WM_ENTERIDLE                    0x0121
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                   | Significado                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="MSGF_DIALOGBOX"></span><span id="msgf_dialogbox"></span><dl> <dt>**MSGF \_ CAIXA**</dt> <dt>0</dt> </dl> | O sistema está ocioso porque uma caixa de diálogo é exibida.<br/> |
| <span id="MSGF_MENU"></span><span id="msgf_menu"></span><dl> <dt>**MSGF \_ MENU**</dt> <dt>2</dt> </dl>                | O sistema está ocioso porque um menu é exibido.<br/>       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para a caixa de diálogo (se *wParam* for **MSGF \_ caixa**) ou janela que contém o menu exibido (se *wParam* for **MSGF \_ menu**).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um aplicativo deve retornar zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

Você pode suprimir a mensagem do **WM \_ ENTERIDLE** para uma caixa de diálogo criando a caixa de diálogo com o estilo de **\_ NOIDLEMSG do DS** .

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

**Conceitua**
</dt> <dt>

[Caixas de diálogo](dialog-boxes.md)
</dt> </dl>

 

