---
title: TCM_SETITEMEXTRA mensagem (Commctrl.h)
description: Define o número de bytes por guia reservado para dados definidos pelo aplicativo em um controle de tabulação. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ SetItemExtra.
ms.assetid: 8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4
keywords:
- TCM_SETITEMEXTRA controles Windows mensagem
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
ms.openlocfilehash: f92fb85f7133053392bee39119c91b55240f84f0a51c8acc7dc9c732b596526c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104756"
---
# <a name="tcm_setitemextra-message"></a>Mensagem TCM \_ SETITEMEXTRA

Define o número de bytes por guia reservado para dados definidos pelo aplicativo em um controle de tabulação. Você pode enviar essa mensagem explicitamente ou usando a [**macro TabCtrl \_ SetItemExtra.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemextra)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de bytes extras.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="remarks"></a>Comentários

Por padrão, o número de bytes extras é quatro. Um aplicativo que altera o número de bytes extras não pode usar a estrutura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) para recuperar e definir os dados definidos pelo aplicativo para uma guia. Em vez disso, você deve definir uma nova estrutura que consiste na [**estrutura TCITEMHEADER**](/windows/win32/api/commctrl/ns-commctrl-tcitemheadera) seguida por membros definidos pelo aplicativo.

Um aplicativo só deve alterar o número de bytes extras quando um controle de tabulação não contém nenhuma guia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





