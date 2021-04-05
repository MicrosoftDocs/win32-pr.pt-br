---
title: Mensagem de TCM_SETITEMEXTRA (commctrl. h)
description: Define o número de bytes por tabulação reservados para dados definidos pelo aplicativo em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ SetItemExtra.
ms.assetid: 8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4
keywords:
- Controles de TCM_SETITEMEXTRA de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETITEMEXTRA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6c7fdb47483ae0ddc841ae5f79b8f913e6a4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085151"
---
# <a name="tcm_setitemextra-message"></a>\_Mensagem SETITEMEXTRA de TCM

Define o número de bytes por tabulação reservados para dados definidos pelo aplicativo em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ SetItemExtra**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de bytes extras.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Por padrão, o número de bytes extras é quatro. Um aplicativo que altera o número de bytes extras não pode usar a estrutura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) para recuperar e definir os dados definidos pelo aplicativo para uma guia. Em vez disso, você deve definir uma nova estrutura que consiste na estrutura [**TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) seguida por membros definidos pelo aplicativo.

Um aplicativo só deve alterar o número de bytes extras quando um controle guia não contiver nenhuma tabulação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





