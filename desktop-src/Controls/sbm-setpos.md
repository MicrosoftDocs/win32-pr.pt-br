---
title: Mensagem de SBM_SETPOS (WinUser. h)
description: A \_ mensagem SBM SETPOS é enviada para definir a posição da caixa de rolagem (Thumb) e, se solicitado, redesenhar a barra de rolagem para refletir a nova posição da caixa de rolagem.
ms.assetid: 6b3c16ba-1cdf-41ff-8546-ba98477af334
keywords:
- Controles de SBM_SETPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- SBM_SETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a7dc99da5f4b3dbb301f15ddd722f1d664932f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455959"
---
# <a name="sbm_setpos-message"></a>\_Mensagem SBM SETPOS

A mensagem **SBM \_ SETPOS** é enviada para definir a posição da caixa de rolagem (Thumb) e, se solicitado, redesenhar a barra de rolagem para refletir a nova posição da caixa de rolagem.

Os aplicativos não devem enviar essa mensagem diretamente. Em vez disso, eles devem usar a função [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) . Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **SetScrollPos** funcione corretamente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica a nova posição da caixa de rolagem. Ele deve estar dentro do intervalo de rolagem. Se esse parâmetro estiver fora do intervalo de rolagem, o valor será arredondado para cima ou para baixo até o valor válido mais próximo.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica se a barra de rolagem deve ser redesenhada para refletir a nova posição da caixa de rolagem. Se esse parâmetro for **true**, a barra de rolagem será redesenhada. Se for **false**, a barra de rolagem não será redesenhada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**ComCtl32.dll versão 5,0**: se a posição da caixa de rolagem foi alterada, o valor de retorno será a posição anterior da caixa de rolagem; caso contrário, será zero.

**ComCtl32.dll versão 6,0**: a posição atual da caixa de rolagem, independentemente se ela foi alterada.

## <a name="remarks"></a>Comentários

Se o controle da barra de rolagem for redesenhado por uma chamada subsequente para outra função, a definição do parâmetro *lParam* como **false** será útil.

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

[**SBM \_ GETPOS**](sbm-getpos.md)
</dt> <dt>

[**GetRange SBM \_**](sbm-getrange.md)
</dt> <dt>

[**\_SETRANGE SBM**](sbm-setrange.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

