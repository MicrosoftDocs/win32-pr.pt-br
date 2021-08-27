---
title: Mensagem de TBM_GETSELEND (commctrl. h)
description: Recupera a posição final do intervalo de seleção atual em um TrackBar.
ms.assetid: e365dd4d-eb49-4107-b6d4-cdb558d27fdb
keywords:
- controles de Windows de mensagem de TBM_GETSELEND
topic_type:
- apiref
api_name:
- TBM_GETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff24c6b8f22aba0eb8f8f3a52d7de2bc812936525a7754bb1fa0afa4054524e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046426"
---
# <a name="tbm_getselend-message"></a>\_Mensagem tbm GETSELEND

Recupera a posição final do intervalo de seleção atual em um TrackBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 32 bits que especifica a posição final do intervalo de seleção atual.

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

[**TBM \_ GETSELSTART**](tbm-getselstart.md)
</dt> <dt>

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

 





