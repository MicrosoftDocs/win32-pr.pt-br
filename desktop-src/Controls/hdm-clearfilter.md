---
title: Mensagem de HDM_CLEARFILTER (commctrl. h)
description: Limpa o filtro de um determinado controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ClearFilter do cabeçalho.
ms.assetid: 74c0265e-68d1-4414-8fd9-20f5f041d4b4
keywords:
- Controles de HDM_CLEARFILTER de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_CLEARFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b1184432517761a567cd76bdd488e4593b1e999
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085826"
---
# <a name="hdm_clearfilter-message"></a>\_Mensagem HDM CLEARFILTER

Limpa o filtro de um determinado controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ ClearFilter do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um valor de coluna que indica qual filtro deve ser limpo.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um número inteiro. O **LRESULT** é convertido em um inteiro que indica **true**(1) ou **false**(0).

## <a name="remarks"></a>Comentários

Se o valor da coluna for especificado como-1, todos os filtros serão limpos e a notificação [HDN \_ FILTERCHANGE](hdn-filterchange.md) será enviada apenas uma vez.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ClearAllFilters de cabeçalho \_**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)
</dt> </dl>

 

 





