---
title: Mensagem de TBM_GETSELSTART (commctrl. h)
description: Recupera a posição inicial do intervalo de seleção atual em um TrackBar.
ms.assetid: 0000df2a-c40d-40c2-b120-e5d4fe6c5016
keywords:
- controles de Windows de mensagem de TBM_GETSELSTART
topic_type:
- apiref
api_name:
- TBM_GETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a654bfcf8756bee5b39ec9fc97b82ffe84e8e48ba39f4ca2f9fab732d0d1962e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046416"
---
# <a name="tbm_getselstart-message"></a>\_Mensagem tbm GETSELSTART

Recupera a posição inicial do intervalo de seleção atual em um TrackBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 32 bits que especifica a posição inicial do intervalo de seleção atual.

## <a name="remarks"></a>Comentários

Um TrackBar pode ter um intervalo de seleção somente se você especificou o estilo de [**\_ ENABLESELRANGE TBS**](trackbar-control-styles.md) quando o criou.

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

[**TBM \_ GETSELEND**](tbm-getselend.md)
</dt> <dt>

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

 





