---
title: Editar estilos de controle (WinUser. h)
description: Para criar um controle de edição usando a função CreateWindow ou CreateWindowEx, especifique a classe EDIT, as constantes de estilo de janela apropriadas e uma combinação dos seguintes estilos de controle de edição.
ms.assetid: 336c69b7-bc23-4b93-8968-ad63a1703385
topic_type:
- apiref
api_name:
- ES_AUTOHSCROLL
- ES_AUTOVSCROLL
- ES_CENTER
- ES_LEFT
- ES_LOWERCASE
- ES_MULTILINE
- ES_NOHIDESEL
- ES_NUMBER
- ES_OEMCONVERT
- ES_PASSWORD
- ES_READONLY
- ES_RIGHT
- ES_UPPERCASE
- ES_WANTRETURN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 9b255aee665c32f9a14be4946dee0122dad626bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751377"
---
# <a name="edit-control-styles"></a><span data-ttu-id="4e154-103">Editar estilos de controle</span><span class="sxs-lookup"><span data-stu-id="4e154-103">Edit Control Styles</span></span>

<span data-ttu-id="4e154-104">Para criar um controle de edição usando a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especifique a classe Edit, as constantes de estilo de janela apropriadas e uma combinação dos seguintes estilos de controle de edição.</span><span class="sxs-lookup"><span data-stu-id="4e154-104">To create an edit control using the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specify the EDIT class, appropriate window style constants, and a combination of the following edit control styles.</span></span> <span data-ttu-id="4e154-105">Depois que o controle tiver sido criado, esses estilos não poderão ser modificados, exceto quando observado.</span><span class="sxs-lookup"><span data-stu-id="4e154-105">After the control has been created, these styles cannot be modified, except as noted.</span></span>

## <a name="example"></a><span data-ttu-id="4e154-106">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4e154-106">Example</span></span>

```cpp
LRESULT MsgCreate(HWND hwnd, UINT uMessage, WPARAM wparam, LPARAM lparam)
{
    lparam;
    wparam;
    uMessage;

    // Create Edit control for typing to be sent to server
    if (NULL == (hOutWnd = CreateWindow("EDIT",
                           NULL,
                           WS_BORDER | WS_CHILD | WS_VISIBLE | WS_VSCROLL | ES_LEFT | 
                           ES_MULTILINE | ES_AUTOVSCROLL,
                           0,0,0,0,
                           hwnd,
                           (HMENU) ID_OUTBOX,
                           (HINSTANCE) GetWindowLongPtr(hwnd, GWLP_HINSTANCE),
                           NULL)))
        return FALSE;
    return TRUE;
}
```

<span data-ttu-id="4e154-107">Exemplo de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) no github.</span><span class="sxs-lookup"><span data-stu-id="4e154-107">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) on GitHub.</span></span>

## <a name="constants"></a><span data-ttu-id="4e154-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="4e154-108">Constants</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="4e154-109">Constante</span><span class="sxs-lookup"><span data-stu-id="4e154-109">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="4e154-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e154-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <span data-ttu-id="4e154-111"><dt><strong>ES_AUTOHSCROLL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4e154-111"><dt><strong>ES_AUTOHSCROLL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e154-112">Rola automaticamente o texto para a direita em 10 caracteres quando o usuário digita um caractere no final da linha.</span><span class="sxs-lookup"><span data-stu-id="4e154-112">Automatically scrolls text to the right by 10 characters when the user types a character at the end of the line.</span></span> <span data-ttu-id="4e154-113">Quando o usuário pressiona a tecla ENTER, o controle rola todo o texto de volta para a posição zero.</span><span class="sxs-lookup"><span data-stu-id="4e154-113">When the user presses the ENTER key, the control scrolls all text back to position zero.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <span data-ttu-id="4e154-114"><dt><strong>ES_AUTOVSCROLL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4e154-114"><dt><strong>ES_AUTOVSCROLL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e154-115">Rola automaticamente o texto uma página para cima quando o usuário pressiona a tecla ENTER na última linha.</span><span class="sxs-lookup"><span data-stu-id="4e154-115">Automatically scrolls text up one page when the user presses the ENTER key on the last line.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_CENTER"></span><span id="es_center"></span><dl> <span data-ttu-id="4e154-116"><dt><strong>ES_CENTER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4e154-116"><dt><strong>ES_CENTER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e154-117">Centraliza o texto em um controle de linha única ou de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="4e154-117">Centers text in a single-line or multiline edit control.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_LEFT"></span><span id="es_left"></span><dl> <span data-ttu-id="4e154-118"><dt><strong>ES_LEFT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4e154-118"><dt><strong>ES_LEFT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e154-119">Alinha o texto com a margem esquerda.</span><span class="sxs-lookup"><span data-stu-id="4e154-119">Aligns text with the left margin.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_LOWERCASE"></span><span id="es_lowercase"></span><dl> <span data-ttu-id="4e154-120"><dt><strong>ES_LOWERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4e154-120"><dt><strong>ES_LOWERCASE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e154-121">Converte todos os caracteres em minúsculas, pois eles são digitados no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="4e154-121">Converts all characters to lowercase as they are typed into the edit control.</span></span><br/> <span data-ttu-id="4e154-122">Para alterar esse estilo depois que o controle tiver sido criado, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4e154-122">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <span data-ttu-id="4e154-123"><dt><strong>ES_MULTILINE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4e154-123"><dt><strong>ES_MULTILINE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e154-124">Designa um controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="4e154-124">Designates a multiline edit control.</span></span> <span data-ttu-id="4e154-125">O padrão é o controle de edição de linha única.</span><span class="sxs-lookup"><span data-stu-id="4e154-125">The default is single-line edit control.</span></span> <br/> <span data-ttu-id="4e154-126">Quando o controle de edição de várias linhas está em uma caixa de diálogo, a resposta padrão para pressionar a tecla ENTER é ativar o botão padrão.</span><span class="sxs-lookup"><span data-stu-id="4e154-126">When the multiline edit control is in a dialog box, the default response to pressing the ENTER key is to activate the default button.</span></span> <span data-ttu-id="4e154-127">Para usar a tecla ENTER como um retorno de carro, use o estilo de <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="4e154-127">To use the ENTER key as a carriage return, use the <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> style.</span></span><br/> <span data-ttu-id="4e154-128">Quando o controle de edição de várias linhas não está em uma caixa de diálogo e o estilo de <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> é especificado, o controle de edição mostra o máximo de linhas possível e rola verticalmente quando o usuário pressiona a tecla Enter.</span><span class="sxs-lookup"><span data-stu-id="4e154-128">When the multiline edit control is not in a dialog box and the <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> style is specified, the edit control shows as many lines as possible and scrolls vertically when the user presses the ENTER key.</span></span> <span data-ttu-id="4e154-129">Se você não especificar <strong>ES_AUTOVSCROLL</strong>, o controle de edição mostrará o máximo de linhas possível e emitirá um aviso sonoro se o usuário pressionar a tecla Enter quando não for possível exibir mais linhas.</span><span class="sxs-lookup"><span data-stu-id="4e154-129">If you do not specify <strong>ES_AUTOVSCROLL</strong>, the edit control shows as many lines as possible and beeps if the user presses the ENTER key when no more lines can be displayed.</span></span><br/> <span data-ttu-id="4e154-130">Se você especificar o estilo de <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> , o controle de edição de várias linhas rolará automaticamente horizontalmente quando o cursor passar da borda direita do controle.</span><span class="sxs-lookup"><span data-stu-id="4e154-130">If you specify the <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> style, the multiline edit control automatically scrolls horizontally when the caret goes past the right edge of the control.</span></span> <span data-ttu-id="4e154-131">Para iniciar uma nova linha, o usuário deve pressionar a tecla ENTER.</span><span class="sxs-lookup"><span data-stu-id="4e154-131">To start a new line, the user must press the ENTER key.</span></span> <span data-ttu-id="4e154-132">Se você não especificar <strong>ES_AUTOHSCROLL</strong>, o controle encapsula automaticamente as palavras no início da próxima linha quando necessário.</span><span class="sxs-lookup"><span data-stu-id="4e154-132">If you do not specify <strong>ES_AUTOHSCROLL</strong>, the control automatically wraps words to the beginning of the next line when necessary.</span></span> <span data-ttu-id="4e154-133">Uma nova linha também será iniciada se o usuário pressionar a tecla ENTER.</span><span class="sxs-lookup"><span data-stu-id="4e154-133">A new line is also started if the user presses the ENTER key.</span></span> <span data-ttu-id="4e154-134">O tamanho da janela determina a posição de WordWrap.</span><span class="sxs-lookup"><span data-stu-id="4e154-134">The window size determines the position of the Wordwrap.</span></span> <span data-ttu-id="4e154-135">Se o tamanho da janela for alterado, a posição Wordwrapping muda e o texto é exibido novamente.</span><span class="sxs-lookup"><span data-stu-id="4e154-135">If the window size changes, the Wordwrapping position changes and the text is redisplayed.</span></span><br/> <span data-ttu-id="4e154-136">Os controles de edição de várias linhas podem ter barras de rolagem.</span><span class="sxs-lookup"><span data-stu-id="4e154-136">Multiline edit controls can have scroll bars.</span></span> <span data-ttu-id="4e154-137">Um controle de edição com barras de rolagem processa suas próprias mensagens da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="4e154-137">An edit control with scroll bars processes its own scroll bar messages.</span></span> <span data-ttu-id="4e154-138">Observe que os controles de edição sem barras de rolagem são rolados conforme descrito nos parágrafos anteriores e processam todas as mensagens de rolagem enviadas pela janela pai.</span><span class="sxs-lookup"><span data-stu-id="4e154-138">Note that edit controls without scroll bars scroll as described in the previous paragraphs and process any scroll messages sent by the parent window.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <span data-ttu-id="4e154-139"><dt><strong>ES_NOHIDESEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4e154-139"><dt><strong>ES_NOHIDESEL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e154-140">Nega o comportamento padrão para um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="4e154-140">Negates the default behavior for an edit control.</span></span> <span data-ttu-id="4e154-141">O comportamento padrão oculta a seleção quando o controle perde o foco de entrada e inverte a seleção quando o controle recebe o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="4e154-141">The default behavior hides the selection when the control loses the input focus and inverts the selection when the control receives the input focus.</span></span> <span data-ttu-id="4e154-142">Se você especificar <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, o texto selecionado será invertido, mesmo que o controle não tenha o foco.</span><span class="sxs-lookup"><span data-stu-id="4e154-142">If you specify <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, the selected text is inverted, even if the control does not have the focus.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_NUMBER"></span><span id="es_number"></span><dl> <span data-ttu-id="4e154-143"><dt><strong>ES_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4e154-143"><dt><strong>ES_NUMBER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e154-144">Permite que apenas os dígitos sejam inseridos no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="4e154-144">Allows only digits to be entered into the edit control.</span></span> <span data-ttu-id="4e154-145">Observe que, mesmo com esse conjunto, ainda é possível colar não dígitos no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="4e154-145">Note that, even with this set, it is still possible to paste non-digits into the edit control.</span></span> <br/> <span data-ttu-id="4e154-146">Para alterar esse estilo depois que o controle tiver sido criado, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4e154-146">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/> <span data-ttu-id="4e154-147">Para traduzir o texto que foi inserido no controle de edição para um valor inteiro, use a função <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>GetDlgItemInt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="4e154-147">To translate text that was entered into the edit control to an integer value, use the <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>GetDlgItemInt</strong></a> function.</span></span> <span data-ttu-id="4e154-148">Para definir o texto do controle de edição para a representação de cadeia de caracteres de um inteiro especificado, use a função <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>SetDlgItemInt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="4e154-148">To set the text of the edit control to the string representation of a specified integer, use the <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>SetDlgItemInt</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_OEMCONVERT"></span><span id="es_oemconvert"></span><dl> <span data-ttu-id="4e154-149"><dt><strong>ES_OEMCONVERT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4e154-149"><dt><strong>ES_OEMCONVERT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e154-150">Converte o texto inserido no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="4e154-150">Converts text entered in the edit control.</span></span> <span data-ttu-id="4e154-151">O texto é convertido do conjunto de caracteres do Windows para o conjunto de caracteres OEM e, em seguida, de volta para o conjunto de caracteres do Windows.</span><span class="sxs-lookup"><span data-stu-id="4e154-151">The text is converted from the Windows character set to the OEM character set and then back to the Windows character set.</span></span> <span data-ttu-id="4e154-152">Isso garante a conversão adequada de caracteres quando o aplicativo chama a função <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> para converter uma cadeia de caracteres do Windows no controle de edição para caracteres OEM.</span><span class="sxs-lookup"><span data-stu-id="4e154-152">This ensures proper character conversion when the application calls the <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> function to convert a Windows string in the edit control to OEM characters.</span></span> <span data-ttu-id="4e154-153">Esse estilo é mais útil para controles de edição que contêm nomes de arquivos que serão usados em sistemas de arquivos que não dão suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="4e154-153">This style is most useful for edit controls that contain file names that will be used on file systems that do not support Unicode.</span></span> <br/> <span data-ttu-id="4e154-154">Para alterar esse estilo depois que o controle tiver sido criado, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4e154-154">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <span data-ttu-id="4e154-155"><dt><strong>ES_PASSWORD</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4e154-155"><dt><strong>ES_PASSWORD</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e154-156">Exibe um asterisco (\*) para cada caractere digitado no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="4e154-156">Displays an asterisk (\*) for each character typed into the edit control.</span></span> <span data-ttu-id="4e154-157">Esse estilo é válido somente para controles de edição de linha única.</span><span class="sxs-lookup"><span data-stu-id="4e154-157">This style is valid only for single-line edit controls.</span></span> <br/> <span data-ttu-id="4e154-158">Para alterar os caracteres exibidos, ou definir ou limpar esse estilo, use a mensagem <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="4e154-158">To change the characters that is displayed, or set or clear this style, use the <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> message.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4e154-159">Para usar Comctl32.dll versão 6, especifique-o em um manifesto.</span><span class="sxs-lookup"><span data-stu-id="4e154-159">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="4e154-160">Para obter mais informações sobre manifestos, consulte <a href="cookbook-overview.md">habilitando estilos visuais</a>.</span><span class="sxs-lookup"><span data-stu-id="4e154-160">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <span data-ttu-id="4e154-161"><dt><strong>ES_READONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4e154-161"><dt><strong>ES_READONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e154-162">Impede que o usuário digite ou edite texto no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="4e154-162">Prevents the user from typing or editing text in the edit control.</span></span><br/> <span data-ttu-id="4e154-163">Para alterar esse estilo depois que o controle tiver sido criado, use a mensagem <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="4e154-163">To change this style after the control has been created, use the <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> message.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_RIGHT"></span><span id="es_right"></span><dl> <span data-ttu-id="4e154-164"><dt><strong>ES_RIGHT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4e154-164"><dt><strong>ES_RIGHT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e154-165">Alinha o texto à direita em um controle de linha única ou de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="4e154-165">Right-aligns text in a single-line or multiline edit control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_UPPERCASE"></span><span id="es_uppercase"></span><dl> <span data-ttu-id="4e154-166"><dt><strong>ES_UPPERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4e154-166"><dt><strong>ES_UPPERCASE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e154-167">Converte todos os caracteres em maiúsculas à medida que eles são digitados no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="4e154-167">Converts all characters to uppercase as they are typed into the edit control.</span></span> <br/> <span data-ttu-id="4e154-168">Para alterar esse estilo depois que o controle tiver sido criado, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4e154-168">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <span data-ttu-id="4e154-169"><dt><strong>ES_WANTRETURN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4e154-169"><dt><strong>ES_WANTRETURN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4e154-170">Especifica que um retorno de carro será inserido quando o usuário pressionar a tecla ENTER ao inserir texto em um controle de edição de várias linhas em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4e154-170">Specifies that a carriage return be inserted when the user presses the ENTER key while entering text into a multiline edit control in a dialog box.</span></span> <span data-ttu-id="4e154-171">Se você não especificar esse estilo, pressionar a tecla ENTER terá o mesmo efeito que pressionar o botão de ação padrão da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4e154-171">If you do not specify this style, pressing the ENTER key has the same effect as pressing the dialog box's default push button.</span></span> <span data-ttu-id="4e154-172">Esse estilo não tem efeito sobre um controle de edição de linha única.</span><span class="sxs-lookup"><span data-stu-id="4e154-172">This style has no effect on a single-line edit control.</span></span> <br/> <span data-ttu-id="4e154-173">Para alterar esse estilo depois que o controle tiver sido criado, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4e154-173">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="4e154-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e154-174">Requirements</span></span>



| <span data-ttu-id="4e154-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e154-175">Requirement</span></span> | <span data-ttu-id="4e154-176">Valor</span><span class="sxs-lookup"><span data-stu-id="4e154-176">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4e154-177">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e154-177">Header</span></span><br/> | <dl> <span data-ttu-id="4e154-178"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e154-178"><dt>Winuser.h</dt></span></span> </dl> |



