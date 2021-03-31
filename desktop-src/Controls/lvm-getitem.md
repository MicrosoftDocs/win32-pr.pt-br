---
title: Mensagem de LVM_GETITEM (commctrl. h)
description: Recupera alguns ou todos os atributos de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItem do ListView.
ms.assetid: 684ad96a-2c3b-4148-b66c-41f8322500bb
keywords:
- Controles de LVM_GETITEM de mensagens do Windows
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
ms.openlocfilehash: c19632567db5e37059b1b028a8ec1fc9385268cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645023"
---
# <a name="lvm_getitem-message"></a>\_Mensagem GETITEM LVM

Recupera alguns ou todos os atributos de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetItem do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que especifica as informações para recuperar e receber informações sobre o item de exibição de lista.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Quando a **mensagem LVM \_ GETITEM** é enviada, os membros **iItem** e **iSubItem** identificam o item ou subitem para recuperar informações e o membro **Mask** especifica quais atributos serão recuperados. Para obter uma lista de valores possíveis, consulte a descrição da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .

Se o \_ sinalizador de texto LVIF for definido no membro **Mask** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) , o membro **pszText** deverá apontar para um buffer válido e o membro **cchTextMax** deverá ser definido como o número de caracteres nesse buffer. Os aplicativos não devem pressupor que o texto será necessariamente colocado no buffer especificado. O controle pode, em vez disso, alterar o membro **pszText** da estrutura para apontar para o novo texto, em vez de colocá-lo no buffer.

Se o membro da **máscara** especificar o \_ valor do estado LVIF, o membro **stateMask** deverá especificar os bits de estado do item a serem recuperados. Na saída, o membro de **estado** contém os valores dos bits de estado especificados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ GETITEMW** (Unicode) e **LVM \_ getitema** (ANSI)<br/>                   |



 

 





