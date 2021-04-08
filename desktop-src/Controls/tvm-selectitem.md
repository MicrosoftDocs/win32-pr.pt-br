---
title: Mensagem de TVM_SELECTITEM (commctrl. h)
description: Seleciona o item de exibição de árvore especificado, rola o item para a exibição ou redesenha o item no estilo usado para indicar o destino de uma operação de arrastar e soltar.
ms.assetid: 8b943958-7b93-4e54-99de-200121cf0752
keywords:
- Controles de TVM_SELECTITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SELECTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94862b64a02cd8972e3da38a75282d99bbc1cbc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824244"
---
# <a name="tvm_selectitem-message"></a>\_Mensagem TVM SELECTITEM

Seleciona o item de exibição de árvore especificado, rola o item para a exibição ou redesenha o item no estilo usado para indicar o destino de uma operação de arrastar e soltar. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)ou [**TreeView \_ SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador de ação. Esse parâmetro pode ser um dos seguintes valores:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <dt><strong>TVGN_CARET</strong></dt> </dl></td>
<td>Define a seleção para o item especificado. A janela pai do controle de exibição de árvore recebe os códigos de notificação <a href="tvn-selchanging.md">TVN_SELCHANGING</a> e <a href="tvn-selchanged.md">TVN_SELCHANGED</a> . <br/></td>
</tr>
<tr class="even">
<td><span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <dt><strong>TVGN_DROPHILITE</strong></dt> </dl></td>
<td>Redesenha o item especificado no estilo usado para indicar o destino de uma operação de arrastar e soltar.<br/></td>
</tr>
<tr class="odd">
<td><span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </dl></td>
<td>Garante que o item especificado esteja visível e, se possível, exiba-o na parte superior da janela do controle. Os controles de exibição de árvore exibem quantos itens forem ajustados na janela. Se o item especificado estiver próximo da parte inferior da hierarquia de itens do controle, ele poderá não se tornar o primeiro item visível, dependendo de quantos itens couberem na janela.<br/></td>
</tr>
<tr class="even">
<td><span id="TVSI_NOSINGLEEXPAND"></span><span id="tvsi_nosingleexpand"></span><dl> <dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </dl></td>
<td>Quando um único item é selecionado, o modo de exibição de árvore não expande os filhos desse item. Isso é válido somente se usado com o sinalizador TVGN_CARET. <br/>
<blockquote>
[!Note]<br />
Para usar esse sinalizador, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte <a href="cookbook-overview.md">habilitando estilos visuais</a>.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para um item. Se *lParam* for **NULL**, o controle será definido como não tem nenhum item selecionado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Se o item especificado for o filho de um item pai recolhido, a lista de itens filho do pai será expandida para revelar o item especificado. Nesse caso, a janela pai do controle recebe os códigos de notificação [TVN \_ doexpanding](tvn-itemexpanding.md) e [TVN \_ ](tvn-itemexpanded.md) .

Usar a macro [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) é equivalente a enviar a mensagem **TVM \_ SelectItem** com *wParam* definido para o valor de cursor TVGN \_ . Usar a macro [**TreeView \_ SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) é equivalente a enviar a mensagem **TVM \_ SELECTITEM** com *wParam* definido para o valor TVGN \_ DROPHILITE. Usar [**TreeView \_ SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) é equivalente a enviar a mensagem **TVM \_ SELECTITEM** com *wParam* definido para o \_ valor TVGN FIRSTVISIBLE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





