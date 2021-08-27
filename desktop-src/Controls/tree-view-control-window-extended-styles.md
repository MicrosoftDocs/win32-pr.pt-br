---
title: Tree-View controle estilos estendidos (CommCtrl.h)
description: Esta seção lista os estilos estendidos usados ao criar controles de exibição de árvore. O valor de estilos estendidos é uma combinação bit a bit desses estilos.
ms.assetid: b45e7b7c-2c7b-49fa-8679-57c478b2f796
topic_type:
- apiref
api_name:
- TVS_EX_AUTOHSCROLL
- TVS_EX_DIMMEDCHECKBOXES
- TVS_EX_DOUBLEBUFFER
- TVS_EX_DRAWIMAGEASYNC
- TVS_EX_EXCLUSIONCHECKBOXES
- TVS_EX_FADEINOUTEXPANDOS
- TVS_EX_MULTISELECT
- TVS_EX_NOINDENTSTATE
- TVS_EX_NOSINGLECOLLAPSE
- TVS_EX_PARTIALCHECKBOXES
- TVS_EX_RICHTOOLTIP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed135e5c1cfd335333251c183b408a59d2768ac
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477382"
---
# <a name="tree-view-control-extended-styles"></a>Tree-View estilos estendidos de controle

Esta seção lista os estilos estendidos usados ao criar controles de exibição de árvore. O valor de estilos estendidos é uma combinação bit a bit desses estilos.




| Constante | Descrição | 
|----------|-------------|
| <span id="TVS_EX_AUTOHSCROLL"></span><span id="tvs_ex_autohscroll"></span><dl><dt><strong>TVS_EX_AUTOHSCROLL</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Remova a barra de rolagem horizontal e a rolagem automática, dependendo da posição do mouse.<br /> | 
| <span id="TVS_EX_DIMMEDCHECKBOXES"></span><span id="tvs_ex_dimmedcheckboxes"></span><dl><dt><strong>TVS_EX_DIMMEDCHECKBOXES</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Inclua o estado da caixa de seleção esmaecida se o controle tiver o <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> de seleção.<br /> | 
| <span id="TVS_EX_DOUBLEBUFFER"></span><span id="tvs_ex_doublebuffer"></span><dl><dt><strong>TVS_EX_DOUBLEBUFFER</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Especifica como a plano de fundo é apagada ou preenchida.<br /> | 
| <span id="TVS_EX_DRAWIMAGEASYNC"></span><span id="tvs_ex_drawimageasync"></span><dl><dt><strong>TVS_EX_DRAWIMAGEASYNC</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Recupera informações de grade do calendário.<br /> | 
| <span id="TVS_EX_EXCLUSIONCHECKBOXES"></span><span id="tvs_ex_exclusioncheckboxes"></span><dl><dt><strong>TVS_EX_EXCLUSIONCHECKBOXES</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Inclua o estado da caixa de seleção de exclusão se o controle tiver o <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> de exclusão.<br /> | 
| <span id="TVS_EX_FADEINOUTEXPANDOS"></span><span id="tvs_ex_fadeinoutexpandos"></span><dl><dt><strong>TVS_EX_FADEINOUTEXPANDOS</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Esmaeça os botões expando para dentro ou para fora quando o mouse se move para fora ou para um estado de passar o mouse sobre o controle.<br /> | 
| <span id="TVS_EX_MULTISELECT"></span><span id="tvs_ex_multiselect"></span><dl><dt><strong>TVS_EX_MULTISELECT</strong></dt></dl> | Sem suporte. Não use.<br /> | 
| <span id="TVS_EX_NOINDENTSTATE"></span><span id="tvs_ex_noindentstate"></span><dl><dt><strong>TVS_EX_NOINDENTSTATE</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Não recua a exibição de árvore para os botões expando.<br /> | 
| <span id="TVS_EX_NOSINGLECOLLAPSE"></span><span id="tvs_ex_nosinglecollapse"></span><dl><dt><strong>TVS_EX_NOSINGLECOLLAPSE</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. <strong>Destinado a uso interno; não recomendado para uso em aplicativos.</strong> Não resvale o item de exibição de árvore selecionado anteriormente, a menos que ele tenha o mesmo pai que a nova seleção. Esse estilo deve ser usado com o <a href="tree-view-control-window-styles.md"><strong>TVS_SINGLEEXPAND</strong></a> estilo. <br /><blockquote>[!Note]<br />Esse estilo pode não ter suporte em versões futuras do Comctl32.dll. Além disso, esse estilo não está definido em commctrl.h. Adicione a seguinte definição aos arquivos de origem do seu aplicativo para usar este estilo: <code>#define TVS_EX_NOSINGLECOLLAPSE 0x0001</code></blockquote><br /> | 
| <span id="TVS_EX_PARTIALCHECKBOXES"></span><span id="tvs_ex_partialcheckboxes"></span><dl><dt><strong>TVS_EX_PARTIALCHECKBOXES</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Inclua o estado parcial da caixa de seleção se o controle tiver o <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> de seleção.<br /> | 
| <span id="TVS_EX_RICHTOOLTIP"></span><span id="tvs_ex_richtooltip"></span><dl><dt><strong>TVS_EX_RICHTOOLTIP</strong></dt></dl> | <a href="common-control-versions.md">Windows Vista</a>. Permitir dicas de ferramenta rich no exibição de árvore (personalizado desenhado com ícone e texto).<br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





