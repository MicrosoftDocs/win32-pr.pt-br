---
title: Mensagem de LVM_SETEXTENDEDLISTVIEWSTYLE (commctrl. h)
description: Define estilos estendidos em controles de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ListView SetExtendedListViewStyle ou ListView \_ SetExtendedListViewStyleEx.
ms.assetid: eb3f47ed-484a-49a8-94b0-e50ee081bd69
keywords:
- controles de Windows de mensagem de LVM_SETEXTENDEDLISTVIEWSTYLE
topic_type:
- apiref
api_name:
- LVM_SETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 336732b927c7ee6170e777f2f7c1cd57eac6baa2c7706870e681f602e2309c37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077276"
---
# <a name="lvm_setextendedlistviewstyle-message"></a>\_Mensagem SETEXTENDEDLISTVIEWSTYLE LVM

Define estilos estendidos em controles de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a macro [**ListView \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) ou [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor **DWORD** que especifica quais estilos em *lParam* devem ser afetados. Esse parâmetro pode ser uma combinação de [**estilos de List-View estendidos**](extended-list-view-styles.md). Somente os estilos estendidos em *wParam* serão alterados. Todos os outros estilos serão mantidos como estão. Se esse parâmetro for zero, todos os estilos em *lParam* serão afetados.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor **DWORD** que especifica os estilos de controle de exibição de lista estendida a serem definidos. Esse parâmetro pode ser uma combinação de [**estilos de List-View estendidos**](extended-list-view-styles.md). Os estilos que não estão definidos, mas que são especificados em *wParam*, são removidos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **DWORD** que contém os estilos de controle de exibição de lista estendida anteriores.

## <a name="remarks"></a>Comentários

O parâmetro *wParam* permite modificar um ou mais estilos estendidos sem precisar recuperar os estilos existentes primeiro. Por exemplo, se você passar [**LVS \_ ex \_ FULLROWSELECT**](extended-list-view-styles.md) para *wParam* e 0 para *lParam*, o estilo **LVS \_ ex \_ FULLROWSELECT** será limpo, mas todos os outros estilos permanecerão os mesmos.

Por motivos de compatibilidade com versões anteriores, a macro [**ListView \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) não foi atualizada para usar *wParam*. Para usar o valor *wParam* , use a macro [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) .

Quando você usa essa mensagem para definir o estilo de [**\_ caixas de \_ seleção LVS ex**](extended-list-view-styles.md) , qualquer índice de imagem de estado definido anteriormente será Descartado. Todas as caixas de seleção serão inicializadas para o estado desmarcado. O índice de imagem de estado está contido em bits 12 a 15 do membro de **estado** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





