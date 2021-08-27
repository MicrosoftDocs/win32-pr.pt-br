---
title: Mensagem de PGM_GETBORDER (commctrl. h)
description: Recupera o tamanho da borda atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetBorder do pager.
ms.assetid: 5d2f49ad-d940-4a0b-b5a0-05d742151b1c
keywords:
- controles de Windows de mensagem de PGM_GETBORDER
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
ms.openlocfilehash: 148b3d840548116d3082e27b5a760650c5802bdb2c6dbc1fc7c94f1df3a3d5b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046856"
---
# <a name="pgm_getborder-message"></a>\_Mensagem GETborder do PGM

Recupera o tamanho da borda atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetBorder do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor INT que contém o tamanho da borda atual, em pixels.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SetBorder do PGM \_**](pgm-setborder.md)
</dt> </dl>

 

 





