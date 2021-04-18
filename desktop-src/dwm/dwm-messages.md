---
title: Mensagens do DWM
description: Esta seção contém informações sobre as mensagens de Gerenciador de Janelas da Área de Trabalho (DWM).
ms.assetid: FF251CDA-7D68-4dd0-A54B-50B07E11C7C1
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), referência
- DWM (Gerenciador de Janelas da Área de Trabalho), referência
- Gerenciador de Janelas da Área de Trabalho (DWM), mensagens
- DWM (Gerenciador de Janelas da Área de Trabalho), mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399db1399cfc7cb60d29f0fa554a2233dc75a279
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "105771454"
---
# <a name="dwm-messages"></a>Mensagens do DWM

Esta seção contém informações sobre as mensagens de Gerenciador de Janelas da Área de Trabalho (DWM).

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
<td><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a><br/></td>
<td>Informa todas as janelas de nível superior que a cor de colorização alterou.<br/></td>
</tr>
<tr class="even">
<td><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a><br/></td>
<td>Informa todas as janelas de nível superior que a composição do DWM foi habilitada ou desabilitada. <br/>
<blockquote>
[!Note]<br />
A partir do Windows 8, a composição do DWM é sempre habilitada, portanto, essa mensagem não é enviada independentemente das alterações no modo de vídeo.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a><br/></td>
<td>Enviado quando a política de renderização de área não cliente é alterada.<br/></td>
</tr>
<tr class="even">
<td><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a><br/></td>
<td>Instrui uma janela para fornecer um bitmap estático a ser usado como uma <em>Visualização dinâmica</em> (também conhecida como <em>visualização de inspeção</em>) dessa janela.<br/></td>
</tr>
<tr class="odd">
<td><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a><br/></td>
<td>Instrui uma janela para fornecer um bitmap estático a ser usado como uma representação em miniatura dessa janela.<br/></td>
</tr>
<tr class="even">
<td><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a><br/></td>
<td>Enviado quando uma janela composta por DWM é maximizada.<br/></td>
</tr>
</tbody>
</table>



 

 

 





