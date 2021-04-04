---
title: Mensagem de LVM_SETITEM (commctrl. h)
description: Define alguns ou todos os atributos de um item de exibição de lista. Você também pode enviar \_ o LVM SETITEM para definir o texto de um subitem. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetItem do ListView.
ms.assetid: f1189b5d-bce7-4569-b4b9-bd750d7ef505
keywords:
- Controles de LVM_SETITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETITEM
- LVM_SETITEMA
- LVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623339c3d1ecc7a74cf20b5e52fb621666391bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009131"
---
# <a name="lvm_setitem-message"></a>\_Mensagem SETITEM LVM

Define alguns ou todos os atributos de um item de exibição de lista. Você também pode enviar \_ o LVM SETITEM para definir o texto de um subitem. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetItem do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que contém os novos atributos de item. Os membros **iItem** e **iSubItem** identificam o item ou subitem, e o membro **Mask** especifica quais atributos definir. Se o membro de **máscara** especificar o \_ valor de texto LVIF, o membro **pszText** será o endereço de uma cadeia de caracteres terminada em nulo e o membro **cchTextMax** será ignorado. Se o membro de **máscara** especificar o \_ valor de estado LVIF, o membro **stateMask** especificará quais Estados de item alterar e o membro de **estado** conterá os valores para esses Estados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Para definir os atributos de um item de exibição de lista, defina o membro **iItem** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) para o índice do item e defina o membro **iSubItem** como zero. Para um item, você pode definir os membros **State**, **pszText**, **iImage** e **lParam** da estrutura **LVITEM** .

Para definir o texto de um subitem, defina os membros **iItem** e **iSubItem** para indicar o subitem específico e use o membro **pszText** para especificar o texto. Como alternativa, você pode usar a [**macro \_ SetItemText do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) para definir o texto de um subitem. Você não pode definir os membros de **estado** ou **lParam** para subitens porque os subitens não têm esses atributos. Na versão 4,70 e posterior, você pode definir o membro **iImage** para subitens. A imagem do subitem será exibida se o controle de exibição de lista tiver o estilo estendido [**LVS \_ ex \_ SUBITEMIMAGES**](extended-list-view-styles.md) . As versões anteriores irão ignorar a imagem do subitem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ SETITEMW** (Unicode) e **LVM \_ setitema** (ANSI)<br/>                   |



 

 





