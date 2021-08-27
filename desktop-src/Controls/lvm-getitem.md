---
title: LVM_GETITEM mensagem (Commctrl.h)
description: Recupera alguns ou todos os atributos de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItem ListView.
ms.assetid: 684ad96a-2c3b-4148-b66c-41f8322500bb
keywords:
- LVM_GETITEM controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_GETITEM
- LVM_GETITEMA
- LVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05338abce0396c5cc527c8a1c04176b3b59243a684c66a263cb190d59ac68b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088896"
---
# <a name="lvm_getitem-message"></a>Mensagem GETITEM LVM \_

Recupera alguns ou todos os atributos de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ GetItem ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que especifica as informações a serem recuperadas e recebe informações sobre o item de exibição de lista.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="remarks"></a>Comentários

Quando a **mensagem \_ GETITEM LVM** é enviada, os membros **iItem** e **iSubItem**  identificam o item ou subitem sobre o qual recuperar informações e o membro de máscara especifica quais atributos recuperar. Para ver uma lista de valores possíveis, consulte a descrição da [**estrutura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema)

Se o sinalizador TEXT LVIF estiver definido no membro de máscara da estrutura \_ [**LVITEM,**](/windows/win32/api/commctrl/ns-commctrl-lvitema) o membro **pszText** deverá apontar para um buffer válido e o membro **cchTextMax** deverá ser definido como o número de caracteres nesse buffer.  Os aplicativos não devem supor que o texto será necessariamente colocado no buffer especificado. Em vez disso, o controle pode alterar o membro **pszText** da estrutura para apontar para o novo texto, em vez de coloque-o no buffer.

Se o **membro mask** especificar o valor LVIF STATE, o membro \_ **stateMask** deverá especificar os bits de estado do item a recuperar. Na saída, o **membro de** estado contém os valores dos bits de estado especificados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ GETITEMW** (Unicode) e **LVM \_ GETITEMA** (ANSI)<br/>                   |



 

 





