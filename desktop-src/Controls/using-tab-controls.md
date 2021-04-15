---
title: Usando controles de guia
description: Este tópico contém dois exemplos que usam controles guia.
ms.assetid: 29cc2f47-5667-4b03-8af8-51995a90a3dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78432e24f85ed3fa6a3c71a056ae25ede920f6e0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104454413"
---
# <a name="using-tab-controls"></a>Usando controles de guia

Este tópico contém dois exemplos que usam controles guia. O primeiro exemplo demonstra como usar um controle guia para alternar entre várias páginas de texto na janela principal de um aplicativo. O segundo exemplo demonstra como usar um controle guia para alternar entre várias páginas de controles em uma caixa de diálogo.

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
<td><a href="create-a-tab-control-in-the-main-window.md">Como criar um controle guia na janela principal</a><br/></td>
<td>O exemplo nesta seção demonstra como criar um controle guia e exibi-lo na área cliente da janela principal do aplicativo. O aplicativo exibe uma terceira janela (um controle estático) na área de exibição do controle guia. A janela pai posiciona e dimensiona o controle de tabulação e o controle estático ao processar a mensagem de <a href="/windows/desktop/winmsg/wm-size"><strong>WM_SIZE</strong></a> . <br/> Há sete guias neste exemplo, uma para cada dia da semana. Quando o usuário seleciona uma guia, o aplicativo exibe o nome do dia correspondente no controle estático. <br/></td>
</tr>
<tr class="even">
<td><a href="create-a-tabbed-dialog-box.md">Como criar uma caixa de diálogo com guias</a><br/></td>
<td>O exemplo nesta seção demonstra como criar uma caixa de diálogo que usa guias para fornecer várias páginas de controles. A caixa de diálogo principal é uma caixa de diálogo modal. Cada página de controles é definida por um modelo de caixa de diálogo que tem o estilo de <a href="/windows/desktop/winmsg/window-styles"><strong>WS_CHILD</strong></a> . Quando uma guia é selecionada, uma caixa de diálogo sem janela restrita é criada para a página de entrada e a caixa de diálogo da página de saída é destruída. <br/>
<blockquote>
[!Note]<br />
Em muitos casos, você pode implementar caixas de diálogo de várias páginas com mais facilidade usando folhas de propriedades. Para obter mais informações sobre folhas de propriedades, consulte <a href="property-sheets.md">about Property Sheets</a>.
</blockquote>
<br/> O modelo da caixa de diálogo principal simplesmente define dois controles Button. Ao processar a mensagem de <a href="/windows/desktop/dlgbox/wm-initdialog"><strong>WM_INITDIALOG</strong></a> , o procedimento da caixa de diálogo cria um controle guia e carrega os recursos de modelo da caixa de diálogo para cada uma das caixas de diálogo filhas. <br/></td>
</tr>
</tbody>
</table>



 

