---
title: Mensagem de EM_GETEDITSTYLE (RichEdit. h)
description: Recupera os sinalizadores de estilo de edição atuais.
ms.assetid: 568e51a4-0767-4a59-bf34-bc0281b5fe65
keywords:
- controles de Windows de mensagem de EM_GETEDITSTYLE
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
ms.openlocfilehash: cb34e4912ff00d76abf8db4c631296836ad9adaf83853aa064c34b11e7f71e20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019704"
---
# <a name="em_geteditstyle-message"></a>\_Mensagem em GETeditstyle

Recupera os sinalizadores de estilo de edição atuais.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna os sinalizadores de estilo de edição atuais, que podem incluir um ou mais dos seguintes valores:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Código de retorno</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>SES_BEEPONMAXTEXT</strong></dt> </dl></td>
<td>A edição avançada chamará o bipe do sistema se o usuário tentar inserir mais do que o máximo de caracteres.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_BIDI</strong></dt> </dl></td>
<td>Ativa o processamento bidirecional. Isso será automaticamente ativado por edição avançada se algum dos seguintes estilos de janela estiver ativo: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a> <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>. No entanto, essa configuração é útil para lidar com esses estilos de janela ao usar uma implementação personalizada de <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> (padrão: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_CTFALLOWEMBED</strong></dt> </dl></td>
<td><strong>Windows XP com SP1</strong>: permitir que objetos inseridos sejam inseridos usando TSF (padrão: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_CTFALLOWPROOFING</strong></dt> </dl></td>
<td><strong>Windows XP com SP1</strong>: permite dicas de revisão de TSF (padrão: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </dl></td>
<td><strong>Windows XP com SP1</strong>: permite dicas do TSF SmartTag (padrão: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_CTFNOLOCK</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: não permita o acesso de leitura/gravação do bloqueio de TSF. Isso pausa a entrada TSF. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: as fontes com uma ligadura de fi são exibidas com recursos padrão de OpenType, resultando em uma tipografia aprimorada (padrão: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_DRAFTMODE</strong></dt> </dl></td>
<td><strong>Windows XP com SP1</strong>: Use as fontes do modo de rascunho para exibir texto. O modo de rascunho é uma opção de acessibilidade em que o controle exibe o texto com uma única fonte; a fonte é determinada pela configuração do sistema para a fonte usada nas caixas de mensagem. Por exemplo, os usuários acessíveis podem ler o texto com mais facilidade se for uniforme, em vez de uma mistura de fontes e estilos (padrão: 0). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_EMULATE10</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: emular o comportamento de RichEdit 1,0. <br/>
<blockquote>
[!Note]<br />
se você realmente quiser esse comportamento, use o Windows riched32.dll em vez de riched20.dll ou msftedit.dll. Riched32.dll tinha mais funcionalidade.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_EMULATESYSEDIT</strong></dt> </dl></td>
<td>Quando esse bit estiver ativado, o Rich Edit tentará emular o controle de edição do sistema (padrão: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </dl></td>
<td>Estende a cor do plano de fundo até as bordas do retângulo do cliente (padrão: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_HIDEGRIDLINES</strong></dt> </dl></td>
<td><strong>Windows XP com SP1</strong>: se a largura das linhas de grade da tabela for zero, as linhas de grade não serão exibidas. Isso é equivalente ao recurso Ocultar linhas de grade no menu de tabela do Word (padrão: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: quando o cursor estiver sobre um link, exiba uma dica de ferramenta com o endereço do link de destino (padrão: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_LOGICALCARET</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: forneça informações lógicas de cursor em vez de um bitmap de cursor, conforme descrito em <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost:: TxSetCaretPos</strong></a> (padrão: 0). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_LOWERCASE</strong></dt> </dl></td>
<td>Converte todos os caracteres de entrada em minúsculas (padrão: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_MAPCPS</strong></dt> </dl></td>
<td>Obsoleto. Não use.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_MULTISELECT</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: habilitar multiseleção com seleções individuais do mouse feitas enquanto a tecla Ctrl é pressionada (padrão: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: não ajuste a altura da linha para texto do leste asiático (padrão: 0 que ajusta a altura da linha em 15%). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </dl></td>
<td>Envia <a href="en-link.md">EN_LINK</a> notificação de links que não têm foco.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_NOIME</strong></dt> </dl></td>
<td>Não permite IMEs para esta instância do controle de edição rico (padrão: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </dl></td>
<td>Quando esse bit estiver ativado, a edição avançada não verificará a sequência de texto digitado. Alguns idiomas (como o tailandês e o vietnamita) exigem a verificação da ordem de sequência de entrada antes de enviá-la para o repositório de backup (padrão: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </dl></td>
<td>Quando KillFocus ocorrer, role até o início do texto (posição do caractere igual a 0) (padrão: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_SMARTDRAGDROP</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: adicionar ou excluir um espaço de acordo com o contexto ao descartar texto (padrão: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_USECRLF</strong></dt> </dl></td>
<td>Obsoleto. Não use.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_WORDDRAGDROP</strong></dt> </dl></td>
<td><strong>Windows 8</strong>: se o word select estiver ativo, verifique se o local de destino está em um limite de palavra (padrão: 0). <br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_UPPERCASE</strong></dt> </dl></td>
<td>Converte todos os caracteres de entrada em maiúsculas (padrão: 0).<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_USEAIMM</strong></dt> </dl></td>
<td>Usa o componente de método de entrada do IMM ativo fornecido com o Internet Explorer 4,0 ou posterior (padrão: 0).<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_USEATFONT</strong></dt> </dl></td>
<td><strong>Windows XP com SP1</strong>: usa uma @ font, que é projetada para texto vertical; Isso é usado com o estilo de janela <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> . O nome de uma @ Font começa com o símbolo @, por exemplo, &quot; @Batang &quot; (padrão: 0, mas é automaticamente ativado para layout de texto vertical). <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>SES_USECTF</strong></dt> </dl></td>
<td><strong>Windows XP com SP1</strong>: ativa o suporte a TSF. (padrão: 0)<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </dl></td>
<td>Ativa a tradução de CRCRLFs para CRs. Quando esse bit estiver ativado e um arquivo for lido no, todas as instâncias de CRCRLF serão convertidas em CRs fixas internamente. Isso afetará a disposição do texto. Observe que, se esse arquivo for salvo como texto sem formatação, o CRs será substituído por CRLF. Este é o padrão de .txt para texto sem formatação (padrão: 0, que exclui CRCRLFs na entrada). <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Redistribuível<br/>          | Edição avançada 3,0<br/>                                                              |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ SETEDITSTYLE**](em-seteditstyle.md)
</dt> </dl>

 

