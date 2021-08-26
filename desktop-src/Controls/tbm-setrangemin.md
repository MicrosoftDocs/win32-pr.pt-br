---
title: TBM_SETRANGEMIN mensagem (Commctrl.h)
description: Define a posição lógica mínima para o controle deslizante em uma barra de faixa.
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- TBM_SETRANGEMIN controles Windows mensagem
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
ms.openlocfilehash: d35cbb162b42636d886cb5e41eb9ba6de1a2101a8327ff8ddffbc71c57fa6735
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046066"
---
# <a name="tbm_setrangemin-message"></a>Mensagem TBM \_ SETRANGEMIN

Define a posição lógica mínima para o controle deslizante em uma barra de faixa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Redesenhar sinalizador. Se esse parâmetro for **TRUE,** a mensagem redesenhará a barra de faixas depois que o intervalo for definido. Se esse parâmetro for **FALSE,** a mensagem define o intervalo, mas não redesenha a barra de faixa.

</dd> <dt>

*lParam* 
</dt> <dd>

Posição mínima para o controle deslizante.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Se a posição atual do controle deslizante for menor que o novo mínimo, a mensagem **\_ SETRANGEMIN TBM** definirá a posição do controle deslizante como o novo valor mínimo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**TBM \_ SETRANGE**](tbm-setrange.md)
</dt> <dt>

[**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)
</dt> </dl>

 

 





