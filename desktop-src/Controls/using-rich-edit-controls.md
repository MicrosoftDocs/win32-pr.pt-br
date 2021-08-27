---
title: Usando controles de edição avançados
description: Esta seção contém tópicos que demonstram como criar e usar controles de edição avançados.
ms.assetid: 2c4717c9-3257-42d5-9c36-89b7e524e788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce4d6565160babc896ea9affe2d5c0c772c5b77e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466164"
---
# <a name="using-rich-edit-controls"></a>Usando controles de edição avançados

Esta seção contém tópicos que demonstram como criar e usar controles de edição avançados.

## <a name="in-this-section"></a>Nesta seção




| Tópico | Descrição | 
|-------|-------------|
| <a href="create-rich-edit-controls.md">Como criar controles de edição avançados</a><br /> | Para criar um controle de edição rico, chame a função <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> , especificando a classe da janela de edição rica. Para o Microsoft rich edit 4,1 (Msftedit.dll), especifique MSFTEDIT_CLASS como a classe de janela. Para todas as versões anteriores, especifique RICHEDIT_CLASS. Para obter mais informações, consulte <a href="about-rich-edit-controls.md">versões do rich edit</a>. <br /> Os controles de edição avançados dão suporte à maioria dos estilos de janela usados com controles de edição, bem como estilos adicionais. Você deve especificar o estilo de janela <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> se desejar permitir mais de uma linha de texto no controle. Para obter mais informações, consulte <a href="rich-edit-control-styles.md">Rich Edit Control Styles</a>. <br /> | 
| <a href="format-text-in-rich-edit-controls.md">Como formatar texto em controles de edição avançados</a><br /> | Um aplicativo pode enviar mensagens para um controle de edição rico a fim de formatar caracteres e parágrafos e recuperar informações de formatação. Os atributos de formatação de parágrafo incluem alinhamento, tabulações, recuos, numeração e tabelas simples. Para caracteres, você pode especificar o nome, o tamanho, a cor e os efeitos da fonte, como negrito, itálico e protegido. <br /> | 
| <a href="interact-with-the-current-selection.md">Como interagir com a seleção atual</a><br /> | O usuário pode selecionar o texto em um controle de edição rico usando o mouse ou o teclado. A <em>seleção atual</em> é o intervalo de caracteres selecionados ou a posição do ponto de inserção se nenhum caractere for selecionado. Um aplicativo pode obter informações sobre a seleção atual, defini-la, determinar quando ela é alterada e mostrar ou ocultar o realce de seleção. <br /> | 
| <a href="use-rich-edit-text-operations.md">Como usar operações de Rich Text de edição</a><br /> | Um aplicativo pode enviar mensagens para recuperar ou localizar texto em um controle de edição rico. Você pode recuperar o texto selecionado ou um intervalo de texto especificado. <br /> | 
| <a href="use-word-and-line-break-information.md">Como usar o Word e as informações de quebra de linha</a><br /> | Um controle de edição rico chama uma função chamada de procedimento de quebra de palavra para localizar quebras entre palavras e determinar onde ela pode quebrar linhas. O controle usa essas informações ao executar operações de quebra automática de texto e ao processar CTRL + tecla de seta para a esquerda e CTRL + seta para a direita combinações de teclas. Um aplicativo pode enviar mensagens para um controle de edição rico para substituir o procedimento de quebra de palavra padrão, para recuperar informações de quebra de palavra e para determinar em qual linha um determinado caractere se encontra. <br /> | 
| <a href="use-rich-edit-clipboard-operations.md">Como usar operações de edição de área de transferência avançadas</a><br /> | Um aplicativo pode colar o conteúdo da área de transferência em um controle de edição rico usando o melhor formato de área de transferência disponível ou um formato de área de transferência específico. Você também pode determinar se um controle de edição rico é capaz de colar um formato de área de transferência. <br /> | 
| <a href="use-streams.md">como usar Fluxos</a><br /> | Você pode usar fluxos para transferir dados para dentro ou para fora de um controle de edição rico. Um fluxo é definido por uma estrutura <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>EDITSTREAM</strong></a> , que especifica um buffer e uma função de retorno de chamada definida pelo aplicativo. <br /> | 
| <a href="automatically-resize-rich-edit-controls.md">Como redimensionar automaticamente os controles de edição avançados</a><br /> | Um aplicativo pode redimensionar um controle de edição rico conforme necessário para que seja sempre o mesmo tamanho que seu conteúdo. Um controle de edição rico dá suporte a essa chamada de funcionalidade <em>inferior</em> , enviando a janela pai um código de notificação <a href="en-requestresize.md">EN_REQUESTRESIZE</a> sempre que o tamanho do conteúdo do controle for alterado. <br /> | 
| <a href="use-rich-edit-control-notification-codes.md">Como usar códigos de notificação de controle de edição avançados</a><br /> | Uma janela pai do controle de edição rico pode processar códigos de notificação para monitorar eventos que afetam o controle. Os controles de edição avançados dão suporte a todos os códigos de notificação usados com controles de edição, bem como a vários outros. <br /> | 
| <a href="use-font-binding-in-rich-edit-controls.md">Como usar a associação de fontes em controles de edição avançados</a><br /> | O Microsoft Rich Edit 3,0 atribui um conjunto de caracteres a caracteres de texto sem formatação, dependendo de seu contexto. Alguns exemplos incluem: <br /><ul><li>Os caracteres gregos são atribuídos <strong>GREEK_CHARSET</strong>.</li><li>Os símbolos Hangul são atribuídos <strong>HANGUL_CHARSET</strong>.</li><li>Os caracteres chineses são atribuídos <strong>SHIFTJIS_CHARSET</strong> se caracteres kana forem encontrados próximo ou <strong>GB2312_CHARSET</strong> se nenhum kana for encontrado próximo.</li><li>Caracteres ANSI não neutros são atribuídos <strong>ANSI_CHARSET</strong> em qualquer evento.</li></ul> | 
| <a href="using-rich-edit-com.md">Como usar OLE em controles de edição Rich</a><br /> | Esta seção contém informações sobre como usar vinculação e incorporação de objetos (OLE) em controles de edição avançados. <br /> | 
| <a href="printing-rich-edit-controls.md">Como imprimir o conteúdo de controles de edição avançados</a><br /> | Esta seção contém informações sobre como imprimir o conteúdo de controles de edição avançados. <br /> | 




 

 

