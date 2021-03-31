---
description: Este tópico descreve as diferenças entre as funções de cadeia de caracteres usadas na manipulação de informações de conjunto de caracteres e Unicode. Essas funções têm implementações de página de código Unicode e do Windows para dar suporte aos parâmetros de página de código Unicode e do Windows.
ms.assetid: 52a15957-b44b-49ba-b915-e5c8e003a7e6
title: Diferenças de função de cadeia de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c940aa8be1603f7958fb1993cc521ca7b1ed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921333"
---
# <a name="string-function-differences"></a>Diferenças de função de cadeia de caracteres

Este tópico descreve as diferenças entre as funções de cadeia de caracteres usadas na manipulação de informações de conjunto de caracteres e Unicode. Essas funções têm implementações de [página de código](code-pages.md) [Unicode](unicode.md) e do Windows para dar suporte aos parâmetros de página de código Unicode e do Windows.

As funções de cadeia de caracteres a seguir não exigem um comentário especial. Suas implementações de página de código Unicode e Windows funcionam de forma idêntica.

-   [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta)
-   [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva)
-   [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [ **StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)
-   [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [ **StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa)
-   [**StrCbLength**](/windows/win32/api/strsafe/nf-strsafe-stringcblengtha), [ **StrCchLength**](/windows/win32/api/strsafe/nf-strsafe-stringcchlengtha)

O valor de comprimento recuperado por uma das funções de comprimento da cadeia de caracteres é sempre baseado na largura normal do caractere: 8 bits para páginas de código do Windows, 16 bits para Unicode. Esse valor é muitas vezes chamado de "contagem de caracteres". Esse termo é estritamente correto, pois as páginas de código do Windows que usam DBCS ( [conjuntos de caracteres de dois bytes](double-byte-character-sets.md) ) têm alguns caracteres de largura total que são representados de fato por dois bytes consecutivos. Uma situação semelhante surge em caso de [substitutos](surrogates-and-supplementary-characters.md) em Unicode.

As funções de cadeia de caracteres a seguir são sensíveis à localidade do thread atual, derivadas do idioma que o usuário seleciona no painel de controle. As funções [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa) e [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia) não executam comparações de bytes como suas namesakes ANSI, por exemplo, [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp). Em vez disso, eles comparam cadeias de caracteres de acordo com as regras da localidade.

-   [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)
-   [**CharLowerBuff**](/windows/win32/api/winuser/nf-winuser-charlowerbuffa)
-   [**CharUpper**](/windows/win32/api/winuser/nf-winuser-charuppera)
-   [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
-   [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)
-   [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)

As seguintes funções são convertidas entre o conjunto de caracteres OEM e a página de código do Windows atual ou Unicode, dependendo de qual versão é usada:

-   [**CharToOem**](/windows/win32/api/winuser/nf-winuser-chartooema)
-   [**CharToOemBuff**](/windows/win32/api/winuser/nf-winuser-chartooembuffa)
-   [**OemToCharBuff**](/windows/win32/api/winuser/nf-winuser-oemtocharbuffa)

As funções de impressão, por exemplo, [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), dão suporte a Unicode fornecendo os seguintes tipos de dados novos e alterados em suas especificações de formato. Essas especificações de formato afetam a maneira como as funções interpretam o parâmetro de entrada correspondente.



| Especificação de formato | Tipo de dados para versão da página de código do Windows | Tipo de dados para a versão Unicode |
|----------------------|-----------------------------------------|-------------------------------|
| c                    | CHAR                                    | WCHAR                         |
| C                    | WCHAR                                   | CHAR                          |
| HC, hC               | CHAR                                    | CHAR                          |
| HS, hS               | LPSTR                                   | LPSTR                         |
| LC, lC               | WCHAR                                   | WCHAR                         |
| ls, lS               | LPWSTR                                  | LPWSTR                        |
| s                    | LPSTR                                   | LPWSTR                        |
| S                    | LPWSTR                                  | LPSTR                         |



 

O tipo de dados para o texto de saída sempre depende da versão da função. Quando o tipo de dados do parâmetro de entrada e o tipo de dados do texto de saída não são aceitos, a função print executa uma conversão de Unicode para a página de código do Windows atual ou vice-versa, conforme necessário.

Para a versão Unicode das funções de impressão, a cadeia de caracteres de formato é Unicode, assim como o texto de saída.

> [!Caution]  
> A manipulação de buffer insatisfatório é incomplicada em muitos problemas de segurança que envolvem saturações de buffer. Consulte a [referência de strsafe. h](../menurc/strsafe-ovw.md). As funções definidas em strsafe. h fornecem processamento adicional para a manipulação de buffer adequada em seu código. Por esse motivo, eles devem substituir suas contrapartes C/C++ internas, bem como implementações específicas do Microsoft Windows. Para obter mais informações, consulte [Considerações sobre segurança: recursos internacionais](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Unicode na API do Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
