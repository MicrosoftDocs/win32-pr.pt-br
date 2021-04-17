---
title: Mensagem de SB_SETBKCOLOR (commctrl. h)
description: Define a cor do plano de fundo em uma barra de status.
ms.assetid: 49bcd816-e3e2-45f4-8845-ef67789b8a01
keywords:
- Controles de SB_SETBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc08687c6d228074bc3e4dd7c8442a1c1e35a835
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369819"
---
# <a name="sb_setbkcolor-message"></a>\_Mensagem de SETBKCOLOR SB

Define a cor do plano de fundo em uma barra de status.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor [**COLORREF**](/windows/desktop/gdi/colorref) que especifica a nova cor do plano de fundo. Especifique o \_ valor padrão do CLR para fazer com que a barra de status Use sua cor de plano de fundo padrão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a cor do plano de fundo anterior ou o \_ padrão CLR se a cor do plano de fundo for a cor padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

