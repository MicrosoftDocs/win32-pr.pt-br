---
title: Mensagem de BCM_SETDROPDOWNSTATE (commctrl. h)
description: Define o estado de menu suspenso para um botão com a lista suspensa estilo TBSTYLE \_ . Envie essa mensagem explicitamente ou usando a \_ macro Setdropstate do botão.
ms.assetid: 725deff4-0bcb-497d-a6cf-e9c98b05f16e
keywords:
- controles de Windows de mensagem de BCM_SETDROPDOWNSTATE
topic_type:
- apiref
api_name:
- BCM_SETDROPDOWNSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 989b4a04502a730c06a906be28a6915a4e604ff22c4b4e5ae9a4b85c8b464f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117833627"
---
# <a name="bcm_setdropdownstate-message"></a>\_Mensagem de lista suspensa do BCM

Define o estado de menu suspenso para um botão com [**a \_ lista**](toolbar-control-and-button-styles.md)suspensa estilo TBSTYLE. Envie essa mensagem explicitamente ou usando a macro [**\_ setdropstate do botão**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Um **bool** que é **verdadeiro** para o estado de BST \_ DROPDOWNPUSHED ou **false** caso contrário.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[Estilos de botão](button-styles.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Tipos de botão](button-types-and-styles.md)
</dt> </dl>

 

 





