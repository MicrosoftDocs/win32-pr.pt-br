---
title: HDM_GETOVERFLOWRECT mensagem (Commctrl.h)
description: Obtém o retângulo delimitador do botão de estouro quando o estilo HDS OVERFLOW é definido no controle de header e \_ o botão de estouro fica visível. Envie essa mensagem explicitamente ou usando a macro \_ GetOverflowRect do header.
ms.assetid: 52fb3dc3-ce22-40da-8222-20fd75c005ae
keywords:
- HDM_GETOVERFLOWRECT controles Windows mensagem
topic_type:
- apiref
api_name:
- HDM_GETOVERFLOWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f48088ad6c4a1d8cc5b843eeafb167f790bdd8eac06c56e6cb74e8afc18d082
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047046"
---
# <a name="hdm_getoverflowrect-message"></a>Mensagem \_ GETOVERFLOWRECT do HDM

Obtém o retângulo delimitador do botão de estouro quando o estilo [**\_ HDS OVERFLOW**](header-control-styles.md) é definido no controle de header e o botão de estouro fica visível. Envie essa mensagem explicitamente ou usando a [**macro \_ GetOverflowRect do header.**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado. Deve ser zero.

</dd> <dt>

*lParam* \[ Em\]
</dt> <dd>

Um ponteiro para uma [**estrutura RECT**](/previous-versions//dd162897(v=vs.85)) para receber as informações de retângulo delimitadores. O remetente da mensagem é responsável por alocar essa estrutura. As coordenadas retornadas na **estrutura RECT** são expressas como coordenadas de tela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se for bem-sucedido; caso contrário, **FALSE.**

## <a name="remarks"></a>Comentários

O controle de header deve ter o estilo **HDF \_ SPLITBUTTON**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Sobre controles de header](header-controls.md)
</dt> </dl>

 

