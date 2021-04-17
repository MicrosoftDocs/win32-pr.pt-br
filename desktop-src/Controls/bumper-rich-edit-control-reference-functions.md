---
title: Funções de edição avançadas
description: Funções de edição avançadas
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99f776b9a08095fa66645713e107a3d66920e80f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105748721"
---
# <a name="rich-edit-functions"></a>Funções de edição avançadas

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
<td><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a><br/></td>
<td>A função <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a> é uma função de retorno de chamada definida pelo aplicativo que é usada com a mensagem de <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a><br/></td>
<td>A função <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a> é uma função de retorno de chamada definida pelo aplicativo usada com as mensagens de <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> e <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> . Ele é usado para transferir um fluxo de dados para dentro ou para fora de um controle de edição rico. O tipo <strong>EditStreamCallback</strong> define um ponteiro para essa função de retorno de chamada. <em>EditStreamCallback</em> é um espaço reservado para o nome da função definida pelo aplicativo. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a><br/></td>
<td>A função <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a> é uma função de retorno de chamada definida pelo aplicativo usada com a mensagem de <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> . Ele determina o índice de caracteres da quebra de palavra ou a classe de caractere e os sinalizadores de quebra de palavras dos caracteres no texto especificado. O tipo <strong>EDITWORDBREAKPROCEX</strong> define um ponteiro para essa função de retorno de chamada. <em>EditWordBreakProcEx</em> é um espaço reservado para o nome da função definida pelo aplicativo. <br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a><br/></td>
<td>Recupera o formato UTF (Unicode Transformation Format)-32 matemático alfanuméricos que corresponde ao caractere básico de plano multilíngüe (BMP) e ao estilo matemático. <br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a><br/></td>
<td>Recupera o estilo matemático e o código de caractere básico de plano multilíngue (BMP) que corresponde ao byte à direita especificado de um par de substitutos de matemática.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a><br/></td>
<td>A função <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a> é uma função de retorno de chamada definida pelo aplicativo usada com a mensagem de <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> . Ele determina como a hifenização é feita em um controle de edição rico da Microsoft.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a><br/></td>
<td>Traduz os objetos internos de matemática, Ruby e outros incorporados no intervalo especificado para o formulário linear.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a><br/></td>
<td>Converte a matemática de formato linear em um intervalo em um formulário interno ou modifica o formulário atual criado. <br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a><br/></td>
<td>Traduz os caracteres matemáticos no intervalo especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a><br/></td>
<td>Registra dois nomes de classe, REListBox20W e RECombobox20W, que podem ser usados para criar janelas de caixa de listagem de edição rica ou de caixa de combinação. <br/>
<blockquote>
[!Note]<br />
Destinado ao uso interno; Não recomendado para uso em aplicativos. Essa função pode não ter suporte em versões futuras.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

