---
title: Mensagem de PGM_GETPOS (commctrl. h)
description: Recupera a posição de rolagem atual do controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetPos do pager.
ms.assetid: 1e0f967a-3290-43b7-b812-8cf56abf2d32
keywords:
- Controles de PGM_GETPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611a27e9cb952c5be190fa041af3d238f0184b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755426"
---
# <a name="pgm_getpos-message"></a>\_Mensagem GETPOS do PGM

Recupera a posição de rolagem atual do controle de pager. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetPos do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor INT que contém a posição de rolagem atual, em pixels.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





