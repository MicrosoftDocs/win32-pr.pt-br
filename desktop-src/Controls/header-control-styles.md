---
title: Estilos de controle de cabeçalho (CommCtrl. h)
description: Os controles de cabeçalho têm um número de estilos, descritos nesta seção, que determinam a aparência e o comportamento do controle. Você define os estilos iniciais ao criar o controle de cabeçalho.
ms.assetid: e47dc6c3-a1af-456c-9235-29ce63f1e13b
topic_type:
- apiref
api_name:
- HDS_BUTTONS
- HDS_DRAGDROP
- HDS_FILTERBAR
- HDS_FLAT
- HDS_FULLDRAG
- HDS_HIDDEN
- HDS_HORZ
- HDS_HOTTRACK
- HDS_CHECKBOXES
- HDS_NOSIZING
- HDS_OVERFLOW
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8450ad39cdb965e3e4be15f0093ec4737a87c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752195"
---
# <a name="header-control-styles"></a>Estilos de controle de cabeçalho

Os controles de cabeçalho têm um número de estilos, descritos nesta seção, que determinam a aparência e o comportamento do controle. Você define os estilos iniciais ao criar o controle de cabeçalho.



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
<td style="text-align: left;"><span id="HDS_BUTTONS"></span><span id="hds_buttons"></span><dl> <dt><strong>HDS_BUTTONS</strong></dt> </dl></td>
<td style="text-align: left;">Cada item do controle tem aparência e se comporta como um botão de ação. Esse estilo será útil se um aplicativo executar uma tarefa quando o usuário clicar em um item no controle de cabeçalho. Por exemplo, um aplicativo pode classificar informações nas colunas de forma diferente, dependendo de qual item o usuário clica. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_DRAGDROP"></span><span id="hds_dragdrop"></span><dl> <dt><strong>HDS_DRAGDROP</strong></dt> </dl></td>
<td style="text-align: left;">Permite reordenação do tipo "arrastar e soltar" de itens de cabeçalho. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FILTERBAR"></span><span id="hds_filterbar"></span><dl> <dt><strong>HDS_FILTERBAR</strong></dt> </dl></td>
<td style="text-align: left;">Inclua uma barra de filtro como parte do controle de cabeçalho padrão. Essa barra permite que os usuários apliquem convenientemente um filtro à exibição. Chamadas para <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> resultarão em um novo tamanho para o controle e farão com que a exibição de lista seja atualizada. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_FLAT"></span><span id="hds_flat"></span><dl> <dt><strong>HDS_FLAT</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versão 6,0 e posterior</a>. Faz com que o controle de cabeçalho seja desenhado simples quando o sistema operacional está em execução no modo clássico. <br/>
<blockquote>
[!Note]<br />
O Comctl32.dll versão 6 não é redistribuível, mas está incluído no Windows. Para usar Comctl32.dll versão 6, especifique-o em um manifesto. Para obter mais informações sobre manifestos, consulte <a href="cookbook-overview.md">habilitando estilos visuais</a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_FULLDRAG"></span><span id="hds_fulldrag"></span><dl> <dt><strong>HDS_FULLDRAG</strong></dt> </dl></td>
<td style="text-align: left;">Faz com que o controle de cabeçalho exiba o conteúdo da coluna mesmo quando o usuário redimensiona uma coluna. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HIDDEN"></span><span id="hds_hidden"></span><dl> <dt><strong>HDS_HIDDEN</strong></dt> </dl></td>
<td style="text-align: left;">Indica um controle de cabeçalho que deve ser ocultado. Esse estilo não oculta o controle. Em vez disso, quando você envia a mensagem de <a href="hdm-layout.md"><strong>HDM_LAYOUT</strong></a> para um controle de cabeçalho com o estilo de HDS_HIDDEN, o controle retorna zero no membro <strong>CY</strong> da estrutura <a href="/windows/win32/api/winuser/ns-winuser-windowpos"><strong>WINDOWPOS</strong></a> . Em seguida, você ocultaria o controle definindo sua altura como zero. Isso pode ser útil quando você deseja usar o controle como um contêiner de informações em vez de um controle visual. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_HORZ"></span><span id="hds_horz"></span><dl> <dt><strong>HDS_HORZ</strong></dt> </dl></td>
<td style="text-align: left;">Cria um controle de cabeçalho com uma orientação horizontal. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_HOTTRACK"></span><span id="hds_hottrack"></span><dl> <dt><strong>HDS_HOTTRACK</strong></dt> </dl></td>
<td style="text-align: left;">Habilita o rastreamento dinâmico. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_CHECKBOXES"></span><span id="hds_checkboxes"></span><dl> <dt><strong>HDS_CHECKBOXES</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versão 6, 0 e posterior</a>. Permite a colocação de caixas de seleção em itens de cabeçalho. Para obter mais informações, consulte o membro <strong>fmt</strong> de <a href="/windows/win32/api/commctrl/ns-commctrl-hditema"><strong>HDITEM</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="HDS_NOSIZING"></span><span id="hds_nosizing"></span><dl> <dt><strong>HDS_NOSIZING</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versão 6, 0 e posterior</a>. O usuário não pode arrastar o divisor no controle de cabeçalho.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="HDS_OVERFLOW"></span><span id="hds_overflow"></span><dl> <dt><strong>HDS_OVERFLOW</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versão 6, 0 e posterior</a>. Um botão é exibido quando nem todos os itens podem ser exibidos dentro do retângulo do controle de cabeçalho. Quando clicado, esse botão envia uma notificação de <a href="hdn-overflowclick.md">HDN_OVERFLOWCLICK</a> .<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentários

Para recuperar e alterar os estilos depois de criar o controle, use as funções [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) e [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



