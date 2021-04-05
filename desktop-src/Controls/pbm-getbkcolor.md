---
title: Mensagem de PBM_GETBKCOLOR (commctrl. h)
description: Obtém a cor do plano de fundo da barra de progresso.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- Controles de PBM_GETBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- PBM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2240025629bbcc242ea7ed47be2e3db42ae73b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824588"
---
# <a name="pbm_getbkcolor-message"></a>Mensagem do GETBKCOLOR do PBM \_

Obtém a cor do plano de fundo da barra de progresso.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a cor do plano de fundo da barra de progresso.

## <a name="remarks"></a>Comentários

Essa é a cor definida pela mensagem [**\_ SETBKCOLOR do PBM**](pbm-setbkcolor.md) . O valor padrão é CLR \_ padrão, que é definido em commctrl. h.

Essa função afeta apenas o modo clássico, não qualquer estilo visual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





