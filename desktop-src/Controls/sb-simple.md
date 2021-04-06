---
title: Mensagem de SB_SIMPLE (commctrl. h)
description: Especifica se uma janela de status exibe texto simples ou exibe todas as partes da janela definidas por uma mensagem do SB \_ SETparts anterior.
ms.assetid: 457209cb-67d4-4a9f-8d18-75aa5eb9ca1d
keywords:
- Controles de SB_SIMPLE de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_SIMPLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f7a462a917c86531cd70f5f5c8ea60bf448ff6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086017"
---
# <a name="sb_simple-message"></a>\_Mensagem simples do SB

Especifica se uma janela de status exibe texto simples ou exibe todas as partes da janela definidas por uma mensagem do [**SB \_ SetParts**](sb-setparts.md) anterior.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador de tipo de exibição. Se esse parâmetro for **true**, a janela exibirá texto simples. Se for **false**, exibirá várias partes.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno não é usado.

## <a name="remarks"></a>Comentários

Se a janela de status estiver sendo alterada de não simples para simples, ou vice-versa, a janela será redesenhada imediatamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





