---
title: Estilos de controle de animação (CommCtrl. h)
description: Esta seção lista os estilos de janela usados com controles de animação.
ms.assetid: ad4fc4fd-166d-4871-9f60-5133a48681aa
topic_type:
- apiref
api_name:
- ACS_AUTOPLAY
- ACS_CENTER
- ACS_TIMER
- ACS_TRANSPARENT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d779b92c51420bc6bd9ad238bcff538dbc85841f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753970"
---
# <a name="animation-control-styles"></a>Estilos de controle de animação

Esta seção lista os estilos de janela usados com controles de animação.



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
<td style="text-align: left;"><span id="ACS_AUTOPLAY"></span><span id="acs_autoplay"></span><dl> <dt><strong>ACS_AUTOPLAY</strong></dt> </dl></td>
<td style="text-align: left;">Começa a reproduzir a animação assim que o clipe AVI é aberto. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_CENTER"></span><span id="acs_center"></span><dl> <dt><strong>ACS_CENTER</strong></dt> </dl></td>
<td style="text-align: left;">Centraliza a animação na janela do controle de animação. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_TIMER"></span><span id="acs_timer"></span><dl> <dt><strong>ACS_TIMER</strong></dt> </dl></td>
<td style="text-align: left;">Por padrão, o controle cria um thread para reproduzir o clipe AVI. Se você definir esse sinalizador, o controle reproduzirá o clipe sem criar um thread; internamente, o controle usa um temporizador do Win32 para sincronizar a reprodução. <br/> <strong>Comctl32.dll versão 6 e posterior:</strong> Não há suporte para esse estilo. Por padrão, o controle reproduz o clipe AVI sem criar um thread.<br/>
<blockquote>
[!Note]<br />
Comctl32.dll versão 6 não é redistribuível. Para usar Comctl32.dll versão 6, especifique-o em um manifesto. Para obter mais informações sobre manifestos, consulte <a href="cookbook-overview.md">habilitando estilos visuais</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_TRANSPARENT"></span><span id="acs_transparent"></span><dl> <dt><strong>ACS_TRANSPARENT</strong></dt> </dl></td>
<td style="text-align: left;">Permite que você coincida a cor do plano de fundo de uma animação com a da janela subjacente, criando um &quot; &quot; plano de fundo transparente. O pai do controle de animação não deve ter o estilo de WS_CLIPCHILDREN (consulte <a href="/windows/desktop/winmsg/window-styles">estilos de janela</a>). O controle envia uma mensagem de <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> para seu pai. Use <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>SetBkColor</strong></a> para definir a cor do plano de fundo para o contexto do dispositivo como um valor apropriado. O controle interpreta o pixel superior esquerdo do primeiro quadro como a cor de fundo padrão da animação. Ele remapeará todos os pixels com essa cor para o valor que você forneceu em resposta a WM_CTLCOLORSTATIC. <br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



