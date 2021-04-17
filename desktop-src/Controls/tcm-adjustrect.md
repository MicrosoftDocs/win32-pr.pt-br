---
title: Mensagem de TCM_ADJUSTRECT (commctrl. h)
description: Calcula a área de exibição de um controle guia, dado um retângulo de janela, ou calcula o retângulo da janela que corresponderia a uma área de exibição especificada. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ AdjustRect.
ms.assetid: 2f14201a-e4a3-4ae5-b9cf-4a674c52f24a
keywords:
- Controles de TCM_ADJUSTRECT de mensagens do Windows
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
ms.openlocfilehash: c9c1612a4f6c2fc436f858807fca59112c376a35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749304"
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

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Essa mensagem se aplica somente a controles de guia que estão na parte superior. Ele não se aplica a controles de guia que estão nos lados ou na parte inferior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

