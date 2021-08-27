---
title: Como usar informações de quebra de linha e palavra
description: Um controle de edição avançada chama uma função chamada um procedimento de quebra de palavras para encontrar quebras entre palavras e determinar onde ele pode quebrar linhas.
ms.assetid: DDCE9814-0D39-494C-953A-FB6A98100EEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178770ce4a7206c18f6fbbc197d92e23ff0139ae637bd5f7ceb4159aee3270ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059686"
---
# <a name="how-to-use-word-and-line-break-information"></a>Como usar informações de quebra de linha e palavra

Um controle de edição avançada chama uma função chamada um procedimento de quebra de palavras para encontrar quebras entre palavras e determinar onde ele pode quebrar linhas. O controle usa essas informações ao executar operações de quebra de texto e ao processar combinações de tecla CTRL+SETA PARA A ESQUERDA e CTRL+SETA PARA A DIREITA. Um aplicativo pode enviar mensagens para um controle de edição rich para substituir o procedimento de quebra de palavras padrão, recuperar informações de quebra de palavras e determinar em qual linha um determinado caractere se enquadra.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções

### <a name="use-word-and-line-break-information"></a>Usar informações de quebra de linha e palavras

Os procedimentos de quebra de palavras para controles de edição avançados são semelhantes aos de controles de edição, mas eles têm funcionalidades adicionais: os procedimentos de quebra de palavras para ambos os tipos de controles podem determinar se um caractere é um delimiter e podem encontrar a quebra de palavra mais próxima antes ou depois da posição especificada. Um delimiter é um caractere que marca o final de uma palavra, como um espaço. Normalmente, em um controle de edição, uma quebra de palavra ocorre somente após delimitadores. No entanto, regras diferentes se aplicam à maioria dos idiomas asiáticos.

Os procedimentos de quebra de palavras para controles de edição rich também agrupam caracteres em classes de caracteres, cada um identificado por um valor no intervalo 0x00 até 0x0F. As quebras ocorrem após delimitadores ou entre caracteres de classes diferentes. Portanto, um procedimento de quebra de palavras com classes diferentes para caracteres alfanuméricos e pontuação encontrará duas quebras de palavra na cadeia de caracteres "Win.doc" (antes e após o período).

A classe de um caractere pode ser combinada com zero ou mais sinalizadores de quebra de palavras para formar um valor de 8 bits. Ao executar operações de quebra de linha, um controle de edição rich usa sinalizadores de quebra de palavras para determinar onde ele pode quebrar linhas. O Rich Edit usa os seguintes sinalizadores de quebra de palavras.



| Sinalizador            | Descrição                                                                                                                       |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| WBF \_ BREAKAFTER | As linhas podem ser interrompidas após o caractere.                                                                                          |
| LINHA DE QUEBRA DO WBF \_  | O caractere é um delimiter. Delimitadores marcam as extremidades das palavras. As linhas podem ser interrompidas após delimitadores.                            |
| WBF \_ ISWHITE    | O caractere é um caractere de espaço em branco. Os caracteres de espaço em branco à frente não são incluídos no comprimento de uma linha durante a quebra. |



 

O valor BREAKAFTER do WBF é usado para permitir o empacotamento após um caractere que não marca o final de uma palavra, como \_ um hífen.

Você pode substituir o procedimento de quebra de palavras padrão para um controle de edição rich com seu próprio procedimento usando a [**mensagem EM \_ SETWORDBREAKPROC.**](em-setwordbreakproc.md) Para obter mais informações sobre procedimentos de quebra de palavras, consulte a descrição da [*função EditWordBreakProc.*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)

> [!Note]  
> Essa substituição não é recomendada para o Microsoft Rich Edit 2.0 e posterior, devido à complexidade da quebra de palavras multilíngue.

 

Para o Microsoft Rich Edit 1.0, você pode usar a mensagem [**EM \_ SETWORDBREAKPROCEX**](em-setwordbreakprocex.md) para substituir o procedimento de quebra de palavras estendida padrão por uma [*função EditWordBreakProcEx.*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) Essa função fornece informações adicionais sobre o texto, como o conjunto de caracteres. Você pode usar a [**mensagem EM \_ GETWORDBREAKPROCEX**](em-getwordbreakprocex.md) para recuperar o endereço do procedimento de quebra de palavras estendido atual. Observe que o Microsoft Rich Edit 2.0 e posterior não são suportados *por EditWordBreakProcEx,* **EM \_ GETWORDBREAKPROCEX** e **EM \_ SETWORDBREAKPROCEX.**

Você pode usar a [**mensagem EM \_ FINDWORDBREAK**](em-findwordbreak.md) para encontrar quebras de palavras ou para determinar a classe de um caractere e sinalizadores de quebra de palavras. Por sua vez, o controle chama seu procedimento de quebra de palavras para obter as informações solicitadas.

Para determinar em qual linha um determinado caractere se enquadra, você pode usar a [**mensagem EM \_ EXLINEFROMCHAR.**](em-exlinefromchar.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de edição rich](using-rich-edit-controls.md)
</dt> <dt>

[Windows demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 