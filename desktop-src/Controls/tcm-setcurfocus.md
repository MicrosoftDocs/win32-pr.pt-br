---
title: Mensagem de TCM_SETCURFOCUS (commctrl. h)
description: Define o foco para uma guia especificada em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ SetCurFocus.
ms.assetid: bcbd5f26-b54e-492b-aff3-357b8ae23969
keywords:
- Controles de TCM_SETCURFOCUS de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe566d1e1b3cc7d257c4756fe123423fc344a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918478"
---
# <a name="tcm_setcurfocus-message"></a>\_Mensagem SETCURFOCUS de TCM

Define o foco para uma guia especificada em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ SetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setcurfocus) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice da guia que obtém o foco.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Se o controle guia tiver o estilo de [**\_ botões de TCS**](tab-control-styles.md) (modo de botão), a guia com o foco poderá ser diferente da guia selecionada. Por exemplo, quando uma guia é selecionada, o usuário pode pressionar as teclas de seta para definir o foco para uma guia diferente sem alterar a guia selecionada. No modo de botão, o **TCM \_ SETCURFOCUS** define o foco de entrada para o botão associado à guia especificada, mas não altera a guia selecionada.

Se o controle guia não tiver o estilo [**de \_ botões de TCS**](tab-control-styles.md) , alterar o foco também alterará a guia selecionada. Nesse caso, o controle guia envia os códigos de notificação [TCN \_ SELCHANGING](tcn-selchanging.md) e [TCN \_ SELCHANGE](tcn-selchange.md) para sua janela pai.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_GETCURFOCUS TCM**](tcm-getcurfocus.md)
</dt> </dl>

 

 





