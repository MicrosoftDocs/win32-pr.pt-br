---
title: Funções DWM
description: Esta seção contém informações sobre as funções Gerenciador de Janelas da Área de Trabalho (DWM).
ms.assetid: 525807fe-c5d7-4997-87b9-a14d02c33cc3
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), referência
- DWM (Gerenciador de Janelas da Área de Trabalho),referência
- Gerenciador de Janelas da Área de Trabalho (DWM), funções
- DWM (Gerenciador de Janelas da Área de Trabalho), funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe8c1db28571fde16cf0fe0f9068f5bd650d31f637776c7bcc00717ab3043997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503301"
---
# <a name="dwm-functions"></a>Funções DWM

Esta seção contém informações sobre as funções Gerenciador de Janelas da Área de Trabalho (DWM).

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
<td>Essa função não é implementada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a><br/></td>
<td>Procedimento de janela padrão para teste de acerto de DWM na área não cliente.<br/> Você também precisa garantir que <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> seja chamado para a <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> mensagem. Se <strong>DwmDefWindowProc</strong> não for chamado para WM_NCMOUSELEAVE mensagem, <strong>a</strong> DWM não <strong></strong>removerá <strong></strong> o realçamento dos botões Maximizar <strong>,</strong>Minimizar e Fechar quando o cursor sair da janela.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a><br/></td>
<td>Essa função não é implementada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a><br/></td>
<td>Habilita o efeito de desfoque em uma janela especificada.<br/></td>
<b>Observação</b> Começando com Windows 8, chamar essa função não resulta no efeito de desfoque, devido a uma alteração de estilo na maneira como as janelas são renderizadas.
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a><br/></td>
<td>Habilita ou desabilita a composição DWM. <br/>
<blockquote>
[!Note]<br />
Essa função foi preterida a partir Windows 8. O DWM não pode mais ser desabilitado programaticamente.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a><br/></td>
<td>Notifica o DWM para optar ou não pelo agendamento do MMCSS (Serviço de Agendamento de Classe Multimídia) enquanto o processo de chamada está ativas.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>Dwmextendframeintoclientarea</strong></a><br/></td>
<td>Estende o quadro da janela para a área do cliente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a><br/></td>
<td>Emite uma chamada de liberação que bloqueia o chamador até o próximo presente, quando todas as atualizações da superfície do Microsoft DirectX que estão pendentes no momento foram feitas. Isso compensa cenas muito complexas ou processos de chamada com prioridade muito baixa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a><br/></td>
<td>Recupera a cor atual usada para composição de vidro DWM. Esse valor é baseado no esquema de cores atual e pode ser modificado pelo usuário. Os aplicativos podem escutar alterações de cor manipulando a <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> de dados.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a><br/></td>
<td>Recupera as informações de tempo de composição atuais para uma janela especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a><br/></td>
<td>Essa função não é implementada.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a><br/></td>
<td>Essa função não é implementada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a><br/></td>
<td>Recupera atributos de transporte.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a><br/></td>
<td><blockquote>
<strong>Observação</strong>  Essa função está disponível publicamente, mas não é funcional, por Windows 10, versão 1803.
</blockquote>
Verifica os requisitos necessários para obter guias na barra de título do aplicativo para a janela especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a><br/></td>
<td>Recupera o valor atual de um atributo especificado aplicado a uma janela.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a><br/></td>
<td>Chamado por um aplicativo para indicar que todos os bitmaps iniciais fornecidos anteriormente de uma janela, miniaturas e representações de espiar, devem ser atualizados.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>Dwmiscompositionenabled</strong></a><br/></td>
<td>Obtém um valor que indica se a composição DWM está habilitada. Aplicativos em máquinas que executam Windows 7 ou anterior podem escutar alterações de estado de composição manipulando a <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> de composição.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a><br/></td>
<td>Altera o número de atções do monitor por meio do qual o quadro anterior será exibido. <br/> <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>Não há mais suporte para DwmModifyPreviousDxFrameDuration.</strong></a> Começando com Windows 8.1, as chamadas para <strong>DwmModifyPreviousDxFrameDuration</strong> sempre retornam E_NOTIMPL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a><br/></td>
<td>Recupera o tamanho da origem da miniatura DWM.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a><br/></td>
<td>Cria uma relação de miniatura DWM entre as janelas de origem e de destino.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a><br/></td>
<td>Notifica a DWM de que um contato de toque foi reconhecido como um gesto e que o DWM deve desenhar comentários para esse gesto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a><br/></td>
<td>Define o número de atções do monitor por meio do qual exibir o quadro apresentado. <br/> Não há mais suporte para <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration.</strong></a> Começando com Windows 8.1, as chamadas para <strong>DwmSetDxFrameDuration</strong> sempre retornam E_NOTIMPL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a><br/></td>
<td>Define um bitmap estático e estranho para exibir <em>uma</em> visualização ao vivo (também conhecida como uma visualização <em>de Espiar</em>) de uma janela ou guia. A barra de tarefas pode usar esse bitmap para mostrar uma visualização de tamanho completo de uma janela ou guia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a><br/></td>
<td>Define um bitmap estático e estranho em uma janela ou guia a ser usado como uma representação em miniatura. A barra de tarefas pode usar esse bitmap como um destino de comutador de miniatura para a janela ou guia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a><br/></td>
<td>Define os parâmetros atuais para a composição do quadro. <br/> <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>Não há mais suporte para DwmSetPresentParameters.</strong></a> Começando com Windows 8.1, as chamadas para <strong>DwmSetPresentParameters</strong> sempre retornam E_NOTIMPL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a><br/></td>
<td>Define o valor de atributos de renderização não cliente para uma janela.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a><br/></td>
<td>Chamado por um aplicativo ou estrutura para especificar o tipo de comentários visuais a ser desenhar em resposta a um contato de toque ou caneta específico.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a><br/></td>
<td>Habilita os comentários gráficos das interações de toque e arrastar para o usuário.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a><br/></td>
<td>Coordena as animações das janelas de ferramentas com o DWM.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a><br/></td>
<td>Remove uma relação de miniatura DWM criada pela <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>função DwmRegisterThumbnail.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a><br/></td>
<td>Atualiza as propriedades de uma miniatura DWM.<br/></td>
</tr>
</tbody>
</table>



 

 

