---
description: Caracteres substitutos e suplementares
ms.assetid: 0dea39e2-a2b4-47fc-b44a-56af8ba1e346
title: Caracteres substitutos e suplementares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b1dc4743627297962c7279449c06cc1ff967ac35f931a6e945b4577c937b59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130046"
---
# <a name="surrogates-and-supplementary-characters"></a>Caracteres substitutos e suplementares

Windows aplicativos normalmente usam UTF-16 para representar [dados de caractere Unicode.](unicode.md) O uso de 16 bits permite a representação direta de 65.536 caracteres exclusivos, mas esse BMP (Plano Multilíngue Básico) não é suficiente para abranger todos os símbolos usados em linguagens humanas. A versão Unicode 4.1 inclui mais de 97.000 caracteres, com mais de 70.000 caracteres somente para chinês.

O padrão Unicode estabeleceu 16 "planos" adicionais de caracteres, cada um com o mesmo tamanho que o BMP. Naturalmente, a maioria dos pontos de código além do BMP ainda não tem caracteres atribuídos a eles, mas a definição dos planos dá a Unicode o potencial de definir 1.114.112 caracteres (ou seja, 26 17 caracteres) dentro do intervalo de pontos de código \* U+0000 a U+10FFFF. Para UTF-16 representar esse conjunto maior de caracteres, o Padrão Unicode define "caracteres suplementares".

## <a name="about-supplementary-characters"></a>Sobre caracteres suplementares

Um caractere suplementar é um caractere localizado além do BMP e um "substituto" é um valor de código UTF-16. Para UTF-16, um "par substituto" é necessário para representar um único caractere suplementar. O primeiro substituto (alto) é um valor de código de 16 bits no intervalo U+D800 a U+DBFF. O segundo substituto (baixo) é um valor de código de 16 bits no intervalo U+DC00 a U+DFFF. Usando o mecanismo substituto, UTF-16 pode dar suporte a todos os 1.114.112 caracteres Unicode potenciais. Para obter mais detalhes sobre caracteres suplementares, substitutos e pares substitutos, consulte [O Padrão Unicode.](https://www.unicode.org/standard/standard.html)

> [!Note]  
> Windows 2000 introduz suporte para entrada básica, saída e classificação simples de caracteres suplementares. No entanto, nem todos os componentes do sistema são compatíveis com caracteres suplementares.

 

O sistema operacional dá suporte a caracteres suplementares das seguintes maneiras:

-   O formato 12 da tabela cmap de fonte OpenType dá suporte diretamente ao código de caracteres de 4 byte. Para obter mais informações, consulte a [especificação de fonte OpenType](/typography/opentype/spec/).
-   Windows dá suporte a [IMEs (editores](../dxtecharts/installing-and-using-input-method-editors.md)de método de entrada) habilitados para substitutos.
-   O [Windows API GDI](../gdi/windows-gdi.md) dá suporte ao formato de 12 tabelas cmap em fontes para que os substitutos possam ser exibidos corretamente.
-   A API [uniscribe](uniscribe.md) dá suporte a caracteres suplementares.
-   [Windows controles](../controls/window-controls.md), incluindo [Editar](../controls/edit-controls.md) e [Edição Rich ,](../controls/rich-edit-controls.md)são suportados por caracteres suplementares.
-   O mecanismo HTML dá suporte a páginas HTML que incluem caracteres suplementares para exibição, edição (por meio Outlook Express) e envio de formulários.
-   A tabela de classificação do sistema operacional dá suporte a caracteres suplementares.

## <a name="general-guidelines-for-software-development-using-supplementary-characters"></a>Diretrizes gerais para o desenvolvimento de software usando caracteres suplementares

UTF-16 lida com caracteres suplementares como pares substitutos. O sistema operacional processa um par substituto da mesma forma que processa marcas [sem espaçamento](using-nonspacing-characters-and-diacritics.md). No momento da exibição, o par substituto é exibido como um glifo por meio de Uniscribe, conforme prescrito pelo Padrão Unicode.

Windows O Vista apresenta três novas macros para ajudar a identificar substitutos e pares substitutos em cadeias de caracteres UTF-16. ELES SÃO [**É \_ SUBSTITUTO \_ ALTO,**](/windows/win32/api/Winnls/nf-winnls-is_high_surrogate) [**É SUBSTITUTO \_ \_ BAIXO**](/windows/win32/api/Winnls/nf-winnls-is_low_surrogate)e [**É PAR \_ \_ SUBSTITUTO**](/windows/win32/api/Winnls/nf-winnls-is_surrogate_pair).

Os aplicativos darão suporte automaticamente a caracteres suplementares se eles deem suporte a Unicode e usarem controles do sistema e funções de API padrão, como [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) e [**DrawText.**](/windows/win32/api/winuser/nf-winuser-drawtext) Portanto, se seu aplicativo usar controles de sistema padrão ou usar chamadas gerais do tipo [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)para exibição, os caracteres suplementares deverão funcionar sem nenhuma codificação especial.

Aplicativos que implementam seu próprio suporte de edição trabalhando em posições de glifo de maneira personalizada podem usar o Uniscribe para todo o processamento de texto. O Uniscribe tem funções separadas para lidar com o processamento de script complexo, como exibição de texto, teste de acerto e movimento do cursor. Um aplicativo deve chamar as funções Uniscribe especificamente para obter esses recursos avançados. Observe que os aplicativos que usam as funções Uniscribe são totalmente multilíngues, mas isso impõe uma penalidade de desempenho. Portanto, alguns aplicativos devem fazer seu próprio processamento de caracteres suplementares.

Como o mecanismo substituto para representar caracteres suplementares é bem definido, seu aplicativo pode incluir código para manipular o processamento de texto substituto UTF-16. Quando o aplicativo encontra um valor UTF-16 separado do intervalo substituto reservado inferior (um substituto baixo) ou do intervalo substituto reservado superior (um substituto alto), o valor deve ser uma metade de um par substituto. Portanto, o aplicativo pode detectar um par substituto fazendo uma verificação de intervalo simples. Se encontrar um valor UTF-16 no intervalo inferior ou superior, ele deverá acompanhar para trás ou encaminhar uma largura de 16 bits para obter o restante do caractere. Ao escrever seu aplicativo, tenha em mente que [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta) e [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva) se movem por pontos de código de 16 bits, não por pares substitutos.

> [!Note]  
> Os pontos de código substituto autônomos têm um substituto alto sem um substituto baixo adjacente ou vice-versa. Esses pontos de código são inválidos e não têm suporte. Seu comportamento é indefinido.

 

Se você estiver desenvolvendo um provedor de fonte ou IME, observe que os sistemas operacionais XP pré-Windows desabilitam o suporte a caracteres suplementares por padrão. Windows XP e posteriores habilitam caracteres suplementares por padrão. Se você fornecer uma fonte e um pacote IME que exija caracteres suplementares, seu aplicativo deverá definir os seguintes valores do Registro:


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

 

 
