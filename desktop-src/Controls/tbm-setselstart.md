---
title: Mensagem de TBM_SETSELSTART (commctrl. h)
description: Define a posição lógica inicial do intervalo de seleção atual em um TrackBar. Essa mensagem será ignorada se o TrackBar não tiver o \_ estilo ENABLESELRANGE TBS.
ms.assetid: eec1019c-6dbe-48c4-9c9d-72d657e80b83
keywords:
- Controles de TBM_SETSELSTART de mensagens do Windows
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
ms.openlocfilehash: 445cb97c73f8e6483b5d4dd76bc3ccf64322e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008847"
---
# <a name="tbm_setselstart-message"></a>\_Mensagem tbm SETSELSTART

Define a posição lógica inicial do intervalo de seleção atual em um TrackBar. Essa mensagem será ignorada se o TrackBar não tiver o [**estilo \_ ENABLESELRANGE TBS**](trackbar-control-styles.md) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador de redesenho. Se esse parâmetro for **true**, a mensagem redesenhará o TrackBar depois que o intervalo de seleção for definido. Se esse parâmetro for **false**, a mensagem definirá o intervalo de seleção, mas não redesenhará o TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>

Posição inicial do intervalo de seleção.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

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

[**TBM \_ GETSELEND**](tbm-getselend.md)
</dt> <dt>

[**TBM \_ GETSELSTART**](tbm-getselstart.md)
</dt> <dt>

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> </dl>

 

 





