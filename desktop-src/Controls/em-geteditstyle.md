---
title: Mensagem de EM_GETEDITSTYLE (RichEdit. h)
description: Recupera os sinalizadores de estilo de edição atuais.
ms.assetid: 568e51a4-0767-4a59-bf34-bc0281b5fe65
keywords:
- Controles de EM_GETEDITSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9264338ea525cc0165e1ed942d90654b95357b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009483"
---
# <a name="em_geteditstyle-message"></a><span data-ttu-id="f317a-104">\_Mensagem em GETeditstyle</span><span class="sxs-lookup"><span data-stu-id="f317a-104">EM\_GETEDITSTYLE message</span></span>

<span data-ttu-id="f317a-105">Recupera os sinalizadores de estilo de edição atuais.</span><span class="sxs-lookup"><span data-stu-id="f317a-105">Retrieves the current edit style flags.</span></span>

## <a name="parameters"></a><span data-ttu-id="f317a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f317a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f317a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f317a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f317a-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f317a-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f317a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f317a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f317a-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f317a-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f317a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f317a-111">Return value</span></span>

<span data-ttu-id="f317a-112">Retorna os sinalizadores de estilo de edição atuais, que podem incluir um ou mais dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="f317a-112">Returns the current edit style flags, which can include one or more of the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f317a-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f317a-113">Return code</span></span></th>
<th><span data-ttu-id="f317a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="f317a-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="f317a-115"><dt><strong>SES_BEEPONMAXTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-115"><dt><strong>SES_BEEPONMAXTEXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-116">A edição avançada chamará o bipe do sistema se o usuário tentar inserir mais do que o máximo de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f317a-116">Rich Edit will call the system beeper if the user attempts to enter more than the maximum characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f317a-117"><dt><strong>SES_BIDI</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-117"><dt><strong>SES_BIDI</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-118">Ativa o processamento bidirecional.</span><span class="sxs-lookup"><span data-stu-id="f317a-118">Turns on bidirectional processing.</span></span> <span data-ttu-id="f317a-119">Isso será automaticamente ativado por edição avançada se algum dos seguintes estilos de janela estiver ativo: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a> <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="f317a-119">This is automatically turned on by Rich Edit if any of the following window styles are active: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>.</span></span> <span data-ttu-id="f317a-120">No entanto, essa configuração é útil para lidar com esses estilos de janela ao usar uma implementação personalizada de <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-120">However, this setting is useful for handling these window styles when using a custom implementation of <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f317a-121"><dt><strong>SES_CTFALLOWEMBED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-121"><dt><strong>SES_CTFALLOWEMBED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-122"><strong>Windows XP com SP1</strong>: permitir que objetos inseridos sejam inseridos usando TSF (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-122"><strong>Windows XP with SP1</strong>: Allow embedded objects to be inserted using TSF (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f317a-123"><dt><strong>SES_CTFALLOWPROOFING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-123"><dt><strong>SES_CTFALLOWPROOFING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-124"><strong>Windows XP com SP1</strong>: permite dicas de revisão de TSF (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-124"><strong>Windows XP with SP1</strong>: Allows TSF proofing tips (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f317a-125"><dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-125"><dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-126"><strong>Windows XP com SP1</strong>: permite dicas do TSF SmartTag (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-126"><strong>Windows XP with SP1</strong>: Allows TSF SmartTag tips (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f317a-127"><dt><strong>SES_CTFNOLOCK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-127"><dt><strong>SES_CTFNOLOCK</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-128"><strong>Windows 8</strong>: não permita o acesso de leitura/gravação ao bloqueio de TSF.</span><span class="sxs-lookup"><span data-stu-id="f317a-128"><strong>Windows 8</strong>: Do not allow the TSF lock read/write access.</span></span> <span data-ttu-id="f317a-129">Isso pausa a entrada TSF.</span><span class="sxs-lookup"><span data-stu-id="f317a-129">This pauses TSF input.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f317a-130"><dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-130"><dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-131"><strong>Windows 8</strong>: as fontes com uma ligadura de fi são exibidas com recursos padrão de OpenType, resultando em uma tipografia aprimorada (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-131"><strong>Windows 8</strong>: Fonts with an fi ligature are displayed with default OpenType features resulting in improved typography (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f317a-132"><dt><strong>SES_DRAFTMODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-132"><dt><strong>SES_DRAFTMODE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-133"><strong>Windows XP com SP1</strong>: Use as fontes do modo de rascunho para exibir texto.</span><span class="sxs-lookup"><span data-stu-id="f317a-133"><strong>Windows XP with SP1</strong>: Use draft mode fonts to display text.</span></span> <span data-ttu-id="f317a-134">O modo de rascunho é uma opção de acessibilidade em que o controle exibe o texto com uma única fonte; a fonte é determinada pela configuração do sistema para a fonte usada nas caixas de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f317a-134">Draft mode is an accessibility option where the control displays the text with a single font; the font is determined by the system setting for the font used in message boxes.</span></span> <span data-ttu-id="f317a-135">Por exemplo, os usuários acessíveis podem ler o texto com mais facilidade se for uniforme, em vez de uma mistura de fontes e estilos (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-135">For example, accessible users may read text easier if it is uniform, rather than a mix of fonts and styles (default: 0).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f317a-136"><dt><strong>SES_EMULATE10</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-136"><dt><strong>SES_EMULATE10</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-137"><strong>Windows 8</strong>: emular o comportamento de RichEdit 1,0.</span><span class="sxs-lookup"><span data-stu-id="f317a-137"><strong>Windows 8</strong>: Emulate RichEdit 1.0 behavior.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="f317a-138">Se você realmente quiser esse comportamento, use o riched32.dll do Windows em vez de riched20.dll ou msftedit.dll.</span><span class="sxs-lookup"><span data-stu-id="f317a-138">If you really want this behavior, use the Windows riched32.dll instead of riched20.dll or msftedit.dll.</span></span> <span data-ttu-id="f317a-139">Riched32.dll tinha mais funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="f317a-139">Riched32.dll had more functionality.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f317a-140"><dt><strong>SES_EMULATESYSEDIT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-140"><dt><strong>SES_EMULATESYSEDIT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-141">Quando esse bit estiver ativado, o Rich Edit tentará emular o controle de edição do sistema (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-141">When this bit is on, rich edit attempts to emulate the system edit control (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f317a-142"><dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-142"><dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-143">Estende a cor do plano de fundo até as bordas do retângulo do cliente (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-143">Extends the background color all the way to the edges of the client rectangle (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f317a-144"><dt><strong>SES_HIDEGRIDLINES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-144"><dt><strong>SES_HIDEGRIDLINES</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-145"><strong>Windows XP com SP1</strong>: se a largura das linhas de grade da tabela for zero, as linhas de grade não serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="f317a-145"><strong>Windows XP with SP1</strong>: If the width of table gridlines is zero, gridlines are not displayed.</span></span> <span data-ttu-id="f317a-146">Isso é equivalente ao recurso Ocultar linhas de grade no menu de tabela do Word (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-146">This is equivalent to the hide gridlines feature in Word's table menu (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f317a-147"><dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-147"><dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-148"><strong>Windows 8</strong>: quando o cursor está sobre um link, exiba uma dica de ferramenta com o endereço do link de destino (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-148"><strong>Windows 8</strong>: When the cursor is over a link, display a tooltip with the target link address (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f317a-149"><dt><strong>SES_LOGICALCARET</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-149"><dt><strong>SES_LOGICALCARET</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-150"><strong>Windows 8</strong>: forneça informações lógicas de cursor em vez de um bitmap de cursor, conforme descrito em <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost:: TxSetCaretPos</strong></a> (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-150"><strong>Windows 8</strong>: Provide logical caret information instead of a caret bitmap as described in <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost::TxSetCaretPos</strong></a> (default: 0).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f317a-151"><dt><strong>SES_LOWERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-151"><dt><strong>SES_LOWERCASE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-152">Converte todos os caracteres de entrada em minúsculas (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-152">Converts all input characters to lowercase (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f317a-153"><dt><strong>SES_MAPCPS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-153"><dt><strong>SES_MAPCPS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-154">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="f317a-154">Obsolete.</span></span> <span data-ttu-id="f317a-155">Não use.</span><span class="sxs-lookup"><span data-stu-id="f317a-155">Do not use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f317a-156"><dt><strong>SES_MULTISELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-156"><dt><strong>SES_MULTISELECT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-157"><strong>Windows 8</strong>: habilite a seleção de seleção com as seleções individuais do mouse feitas enquanto a tecla CTRL é pressionada (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-157"><strong>Windows 8</strong>: Enable multiselection with individual mouse selections made while the Ctrl key is pressed (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f317a-158"><dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-158"><dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-159"><strong>Windows 8</strong>: não ajuste a altura da linha para texto do Leste Asiático (padrão: 0 que ajusta a altura da linha em 15%).</span><span class="sxs-lookup"><span data-stu-id="f317a-159"><strong>Windows 8</strong>: Do not adjust line height for East Asian text (default: 0 which adjusts the line height by 15%).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f317a-160"><dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-160"><dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-161">Envia <a href="en-link.md">EN_LINK</a> notificação de links que não têm foco.</span><span class="sxs-lookup"><span data-stu-id="f317a-161">Sends <a href="en-link.md">EN_LINK</a> notification from links that do not have focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f317a-162"><dt><strong>SES_NOIME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-162"><dt><strong>SES_NOIME</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-163">Não permite IMEs para esta instância do controle de edição rico (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-163">Disallows IMEs for this instance of the rich edit control (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f317a-164"><dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-164"><dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-165">Quando esse bit estiver ativado, a edição avançada não verificará a sequência de texto digitado.</span><span class="sxs-lookup"><span data-stu-id="f317a-165">When this bit is on, rich edit does not verify the sequence of typed text.</span></span> <span data-ttu-id="f317a-166">Alguns idiomas (como o tailandês e o vietnamita) exigem a verificação da ordem de sequência de entrada antes de enviá-la para o repositório de backup (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-166">Some languages (such as Thai and Vietnamese) require verifying the input sequence order before submitting it to the backing store (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f317a-167"><dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-167"><dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-168">Quando KillFocus ocorrer, role até o início do texto (posição do caractere igual a 0) (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-168">When KillFocus occurs, scroll to the beginning of the text (character position equal to 0) (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f317a-169"><dt><strong>SES_SMARTDRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-169"><dt><strong>SES_SMARTDRAGDROP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-170"><strong>Windows 8</strong>: Adicione ou exclua um espaço de acordo com o contexto ao descartar texto (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-170"><strong>Windows 8</strong>: Add or delete a space according to the context when dropping text (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f317a-171"><dt><strong>SES_USECRLF</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-171"><dt><strong>SES_USECRLF</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-172">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="f317a-172">Obsolete.</span></span> <span data-ttu-id="f317a-173">Não use.</span><span class="sxs-lookup"><span data-stu-id="f317a-173">Do not use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f317a-174"><dt><strong>SES_WORDDRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-174"><dt><strong>SES_WORDDRAGDROP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-175"><strong>Windows 8</strong>: se o Word Select estiver ativo, verifique se o local de destino está em um limite de palavra (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-175"><strong>Windows 8</strong>: If word select is active, ensure that the drop location is at a word boundary (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f317a-176"><dt><strong>SES_UPPERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-176"><dt><strong>SES_UPPERCASE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-177">Converte todos os caracteres de entrada em maiúsculas (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-177">Converts all input characters to uppercase (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f317a-178"><dt><strong>SES_USEAIMM</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-178"><dt><strong>SES_USEAIMM</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-179">Usa o componente de método de entrada do IMM ativo fornecido com o Internet Explorer 4,0 ou posterior (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="f317a-179">Uses the Active IMM input method component that ships with Internet Explorer 4.0 or later (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f317a-180"><dt><strong>SES_USEATFONT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-180"><dt><strong>SES_USEATFONT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-181"><strong>Windows XP com SP1</strong>: usa uma @ Font, que é projetada para texto vertical; Isso é usado com o estilo de janela <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f317a-181"><strong>Windows XP with SP1</strong>: Uses an @ font, which is designed for vertical text; this is used with the <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> window style.</span></span> <span data-ttu-id="f317a-182">O nome de uma @ Font começa com o símbolo @, por exemplo, &quot; @Batang &quot; (padrão: 0, mas é automaticamente ativado para layout de texto vertical).</span><span class="sxs-lookup"><span data-stu-id="f317a-182">The name of an @ font begins with the @ symbol, for example, &quot;@Batang&quot; (default: 0, but is automatically turned on for vertical text layout).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="f317a-183"><dt><strong>SES_USECTF</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-183"><dt><strong>SES_USECTF</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-184"><strong>Windows XP com SP1</strong>: ativa o suporte a TSF.</span><span class="sxs-lookup"><span data-stu-id="f317a-184"><strong>Windows XP with SP1</strong>: Turns on TSF support.</span></span> <span data-ttu-id="f317a-185">(padrão: 0)</span><span class="sxs-lookup"><span data-stu-id="f317a-185">(default: 0)</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="f317a-186"><dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f317a-186"><dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="f317a-187">Ativa a tradução de CRCRLFs para CRs.</span><span class="sxs-lookup"><span data-stu-id="f317a-187">Turns on translation of CRCRLFs to CRs.</span></span> <span data-ttu-id="f317a-188">Quando esse bit estiver ativado e um arquivo for lido no, todas as instâncias de CRCRLF serão convertidas em CRs fixas internamente.</span><span class="sxs-lookup"><span data-stu-id="f317a-188">When this bit is on and a file is read in, all instances of CRCRLF will be converted to hard CRs internally.</span></span> <span data-ttu-id="f317a-189">Isso afetará a disposição do texto.</span><span class="sxs-lookup"><span data-stu-id="f317a-189">This will affect the text wrapping.</span></span> <span data-ttu-id="f317a-190">Observe que, se esse arquivo for salvo como texto sem formatação, o CRs será substituído por CRLF.</span><span class="sxs-lookup"><span data-stu-id="f317a-190">Note that if such a file is saved as plain text, the CRs will be replaced by CRLFs.</span></span> <span data-ttu-id="f317a-191">Este é o padrão. txt para texto sem formatação (padrão: 0, que exclui CRCRLFs na entrada).</span><span class="sxs-lookup"><span data-stu-id="f317a-191">This is the .txt standard for plain text (default: 0, which deletes CRCRLFs on input).</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="f317a-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f317a-192">Requirements</span></span>



| <span data-ttu-id="f317a-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="f317a-193">Requirement</span></span> | <span data-ttu-id="f317a-194">Valor</span><span class="sxs-lookup"><span data-stu-id="f317a-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f317a-195">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f317a-195">Minimum supported client</span></span><br/> | <span data-ttu-id="f317a-196">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f317a-196">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f317a-197">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f317a-197">Minimum supported server</span></span><br/> | <span data-ttu-id="f317a-198">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f317a-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f317a-199">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f317a-199">Redistributable</span></span><br/>          | <span data-ttu-id="f317a-200">Edição avançada 3,0</span><span class="sxs-lookup"><span data-stu-id="f317a-200">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="f317a-201">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f317a-201">Header</span></span><br/>                   | <dl> <span data-ttu-id="f317a-202"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f317a-202"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f317a-203">Confira também</span><span class="sxs-lookup"><span data-stu-id="f317a-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f317a-204">**em \_ SETeditstyle**</span><span class="sxs-lookup"><span data-stu-id="f317a-204">**EM\_SETEDITSTYLE**</span></span>](em-seteditstyle.md)
</dt> </dl>

 

