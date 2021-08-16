---
title: List-View de janela (CommCtrl.h)
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
# <a name="list-view-window-styles"></a>List-View de janela

Os estilos de janela a seguir são específicos para controles de exibição de lista.



| Constante                                                                                                                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVS_ALIGNLEFT"></span><span id="lvs_alignleft"></span><dl> <dt>**LVS \_ ALIGNLEFT**</dt> </dl>                   | Os itens são alinhados à esquerda no ícone e na exibição de ícone pequeno. <br/>                                                                                                                                                                                                                                                                                             |
| <span id="LVS_ALIGNMASK"></span><span id="lvs_alignmask"></span><dl> <dt>**LVS \_ ALIGNMASK**</dt> </dl>                   | O alinhamento atual do controle. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="LVS_ALIGNTOP"></span><span id="lvs_aligntop"></span><dl> <dt>**LVS \_ ALIGNTOP**</dt> </dl>                      | Os itens são alinhados com a parte superior do controle de exibição de lista no ícone e na exibição de ícone pequeno. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_AUTOARRANGE"></span><span id="lvs_autoarrange"></span><dl> <dt>**LVS \_ AUTOARRANGE**</dt> </dl>             | Os ícones são mantidos organizados automaticamente no ícone e na exibição de ícone pequeno. <br/>                                                                                                                                                                                                                                                                              |
| <span id="LVS_EDITLABELS"></span><span id="lvs_editlabels"></span><dl> <dt>**LVS \_ EDITLABELS**</dt> </dl>                | O texto do item pode ser editado no local. A janela pai deve processar o [código de notificação LVN \_ ENDLABELEDIT.](lvn-endlabeledit.md) <br/>                                                                                                                                                                                                               |
| <span id="LVS_ICON"></span><span id="lvs_icon"></span><dl> <dt>**ÍCONE \_ LVS**</dt> </dl>                                  | Esse estilo especifica a exibição de ícone. <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_LIST"></span><span id="lvs_list"></span><dl> <dt>**LVS \_ LIST**</dt> </dl>                                  | Esse estilo especifica a exibição de lista. <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_NOCOLUMNHEADER"></span><span id="lvs_nocolumnheader"></span><dl> <dt>**LVS \_ NOCOLUMNHEADER**</dt> </dl>    | Os headers de coluna não são exibidos na exibição de relatório. Por padrão, as colunas têm os headers na exibição de relatório. <br/>                                                                                                                                                                                                                                               |
| <span id="LVS_NOLABELWRAP"></span><span id="lvs_nolabelwrap"></span><dl> <dt>**LVS \_ NOLABELWRAP**</dt> </dl>             | O texto do item é exibido em uma única linha na exibição de ícone. Por padrão, o texto do item pode ser wrap na exibição de ícone. <br/>                                                                                                                                                                                                                                              |
| <span id="LVS_NOSCROLL"></span><span id="lvs_noscroll"></span><dl> <dt>**LVS \_ NOSCROLL**</dt> </dl>                      | A rolagem está desabilitada. Todos os itens devem estar dentro da área do cliente. Esse estilo não é compatível com os estilos **LVS \_ LIST** ou **LVS \_ REPORT.** Consulte o artigo da Base de Dados de Conhecimento Q137520 para mais discussão. <br/>                                                                                                                                      |
| <span id="LVS_NOSORTHEADER"></span><span id="lvs_nosortheader"></span><dl> <dt>**LVS \_ NOSORTHEADER**</dt> </dl>          | Os headers de coluna não funcionam como botões. Esse estilo poderá ser usado se clicar em um header de coluna na exibição de relatório não executar uma ação, como classificação. <br/>                                                                                                                                                                                       |
| <span id="LVS_OWNERDATA"></span><span id="lvs_ownerdata"></span><dl> <dt>**LVS \_ OWNERDATA**</dt> </dl>                   | [Versão 4.70.](common-control-versions.md) Esse estilo especifica um controle de exibição de lista virtual. Para obter mais informações sobre esse estilo de controle de lista, consulte [About List-View Controls](list-view-controls-overview.md). <br/>                                                                                                                             |
| <span id="LVS_OWNERDRAWFIXED"></span><span id="lvs_ownerdrawfixed"></span><dl> <dt>**LVS \_ OWNERDRAWFIXED**</dt> </dl>    | A janela proprietário pode pintar itens na exibição de relatório. O controle de exibição de lista envia [**uma mensagem WM \_ DRAWITEM**](wm-drawitem.md) para pintar cada item; ele não envia mensagens separadas para cada subitem. O **membro iItemData** da estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contém os dados do item de exibição de lista especificado. <br/> |
| <span id="LVS_REPORT"></span><span id="lvs_report"></span><dl> <dt>**RELATÓRIO \_ LVS**</dt> </dl>                            | Esse estilo especifica a exibição de relatório. Ao usar o estilo relatório LVS com um controle de exibição de lista, a primeira \_ coluna sempre é alinhada à esquerda. Não é possível usar LVCFMT \_ RIGHT para alterar esse alinhamento. Consulte [**LVCOLUMN para**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) obter mais informações sobre o alinhamento da coluna. <br/>                                                                      |
| <span id="LVS_SHAREIMAGELISTS"></span><span id="lvs_shareimagelists"></span><dl> <dt>**LVS \_ SHAREIMAGELISTS**</dt> </dl> | A lista de imagens não será excluída quando o controle for destruído. Esse estilo permite o uso das mesmas listas de imagens com vários controles de exibição de lista. <br/>                                                                                                                                                                                          |
| <span id="LVS_SHOWSELALWAYS"></span><span id="lvs_showselalways"></span><dl> <dt>**LVS \_ SHOWSELALWAYS**</dt> </dl>       | A seleção, se alguma, é sempre mostrada, mesmo que o controle não tenha o foco. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SINGLESEL"></span><span id="lvs_singlesel"></span><dl> <dt>**LVS \_ SINGLESEL**</dt> </dl>                   | Somente um item de cada vez pode ser selecionado. Por padrão, vários itens podem ser selecionados. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SMALLICON"></span><span id="lvs_smallicon"></span><dl> <dt>**LVS \_ SMALLICON**</dt> </dl>                   | Esse estilo especifica a exibição de ícone pequeno. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="LVS_SORTASCENDING"></span><span id="lvs_sortascending"></span><dl> <dt>**LVS \_ SORTASCENDING**</dt> </dl>       | Os índices de item são classificação com base no texto do item em ordem crescente. <br/>                                                                                                                                                                                                                                                                                  |
| <span id="LVS_SORTDESCENDING"></span><span id="lvs_sortdescending"></span><dl> <dt>**LVS \_ SORTDESCENDING**</dt> </dl>    | Os índices de item são classificação com base no texto do item em ordem decrescente. <br/>                                                                                                                                                                                                                                                                                 |
| <span id="LVS_TYPEMASK"></span><span id="lvs_typemask"></span><dl> <dt>**LVS \_ TYPEMASK**</dt> </dl>                      | Determina o estilo de janela atual do controle. <br/>                                                                                                                                                                                                                                                                                                  |
| <span id="LVS_TYPESTYLEMASK"></span><span id="lvs_typestylemask"></span><dl> <dt>**LVS \_ TYPESTYLEMASK**</dt> </dl>       | Determina os estilos de janela que controlam o alinhamento do item, a aparência e o comportamento do header. <br/>                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>Comentários

Para os estilos **LVS \_ SORTASCENDING** e **LVS \_ SORTDESCENDING,** os índices de item são classificação com base no texto do item em ordem crescente ou decrescente, respectivamente. Como as **exibições LVS \_ LIST** e **LVS \_ REPORT** exibem itens na mesma ordem que seus índices, os resultados da classificação são imediatamente visíveis para o usuário. As **exibições LVS \_ ICON** e **LVS \_ SMALLICON** não usam índices de item para determinar a posição dos ícones. Com essas exibições, os resultados da classificação não são visíveis para o usuário.

Você pode usar a máscara **\_ TYPEMASK LVS** para isolar os estilos de janela que correspondem à exibição atual: **LVS \_ ICON,** **LVS \_ LIST,** **LVS \_ REPORT** e **LVS \_ SMALLICON.**

Você pode usar a máscara **LVS \_ ALIGNMASK** para isolar os estilos de janela que especificam o alinhamento de itens: **LVS \_ ALIGNLEFT** e **LVS \_ ALIGNTOP**.

Você pode usar a máscara **LVS \_ TYPESTYLEMASK** para isolar os estilos de janela que controlam o alinhamento do item (**LVS \_ ALIGNLEFT** e **LVS \_ ALIGNTOP**) e aqueles que controlam a aparência e o comportamento do header (**LVS \_ NOCOLUMNHEADER** e **LVS \_ NOSORTHEADER**).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estilos e exibições de exibição de lista](list-view-controls-overview.md)
</dt> </dl>

 

 





