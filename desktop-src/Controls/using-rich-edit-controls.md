---
title: Usando controles de edição rich
description: Esta seção contém tópicos que demonstram como criar e usar controles de edição rich.
ms.assetid: 2c4717c9-3257-42d5-9c36-89b7e524e788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c31f1d6a5fc743221cef282737e4c93d10fb9bd015e75f898f72726b74c5019d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077770"
---
# <a name="using-rich-edit-controls"></a>Usando controles de edição rich

Esta seção contém tópicos que demonstram como criar e usar controles de edição rich.

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
<td><a href="create-rich-edit-controls.md">Como criar controles de edição rich</a><br/></td>
<td>Para criar um controle de edição avançada, chame a <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>função CreateWindowEx,</strong></a> especificando a classe de janela de edição avançada. Para Microsoft Rich Edit 4.1 (Msftedit.dll), especifique MSFTEDIT_CLASS como a classe de janela. Para todas as versões anteriores, especifique RICHEDIT_CLASS. Para obter mais informações, consulte <a href="about-rich-edit-controls.md">Versões do Rich Edit.</a> <br/> Controles de edição rich suportam a maioria dos estilos de janela usados com controles de edição, bem como estilos adicionais. Você deve especificar o <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> de janela se quiser permitir mais de uma linha de texto no controle . Para obter mais informações, consulte <a href="rich-edit-control-styles.md">Estilos de controle de edição rich</a>. <br/></td>
</tr>
<tr class="even">
<td><a href="format-text-in-rich-edit-controls.md">Como formatar texto em controles de edição rich</a><br/></td>
<td>Um aplicativo pode enviar mensagens para um controle de edição rico para formatar caracteres e parágrafos e recuperar informações de formatação. Os atributos de formatação de parágrafo incluem alinhamento, guias, recuos, numeração e tabelas simples. Para caracteres, você pode especificar o nome da fonte, o tamanho, a cor e os efeitos, como negrito, itálico e protegido. <br/></td>
</tr>
<tr class="odd">
<td><a href="interact-with-the-current-selection.md">Como interagir com a seleção atual</a><br/></td>
<td>O usuário pode selecionar o texto em um controle de edição rico usando o mouse ou o teclado. A <em>seleção atual</em> é o intervalo de caracteres selecionados ou a posição do ponto de inserção se nenhum caractere for selecionado. Um aplicativo pode obter informações sobre a seleção atual, defini-la, determinar quando ele muda e mostrar ou ocultar o realçando da seleção. <br/></td>
</tr>
<tr class="even">
<td><a href="use-rich-edit-text-operations.md">Como usar operações de edição de texto rich</a><br/></td>
<td>Um aplicativo pode enviar mensagens para recuperar ou encontrar texto em um controle de edição rico. Você pode recuperar o texto selecionado ou um intervalo de texto especificado. <br/></td>
</tr>
<tr class="odd">
<td><a href="use-word-and-line-break-information.md">Como usar informações de quebra de linha e palavra</a><br/></td>
<td>Um controle de edição avançada chama uma função chamada um procedimento de quebra de palavras para encontrar quebras entre palavras e determinar onde ele pode quebrar linhas. O controle usa essas informações ao executar operações de quebra de texto e ao processar combinações de tecla CTRL+SETA PARA A ESQUERDA e CTRL+SETA PARA A DIREITA. Um aplicativo pode enviar mensagens para um controle de edição rich para substituir o procedimento de quebra de palavras padrão, recuperar informações de quebra de palavras e determinar em qual linha um determinado caractere se enquadra. <br/></td>
</tr>
<tr class="even">
<td><a href="use-rich-edit-clipboard-operations.md">Como usar operações de área de transferência de edição rica</a><br/></td>
<td>Um aplicativo pode colar o conteúdo da área de transferência em um controle de edição rico usando o melhor formato de área de transferência disponível ou um formato de área de transferência específico. Você também pode determinar se um controle de edição rico é capaz de colar um formato de área de transferência. <br/></td>
</tr>
<tr class="odd">
<td><a href="use-streams.md">Como usar Fluxos</a><br/></td>
<td>Você pode usar fluxos para transferir dados para dentro ou fora de um controle de edição rico. Um fluxo é definido por uma <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>estrutura EDITSTREAM,</strong></a> que especifica um buffer e uma função de retorno de chamada definida pelo aplicativo. <br/></td>
</tr>
<tr class="even">
<td><a href="automatically-resize-rich-edit-controls.md">Como reorganizar automaticamente controles de edição rich</a><br/></td>
<td>Um aplicativo pode reorganizar um controle de edição rico conforme necessário para que ele sempre tenha o mesmo tamanho que seu conteúdo. Um controle de edição avançada dá suporte a essa funcionalidade <a href="en-requestresize.md"></a> chamada <em>bottomless</em> enviando à janela pai um código de EN_REQUESTRESIZE de notificação sempre que o tamanho do conteúdo do controle mudar. <br/></td>
</tr>
<tr class="odd">
<td><a href="use-rich-edit-control-notification-codes.md">Como usar códigos de notificação de controle de edição rich</a><br/></td>
<td>A janela pai de um controle de edição rica pode processar códigos de notificação para monitorar eventos que afetam o controle. Controles de edição rich suportam todos os códigos de notificação usados com controles de edição, bem como vários outros. <br/></td>
</tr>
<tr class="even">
<td><a href="use-font-binding-in-rich-edit-controls.md">Como usar a associação de fonte em controles de edição rich</a><br/></td>
<td>O Microsoft Rich Edit 3.0 atribui um conjunto de caracteres a caracteres de texto sem-texto, dependendo do contexto. Alguns exemplos incluem: <br/>
<ul>
<li>Caracteres gregos são <strong>atribuídos GREEK_CHARSET</strong>.</li>
<li>Os símbolos hangul são atribuídos <strong>HANGUL_CHARSET</strong>.</li>
<li>Caracteres chineses são atribuídos <strong>SHIFTJIS_CHARSET</strong> caracteres kana são encontrados próximos <strong>ou</strong> GB2312_CHARSET se nenhum kana for encontrado próximo.</li>
<li>Caracteres ANSI não neutros são atribuídos <strong>ANSI_CHARSET</strong> em qualquer evento.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="using-rich-edit-com.md">Como usar o OLE em controles de edição rich</a><br/></td>
<td>Esta seção contém informações sobre como usar a vinculação de objeto e a incorporação (OLE) em controles de edição rich. <br/></td>
</tr>
<tr class="even">
<td><a href="printing-rich-edit-controls.md">Como imprimir o conteúdo de controles de edição rich</a><br/></td>
<td>Esta seção contém informações sobre como imprimir o conteúdo de controles de edição rich. <br/></td>
</tr>
</tbody>
</table>



 

 

