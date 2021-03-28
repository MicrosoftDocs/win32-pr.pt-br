---
description: 'Um aplicativo pode usar seis funções para definir os atributos de formatação de texto para um contexto de dispositivo: SetBkColor, SetBkMode, SetTextAlign, SetTextCharacterExtra, SetTextColor e SetTextJustification.'
ms.assetid: fd4d81ee-7f8f-41e8-88a5-d3ed89f4c7bd
title: Atributos de Text-Formatting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d345bfcfe1693a7ff0b25bb323615dffe221ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550844"
---
# <a name="text-formatting-attributes"></a>Atributos de Text-Formatting

Um aplicativo pode usar seis funções para definir os atributos de formatação de texto para um contexto de dispositivo: [SetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor), [SetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode), [SetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign), [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra), [SetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor)e [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification). Essas funções afetam o alinhamento de texto, o espaçamento entre caracteres, a justificação de texto e as cores de texto e de plano de fundo. Além disso, seis outras funções podem ser usadas para recuperar os atributos de formatação de texto atuais para qualquer contexto de dispositivo: [GetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor), [GetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode), [GetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign), [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra), [GetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor)e [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a).

## <a name="text-alignment"></a>Alinhamento de texto

Os aplicativos podem usar a função [SetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) para especificar como o sistema deve posicionar os caracteres em uma cadeia de texto quando eles chamam uma das funções de desenho. Essa função pode ser usada para posicionar títulos, números de página, textos explicativos e assim por diante. O sistema posiciona uma cadeia de caracteres de texto alinhando um ponto de referência em um retângulo imaginário que circunda a cadeia de caracteres, com a posição atual do cursor ou com um ponto passado como um argumento para uma das funções de desenho de texto. A função [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) permite que o aplicativo especifique o local desse ponto de referência. A seguir está uma lista dos possíveis locais de ponto de referência.



| Location         | Descrição                                                                                                             |
|------------------|-------------------------------------------------------------------------------------------------------------------------|
| esquerda/inferior      | O ponto de referência está localizado no canto inferior esquerdo do retângulo.                                               |
| linha esquerda/base   | O ponto de referência está localizado na interseção da linha de base de célula de caractere e na borda esquerda do retângulo.  |
| esquerda/superior         | O ponto de referência está localizado no canto superior esquerdo do retângulo.                                                 |
| centro/inferior    | O ponto de referência está localizado no centro da parte inferior do retângulo.                                            |
| Central/linha de base | O ponto de referência está localizado na interseção da linha de base de célula de caractere e no centro do retângulo.     |
| central/superior       | O ponto de referência está localizado no centro da parte superior do retângulo.                                               |
| direita/inferior     | O ponto de referência está localizado no canto inferior direito do retângulo.                                              |
| direita/linha de base  | O ponto de referência está localizado na interseção da linha de base de célula de caracteres e na borda direita do retângulo. |
| direita/superior        | O ponto de referência está localizado no canto superior direito do retângulo.                                                |



 

A ilustração a seguir mostra uma cadeia de texto desenhada chamando a função [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) . Antes de desenhar o texto, a função [SetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) foi chamada para realocar o ponto de referência em cada um dos nove locais possíveis.

![ilustração mostrando o mesmo texto nove vezes, um para cada local de ponto de referência possível](images/csftx-04.png)

O alinhamento de texto padrão para um contexto de dispositivo é o canto superior esquerdo do retângulo imaginário que circunda o texto. Um aplicativo pode recuperar a configuração de alinhamento de texto atual para qualquer contexto de dispositivo chamando a função [GetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) .

## <a name="intercharacter-spacing"></a>Espaçamento entre caracteres

Os aplicativos podem usar a função [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) para alterar o espaçamento entre caracteres de todas as operações de saída de texto em um contexto de dispositivo especificado. A ilustração a seguir mostra uma cadeia de texto desenhada duas vezes chamando a função [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) . Antes de desenhar o texto da segunda vez, a função [**SetTextCharacterExtra**](/windows/win32/api/wingdi/nf-wingdi-settextcharacterextra) foi chamada para incrementar o espaçamento entre caracteres.

![a ilustração shoing o mesmo texto duas vezes: primeiro com o espaçamento normal entre caracteres e, em seguida, com espaçamento maior](images/csftx-06.png)

O valor de espaçamento entre caracteres padrão para qualquer contexto de dispositivo é zero. Um aplicativo pode recuperar o valor de espaçamento entre caracteres atual para um contexto de dispositivo chamando a função [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) .

## <a name="text-justification"></a>Justificação de texto

Os aplicativos podem usar as funções [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) e [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) para justificar uma linha de texto. A justificação de texto é uma operação comum em qualquer publicação de área de trabalho e na maioria dos aplicativos de processamento de texto. A função [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) computa a largura e a altura de uma cadeia de caracteres de texto. Depois que a largura é calculada, o aplicativo pode chamar a função [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) para distribuir o espaçamento adicional entre cada uma das palavras em uma linha de texto. A ilustração a seguir mostra um parágrafo de texto impresso duas vezes: no primeiro parágrafo, o texto não foi justificado; no segundo parágrafo, o texto foi justificado chamando as funções **GetTextExtentPoint32** e **SetTextJustification** .

![ilustração mostrando um parágrafo que se alinha somente à esquerda e, em seguida, o mesmo parágrafo alinhado à esquerda e à direita](images/csftx-05.png)

## <a name="text-and-background-color"></a>Cor do texto e do plano de fundo

Os aplicativos podem usar a função [SetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor) para definir a cor do texto desenhado na área do cliente de suas janelas, bem como a cor do texto desenhado em uma impressora colorida. Um aplicativo pode usar a função [SetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor) para definir a cor que aparece atrás de cada caractere e a função [SetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode) para especificar como o sistema deve misturar a cor do plano de fundo selecionada com a cor ou as cores atuais na exibição do vídeo.

A cor de texto padrão para um contexto de dispositivo de exibição é preta; a cor do plano de fundo padrão é branca; e o modo em segundo plano padrão é opaco. Um aplicativo pode recuperar a cor do texto atual para um contexto de dispositivo chamando a função [GetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor) . Um aplicativo pode recuperar a cor do plano de fundo atual para um contexto de dispositivo chamando a função [GetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor) e o modo de segundo plano atual chamando a função [GetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode) .

 

 
