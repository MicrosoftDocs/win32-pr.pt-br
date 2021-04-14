---
title: Mensagem de TVM_EXPAND (commctrl. h)
description: A \_ mensagem de expansão TVM expande ou recolhe a lista de itens filho associados ao item pai especificado, se houver. Você pode enviar essa mensagem explicitamente ou usando a macro de \_ expansão do TreeView.
ms.assetid: d6c2e5b2-ce36-4c2b-b527-91c6de56e305
keywords:
- Controles de TVM_EXPAND de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_EXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d5cd7577c6f4581865569c3aefca93f13aa305
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455736"
---
# <a name="tvm_expand-message"></a>TVM \_ expandir mensagem

A mensagem de **\_ expansão TVM** expande ou recolhe a lista de itens filho associados ao item pai especificado, se houver. Você pode enviar essa mensagem explicitamente ou usando a macro [**de \_ expansão do TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador de ação. Esse parâmetro pode ser um ou mais dos seguintes valores:



| Valor                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVE_COLLAPSE"></span><span id="tve_collapse"></span><dl> <dt>**\_recolher TVE**</dt> </dl>                | Recolhe a lista. <br/>                                                                                                                                                                                                                                                       |
| <span id="TVE_COLLAPSERESET"></span><span id="tve_collapsereset"></span><dl> <dt>**TVE \_ COLLAPSERESET**</dt> </dl> | Recolhe a lista e remove os itens filho. O sinalizador de estado [**TVIS \_ EXPANDEDONCE**](tree-view-control-item-states.md) é redefinido. Esse sinalizador deve ser usado com o \_ sinalizador de recolhimento TVE.<br/>                                                                 |
| <span id="TVE_EXPAND"></span><span id="tve_expand"></span><dl> <dt>**TVE \_ expandir**</dt> </dl>                      | Expande a lista.<br/>                                                                                                                                                                                                                                                          |
| <span id="TVE_EXPANDPARTIAL"></span><span id="tve_expandpartial"></span><dl> <dt>**TVE \_ EXPANDPARTIAL**</dt> </dl> | [Versão 4,70](common-control-versions.md). Expande parcialmente a lista. Nesse estado, os itens filho são visíveis e o sinal de adição (+) do item pai, indicando que ele pode ser expandido, é exibido. Esse sinalizador deve ser usado em combinação com o \_ sinalizador de expansão TVE.<br/> |
| <span id="TVE_TOGGLE"></span><span id="tve_toggle"></span><dl> <dt>**alternância de TVE \_**</dt> </dl>                      | Recolhe a lista se ela for expandida ou a expandir se ela estiver recolhida.<br/>                                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Manipule o item pai para expandir ou recolher.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se a operação tiver sido bem-sucedida ou zero caso contrário.

## <a name="remarks"></a>Comentários

Expandir um nó que já está expandido é considerado uma operação bem-sucedida e [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) retorna um valor diferente de zero. O recolhimento de um nó retornará zero se o nó já estiver recolhido; caso contrário, ele retornará diferente de zero. A tentativa de expandir ou recolher um nó que não tem filhos é considerada uma falha e **SendMessage** retorna zero.

Quando um item é expandido pela primeira vez por uma mensagem de **\_ expansão TVM** , a ação gera códigos de notificação de TVN e [TVN \_](tvn-itemexpanded.md) de itens de TVIS e o sinalizador de estado [**\_ EXPANDEDONCE**](tree-view-control-item-states.md) do item é definido. [ \_](tvn-itemexpanding.md) Desde que esse sinalizador de estado permaneça definido, as mensagens de **\_ expansão TVM** subsequentes não gerarão \_ notificações de TVN ou de doexpanding TVN \_ . Para redefinir o sinalizador de estado **TVIS \_ EXPANDEDONCE** , você deve enviar uma mensagem **TVM \_ Expand** com os \_ sinalizadores TVE Collapse e TVE \_ COLLAPSERESET definidos. A tentativa de definir explicitamente **TVIS \_ EXPANDEDONCE** resultará em um comportamento imprevisível.

A operação de expansão poderá falhar se o proprietário do controle TreeView negar a operação em resposta a uma notificação [de \_ TVN](tvn-itemexpanding.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

