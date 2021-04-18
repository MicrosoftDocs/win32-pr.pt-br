---
title: Estilos estendidos de controle de Tree-View (CommCtrl. h)
description: Esta seção lista os estilos estendidos usados ao criar controles de exibição em árvore. O valor dos estilos estendidos é uma combinação bit-a-bit desses estilos.
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
ms.openlocfilehash: 3ec20467e6a6bdeb98d57661d30292b55d4532f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749300"
---
# <a name="tree-view-control-extended-styles"></a>Tree-View estilos estendidos de controle

Esta seção lista os estilos estendidos usados ao criar controles de exibição em árvore. O valor dos estilos estendidos é uma combinação bit-a-bit desses estilos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="TVS_EX_AUTOHSCROLL"></span><span id="tvs_ex_autohscroll"></span><dl> <dt><strong>TVS_EX_AUTOHSCROLL</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Remova a barra de rolagem horizontal e a rolagem automática, dependendo da posição do mouse.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TVS_EX_DIMMEDCHECKBOXES"></span><span id="tvs_ex_dimmedcheckboxes"></span><dl> <dt><strong>TVS_EX_DIMMEDCHECKBOXES</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Inclua o estado de caixa de seleção esmaecida se o controle tiver o estilo de <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TVS_EX_DOUBLEBUFFER"></span><span id="tvs_ex_doublebuffer"></span><dl> <dt><strong>TVS_EX_DOUBLEBUFFER</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Especifica como o plano de fundo é apagado ou preenchido.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TVS_EX_DRAWIMAGEASYNC"></span><span id="tvs_ex_drawimageasync"></span><dl> <dt><strong>TVS_EX_DRAWIMAGEASYNC</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Recupera informações da grade de calendário.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TVS_EX_EXCLUSIONCHECKBOXES"></span><span id="tvs_ex_exclusioncheckboxes"></span><dl> <dt><strong>TVS_EX_EXCLUSIONCHECKBOXES</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Inclua o estado da caixa de seleção de exclusão se o controle tiver o estilo de <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TVS_EX_FADEINOUTEXPANDOS"></span><span id="tvs_ex_fadeinoutexpandos"></span><dl> <dt><strong>TVS_EX_FADEINOUTEXPANDOS</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Esmaecer botões de expansão para dentro ou para fora quando o mouse sai ou para um estado focalizando o controle.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TVS_EX_MULTISELECT"></span><span id="tvs_ex_multiselect"></span><dl> <dt><strong>TVS_EX_MULTISELECT</strong></dt> </dl></td>
<td style="text-align: left;">Não há suporte. Não use.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TVS_EX_NOINDENTSTATE"></span><span id="tvs_ex_noindentstate"></span><dl> <dt><strong>TVS_EX_NOINDENTSTATE</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Não recue o modo de exibição de árvore para os botões expando.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TVS_EX_NOSINGLECOLLAPSE"></span><span id="tvs_ex_nosinglecollapse"></span><dl> <dt><strong>TVS_EX_NOSINGLECOLLAPSE</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. <strong>Destinado ao uso interno; Não recomendado para uso em aplicativos.</strong> Não recolha o item de exibição de árvore selecionado anteriormente, a menos que ele tenha o mesmo pai da nova seleção. Esse estilo deve ser usado com o estilo de <a href="tree-view-control-window-styles.md"><strong>TVS_SINGLEEXPAND</strong></a> . <br/>
<blockquote>
[!Note]<br />
Esse estilo pode não ter suporte em versões futuras do Comctl32.dll. Além disso, esse estilo não é definido em commctrl. h. Adicione a seguinte definição aos arquivos de origem do seu aplicativo para usar este estilo: <code>#define TVS_EX_NOSINGLECOLLAPSE 0x0001</code>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="TVS_EX_PARTIALCHECKBOXES"></span><span id="tvs_ex_partialcheckboxes"></span><dl> <dt><strong>TVS_EX_PARTIALCHECKBOXES</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Inclua o estado de caixa de seleção parcial se o controle tiver o estilo de <a href="tree-view-control-window-styles.md"><strong>TVS_CHECKBOXES</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="TVS_EX_RICHTOOLTIP"></span><span id="tvs_ex_richtooltip"></span><dl> <dt><strong>TVS_EX_RICHTOOLTIP</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Windows Vista</a>. Permitir dicas de ferramenta avançadas no modo de exibição de árvore (desenho personalizado com ícone e texto).<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





