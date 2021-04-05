---
title: Mensagem de SBM_GETPOS (WinUser. h)
description: A \_ mensagem SBM GETPOS é enviada para recuperar a posição atual da caixa de rolagem de um controle de barra de rolagem.
ms.assetid: 00344d93-f205-4cda-aa25-6dd065f41b6e
keywords:
- Controles de SBM_GETPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- SBM_GETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d088fc790985e57928f1ab56cd42254b1a087dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918862"
---
# <a name="sbm_getpos-message"></a>\_Mensagem SBM GETPOS

A mensagem **SBM \_ GETPOS** é enviada para recuperar a posição atual da caixa de rolagem de um controle de barra de rolagem. A posição atual é um valor relativo que depende do intervalo de rolagem atual. Por exemplo, se o intervalo de rolagem for de 0 a 100 e a caixa de rolagem estiver no meio da barra, a posição atual será 50.

Os aplicativos não devem enviar essa mensagem diretamente. Em vez disso, eles devem usar a função [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) . Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **GetScrollPos** funcione corretamente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é a posição atual da caixa de rolagem na barra de rolagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**GetRange SBM \_**](sbm-getrange.md)
</dt> <dt>

[**SBM \_ SETPOS**](sbm-setpos.md)
</dt> <dt>

[**\_SETRANGE SBM**](sbm-setrange.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

