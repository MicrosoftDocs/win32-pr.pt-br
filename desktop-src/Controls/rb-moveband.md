---
title: RB_MOVEBAND mensagem (Commctrl.h)
description: Move uma faixa de um índice para outro.
ms.assetid: bb5b45de-957e-46fb-b59a-18b55b69c395
keywords:
- RB_MOVEBAND controles de Windows mensagem
topic_type:
- apiref
api_name:
- RB_MOVEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ab45f63b46b8bb883ef9f1fd8708f915dba2a6860ef2f6fabb09e2b00bd8fe6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798536"
---
# <a name="rb_moveband-message"></a>Mensagem RB \_ MOVEBAND

Move uma faixa de um índice para outro.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice baseado em zero da banda a ser movida.

</dd> <dt>

*lParam* 
</dt> <dd>

Índice baseado em zero da nova posição de banda.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se for bem-sucedido ou zero caso contrário.

## <a name="remarks"></a>Comentários

Essa mensagem provavelmente alterará o índice de outras faixas no controle de barra de rebar. Se uma banda for movida do índice 6 para o índice 0, todas as faixas entre elas terão seu índice incrementado em um.

*lParam* nunca deve ser maior que o número de faixas menos uma. O número de faixas pode ser obtido com a [**mensagem \_ GETBANDCOUNT do RB.**](rb-getbandcount.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





