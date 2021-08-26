---
title: Mensagem de TCM_ADJUSTRECT (commctrl. h)
description: Calcula a área de exibição de um controle guia, dado um retângulo de janela, ou calcula o retângulo da janela que corresponderia a uma área de exibição especificada. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ AdjustRect.
ms.assetid: 2f14201a-e4a3-4ae5-b9cf-4a674c52f24a
keywords:
- controles de Windows de mensagem de TCM_ADJUSTRECT
topic_type:
- apiref
api_name:
- TCM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba09a88f12a25b87f507d70961a816412f2679da0fb9e1cb6ed6c760ecca320e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105006"
---
# <a name="tcm_adjustrect-message"></a>\_Mensagem ADJUSTRECT de TCM

Calcula a área de exibição de um controle guia, dado um retângulo de janela, ou calcula o retângulo da janela que corresponderia a uma área de exibição especificada. Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Operação a ser executada. Se esse parâmetro for **true**, *lParam* especificará um retângulo de exibição e receberá o retângulo de janela correspondente. Se esse parâmetro for **false**, *lParam* especificará um retângulo de janela e receberá a área de exibição correspondente.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica o retângulo fornecido e recebe o retângulo calculado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Essa mensagem se aplica somente a controles de guia que estão na parte superior. Ele não se aplica a controles de guia que estão nos lados ou na parte inferior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

