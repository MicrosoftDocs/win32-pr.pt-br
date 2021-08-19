---
title: TBM_SETSELSTART mensagem (Commctrl.h)
description: Define a posição lógica inicial do intervalo de seleção atual em uma barra de faixa. Essa mensagem será ignorada se a barra de faixas não tiver o estilo TBS \_ ENABLESELRANGE.
ms.assetid: eec1019c-6dbe-48c4-9c9d-72d657e80b83
keywords:
- TBM_SETSELSTART controles de Windows mensagem
topic_type:
- apiref
api_name:
- TBM_SETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f8cfdc938da5c7f5904e79f55177fe6f8eccba10f37dfdadb613c581cc809fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829310"
---
# <a name="tbm_setselstart-message"></a>Mensagem TBM \_ SETSELSTART

Define a posição lógica inicial do intervalo de seleção atual em uma barra de faixa. Essa mensagem será ignorada se a barra de faixas não tiver o [**estilo TBS \_ ENABLESELRANGE.**](trackbar-control-styles.md)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Redesenhar sinalizador. Se esse parâmetro for **TRUE,** a mensagem redesenhará a barra de faixas depois que o intervalo de seleção for definido. Se esse parâmetro for **FALSE,** a mensagem define o intervalo de seleção, mas não redesenha a barra de faixas.

</dd> <dt>

*lParam* 
</dt> <dd>

Posição inicial do intervalo de seleção.

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

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> </dl>

 

 





