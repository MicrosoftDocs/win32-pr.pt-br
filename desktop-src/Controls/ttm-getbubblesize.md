---
title: Mensagem de TTM_GETBUBBLESIZE (commctrl. h)
description: Retorna a largura e a altura de um controle ToolTip.
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- controles de Windows de mensagem de TTM_GETBUBBLESIZE
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
ms.openlocfilehash: 8354a93521b6adac9306374f5bfbc99e84738ac87f0471a22f199b7b611f100b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769376"
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

## <a name="return-value"></a>Valor retornado

Retorna a largura da dica de ferramenta na palavra inferior e a altura da palavra alta se for bem-sucedida. Caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

Se os sinalizadores de faixa de TTF \_ e de TTF \_ absoluto estiverem definidos no membro **UFlags** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) da dica de ferramenta, essa mensagem poderá ser usada para ajudar a posicionar a dica de ferramenta com precisão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





