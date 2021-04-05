---
title: Mensagem de CB_GETITEMHEIGHT (WinUser. h)
description: Determina a altura dos itens de lista ou o campo de seleção em uma caixa de combinação.
ms.assetid: 72fba6ca-0a51-4801-bd45-5f5a7d5ebee2
keywords:
- Controles de CB_GETITEMHEIGHT de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4aac9d8f9a430c056f8b91a9306d77c182f4c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824408"
---
# <a name="cb_getitemheight-message"></a>\_Mensagem de GETITEMHEIGHT CB

Determina a altura dos itens de lista ou o campo de seleção em uma caixa de combinação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O componente da caixa de combinação cuja altura deve ser recuperada. Esse parâmetro deve ser-1 para recuperar a altura do campo de seleção. Ele deve ser zero para recuperar a altura dos itens de lista, a menos que a caixa de combinação tenha o estilo [**\_ OwnerDrawVariable do CBS**](combo-box-styles.md) . Nesse caso, o parâmetro *wParam* é o índice de base zero de um item de lista específico.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é a altura, em pixels, dos itens da lista em uma caixa de combinação. Se a caixa de combinação tiver o estilo [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) , será a altura do item especificado pelo parâmetro *wParam* . Se *wParam* for-1, o valor de retorno será a altura da parte do controle de edição (ou texto estático) da caixa de combinação. Se ocorrer um erro, o valor de retorno será CB \_ Err.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_SETITEMHEIGHT CB**](cb-setitemheight.md)
</dt> <dt>

[**MEASUREITEM do WM \_**](wm-measureitem.md)
</dt> </dl>

 

 





