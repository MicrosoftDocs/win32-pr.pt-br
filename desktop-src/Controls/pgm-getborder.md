---
title: Mensagem de PGM_GETBORDER (commctrl. h)
description: Recupera o tamanho da borda atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetBorder do pager.
ms.assetid: 5d2f49ad-d940-4a0b-b5a0-05d742151b1c
keywords:
- Controles de PGM_GETBORDER de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_GETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be510af44c9cf53000420531843a79e9856c40dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753791"
---
# <a name="pgm_getborder-message"></a>\_Mensagem GETborder do PGM

Recupera o tamanho da borda atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetBorder do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor INT que contém o tamanho da borda atual, em pixels.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SetBorder do PGM \_**](pgm-setborder.md)
</dt> </dl>

 

 





