---
title: Mensagem de TBM_SETRANGEMIN (commctrl. h)
description: Define a posição lógica mínima para o controle deslizante em um TrackBar.
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- Controles de TBM_SETRANGEMIN de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34c2e70aa6247cb970e576c915bdcd28cd18d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917982"
---
# <a name="tbm_setrangemin-message"></a>\_Mensagem tbm SETRANGEMIN

Define a posição lógica mínima para o controle deslizante em um TrackBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador de redesenho. Se esse parâmetro for **true**, a mensagem redesenhará o TrackBar depois que o intervalo for definido. Se esse parâmetro for **false**, a mensagem definirá o intervalo, mas não redesenhará o TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>

Posição mínima do controle deslizante.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Se a posição do controle deslizante atual for menor que o novo mínimo, a mensagem **tbm \_ SETRANGEMIN** definirá a posição do controle deslizante como o novo valor mínimo.

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

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> </dl>

 

 





