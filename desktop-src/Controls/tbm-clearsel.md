---
title: Mensagem de TBM_CLEARSEL (commctrl. h)
description: Limpa o intervalo de seleção atual em um TrackBar.
ms.assetid: ccf69fb7-d616-4a7a-8c7c-7a82827758b1
keywords:
- controles de Windows de mensagem de TBM_CLEARSEL
topic_type:
- apiref
api_name:
- TBM_CLEARSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 627f2c872b47bf76312856fd81d42bfe8f2739e53efb3c37492b203b150b8e8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046756"
---
# <a name="tbm_clearsel-message"></a>\_Mensagem tbm CLEARSEL

Limpa o intervalo de seleção atual em um TrackBar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador de redesenho. Se esse parâmetro for **true**, o TrackBar será redesenhado depois que a seleção for desmarcada.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

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

[**TBM \_ SETSEL**](tbm-setsel.md)
</dt> <dt>

[**TBM \_ SETSELEND**](tbm-setselend.md)
</dt> <dt>

[**TBM \_ SETSELSTART**](tbm-setselstart.md)
</dt> </dl>

 

 





