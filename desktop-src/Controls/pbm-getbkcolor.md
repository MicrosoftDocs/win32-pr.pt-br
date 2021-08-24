---
title: Mensagem de PBM_GETBKCOLOR (commctrl. h)
description: Obtém a cor do plano de fundo da barra de progresso.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- controles de Windows de mensagem de PBM_GETBKCOLOR
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
ms.openlocfilehash: 1462d864df0440cd0567e6d6b1d04261818bb98ab4a6b5a803272e63abcb8d5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919516"
---
# <a name="pbm_getbkcolor-message"></a>Mensagem do GETBKCOLOR do PBM \_

Obtém a cor do plano de fundo da barra de progresso.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a cor do plano de fundo da barra de progresso.

## <a name="remarks"></a>Comentários

Essa é a cor definida pela mensagem [**\_ SETBKCOLOR do PBM**](pbm-setbkcolor.md) . O valor padrão é CLR \_ padrão, que é definido em commctrl. h.

Essa função afeta apenas o modo clássico, não qualquer estilo visual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





