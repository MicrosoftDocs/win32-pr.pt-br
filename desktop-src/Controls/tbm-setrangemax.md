---
title: Mensagem de TBM_SETRANGEMAX (commctrl. h)
description: Define a posição lógica máxima para o controle deslizante em um TrackBar.
ms.assetid: 8e9d8fd3-2ee3-4fb6-aa1f-9d6e999ef330
keywords:
- controles de Windows de mensagem de TBM_SETRANGEMAX
topic_type:
- apiref
api_name:
- TBM_SETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f26b4a588e67164b96db8256116466206d0274a5bc64caedbcb1ccf25135ce62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829589"
---
# <a name="tbm_setrangemax-message"></a>\_Mensagem tbm SETRANGEMAX

Define a posição lógica máxima para o controle deslizante em um TrackBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador de redesenho. Se esse parâmetro for **true**, o TrackBar será redesenhado depois que o intervalo for definido. Se esse parâmetro for **false**, a mensagem definirá o intervalo, mas não redesenhará o TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>

Posição máxima do controle deslizante.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Se a posição do controle deslizante atual for maior que o novo máximo, a mensagem **tbm \_ SETRANGEMAX** definirá a posição do controle deslizante como o novo valor máximo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_SETRANGE tbm**](tbm-setrange.md)
</dt> <dt>

[**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)
</dt> </dl>

 

 





