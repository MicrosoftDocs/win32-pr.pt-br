---
title: TBM_SETSELEND mensagem (Commctrl.h)
description: Define a posição lógica final do intervalo de seleção atual em uma barra de faixa. Essa mensagem será ignorada se a barra de faixas não tiver o estilo TBS \_ ENABLESELRANGE.
ms.assetid: 1feec14c-1607-49d5-a147-af2443f82dc1
keywords:
- TBM_SETSELEND controles de Windows mensagem
topic_type:
- apiref
api_name:
- TBM_SETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9ee524bf6a519a7d0071e4149ed03191a9aec989e2deefe596cca1072dbd098
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167061"
---
# <a name="tbm_setselend-message"></a>Mensagem TBM \_ SETSELEND

Define a posição lógica final do intervalo de seleção atual em uma barra de faixa. Essa mensagem será ignorada se a barra de faixas não tiver o [**estilo TBS \_ ENABLESELRANGE.**](trackbar-control-styles.md)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Redesenhar sinalizador. Se esse parâmetro for **TRUE,** a mensagem redesenhará a barra de faixas depois que o intervalo de seleção for definido. Se esse parâmetro for **FALSE,** a mensagem define o intervalo de seleção, mas não redesenha a barra de faixas.

</dd> <dt>

*lParam* 
</dt> <dd>

Posição lógica final do intervalo de seleção.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

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

[**TBM \_ GETSELEND**](tbm-getselend.md)
</dt> <dt>

[**TBM \_ GETSELSTART**](tbm-getselstart.md)
</dt> <dt>

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

 





