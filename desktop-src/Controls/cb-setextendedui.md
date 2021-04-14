---
title: Mensagem de CB_SETEXTENDEDUI (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de SETEXTENDEDUI CB para selecionar a interface do usuário padrão ou a interface do usuário estendida para uma caixa de combinação que tem o \_ estilo de lista suspensa CBS ou CBS \_ DROPDOWNLIST.
ms.assetid: c489e484-777e-4afa-996b-1ec3eb6552ab
keywords:
- Controles de CB_SETEXTENDEDUI de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f94c31c8bc5457799d0038ecd8340c03c55aed91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455119"
---
# <a name="cb_setextendedui-message"></a>\_Mensagem de SETEXTENDEDUI CB

Um aplicativo envia uma mensagem de **\_ SETEXTENDEDUI CB** para selecionar a interface do usuário padrão ou a interface do usuário estendida para uma caixa de combinação que tem o estilo de [**\_ lista suspensa CBS**](combo-box-styles.md) ou [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um **bool** que especifica se a caixa de combinação usa a interface do usuário estendida (**true**) ou a interface do usuário padrão (**false**).

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com sucesso, o valor de retorno será CB \_ OK. Se ocorrer um erro, será CB \_ Err.

## <a name="remarks"></a>Comentários

Por padrão, a tecla F4 é aberta ou fecha a lista e a seta para baixo altera a seleção atual. Na interface do usuário estendida, a tecla F4 é desabilitada e a tecla de seta para baixo abre a lista suspensa. A roda do mouse, que normalmente rola pelos itens da lista, não tem efeito quando a interface do usuário estendida está definida.

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

[**\_GETEXTENDEDUI CB**](cb-getextendedui.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Recursos da caixa de combinação](combo-box-features.md)
</dt> </dl>

 

 





