---
title: List-View estilos de janela (CommCtrl. h)
description: Os estilos de janela a seguir são específicos para controles de exibição de lista.
ms.assetid: 8b57239b-112e-4fb6-b394-15501bd3f5b3
topic_type:
- apiref
api_name:
- LVS_ALIGNLEFT
- LVS_ALIGNMASK
- LVS_ALIGNTOP
- LVS_AUTOARRANGE
- LVS_EDITLABELS
- LVS_ICON
- LVS_LIST
- LVS_NOCOLUMNHEADER
- LVS_NOLABELWRAP
- LVS_NOSCROLL
- LVS_NOSORTHEADER
- LVS_OWNERDATA
- LVS_OWNERDRAWFIXED
- LVS_REPORT
- LVS_SHAREIMAGELISTS
- LVS_SHOWSELALWAYS
- LVS_SINGLESEL
- LVS_SMALLICON
- LVS_SORTASCENDING
- LVS_SORTDESCENDING
- LVS_TYPEMASK
- LVS_TYPESTYLEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3e326f4508d08f1052747e64ea5eba184f45f7e73a1cb55539255a27fd8c8c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412021"
---
# <a name="list-view-window-styles"></a>List-View estilos de janela

Os estilos de janela a seguir são específicos para controles de exibição de lista.



| Constante                                                                                                                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVS_ALIGNLEFT"></span><span id="lvs_alignleft"></span><dl> <dt>**LVS \_ ALIGNLEFT**</dt> </dl>                   | Os itens são alinhados à esquerda no ícone e na exibição de ícone pequeno. <br/>                                                                                                                                                                                                                                                                                             |
| <span id="LVS_ALIGNMASK"></span><span id="lvs_alignmask"></span><dl> <dt>**LVS \_ ALIGNMASK**</dt> </dl>                   | O alinhamento atual do controle. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="LVS_ALIGNTOP"></span><span id="lvs_aligntop"></span><dl> <dt>**LVS \_ ALIGNTOP**</dt> </dl>                      | Os itens são alinhados com a parte superior do controle de exibição de lista no ícone e no modo de exibição de ícone pequeno. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_AUTOARRANGE"></span><span id="lvs_autoarrange"></span><dl> <dt>**AutoOrganizar LVS \_**</dt> </dl>             | Os ícones são mantidos automaticamente organizados no ícone e na exibição de ícones pequenos. <br/>                                                                                                                                                                                                                                                                              |
| <span id="LVS_EDITLABELS"></span><span id="lvs_editlabels"></span><dl> <dt>**LVS \_ EDITLABELS**</dt> </dl>                | O texto do item pode ser editado no local. A janela pai deve processar o código de notificação [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) . <br/>                                                                                                                                                                                                               |
| <span id="LVS_ICON"></span><span id="lvs_icon"></span><dl> <dt>**ícone de LVS \_**</dt> </dl>                                  | Este estilo especifica a exibição de ícone. <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_LIST"></span><span id="lvs_list"></span><dl> <dt>**lista de LVS \_**</dt> </dl>                                  | Este estilo especifica a exibição de lista. <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_NOCOLUMNHEADER"></span><span id="lvs_nocolumnheader"></span><dl> <dt>**LVS \_ NOcolumnheader**</dt> </dl>    | Os cabeçalhos de coluna não são exibidos no modo de exibição de relatório. Por padrão, as colunas têm cabeçalhos na exibição de relatório. <br/>                                                                                                                                                                                                                                               |
| <span id="LVS_NOLABELWRAP"></span><span id="lvs_nolabelwrap"></span><dl> <dt>**LVS \_ NOLABELWRAP**</dt> </dl>             | O texto do item é exibido em uma única linha na exibição de ícones. Por padrão, o texto do item pode ser quebrado na exibição de ícones. <br/>                                                                                                                                                                                                                                              |
| <span id="LVS_NOSCROLL"></span><span id="lvs_noscroll"></span><dl> <dt>**LVS \_ NOscroll**</dt> </dl>                      | A rolagem está desabilitada. Todos os itens devem estar dentro da área do cliente. Este estilo não é compatível com a **\_ lista LVS** ou os estilos de **\_ relatório LVS** . Consulte o artigo da base de dados de conhecimento Q137520 para mais discussões. <br/>                                                                                                                                      |
| <span id="LVS_NOSORTHEADER"></span><span id="lvs_nosortheader"></span><dl> <dt>**LVS \_ NOSORTHEADER**</dt> </dl>          | Os cabeçalhos de coluna não funcionam como botões. Esse estilo pode ser usado se você clicar em um cabeçalho de coluna no modo de exibição de relatório não executar uma ação, como classificação. <br/>                                                                                                                                                                                       |
| <span id="LVS_OWNERDATA"></span><span id="lvs_ownerdata"></span><dl> <dt>**LVS \_ OWNERDATA**</dt> </dl>                   | [Versão 4,70](common-control-versions.md). Este estilo especifica um controle de exibição de lista virtual. Para obter mais informações sobre esse estilo de controle de lista, consulte [sobre controles de List-View](list-view-controls-overview.md). <br/>                                                                                                                             |
| <span id="LVS_OWNERDRAWFIXED"></span><span id="lvs_ownerdrawfixed"></span><dl> <dt>**LVS \_ OwnerDrawFixed**</dt> </dl>    | A janela do proprietário pode pintar itens na exibição de relatório. O controle List-View envia uma mensagem do [**WM \_ DRAWITEM**](wm-drawitem.md) para pintar cada item; ele não envia mensagens separadas para cada subitem. O membro **iItemData** da estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contém os dados do item para o item de exibição de lista especificado. <br/> |
| <span id="LVS_REPORT"></span><span id="lvs_report"></span><dl> <dt>**relatório de LVS \_**</dt> </dl>                            | Este estilo especifica a exibição de relatório. Ao usar o \_ estilo de relatório LVS com um controle de exibição de lista, a primeira coluna é sempre alinhada à esquerda. Não é possível usar LVCFMT \_ direito para alterar esse alinhamento. Consulte [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) para obter mais informações sobre o alinhamento de colunas. <br/>                                                                      |
| <span id="LVS_SHAREIMAGELISTS"></span><span id="lvs_shareimagelists"></span><dl> <dt>**LVS \_ SHAREIMAGELISTS**</dt> </dl> | A lista de imagens não será excluída quando o controle for destruído. Esse estilo permite o uso das mesmas listas de imagens com vários controles de exibição de lista. <br/>                                                                                                                                                                                          |
| <span id="LVS_SHOWSELALWAYS"></span><span id="lvs_showselalways"></span><dl> <dt>**LVS \_ SHOWSELALWAYS**</dt> </dl>       | A seleção, se houver, sempre será mostrada, mesmo se o controle não tiver o foco. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SINGLESEL"></span><span id="lvs_singlesel"></span><dl> <dt>**LVS \_ SINGLESEL**</dt> </dl>                   | Somente um item por vez pode ser selecionado. Por padrão, vários itens podem ser selecionados. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SMALLICON"></span><span id="lvs_smallicon"></span><dl> <dt>**LVS \_ SMALLICON**</dt> </dl>                   | Este estilo especifica a exibição de ícones pequenos. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="LVS_SORTASCENDING"></span><span id="lvs_sortascending"></span><dl> <dt>**LVS \_ SORTASCENDING**</dt> </dl>       | Os índices de item são classificados com base no texto do item em ordem crescente. <br/>                                                                                                                                                                                                                                                                                  |
| <span id="LVS_SORTDESCENDING"></span><span id="lvs_sortdescending"></span><dl> <dt>**LVS \_ SORTDESCENDING**</dt> </dl>    | Os índices de item são classificados com base no texto do item em ordem decrescente. <br/>                                                                                                                                                                                                                                                                                 |
| <span id="LVS_TYPEMASK"></span><span id="lvs_typemask"></span><dl> <dt>**LVS \_ TYPEMASK**</dt> </dl>                      | Determina o estilo da janela atual do controle. <br/>                                                                                                                                                                                                                                                                                                  |
| <span id="LVS_TYPESTYLEMASK"></span><span id="lvs_typestylemask"></span><dl> <dt>**LVS \_ TYPESTYLEMASK**</dt> </dl>       | Determina os estilos de janela que controlam o alinhamento do item e o comportamento e a aparência do cabeçalho. <br/>                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>Comentários

Para os estilos **LVS \_ SORTASCENDING** e **LVS \_ SORTDESCENDING** , os índices de itens são classificados com base no texto do item em ordem crescente ou decrescente, respectivamente. Como a **\_ lista de LVS** e as exibições de **\_ relatório LVS** exibem itens na mesma ordem que seus índices, os resultados da classificação são imediatamente visíveis para o usuário. As exibições **\_ ícone LVS** e **LVS \_ SMALLICON** não usam índices de item para determinar a posição dos ícones. Com essas exibições, os resultados da classificação não são visíveis para o usuário.

Você pode usar a máscara **LVS \_ TYPEMASK** para isolar os estilos de janela que correspondem à exibição atual **: \_ ícone de LVS**, **\_ lista de LVS**, **\_ relatório de LVS** e **LVS \_ SMALLICON**.

Você pode usar a máscara **LVS \_ ALIGNMASK** para isolar os estilos de janela que especificam o alinhamento dos itens: **LVS \_ ALIGNLEFT** e **LVS \_ ALIGNTOP**.

Você pode usar a **máscara \_ LVS TYPESTYLEMASK** para isolar os estilos de janela que controlam o alinhamento do item (**LVS \_ ALIGNLEFT** e LVS ALIGNTOP) e aqueles que controlam a aparência e o comportamento do cabeçalho (**LVS \_ nocolumnheader** e **LVS \_ NOSORTHEADER**). **\_**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Exibições e estilos de exibição de lista](list-view-controls-overview.md)
</dt> </dl>

 

 





