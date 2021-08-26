---
title: BCM_SETSPLITINFO mensagem (Commctrl.h)
description: Define informações para um controle de botão de divisão. Envie essa mensagem explicitamente ou usando a \_ macro SetSplitInfo do botão.
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- BCM_SETSPLITINFO controles de Windows mensagem
topic_type:
- apiref
api_name:
- BCM_SETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17332ce5f10fa612d739598222e4973000961435fa525190a650adaa9aa9fc4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921416"
---
# <a name="bcm_setsplitinfo-message"></a>Mensagem BCM \_ SETSPLITINFO

Define informações para um controle de botão de divisão. Envie essa mensagem explicitamente ou usando a [**macro \_ SetSplitInfo do**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) botão.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* \[ Em\]
</dt> <dd>

Um ponteiro para uma estrutura [**\_ BUTTON SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) que contém informações sobre o botão de divisão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="remarks"></a>Comentários

Use essa mensagem somente com os estilos de botão [**BS \_ SPLITBUTTON**](button-styles.md) e [**BS \_ DEFSPLITBUTTON.**](button-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[Estilos de botão](button-styles.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Tipos de botão](button-types-and-styles.md)
</dt> </dl>

 

 





