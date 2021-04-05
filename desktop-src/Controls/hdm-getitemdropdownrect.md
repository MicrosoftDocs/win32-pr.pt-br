---
title: Mensagem de HDM_GETITEMDROPDOWNRECT (commctrl. h)
description: Obtém o retângulo delimitador do botão de divisão para um item de cabeçalho com o estilo HDF \_ SPLITBUTTON. Envie essa mensagem explicitamente ou usando a \_ macro GetItemDropDownRect do cabeçalho.
ms.assetid: d7188dfb-4ffa-4641-b210-2c2ec480ca13
keywords:
- Controles de HDM_GETITEMDROPDOWNRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86f3df8de5224e79ca4e15ea18409e13972ca5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009400"
---
# <a name="hdm_getitemdropdownrect-message"></a>\_Mensagem HDM GETITEMDROPDOWNRECT

Obtém o retângulo delimitador do botão de divisão para um item de cabeçalho com o estilo **HDF \_ SPLITBUTTON**. Envie essa mensagem explicitamente ou usando a macro [**\_ GetItemDropDownRect do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

O índice de base zero do item de controle de cabeçalho para o qual recuperar o retângulo delimitador.

</dd> <dt>

*lParam* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma estrutura [**Rect**](/windows/win32/api/windef/ns-windef-rect) que recebe as informações do retângulo delimitador. O remetente da mensagem é responsável por alocar essa estrutura. As coordenadas retornadas na estrutura RECT são expressas em relação ao pai do controle de cabeçalho.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

O item de cabeçalho deve ter o estilo **HDF \_ SPLITBUTTON**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Sobre controles de cabeçalho](header-controls.md)
</dt> </dl>

 

 





