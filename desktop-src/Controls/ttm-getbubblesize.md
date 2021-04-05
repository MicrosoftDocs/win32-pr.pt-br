---
title: Mensagem de TTM_GETBUBBLESIZE (commctrl. h)
description: Retorna a largura e a altura de um controle ToolTip.
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- Controles de TTM_GETBUBBLESIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_GETBUBBLESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48b48bda0f795473cb48303e88bbf3c1c35df7cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085579"
---
# <a name="ttm_getbubblesize-message"></a>TTM \_ GETbubbleize mensagem

Retorna a largura e a altura de um controle ToolTip.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para a estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) da dica de ferramenta.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a largura da dica de ferramenta na palavra inferior e a altura da palavra alta se for bem-sucedida. Caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Se os sinalizadores de faixa de TTF \_ e de TTF \_ absoluto estiverem definidos no membro **UFlags** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) da dica de ferramenta, essa mensagem poderá ser usada para ajudar a posicionar a dica de ferramenta com precisão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





