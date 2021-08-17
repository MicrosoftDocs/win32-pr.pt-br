---
title: EM_NOSETFOCUS mensagem (Commctrl.h)
description: Impede que um controle de edição de linha única receba o foco do teclado. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Editar NoSetFocus.
ms.assetid: aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c
keywords:
- EM_NOSETFOCUS controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_NOSETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02ac35a30ff3deac7e9d6d227a6e8c403e6096e272ea89067dd817add9b2426e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831188"
---
# <a name="em_nosetfocus-message"></a>Mensagem EM \_ NOSETFOCUS

\[Destinado a uso interno; não recomendado para uso em aplicativos. Essa mensagem pode não ter suporte em versões futuras do Windows.\]

Impede que um controle de edição de linha única receba o foco do teclado. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ Editar NoSetFocus.**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)

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

## <a name="return-value"></a>Valor retornado

O valor de retorno não é usado.

## <a name="security-considerations"></a>Considerações de segurança

Usar essa mensagem pode comprometer a segurança do programa.

## <a name="remarks"></a>Comentários

Essa mensagem será ignorada se o controle de edição não for um controle de edição de linha única.

Depois que essa mensagem é enviada, o efeito é permanente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Editar \_ NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
</dt> <dt>

[**EM \_ TAKEFOCUS**](em-takefocus.md)
</dt> </dl>

 

 





