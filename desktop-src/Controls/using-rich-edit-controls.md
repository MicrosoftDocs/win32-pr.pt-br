---
title: Usando controles de edição avançados
description: Esta seção contém tópicos que demonstram como criar e usar controles de edição avançados.
ms.assetid: 2c4717c9-3257-42d5-9c36-89b7e524e788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0489660bb6849d0de76ae7fc2f4e21ca931662a8
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104454415"
---
# <a name="using-rich-edit-controls"></a><span data-ttu-id="bebdc-103">Usando controles de edição avançados</span><span class="sxs-lookup"><span data-stu-id="bebdc-103">Using Rich Edit Controls</span></span>

<span data-ttu-id="bebdc-104">Esta seção contém tópicos que demonstram como criar e usar controles de edição avançados.</span><span class="sxs-lookup"><span data-stu-id="bebdc-104">This section contains topics that demonstrate how to create and use rich edit controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bebdc-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="bebdc-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bebdc-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="bebdc-106">Topic</span></span></th>
<th><span data-ttu-id="bebdc-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="bebdc-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bebdc-108"><a href="create-rich-edit-controls.md">Como criar controles de edição avançados</a></span><span class="sxs-lookup"><span data-stu-id="bebdc-108"><a href="create-rich-edit-controls.md">How to Create Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="bebdc-109">Para criar um controle de edição rico, chame a função <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> , especificando a classe da janela de edição rica.</span><span class="sxs-lookup"><span data-stu-id="bebdc-109">To create a rich edit control, call the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> function, specifying the rich edit window class.</span></span> <span data-ttu-id="bebdc-110">Para o Microsoft rich edit 4,1 (Msftedit.dll), especifique MSFTEDIT_CLASS como a classe de janela.</span><span class="sxs-lookup"><span data-stu-id="bebdc-110">For Microsoft Rich Edit 4.1 (Msftedit.dll), specify MSFTEDIT_CLASS as the window class.</span></span> <span data-ttu-id="bebdc-111">Para todas as versões anteriores, especifique RICHEDIT_CLASS.</span><span class="sxs-lookup"><span data-stu-id="bebdc-111">For all previous versions, specify RICHEDIT_CLASS.</span></span> <span data-ttu-id="bebdc-112">Para obter mais informações, consulte <a href="about-rich-edit-controls.md">versões do rich edit</a>.</span><span class="sxs-lookup"><span data-stu-id="bebdc-112">For more information, see <a href="about-rich-edit-controls.md">Versions of Rich Edit</a>.</span></span> <br/> <span data-ttu-id="bebdc-113">Os controles de edição avançados dão suporte à maioria dos estilos de janela usados com controles de edição, bem como estilos adicionais.</span><span class="sxs-lookup"><span data-stu-id="bebdc-113">Rich edit controls support most of the window styles used with edit controls as well as additional styles.</span></span> <span data-ttu-id="bebdc-114">Você deve especificar o estilo de janela <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> se desejar permitir mais de uma linha de texto no controle.</span><span class="sxs-lookup"><span data-stu-id="bebdc-114">You should specify the <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> window style if you want to allow more than one line of text in the control.</span></span> <span data-ttu-id="bebdc-115">Para obter mais informações, consulte <a href="rich-edit-control-styles.md">Rich Edit Control Styles</a>.</span><span class="sxs-lookup"><span data-stu-id="bebdc-115">For more information, see <a href="rich-edit-control-styles.md">Rich Edit Control Styles</a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bebdc-116"><a href="format-text-in-rich-edit-controls.md">Como formatar texto em controles de edição avançados</a></span><span class="sxs-lookup"><span data-stu-id="bebdc-116"><a href="format-text-in-rich-edit-controls.md">How to Format Text in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="bebdc-117">Um aplicativo pode enviar mensagens para um controle de edição rico a fim de formatar caracteres e parágrafos e recuperar informações de formatação.</span><span class="sxs-lookup"><span data-stu-id="bebdc-117">An application can send messages to a rich edit control in order to format characters and paragraphs and retrieve formatting information.</span></span> <span data-ttu-id="bebdc-118">Os atributos de formatação de parágrafo incluem alinhamento, tabulações, recuos, numeração e tabelas simples.</span><span class="sxs-lookup"><span data-stu-id="bebdc-118">Paragraph formatting attributes include alignment, tabs, indents, numbering, and simple tables.</span></span> <span data-ttu-id="bebdc-119">Para caracteres, você pode especificar o nome, o tamanho, a cor e os efeitos da fonte, como negrito, itálico e protegido.</span><span class="sxs-lookup"><span data-stu-id="bebdc-119">For characters, you can specify font name, size, color, and effects such as bold, italic, and protected.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bebdc-120"><a href="interact-with-the-current-selection.md">Como interagir com a seleção atual</a></span><span class="sxs-lookup"><span data-stu-id="bebdc-120"><a href="interact-with-the-current-selection.md">How to Interact with the Current Selection</a></span></span><br/></td>
<td><span data-ttu-id="bebdc-121">O usuário pode selecionar o texto em um controle de edição rico usando o mouse ou o teclado.</span><span class="sxs-lookup"><span data-stu-id="bebdc-121">The user can select text in a rich edit control by using the mouse or the keyboard.</span></span> <span data-ttu-id="bebdc-122">A <em>seleção atual</em> é o intervalo de caracteres selecionados ou a posição do ponto de inserção se nenhum caractere for selecionado.</span><span class="sxs-lookup"><span data-stu-id="bebdc-122">The <em>current selection</em> is the range of selected characters, or the position of the insertion point if no characters are selected.</span></span> <span data-ttu-id="bebdc-123">Um aplicativo pode obter informações sobre a seleção atual, defini-la, determinar quando ela é alterada e mostrar ou ocultar o realce de seleção.</span><span class="sxs-lookup"><span data-stu-id="bebdc-123">An application can get information about the current selection, set it, determine when it changes, and show or hide the selection highlight.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bebdc-124"><a href="use-rich-edit-text-operations.md">Como usar operações de Rich Text de edição</a></span><span class="sxs-lookup"><span data-stu-id="bebdc-124"><a href="use-rich-edit-text-operations.md">How to Use Rich Edit Text Operations</a></span></span><br/></td>
<td><span data-ttu-id="bebdc-125">Um aplicativo pode enviar mensagens para recuperar ou localizar texto em um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="bebdc-125">An application can send messages to retrieve or find text in a rich edit control.</span></span> <span data-ttu-id="bebdc-126">Você pode recuperar o texto selecionado ou um intervalo de texto especificado.</span><span class="sxs-lookup"><span data-stu-id="bebdc-126">You can retrieve either the selected text or a specified range of text.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bebdc-127"><a href="use-word-and-line-break-information.md">Como usar o Word e as informações de quebra de linha</a></span><span class="sxs-lookup"><span data-stu-id="bebdc-127"><a href="use-word-and-line-break-information.md">How to Use Word and Line Break Information</a></span></span><br/></td>
<td><span data-ttu-id="bebdc-128">Um controle de edição rico chama uma função chamada de procedimento de quebra de palavra para localizar quebras entre palavras e determinar onde ela pode quebrar linhas.</span><span class="sxs-lookup"><span data-stu-id="bebdc-128">A rich edit control calls a function called a word-break procedure to find breaks between words and to determine where it can break lines.</span></span> <span data-ttu-id="bebdc-129">O controle usa essas informações ao executar operações de quebra automática de texto e ao processar CTRL + tecla de seta para a esquerda e CTRL + seta para a direita combinações de teclas.</span><span class="sxs-lookup"><span data-stu-id="bebdc-129">The control uses this information when performing word-wrap operations and when processing CTRL+LEFT ARROW key and CTRL+RIGHT ARROW key combinations.</span></span> <span data-ttu-id="bebdc-130">Um aplicativo pode enviar mensagens para um controle de edição rico para substituir o procedimento de quebra de palavra padrão, para recuperar informações de quebra de palavra e para determinar em qual linha um determinado caractere se encontra.</span><span class="sxs-lookup"><span data-stu-id="bebdc-130">An application can send messages to a rich edit control to replace the default word-break procedure, to retrieve word-break information, and to determine what line a given character falls on.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bebdc-131"><a href="use-rich-edit-clipboard-operations.md">Como usar operações de edição de área de transferência avançadas</a></span><span class="sxs-lookup"><span data-stu-id="bebdc-131"><a href="use-rich-edit-clipboard-operations.md">How to Use Rich Edit Clipboard Operations</a></span></span><br/></td>
<td><span data-ttu-id="bebdc-132">Um aplicativo pode colar o conteúdo da área de transferência em um controle de edição rico usando o melhor formato de área de transferência disponível ou um formato de área de transferência específico.</span><span class="sxs-lookup"><span data-stu-id="bebdc-132">An application can paste the contents of the clipboard into a rich edit control by using either the best available clipboard format or a specific clipboard format.</span></span> <span data-ttu-id="bebdc-133">Você também pode determinar se um controle de edição rico é capaz de colar um formato de área de transferência.</span><span class="sxs-lookup"><span data-stu-id="bebdc-133">You can also determine whether a rich edit control is capable of pasting a clipboard format.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bebdc-134"><a href="use-streams.md">Como usar fluxos</a></span><span class="sxs-lookup"><span data-stu-id="bebdc-134"><a href="use-streams.md">How to Use Streams</a></span></span><br/></td>
<td><span data-ttu-id="bebdc-135">Você pode usar fluxos para transferir dados para dentro ou para fora de um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="bebdc-135">You can use streams to transfer data into or out of a rich edit control.</span></span> <span data-ttu-id="bebdc-136">Um fluxo é definido por uma estrutura <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>EDITSTREAM</strong></a> , que especifica um buffer e uma função de retorno de chamada definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bebdc-136">A stream is defined by an <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>EDITSTREAM</strong></a> structure, which specifies a buffer and an application-defined callback function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bebdc-137"><a href="automatically-resize-rich-edit-controls.md">Como redimensionar automaticamente os controles de edição avançados</a></span><span class="sxs-lookup"><span data-stu-id="bebdc-137"><a href="automatically-resize-rich-edit-controls.md">How to Automatically Resize Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="bebdc-138">Um aplicativo pode redimensionar um controle de edição rico conforme necessário para que seja sempre o mesmo tamanho que seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="bebdc-138">An application can resize a rich edit control as needed so that it is always the same size as its contents.</span></span> <span data-ttu-id="bebdc-139">Um controle de edição rico dá suporte a essa chamada de funcionalidade <em>inferior</em> , enviando a janela pai um código de notificação <a href="en-requestresize.md">EN_REQUESTRESIZE</a> sempre que o tamanho do conteúdo do controle for alterado.</span><span class="sxs-lookup"><span data-stu-id="bebdc-139">A rich edit control supports this so-called <em>bottomless</em> functionality by sending its parent window an <a href="en-requestresize.md">EN_REQUESTRESIZE</a> notification code whenever the size of the control's content changes.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bebdc-140"><a href="use-rich-edit-control-notification-codes.md">Como usar códigos de notificação de controle de edição avançados</a></span><span class="sxs-lookup"><span data-stu-id="bebdc-140"><a href="use-rich-edit-control-notification-codes.md">How to Use Rich Edit Control Notification Codes</a></span></span><br/></td>
<td><span data-ttu-id="bebdc-141">Uma janela pai do controle de edição rico pode processar códigos de notificação para monitorar eventos que afetam o controle.</span><span class="sxs-lookup"><span data-stu-id="bebdc-141">A rich edit control's parent window can process notification codes to monitor events that affect the control.</span></span> <span data-ttu-id="bebdc-142">Os controles de edição avançados dão suporte a todos os códigos de notificação usados com controles de edição, bem como a vários outros.</span><span class="sxs-lookup"><span data-stu-id="bebdc-142">Rich edit controls support all of the notification codes that are used with edit controls, as well as several additional ones.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bebdc-143"><a href="use-font-binding-in-rich-edit-controls.md">Como usar a associação de fontes em controles de edição avançados</a></span><span class="sxs-lookup"><span data-stu-id="bebdc-143"><a href="use-font-binding-in-rich-edit-controls.md">How to Use Font Binding in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="bebdc-144">O Microsoft Rich Edit 3,0 atribui um conjunto de caracteres a caracteres de texto sem formatação, dependendo de seu contexto.</span><span class="sxs-lookup"><span data-stu-id="bebdc-144">Microsoft Rich Edit 3.0 assigns a character set to plain-text characters depending on their context.</span></span> <span data-ttu-id="bebdc-145">Alguns exemplos incluem:</span><span class="sxs-lookup"><span data-stu-id="bebdc-145">Some examples are:</span></span> <br/>
<ul>
<li><span data-ttu-id="bebdc-146">Os caracteres gregos são atribuídos <strong>GREEK_CHARSET</strong>.</span><span class="sxs-lookup"><span data-stu-id="bebdc-146">Greek characters are assigned <strong>GREEK_CHARSET</strong>.</span></span></li>
<li><span data-ttu-id="bebdc-147">Os símbolos Hangul são atribuídos <strong>HANGUL_CHARSET</strong>.</span><span class="sxs-lookup"><span data-stu-id="bebdc-147">Hangul symbols are assigned <strong>HANGUL_CHARSET</strong>.</span></span></li>
<li><span data-ttu-id="bebdc-148">Os caracteres chineses são atribuídos <strong>SHIFTJIS_CHARSET</strong> se caracteres kana forem encontrados próximo ou <strong>GB2312_CHARSET</strong> se nenhum kana for encontrado próximo.</span><span class="sxs-lookup"><span data-stu-id="bebdc-148">Chinese characters are assigned <strong>SHIFTJIS_CHARSET</strong> if kana characters are found nearby, or <strong>GB2312_CHARSET</strong> if no kana are found nearby.</span></span></li>
<li><span data-ttu-id="bebdc-149">Caracteres ANSI não neutros são atribuídos <strong>ANSI_CHARSET</strong> em qualquer evento.</span><span class="sxs-lookup"><span data-stu-id="bebdc-149">Non-neutral ANSI characters are assigned <strong>ANSI_CHARSET</strong> in any event.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bebdc-150"><a href="using-rich-edit-com.md">Como usar OLE em controles de edição Rich</a></span><span class="sxs-lookup"><span data-stu-id="bebdc-150"><a href="using-rich-edit-com.md">How to Use OLE in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="bebdc-151">Esta seção contém informações sobre como usar vinculação e incorporação de objetos (OLE) em controles de edição avançados.</span><span class="sxs-lookup"><span data-stu-id="bebdc-151">This section contains information about using object linking and embedding (OLE) in rich edit controls.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bebdc-152"><a href="printing-rich-edit-controls.md">Como imprimir o conteúdo de controles de edição avançados</a></span><span class="sxs-lookup"><span data-stu-id="bebdc-152"><a href="printing-rich-edit-controls.md">How to Print the Contents of Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="bebdc-153">Esta seção contém informações sobre como imprimir o conteúdo de controles de edição avançados.</span><span class="sxs-lookup"><span data-stu-id="bebdc-153">This section contains information about how to print the contents of rich edit controls.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

 

