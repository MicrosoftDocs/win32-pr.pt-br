---
title: Funções do DWM
description: Esta seção contém informações sobre as funções de Gerenciador de Janelas da Área de Trabalho (DWM).
ms.assetid: 525807fe-c5d7-4997-87b9-a14d02c33cc3
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), referência
- DWM (Gerenciador de Janelas da Área de Trabalho), referência
- Gerenciador de Janelas da Área de Trabalho (DWM), funções
- DWM (Gerenciador de Janelas da Área de Trabalho), funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067f836e7fa8b5b84be02a402a3e0b3d0f78d1c1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104294549"
---
# <a name="dwm-functions"></a>Funções do DWM

Esta seção contém informações sobre as funções de Gerenciador de Janelas da Área de Trabalho (DWM).

## <a name="in-this-section"></a>Nesta seção



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a><br/></td>
<td>Esta função não está implementada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a><br/></td>
<td>Procedimento de janela padrão para teste de clique de DWM na área não cliente.<br/> Você também precisa garantir que <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> seja chamado para a mensagem de <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> . Se <strong>DwmDefWindowProc</strong> não for chamado para a mensagem de <strong>WM_NCMOUSELEAVE</strong> , o DWM não removerá o realce dos botões <strong>maximizar</strong>, <strong>minimizar</strong>e <strong>fechar</strong> quando o cursor sair da janela.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a><br/></td>
<td>Esta função não está implementada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a><br/></td>
<td>Habilita o efeito de desfoque em uma janela especificada.<br/></td>
<b>Observação</b> A partir do Windows 8, chamar essa função não resulta no efeito de desfoque, devido a uma alteração de estilo na maneira como as janelas são renderizadas.
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a><br/></td>
<td>Habilita ou desabilita a composição do DWM. <br/>
<blockquote>
[!Note]<br />
Essa função foi preterida a partir do Windows 8. O DWM não pode mais ser desabilitado por meio de programação.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a><br/></td>
<td>Notifica o DWM para aceitar ou sair do agendamento do serviço de agendamento de classe de multimídia (MMCSS) enquanto o processo de chamada está ativo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a><br/></td>
<td>Estende o quadro da janela para a área do cliente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a><br/></td>
<td>Emite uma chamada de liberação que bloqueia o chamador até o próximo momento, quando todas as atualizações da superfície do Microsoft DirectX que estão pendentes no momento foram feitas. Isso compensa cenas muito complexas ou processos de chamada com prioridade muito baixa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a><br/></td>
<td>Recupera a cor atual usada para composição do DWM Glass. Esse valor é baseado no esquema de cores atual e pode ser modificado pelo usuário. Os aplicativos podem escutar alterações de cores manipulando a notificação de <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a><br/></td>
<td>Recupera as informações de tempo de composição atuais para uma janela especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a><br/></td>
<td>Esta função não está implementada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a><br/></td>
<td>Esta função não está implementada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a><br/></td>
<td>Recupera atributos de transporte.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a><br/></td>
<td><blockquote>
<strong>Observação</strong>  Essa função está disponível publicamente, mas não funcional, para o Windows 10, versão 1803.
</blockquote>
Verifica os requisitos necessários para obter guias na barra de título do aplicativo para a janela especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a><br/></td>
<td>Recupera o valor atual de um atributo especificado aplicado a uma janela.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a><br/></td>
<td>Chamado por um aplicativo para indicar que todos os bitmaps icônico fornecidos anteriormente de uma janela, miniaturas e representações de inspeção, devem ser atualizados.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a><br/></td>
<td>Obtém um valor que indica se a composição do DWM está habilitada. Os aplicativos em computadores que executam o Windows 7 ou anterior podem escutar alterações de estado de composição manipulando a notificação de <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a><br/></td>
<td>Altera o número de atualizações do monitor por meio do qual o quadro anterior será exibido. <br/> Não há mais suporte para <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> . Começando com Windows 8.1, chamadas para <strong>DwmModifyPreviousDxFrameDuration</strong> sempre retornam E_NOTIMPL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a><br/></td>
<td>Recupera o tamanho da origem da miniatura do DWM.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a><br/></td>
<td>Cria uma relação de miniatura do DWM entre as janelas de destino e de origem.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a><br/></td>
<td>Notifica o DWM de que um contato de toque foi reconhecido como um gesto e que o DWM deve desenhar comentários para esse gesto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a><br/></td>
<td>Define o número de atualizações do monitor por meio do qual exibir o quadro apresentado. <br/> Não há mais suporte para <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> . Começando com Windows 8.1, chamadas para <strong>DwmSetDxFrameDuration</strong> sempre retornam E_NOTIMPL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a><br/></td>
<td>Define um bitmap estático icônico para exibir uma <em>Visualização dinâmica</em> (também conhecida como visualização de <em>inspeção</em>) de uma janela ou guia. A barra de tarefas pode usar esse bitmap para mostrar uma visualização de tamanho completo de uma janela ou guia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a><br/></td>
<td>Define um bitmap estático icônico em uma janela ou guia para usar como uma representação em miniatura. A barra de tarefas pode usar esse bitmap como um destino de alternância de miniatura para a janela ou guia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a><br/></td>
<td>Define os parâmetros atuais para composição de quadros. <br/> Não há mais suporte para <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> . Começando com Windows 8.1, chamadas para <strong>DwmSetPresentParameters</strong> sempre retornam E_NOTIMPL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a><br/></td>
<td>Define o valor de atributos de renderização que não são de cliente para uma janela.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a><br/></td>
<td>Chamado por um aplicativo ou estrutura para especificar o tipo de comentário visual a ser desenhado em resposta a um contato de caneta ou toque específico.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a><br/></td>
<td>Habilita os comentários gráficos de toque e arrasta as interações para o usuário.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a><br/></td>
<td>Coordena as animações de janelas de ferramentas com o DWM.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a><br/></td>
<td>Remove uma relação de miniatura do DWM criada pela função <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a><br/></td>
<td>Atualiza as propriedades de uma miniatura do DWM.<br/></td>
</tr>
</tbody>
</table>



 

 

