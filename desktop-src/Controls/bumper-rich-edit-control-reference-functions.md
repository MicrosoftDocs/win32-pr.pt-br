---
title: Funções de edição avançadas
description: Funções de edição avançadas
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1b74069b63220a07bfb1bd5e3f5a1ad99a6c6c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482452"
---
# <a name="rich-edit-functions"></a>Funções de edição avançadas

## <a name="in-this-section"></a>Nesta seção




| Tópico | Descrição | 
|-------|-------------|
| <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a><br /> | A <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>função AutoCorrectProc</em></a> é uma função de retorno de chamada definida pelo aplicativo que é usada com a <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> mensagem.<br /> | 
| <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>Editstreamcallback</em></a><br /> | A <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>função EditStreamCallback</em></a> é uma função de retorno de chamada definida pelo aplicativo usada com as <a href="em-streamin.md"><strong>mensagens EM_STREAMIN</strong></a> e <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> aplicativo. Ele é usado para transferir um fluxo de dados para dentro ou fora de um controle de edição rico. O <strong>tipo EDITSTREAMCALLBACK</strong> define um ponteiro para essa função de retorno de chamada. <em>EditStreamCallback</em> é um espaço reservado para o nome da função definida pelo aplicativo. <br /> | 
| <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a><br /> | A <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>função EditWordBreakProcEx</em></a> é uma função de retorno de chamada definida pelo aplicativo usada com a <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> de texto. Ele determina o índice de caracteres da quebra de palavras ou da classe de caracteres e dos sinalizadores de quebra de palavras dos caracteres no texto especificado. O <strong>tipo EDITWORDBREAKPROCEX</strong> define um ponteiro para essa função de retorno de chamada. <em>EditWordBreakProcEx é</em> um espaço reservado para o nome da função definida pelo aplicativo. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a><br /> | Recupera o caractere alfanumérico matemático UTF (Formato de Transformação Unicode)-32 que corresponde ao caractere BMP (Plano Multilíngue Básico) e ao estilo de matemática especificados. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a><br /> | Recupera o estilo matemático e o código de caractere BMP (Plano Multilíngue Básico) que corresponde ao byte à direita especificado de um par substituto de matemática.<br /> | 
| <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a><br /> | A <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>função HyphenateProc</em></a> é uma função de retorno de chamada definida pelo aplicativo usada com a <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> mensagem. Ele determina como a hifenização é feita em um controle Microsoft Rich Edit.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a><br /> | Converte a matemática, o ruby e outros objetos embutidos no intervalo especificado para a forma linear.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a><br /> | Converte a matemática de formato linear em um intervalo em um formulário criado ou modifica o formulário criado atual. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a><br /> | Converte os caracteres matemáticos no intervalo especificado.<br /> | 
| <a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a><br /> | Registra dois nomes de classe, REListBox20W e RECombobox20W, que podem ser usados para criar janelas de caixa de listagem ou caixa de combinação Rich Edit. <br /><blockquote>[!Note]<br />Destinado a uso interno; não recomendado para uso em aplicativos. Essa função pode não ter suporte em versões futuras.</blockquote><br /> | 




 

 

