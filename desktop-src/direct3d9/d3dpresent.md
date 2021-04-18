---
description: Descreve a relação entre a taxa de atualização do adaptador e a taxa na qual as operações presentes ou presentes são concluídas. Esses valores também servem como valores de sinalizador para o campo PresentationIntervals de D3DCAPS9.
ms.assetid: a7d774c1-93c0-47d8-a8a7-e66e394726a3
title: D3DPRESENT (D3d9.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15b8bf496c8c8e10d50b23ad4f784634fb983d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105810776"
---
# <a name="d3dpresent"></a>D3DPRESENT

Descreve a relação entre a taxa de atualização do adaptador e a taxa na qual as operações [**presentes**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) ou [**presentes**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) são concluídas. Esses valores também servem como valores de sinalizador para o campo PresentationIntervals de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

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
<td style="text-align: left;"><span id="D3DPRESENT_DONOTFLIP"></span><span id="d3dpresent_donotflip"></span><dl> <dt><strong>D3DPRESENT_DONOTFLIP</strong></dt> </dl></td>
<td style="text-align: left;">Use o buffer frontal como a superfície de origem e de destino durante a renderização. Uma sincronização de quadros está agendada, mas a superfície exibida não é alterada. Esse sinalizador só está disponível quando o aplicativo está no modo de tela inteira e D3DSWAPEFFECT_FLIPEX foi especificado. <br/> Esse sinalizador está disponível somente no Direct3D 9Ex.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_DONOTWAIT"></span><span id="d3dpresent_donotwait"></span><dl> <dt><strong>D3DPRESENT_DONOTWAIT</strong></dt> </dl></td>
<td style="text-align: left;">Uma apresentação não pode ser agendada por um dispositivo Hal. Se esse sinalizador for definido em uma chamada para <a href="/windows/desktop/api"><strong>presente</strong></a>e o hardware estiver ocupado processando ou aguardando um intervalo de sincronização vertical, a apresentação retornará D3DERR_WASSTILLDRAWING para indicar que a operação blit está incompleta.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_FLIPRESTART"></span><span id="d3dpresent_fliprestart"></span><dl> <dt><strong>D3DPRESENT_FLIPRESTART</strong></dt> </dl></td>
<td style="text-align: left;">Reservado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_FORCEIMMEDIATE"></span><span id="d3dpresent_forceimmediate"></span><dl> <dt><strong>D3DPRESENT_FORCEIMMEDIATE</strong></dt> </dl></td>
<td style="text-align: left;">D3DPRESENT_INTERVAL_IMMEDIATE é imposta nesta chamada <a href="/windows/desktop/api"><strong>atual</strong></a> . Esse sinalizador só pode ser especificado ao usar D3DSWAPEFFECT_FLIPEX. Os comportamentos de apresentação em janela e em tela inteira são os mesmos. Isso é especialmente útil para aplicativos de mídia que desejam descartar os quadros que foram detectados como atrasados e apresentar quadros subsequentes no momento da composição. Um erro de parâmetro inválido será retornado se esse sinalizador for especificado incorretamente. Quando vários quadros consecutivos com D3DPRESENT_FORCEIMMEDIATEs são enfileirados, somente o último quadro é exibido, para apresentação em janela e em tela inteira.<br/> Esse sinalizador está disponível no Direct3D 9Ex no Windows 7 ou em sistemas operacionais posteriores.<br/> Ao usar D3DSWAPEFFECT_FLIPEX, cada quadro apresentado usando D3DPRESENT_INTERVAL_IMMEDIATE ou D3DPRESENT_INTERVAL_FORCEIMMEDIATE substituirá o intervalo atual do quadro anterior. Por exemplo, se você enfileirar os quadros a seguir usando os seguintes efeitos de permuta: quadro A (D3DPRESENT_INTERVAL_ONE), quadro B (D3DPRESENT_INTERVAL_ONE), quadro C (D3DPRESENT_INTERVAL_ONE), quadro D (D3DPRESENT_INTERVAL_FORCEIMMEDIATE), o quadro D substituirá o intervalo atual do quadro C. Os quadros exibidos por intervalo atual são o quadro A, quadro B, (quadro C substituído por) quadro D.<br/> Consulte Observações.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_DEFAULT"></span><span id="d3dpresent_interval_default"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_DEFAULT</strong></dt> </dl></td>
<td style="text-align: left;">Isso é quase equivalente ao D3DPRESENT_INTERVAL_ONE. Consulte Observações.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_ONE"></span><span id="d3dpresent_interval_one"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_ONE</strong></dt> </dl></td>
<td style="text-align: left;">O driver aguardará o período de retrace vertical (o tempo de execução passará a &quot; seguir &quot; para evitar a subdivisão). As operações <a href="/windows/desktop/api"><strong>presentes</strong></a> não serão afetadas com mais frequência do que a atualização da tela; o tempo de execução concluirá, no máximo, uma operação presente por período de atualização do adaptador. Isso é equivalente a usar D3DSWAPEFFECT_COPYVSYNC no DirectX 8,1. Essa opção está sempre disponível para cadeias de troca de tela inteira e em janelas. Consulte Observações.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_TWO"></span><span id="d3dpresent_interval_two"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_TWO</strong></dt> </dl></td>
<td style="text-align: left;">O driver aguardará o período de retrace vertical. As operações <a href="/windows/desktop/api"><strong>atuais</strong></a> não serão afetadas com mais frequência do que todas as segunda atualização de tela. Verifique a Cap PresentationIntervals (consulte <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>) para ver se D3DPRESENT_INTERVAL_TWO é suportada pelo driver.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_THREE"></span><span id="d3dpresent_interval_three"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_THREE</strong></dt> </dl></td>
<td style="text-align: left;">O driver aguardará o período de retrace vertical. As operações <a href="/windows/desktop/api"><strong>presentes</strong></a> não serão afetadas com mais frequência do que todas as outras atualizações de tela. Verifique a Cap PresentationIntervals (consulte <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>) para ver se D3DPRESENT_INTERVAL_THREE é suportada pelo driver.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_FOUR"></span><span id="d3dpresent_interval_four"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_FOUR</strong></dt> </dl></td>
<td style="text-align: left;">O driver aguardará o período de retrace vertical. As operações <a href="/windows/desktop/api"><strong>presentes</strong></a> não serão afetadas com mais frequência do que toda quarta tela de atualização. Verifique o membro PresentationIntervals (consulte <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>) para ver se D3DPRESENT_INTERVAL_FOUR é suportado pelo driver.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_INTERVAL_IMMEDIATE"></span><span id="d3dpresent_interval_immediate"></span><dl> <dt><strong>D3DPRESENT_INTERVAL_IMMEDIATE</strong></dt> </dl></td>
<td style="text-align: left;">O tempo de execução atualiza a área do cliente da janela imediatamente e pode fazer isso mais de uma vez durante o período de atualização do adaptador. Isso é equivalente a usar D3DSWAPEFFECT_COPY no DirectX 8. As operações <a href="/windows/desktop/api"><strong>presentes</strong></a> podem ser afetadas imediatamente. Essa opção está sempre disponível para cadeias de troca de tela inteira e em janelas. Consulte Observações.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_LINEAR_CONTENT"></span><span id="d3dpresent_linear_content"></span><dl> <dt><strong>D3DPRESENT_LINEAR_CONTENT</strong></dt> </dl></td>
<td style="text-align: left;">O conteúdo do buffer de fundo a ser apresentado está no espaço de cores linear. <br/>
<ul>
<li>A apresentação converterá implicitamente o espaço linear em sRGB (gama = 2,2). Essa é a única conversão com suporte.</li>
<li>Como esse sinalizador representa uma propriedade do conteúdo do buffer de fundo, o sinalizador pode ser especificado durante uma chamada <a href="/windows/desktop/api"><strong>atual</strong></a> . Em outras palavras, um aplicativo pode apresentar conteúdo linear em um único quadro e, em seguida, alternar para o conteúdo corrigido na próxima.</li>
<li>Esse sinalizador é ignorado quando a cadeia de permuta está em tela inteira. (Observe que esse sinalizador está disponível apenas na versão da cadeia de permuta explícita do <a href="/windows/desktop/api"><strong>presente</strong></a>. O método <a href="/windows/desktop/api"><strong>Present</strong></a> não assume um parâmetro flags.)</li>
<li>Esse sinalizador é sempre aceito, mas só entrará em vigor quando o driver expõe >D3DCAPS3_LINEAR_TO_SRGB_PresentATION.</li>
<li>O único formato de buffer de fundo com suporte é <a href="d3dformat.md">X8R8G8B8</a>.</li>
</ul>
Consulte <a href="gamma.md">cadeias de permuta em janelas</a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_VIDEO_RESTRICT_TO_MONITOR"></span><span id="d3dpresent_video_restrict_to_monitor"></span><dl> <dt><strong>D3DPRESENT_VIDEO_RESTRICT_TO_MONITOR</strong></dt> </dl></td>
<td style="text-align: left;">Corta o conteúdo renderizado para o monitor/dispositivo no qual o adaptador está direcionando, mostra miniaturas para o conteúdo na exibição de Flip3D e miniaturas de barra de tarefas em outros monitores. <br/> Esse sinalizador está disponível somente no Direct3D 9Ex.<br/> Consulte <a href="/windows/desktop/dwm/dwm-overview">Gerenciador de janelas da área de trabalho</a> para obter mais detalhes sobre esse recurso do Windows Vista. Se você não estiver executando no modo de composição de área de trabalho, o sinalizador dará o mesmo comportamento que <a href="d3dpresentflag.md">D3DPRESENTFLAG_DEVICECLIP</a>.<br/>
<blockquote>
[!Note]<br />
Esse sinalizador só deve ser usado com o efeito de permuta D3DSWAPEFFECT_FLIPEX. O uso desse sinalizador com <em>outros</em> efeitos de permuta está sendo preterido e pode não funcionar em versões futuras do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_UPDATEOVERLAYONLY"></span><span id="d3dpresent_updateoverlayonly"></span><dl> <dt><strong>D3DPRESENT_UPDATEOVERLAYONLY</strong></dt> </dl></td>
<td style="text-align: left;">Atualiza a posição de sobreposição ou os dados de COLORKEY sem causar uma inversão real e sem alterar a duração com a qual a imagem é exibida.<br/> Esse sinalizador está disponível somente no Direct3D 9Ex.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="D3DPRESENT_HIDEOVERLAY"></span><span id="d3dpresent_hideoverlay"></span><dl> <dt><strong>D3DPRESENT_HIDEOVERLAY</strong></dt> </dl></td>
<td style="text-align: left;">Desativa o hardware de sobreposição.<br/> Esse sinalizador está disponível somente no Direct3D 9Ex.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="D3DPRESENT_UPDATECOLORKEY"></span><span id="d3dpresent_updatecolorkey"></span><dl> <dt><strong>D3DPRESENT_UPDATECOLORKEY</strong></dt> </dl></td>
<td style="text-align: left;">Redesenha os dados de COLORKEY.<br/> Esse sinalizador está disponível somente no Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Comentários

O modo de janela dá suporte ao \_ \_ padrão de intervalo D3DPRESENT, D3DPRESENT \_ intervalo \_ imediato e D3DPRESENT \_ intervalo \_ um. \_ \_ O padrão de intervalo D3DPRESENT e o intervalo de D3DPRESENT \_ \_ são quase equivalentes (consulte as informações sobre a resolução do timer abaixo). Eles são executados de forma semelhante para copiar \_ vsync, pois há apenas um presente por quadro, e eles impedem a subdivisão com o feixe. Por outro lado, o intervalo de D3DPRESENT \_ \_ imediato tentará fornecer uma taxa de apresentação ilimitada.

O modo de tela inteira dá suporte ao uso semelhante ao modo de janela ao dar suporte ao \_ intervalo D3DPRESENT \_ imediato, independentemente da taxa de atualização ou do efeito de permuta. O \_ \_ padrão de intervalo D3DPRESENT usa a resolução de temporizador do sistema padrão, enquanto o intervalo de D3DPRESENT \_ \_ chama [**timeBeginPeriod**](/windows/win32/api/timeapi/nf-timeapi-timebeginperiod) para aprimorar a resolução do temporizador do sistema. Isso melhora a qualidade da sincronização vertical, mas consome um pouco mais tempo de processamento. Ambos os parâmetros tentam sincronizar verticalmente.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9. h</dt> </dl> |

## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes do Direct3D](dx9-graphics-reference-d3d-constants.md)
