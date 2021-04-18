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
# <a name="edit-control-styles"></a>Editar estilos de controle

Para criar um controle de edição usando a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especifique a classe Edit, as constantes de estilo de janela apropriadas e uma combinação dos seguintes estilos de controle de edição. Depois que o controle tiver sido criado, esses estilos não poderão ser modificados, exceto quando observado.

## <a name="example"></a>Exemplo

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

Exemplo de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) no github.

## <a name="constants"></a>Constantes

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
<td style="text-align: left;"><span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <dt><strong>ES_AUTOHSCROLL</strong></dt> </dl></td>
<td style="text-align: left;">Rola automaticamente o texto para a direita em 10 caracteres quando o usuário digita um caractere no final da linha. Quando o usuário pressiona a tecla ENTER, o controle rola todo o texto de volta para a posição zero.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <dt><strong>ES_AUTOVSCROLL</strong></dt> </dl></td>
<td style="text-align: left;">Rola automaticamente o texto uma página para cima quando o usuário pressiona a tecla ENTER na última linha.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_CENTER"></span><span id="es_center"></span><dl> <dt><strong>ES_CENTER</strong></dt> </dl></td>
<td style="text-align: left;">Centraliza o texto em um controle de linha única ou de edição de várias linhas.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_LEFT"></span><span id="es_left"></span><dl> <dt><strong>ES_LEFT</strong></dt> </dl></td>
<td style="text-align: left;">Alinha o texto com a margem esquerda.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_LOWERCASE"></span><span id="es_lowercase"></span><dl> <dt><strong>ES_LOWERCASE</strong></dt> </dl></td>
<td style="text-align: left;">Converte todos os caracteres em minúsculas, pois eles são digitados no controle de edição.<br/> Para alterar esse estilo depois que o controle tiver sido criado, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <dt><strong>ES_MULTILINE</strong></dt> </dl></td>
<td style="text-align: left;">Designa um controle de edição de várias linhas. O padrão é o controle de edição de linha única. <br/> Quando o controle de edição de várias linhas está em uma caixa de diálogo, a resposta padrão para pressionar a tecla ENTER é ativar o botão padrão. Para usar a tecla ENTER como um retorno de carro, use o estilo de <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> .<br/> Quando o controle de edição de várias linhas não está em uma caixa de diálogo e o estilo de <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> é especificado, o controle de edição mostra o máximo de linhas possível e rola verticalmente quando o usuário pressiona a tecla Enter. Se você não especificar <strong>ES_AUTOVSCROLL</strong>, o controle de edição mostrará o máximo de linhas possível e emitirá um aviso sonoro se o usuário pressionar a tecla Enter quando não for possível exibir mais linhas.<br/> Se você especificar o estilo de <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> , o controle de edição de várias linhas rolará automaticamente horizontalmente quando o cursor passar da borda direita do controle. Para iniciar uma nova linha, o usuário deve pressionar a tecla ENTER. Se você não especificar <strong>ES_AUTOHSCROLL</strong>, o controle encapsula automaticamente as palavras no início da próxima linha quando necessário. Uma nova linha também será iniciada se o usuário pressionar a tecla ENTER. O tamanho da janela determina a posição de WordWrap. Se o tamanho da janela for alterado, a posição Wordwrapping muda e o texto é exibido novamente.<br/> Os controles de edição de várias linhas podem ter barras de rolagem. Um controle de edição com barras de rolagem processa suas próprias mensagens da barra de rolagem. Observe que os controles de edição sem barras de rolagem são rolados conforme descrito nos parágrafos anteriores e processam todas as mensagens de rolagem enviadas pela janela pai.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <dt><strong>ES_NOHIDESEL</strong></dt> </dl></td>
<td style="text-align: left;">Nega o comportamento padrão para um controle de edição. O comportamento padrão oculta a seleção quando o controle perde o foco de entrada e inverte a seleção quando o controle recebe o foco de entrada. Se você especificar <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, o texto selecionado será invertido, mesmo que o controle não tenha o foco.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_NUMBER"></span><span id="es_number"></span><dl> <dt><strong>ES_NUMBER</strong></dt> </dl></td>
<td style="text-align: left;">Permite que apenas os dígitos sejam inseridos no controle de edição. Observe que, mesmo com esse conjunto, ainda é possível colar não dígitos no controle de edição. <br/> Para alterar esse estilo depois que o controle tiver sido criado, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/> Para traduzir o texto que foi inserido no controle de edição para um valor inteiro, use a função <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>GetDlgItemInt</strong></a> . Para definir o texto do controle de edição para a representação de cadeia de caracteres de um inteiro especificado, use a função <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>SetDlgItemInt</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_OEMCONVERT"></span><span id="es_oemconvert"></span><dl> <dt><strong>ES_OEMCONVERT</strong></dt> </dl></td>
<td style="text-align: left;">Converte o texto inserido no controle de edição. O texto é convertido do conjunto de caracteres do Windows para o conjunto de caracteres OEM e, em seguida, de volta para o conjunto de caracteres do Windows. Isso garante a conversão adequada de caracteres quando o aplicativo chama a função <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> para converter uma cadeia de caracteres do Windows no controle de edição para caracteres OEM. Esse estilo é mais útil para controles de edição que contêm nomes de arquivos que serão usados em sistemas de arquivos que não dão suporte a Unicode. <br/> Para alterar esse estilo depois que o controle tiver sido criado, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <dt><strong>ES_PASSWORD</strong></dt> </dl></td>
<td style="text-align: left;">Exibe um asterisco (*) para cada caractere digitado no controle de edição. Esse estilo é válido somente para controles de edição de linha única. <br/> Para alterar os caracteres exibidos, ou definir ou limpar esse estilo, use a mensagem <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> . <br/>
<blockquote>
[!Note]<br />
Para usar Comctl32.dll versão 6, especifique-o em um manifesto. Para obter mais informações sobre manifestos, consulte <a href="cookbook-overview.md">habilitando estilos visuais</a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <dt><strong>ES_READONLY</strong></dt> </dl></td>
<td style="text-align: left;">Impede que o usuário digite ou edite texto no controle de edição.<br/> Para alterar esse estilo depois que o controle tiver sido criado, use a mensagem <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> . <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_RIGHT"></span><span id="es_right"></span><dl> <dt><strong>ES_RIGHT</strong></dt> </dl></td>
<td style="text-align: left;">Alinha o texto à direita em um controle de linha única ou de edição de várias linhas.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_UPPERCASE"></span><span id="es_uppercase"></span><dl> <dt><strong>ES_UPPERCASE</strong></dt> </dl></td>
<td style="text-align: left;">Converte todos os caracteres em maiúsculas à medida que eles são digitados no controle de edição. <br/> Para alterar esse estilo depois que o controle tiver sido criado, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <dt><strong>ES_WANTRETURN</strong></dt> </dl></td>
<td style="text-align: left;">Especifica que um retorno de carro será inserido quando o usuário pressionar a tecla ENTER ao inserir texto em um controle de edição de várias linhas em uma caixa de diálogo. Se você não especificar esse estilo, pressionar a tecla ENTER terá o mesmo efeito que pressionar o botão de ação padrão da caixa de diálogo. Esse estilo não tem efeito sobre um controle de edição de linha única. <br/> Para alterar esse estilo depois que o controle tiver sido criado, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WinUser. h</dt> </dl> |



