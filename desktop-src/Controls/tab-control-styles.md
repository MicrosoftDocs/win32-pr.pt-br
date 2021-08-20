---
title: Estilos de controle de guia (CommCtrl. h)
description: Esta seção lista os estilos de controle de guia com suporte.
ms.assetid: a01a6609-b02e-4ada-afa0-ed5ad8dde0d6
topic_type:
- apiref
api_name:
- TCS_BOTTOM
- TCS_BUTTONS
- TCS_FIXEDWIDTH
- TCS_FLATBUTTONS
- TCS_FOCUSNEVER
- TCS_FOCUSONBUTTONDOWN
- TCS_FORCEICONLEFT
- TCS_FORCELABELLEFT
- TCS_HOTTRACK
- TCS_MULTILINE
- TCS_MULTISELECT
- TCS_OWNERDRAWFIXED
- TCS_RAGGEDRIGHT
- TCS_RIGHT
- TCS_RIGHTJUSTIFY
- TCS_SCROLLOPPOSITE
- TCS_SINGLELINE
- TCS_TABS
- TCS_TOOLTIPS
- TCS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4dfdcfb17b2f4a8ffebd4a7cfba5042e19ba2b566d4b03635032438a2f7fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078410"
---
# <a name="tab-control-styles"></a>Estilos de controle de guia

Esta seção lista os estilos de controle de guia com suporte.



| Constante                                                                                                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_BOTTOM"></span><span id="tcs_bottom"></span><dl> <dt>**\_parte inferior do TCS**</dt> </dl>                                  | [Versão 4,70](common-control-versions.md). As guias aparecem na parte inferior do controle. Esse valor é igual a TCS \_ à direita. Esse estilo não terá suporte se você usar ComCtl32.dll versão 6.<br/>                                                                                                                                                                 |
| <span id="TCS_BUTTONS"></span><span id="tcs_buttons"></span><dl> <dt>**botões de TCS \_**</dt> </dl>                               | As guias aparecem como botões e nenhuma borda é desenhada em torno da área de exibição.<br/>                                                                                                                                                                                                                                                                             |
| <span id="TCS_FIXEDWIDTH"></span><span id="tcs_fixedwidth"></span><dl> <dt>**FIXEDWIDTH de TCS \_**</dt> </dl>                      | Todas as guias têm a mesma largura. Esse estilo não pode ser combinado com o \_ estilo de RIGHTJUSTIFY de TCS.<br/>                                                                                                                                                                                                                                                        |
| <span id="TCS_FLATBUTTONS"></span><span id="tcs_flatbuttons"></span><dl> <dt>**FLATBUTTONS de TCS \_**</dt> </dl>                   | [Versão 4,71](common-control-versions.md). As guias selecionadas aparecem como sendo recuadas em segundo plano enquanto outras guias aparecem como estando no mesmo plano que o plano de fundo. Esse estilo só afeta os controles de guia com o estilo de botões de TCS \_ .<br/>                                                                                                     |
| <span id="TCS_FOCUSNEVER"></span><span id="tcs_focusnever"></span><dl> <dt>**FOCUSNEVER de TCS \_**</dt> </dl>                      | O controle guia não recebe o foco de entrada quando clicado.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="TCS_FOCUSONBUTTONDOWN"></span><span id="tcs_focusonbuttondown"></span><dl> <dt>**FOCUSONBUTTONDOWN de TCS \_**</dt> </dl> | O controle guia recebe o foco de entrada quando clicado.<br/>                                                                                                                                                                                                                                                                                              |
| <span id="TCS_FORCEICONLEFT"></span><span id="tcs_forceiconleft"></span><dl> <dt>**FORCEICONLEFT de TCS \_**</dt> </dl>             | Os ícones são alinhados com a borda esquerda de cada guia de largura fixa. Esse estilo só pode ser usado com o estilo de FIXEDWIDTH de TCS \_ .<br/>                                                                                                                                                                                                                           |
| <span id="TCS_FORCELABELLEFT"></span><span id="tcs_forcelabelleft"></span><dl> <dt>**FORCELABELLEFT de TCS \_**</dt> </dl>          | Os rótulos são alinhados com a borda esquerda de cada guia de largura fixa; ou seja, o rótulo é exibido imediatamente à direita do ícone em vez de ser centralizado. Esse estilo só pode ser usado com o estilo de FIXEDWIDTH de TCS \_ e implica o estilo de TCS \_ FORCEICONLEFT.<br/>                                                                             |
| <span id="TCS_HOTTRACK"></span><span id="tcs_hottrack"></span><dl> <dt>**HOTTRACK de TCS \_**</dt> </dl>                            | [Versão 4,70](common-control-versions.md). Os itens sob o ponteiro são realçados automaticamente. Você pode verificar se o rastreamento dinâmico está habilitado chamando [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa). <br/>                                                                                                                              |
| <span id="TCS_MULTILINE"></span><span id="tcs_multiline"></span><dl> <dt>**multilinha de TCS \_**</dt> </dl>                         | Várias linhas de guias são exibidas, se necessário, para que todas as guias fiquem visíveis ao mesmo tempo.<br/>                                                                                                                                                                                                                                                                 |
| <span id="TCS_MULTISELECT"></span><span id="tcs_multiselect"></span><dl> <dt>**TCS \_ MULTIseleção**</dt> </dl>                   | [Versão 4,70](common-control-versions.md). Várias guias podem ser selecionadas mantendo a tecla CTRL pressionada ao clicar. Esse estilo deve ser usado com o estilo de botões de TCS \_ .<br/>                                                                                                                                                                         |
| <span id="TCS_OWNERDRAWFIXED"></span><span id="tcs_ownerdrawfixed"></span><dl> <dt>**OwnerDrawFixed de TCS \_**</dt> </dl>          | A janela pai é responsável por desenhar guias.<br/>                                                                                                                                                                                                                                                                                                  |
| <span id="TCS_RAGGEDRIGHT"></span><span id="tcs_raggedright"></span><dl> <dt>**RAGGEDRIGHT de TCS \_**</dt> </dl>                   | Linhas de guias não serão ampliadas para preencher toda a largura do controle. Esse estilo é o padrão.<br/>                                                                                                                                                                                                                                              |
| <span id="TCS_RIGHT"></span><span id="tcs_right"></span><dl> <dt>**TCS \_ à direita**</dt> </dl>                                     | [Versão 4,70](common-control-versions.md). As guias aparecem verticalmente no lado direito dos controles que usam o \_ estilo vertical de TCS. Esse valor é igual a TCS \_ inferior. Esse estilo não terá suporte se você usar estilos visuais.<br/>                                                                                                                            |
| <span id="TCS_RIGHTJUSTIFY"></span><span id="tcs_rightjustify"></span><dl> <dt>**RIGHTJUSTIFY de TCS \_**</dt> </dl>                | A largura de cada guia é aumentada, se necessário, para que cada linha de guias preencha toda a largura do controle guia. Este estilo de janela é ignorado, a menos que o estilo de multilinha de TCS \_ também seja especificado.<br/>                                                                                                                                               |
| <span id="TCS_SCROLLOPPOSITE"></span><span id="tcs_scrollopposite"></span><dl> <dt>**SCROLLOPPOSITE de TCS \_**</dt> </dl>          | [Versão 4,70](common-control-versions.md). As guias desnecessárias rolam para o lado oposto do controle quando uma guia é selecionada.<br/>                                                                                                                                                                                                                       |
| <span id="TCS_SINGLELINE"></span><span id="tcs_singleline"></span><dl> <dt>**\_individualização de TCS**</dt> </dl>                      | Somente uma linha de guias é exibida. O usuário pode rolar para ver mais guias, se necessário. Esse estilo é o padrão.<br/>                                                                                                                                                                                                                                   |
| <span id="TCS_TABS"></span><span id="tcs_tabs"></span><dl> <dt>**guias de TCS \_**</dt> </dl>                                        | As guias aparecem como guias e uma borda é desenhada em torno da área de exibição. Esse estilo é o padrão.<br/>                                                                                                                                                                                                                                                      |
| <span id="TCS_TOOLTIPS"></span><span id="tcs_tooltips"></span><dl> <dt>**Dicas de ferramentas de TCS \_**</dt> </dl>                            | O controle guia tem um controle ToolTip associado a ele. <br/>                                                                                                                                                                                                                                                                                          |
| <span id="TCS_VERTICAL"></span><span id="tcs_vertical"></span><dl> <dt>**TCS \_ vertical**</dt> </dl>                            | [Versão 4,70](common-control-versions.md). As guias são exibidas no lado esquerdo do controle, com o texto de tabulação exibido verticalmente. Esse estilo é válido somente quando usado com o estilo de multilinha de TCS \_ . Para fazer com que as guias sejam exibidas no lado direito do controle, use também o estilo de TCS \_ à direita. Esse estilo não terá suporte se você usar ComCtl32.dll versão 6.<br/> |



## <a name="remarks"></a>Comentários

Os estilos a seguir podem ser modificados após a criação do controle.

-   \_parte inferior do TCS
-   botões de TCS \_
-   FIXEDWIDTH de TCS \_
-   FLATBUTTONS de TCS \_
-   FORCEICONLEFT de TCS \_
-   FORCELABELLEFT de TCS \_
-   multilinha de TCS \_
-   OwnerDrawFixed de TCS \_
-   RAGGEDRIGHT de TCS \_
-   TCS \_ à direita
-   TCS \_ vertical

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

