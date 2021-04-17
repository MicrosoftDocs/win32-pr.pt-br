---
description: Caracteres substitutos e suplementares
ms.assetid: 0dea39e2-a2b4-47fc-b44a-56af8ba1e346
title: Caracteres substitutos e suplementares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8d6b738955c8b8de4f6cb0ae43c78f86752a928
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751462"
---
# <a name="surrogates-and-supplementary-characters"></a>Caracteres substitutos e suplementares

Os aplicativos do Windows normalmente usam UTF-16 para representar dados de caractere [Unicode](unicode.md) . O uso de 16 bits permite a representação direta de 65.536 caracteres exclusivos, mas esse BMP (plano multilíngüe básico) não é quase suficiente para abranger todos os símbolos usados em idiomas humanos. A versão 4,1 do Unicode inclui mais de 97.000 caracteres, com mais de 70.000 caracteres somente para chinês.

O padrão Unicode estabeleceu 16 "planos" adicionais de caracteres, cada um com o mesmo tamanho do BMP. Naturalmente, a maioria dos pontos de código além do BMP ainda não tem caracteres atribuídos a eles, mas a definição dos planos fornece ao Unicode o potencial para definir 1.114.112 caracteres (ou seja, 2 ¹ ⁶ \* 17 caracteres) dentro do intervalo de pontos de código U + 0000 a u + 10FFFF. Para que o UTF-16 represente esse conjunto maior de caracteres, o padrão Unicode define "caracteres suplementares".

## <a name="about-supplementary-characters"></a>Sobre caracteres suplementares

Um caractere suplementar é um caractere localizado além do BMP, e um "substituto" é um valor de código UTF-16. Para UTF-16, um "par substituto" é necessário para representar um único caractere suplementar. O primeiro substituto (alto) é um valor de código de 16 bits no intervalo U + D800 a U + DBFF. O segundo substituto (baixo) é um valor de código de 16 bits no intervalo U + DC00 a U + DFFF. Usando o mecanismo substituto, o UTF-16 pode dar suporte a todos os 1.114.112 caracteres Unicode potenciais. Para obter mais detalhes sobre caracteres suplementares, substitutos e pares substitutos, consulte [o padrão Unicode](https://www.unicode.org/standard/standard.html).

> [!Note]  
> O Windows 2000 apresenta suporte para entrada básica, saída e classificação simples de caracteres suplementares. No entanto, nem todos os componentes do sistema são compatíveis com caracteres suplementares.

 

O sistema operacional dá suporte a caracteres suplementares das seguintes maneiras:

-   O formato 12 da tabela de mapa de fontes OpenType dá suporte diretamente ao código de caractere de 4 bytes. Para obter mais informações, consulte a [especificação de fonte OpenType](/typography/opentype/spec/).
-   O Windows oferece suporte a [IMEs (editores de método de entrada)](../dxtecharts/installing-and-using-input-method-editors.md)habilitados para substituto.
-   A API [GDI do Windows](../gdi/windows-gdi.md) dá suporte ao formato 12 tabelas de CMap em fontes para que os substitutos possam ser exibidos corretamente.
-   A API do [Uniscribe](uniscribe.md) dá suporte a caracteres suplementares.
-   Os [controles do Windows](../controls/window-controls.md), incluindo [edição](../controls/edit-controls.md) e [edição avançada](../controls/rich-edit-controls.md), dão suporte a caracteres suplementares.
-   O mecanismo HTML dá suporte a páginas HTML que incluem caracteres suplementares para exibição, edição (através do Outlook Express) e envio de formulários.
-   A tabela de classificação do sistema operacional dá suporte a caracteres suplementares.

## <a name="general-guidelines-for-software-development-using-supplementary-characters"></a>Diretrizes gerais para o desenvolvimento de software usando caracteres suplementares

O UTF-16 lida com caracteres suplementares como pares substitutos. O sistema operacional processa um par substituto da mesma forma que processa marcas de não [espaçamento](using-nonspacing-characters-and-diacritics.md). No momento da exibição, o par alternativo é exibido como um glifo por meio do Uniscribe, conforme prescrito pelo padrão Unicode.

O Windows Vista apresenta três novas macros para ajudar a identificar substitutos e pares substitutos em cadeias de caracteres UTF-16. Esses são [**\_ \_ substitutos altos**](/windows/win32/api/Winnls/nf-winnls-is_high_surrogate), são de [**\_ baixo \_ substituto**](/windows/win32/api/Winnls/nf-winnls-is_low_surrogate)e [**são \_ \_ pares substitutos**](/windows/win32/api/Winnls/nf-winnls-is_surrogate_pair).

Os aplicativos dão suporte automaticamente a caracteres suplementares se eles dão suporte a Unicode e usam controles do sistema e funções de API padrão, como [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) e [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext). Portanto, se seu aplicativo usar controles de sistema padrão ou usar chamadas gerais de tipo [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)para exibir, caracteres suplementares devem funcionar sem qualquer codificação especial.

Os aplicativos que implementam seu próprio suporte de edição ao trabalhar com posições de glifo de maneira personalizada podem usar o Uniscribe para todo o processamento de texto. O Uniscribe tem funções separadas para lidar com processamento de script complexo, como exibição de texto, teste de clique e movimento de cursor. Um aplicativo deve chamar as funções de Uniscribe especificamente para obter esses recursos avançados. Observe que os aplicativos que usam as funções de Uniscribe são totalmente multilíngues, mas isso impõe uma penalidade de desempenho. Portanto, alguns aplicativos devem fazer seu próprio processamento de caracteres suplementares.

Como o mecanismo substituto para representar caracteres suplementares é bem definido, seu aplicativo pode incluir código para manipular o processamento de texto substituto UTF-16. Quando o aplicativo encontra um valor UTF-16 separado do intervalo substituto inferior reservado (um substituto baixo) ou o intervalo substituto Superior reservado (um substituto alto), o valor deve ser uma metade de um par alternativo. Assim, o aplicativo pode detectar um par alternativo fazendo uma verificação de intervalo simples. Se encontrar um valor UTF-16 no intervalo inferior ou superior, ele deverá rastrear a largura de 1 16 bits para trás ou para frente para obter o restante do caractere. Ao escrever seu aplicativo, tenha em mente que [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta) e [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva) se movem por pontos de código de 16 bits, não por pares substitutos.

> [!Note]  
> Pontos de código substituto autônomos têm um substituto alto sem um substituto baixo adjacente ou vice-versa. Esses pontos de código são inválidos e não têm suporte. Seu comportamento é indefinido.

 

Se você estiver desenvolvendo um provedor de fonte ou IME, observe que os sistemas operacionais anteriores ao Windows XP desabilitam o suporte a caracteres suplementares por padrão. O Windows XP e posteriores habilitam caracteres suplementares por padrão. Se você fornecer uma fonte e um pacote do IME que exija caracteres suplementares, seu aplicativo deverá definir os seguintes valores de registro:


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\LanguagePack]
SURROGATE=(REG_DWORD)0x00000002

[HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\International\Scripts\42]
IEFixedFontName=[Surrogate Font Face Name]
IEPropFontName=[Surrogate Font Face Name]
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conjuntos de caracteres](character-sets.md)
</dt> </dl>

 

 
