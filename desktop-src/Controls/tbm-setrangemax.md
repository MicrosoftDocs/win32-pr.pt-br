---
title: Mensagem de TBM_SETRANGEMAX (commctrl. h)
description: Define a posição lógica máxima para o controle deslizante em um TrackBar.
ms.assetid: 8e9d8fd3-2ee3-4fb6-aa1f-9d6e999ef330
keywords:
- Controles de TBM_SETRANGEMAX de mensagens do Windows
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
ms.openlocfilehash: b43997725e2fa88db3f9d4dc2fec1d51255cbb0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454619"
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

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Se a posição do controle deslizante atual for maior que o novo máximo, a mensagem **tbm \_ SETRANGEMAX** definirá a posição do controle deslizante como o novo valor máximo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_SETRANGE tbm**](tbm-setrange.md)
</dt> <dt>

[**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)
</dt> </dl>

 

 





