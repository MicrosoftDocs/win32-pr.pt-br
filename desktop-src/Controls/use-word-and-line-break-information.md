---
title: Como usar o Word e as informações de quebra de linha
description: Um controle de edição rico chama uma função chamada de procedimento de quebra de palavra para localizar quebras entre palavras e determinar onde ela pode quebrar linhas.
ms.assetid: DDCE9814-0D39-494C-953A-FB6A98100EEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feb90064e455bfeb8ee126e6107d75ef29b3a4f3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105754800"
---
# <a name="how-to-use-word-and-line-break-information"></a>Como usar o Word e as informações de quebra de linha

Um controle de edição rico chama uma função chamada de procedimento de quebra de palavra para localizar quebras entre palavras e determinar onde ela pode quebrar linhas. O controle usa essas informações ao executar operações de quebra automática de texto e ao processar CTRL + tecla de seta para a esquerda e CTRL + seta para a direita combinações de teclas. Um aplicativo pode enviar mensagens para um controle de edição rico para substituir o procedimento de quebra de palavra padrão, para recuperar informações de quebra de palavra e para determinar em qual linha um determinado caractere se encontra.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="use-word-and-line-break-information"></a>Usar informações de quebra de linha e de palavras

Os procedimentos de quebra de palavras para controles de edição avançados são semelhantes aos de controles de edição, mas têm recursos adicionais: os procedimentos de quebra de palavras para ambos os tipos de controles podem determinar se um caractere é um delimitador e encontrar a quebra de palavra mais próxima antes ou depois da posição especificada. Um delimitador é um caractere que marca o final de uma palavra, como um espaço. Normalmente, em um controle de edição, uma quebra de palavra ocorre somente após os delimitadores. No entanto, regras diferentes se aplicam à maioria dos idiomas asiáticos.

Os procedimentos de quebra de palavras para controles de edição avançados também agrupam caracteres em classes de caracteres, cada um identificado por um valor no intervalo de 0x00 a 0x0F. As quebras ocorrem após delimitadores ou entre caracteres de classes diferentes. Assim, um procedimento de quebra de palavra com classes diferentes para caracteres alfanuméricos e de Pontuação encontraria duas quebras de palavra na cadeia de caracteres "Win.doc" (antes e depois do período).

A classe de um caractere pode ser combinada com zero ou mais sinalizadores de quebra de palavras para formar um valor de 8 bits. Ao executar operações de quebra automática de linha, um controle de edição rico usa sinalizadores de quebra de palavras para determinar onde ele pode quebrar linhas. A edição avançada usa os seguintes sinalizadores de quebra de palavra.



| Sinalizador            | Descrição                                                                                                                       |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| WBF \_ BREAKAFTER | As linhas podem ser quebradas após o caractere.                                                                                          |
| \_divisão WBF  | O caractere é um delimitador. Os delimitadores marcam as extremidades das palavras. As linhas podem ser quebradas após os delimitadores.                            |
| WBF \_ ISwhite    | O caractere é um caractere de espaço em branco. Os caracteres de espaço em branco à direita não são incluídos no comprimento de uma linha durante o encapsulamento. |



 

O \_ valor de BREAKAFTER WBF é usado para permitir o encapsulamento após um caractere que não marca o fim de uma palavra, como um hífen.

Você pode substituir o procedimento de quebra de palavra padrão por um controle de edição rico por seu próprio procedimento usando a mensagem em [**\_ SETWORDBREAKPROC**](em-setwordbreakproc.md) . Para obter mais informações sobre os procedimentos de quebra de palavras, consulte a descrição da função [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) .

> [!Note]  
> Essa substituição não é recomendada para o Microsoft rich edit 2,0 e posterior, devido à complexidade da separação de palavras multilíngues.

 

Para o Microsoft Rich Edit 1,0, você pode usar a mensagem em [**\_ SETWORDBREAKPROCEX**](em-setwordbreakprocex.md) para substituir o procedimento de quebra de palavra estendido padrão por uma função [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) . Essa função fornece informações adicionais sobre o texto, como o conjunto de caracteres. Você pode usar a mensagem em [**\_ GETWORDBREAKPROCEX**](em-getwordbreakprocex.md) para recuperar o endereço do procedimento de quebra de palavra estendido atual. Observe que o Microsoft rich edit 2,0 e posterior não dão suporte a *EditWordBreakProcEx*, em **\_ GETWORDBREAKPROCEX** e em **\_ SETWORDBREAKPROCEX**.

Você pode usar a mensagem em [**\_ FINDWORDBREAK**](em-findwordbreak.md) para localizar quebras de palavras ou para determinar a classe de um caractere e os sinalizadores de quebra de palavras. Por sua vez, o controle chama seu procedimento de quebra de palavra para obter as informações solicitadas.

Para determinar em qual linha um determinado caractere se encontra, você pode usar a mensagem em [**\_ EXLINEFROMCHAR**](em-exlinefromchar.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de edição avançados](using-rich-edit-controls.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 