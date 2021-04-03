---
title: Mensagem de SBM_SETRANGE (WinUser. h)
description: A \_ mensagem SETRANGE SBM é enviada para definir os valores de posição mínima e máxima para o controle barra de rolagem.
ms.assetid: 9cf84354-3944-4c10-9b59-39427b840868
keywords:
- Controles de SBM_SETRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- SBM_SETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7a720531ae58fdb0712b8f23fd1aef88b3e4caa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824718"
---
# <a name="sbm_setrange-message"></a>\_Mensagem SETRANGE SBM

A **mensagem \_ SETRANGE SBM** é enviada para definir os valores de posição mínima e máxima para o controle barra de rolagem.

Os aplicativos não devem enviar essa mensagem diretamente. Em vez disso, eles devem usar a função [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) . Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **SetScrollRange** funcione corretamente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica a posição de rolagem mínima.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica a posição máxima da rolagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**ComCtl32.dll versão 5,0**: se a posição da caixa de rolagem foi alterada, o valor de retorno será a posição anterior da caixa de rolagem; caso contrário, será zero.

**ComCtl32.dll versão 6,0**: a posição atual da caixa de rolagem, independentemente se ela foi alterada.

## <a name="remarks"></a>Comentários

Os valores de posição mínimo e máximo padrão são zero. A diferença entre os valores especificados pelos parâmetros *wParam* e *lParam* não deve ser maior que MAXLONG.

Se os valores mínimo e máximo da posição forem iguais, o controle da barra de rolagem ficará oculto e, em vigor, desabilitado.

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

[**SBM \_ SETPOS**](sbm-setpos.md)
</dt> <dt>

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 

