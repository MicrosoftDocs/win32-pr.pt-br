---
title: Mensagem de SBM_SETRANGEREDRAW (WinUser. h)
description: Um aplicativo envia a \_ mensagem SBM SETRANGEREDRAW para um controle de barra de rolagem para definir os valores de posição mínimo e máximo e redesenhar o controle.
ms.assetid: badb58cc-9e3a-4766-a67f-631a7feb6285
keywords:
- Controles de SBM_SETRANGEREDRAW de mensagens do Windows
topic_type:
- apiref
api_name:
- SBM_SETRANGEREDRAW
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37c77a8f062ba3c7a8b73adc4338a11cdcf59442
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008850"
---
# <a name="sbm_setrangeredraw-message"></a>\_Mensagem SBM SETRANGEREDRAW

Um aplicativo envia a mensagem **SBM \_ SETRANGEREDRAW** para um controle de barra de rolagem para definir os valores de posição mínimo e máximo e redesenhar o controle.

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

[**\_SETRANGE SBM**](sbm-setrange.md)
</dt> </dl>

 

 





