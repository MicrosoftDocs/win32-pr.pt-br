---
description: Este tópico fornece informações sobre considerações de segurança relacionadas aos recursos de suporte internacional.
ms.assetid: 4034f479-ad29-4c6f-82c6-977f420c4d4d
title: 'Considerações sobre segurança: recursos internacionais'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2e61566fdf51b80a76e5c8997018f35ce421dee6dd0e1b9e290888d96576249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147039"
---
# <a name="security-considerations-international-features"></a>Considerações sobre segurança: recursos internacionais

Este tópico fornece informações sobre considerações de segurança relacionadas aos recursos de suporte internacional. Você pode usá-lo como um ponto de partida e, em seguida, ver a documentação da tecnologia internacional de interesse para considerações de segurança específicas de tecnologia.

Este tópico inclui as seções a seguir.

-   [Considerações de segurança para funções de conversão de caracteres](#security-considerations-for-character-conversion-functions)
-   [Considerações de segurança para funções de comparação](#security-considerations-for-comparison-functions)
-   [Considerações de segurança para conjuntos de caracteres em nomes de arquivos](#security-considerations-for-character-sets-in-file-names)
-   [Considerações de segurança para nomes de domínio internacionalizados](#security-considerations-for-internationalized-domain-names)
-   [Considerações de segurança para funções ANSI](#security-considerations-for-ansi-functions)
-   [Considerações de segurança para normalização de Unicode](#security-considerations-for-unicode-normalization)

## <a name="security-considerations-for-character-conversion-functions"></a>Considerações de segurança para funções de conversão de caracteres

[**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) são as funções Unicode e de conjunto de caracteres usadas com mais frequência para converter caracteres entre ANSI e Unicode. Essas funções têm o potencial de causar riscos de segurança porque elas contam os elementos dos buffers de entrada e de saída de forma diferente. Por exemplo, [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) usa um buffer de entrada contado em bytes e coloca os caracteres convertidos em um buffer dimensionado em caracteres Unicode. Quando seu aplicativo usa essa função, ele deve dimensionar os buffers corretamente para evitar uma saturação de buffer.

[**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) assume como padrão o mapeamento "melhor ajuste" para páginas de código, como 1252. No entanto, esse tipo de mapeamento permite várias representações da mesma cadeia de caracteres, potencialmente deixando seu aplicativo vulnerável a ataques. Por exemplo, A letra latina maiúscula A com trema ("Ä") pode ser mapeada para a letra latina maiúscula A ("A"); um caractere Unicode em um idioma asiático pode ser mapeado para uma barra ("/"). O uso do sinalizador WC \_ nenhum \_ melhor \_ ajuste de \_ caracteres é preferencial de uma perspectiva de segurança.

Algumas páginas de código, por exemplo, as páginas de código 5022x (ISO-2022-x), são inerentemente inseguras, pois permitem várias representações da mesma cadeia de caracteres. O código escrito corretamente executa verificações de segurança no formato Unicode, mas esses tipos de páginas de código expandem o ataque susceptibilidade de seus aplicativos e devem ser evitados, se possível.

## <a name="security-considerations-for-comparison-functions"></a>Considerações de segurança para funções de comparação

Comparações de cadeia de caracteres podem potencialmente apresentar problemas de segurança. Como todas as funções de comparação são ligeiramente diferentes, uma função pode relatar duas cadeias de caracteres como iguais, enquanto outra função pode considerá-las distintas. A seguir estão várias funções que seus aplicativos podem usar para comparar cadeias de caracteres:

-   [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia). Compara duas cadeias de caracteres de caractere de acordo com as regras da localidade, sem diferenciação de maiúsculas e minúsculas. A função compara as cadeias de caracteres, verificando os primeiros e assim por diante, os segundo caracteres entre si e assim por diante, até encontrar uma desigualdade ou atingir as extremidades das cadeias de caracteres.
-   [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa). Compara Cadeias de caracteres usando técnicas semelhantes às de [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia). A única diferença é que o [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) executa uma comparação de cadeia de caracteres que diferencia maiúsculas de minúsculas.
-   [**comparestring**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) (Windows Vista e posterior). Execute uma comparação de cadeia de caracteres em uma localidade fornecida pelo aplicativo. [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) é semelhante a [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw), mas identifica uma localidade por [nome de localidade](locale-names.md) em vez de [identificador de localidade](locale-identifiers.md). Essas funções são semelhantes a [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) e [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) , exceto que operam em uma localidade específica, em vez de uma localidade selecionada pelo usuário.
-   [**CompareStringOrdinal**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringordinal) (Windows Vista e posterior). Compara duas cadeias de caracteres Unicode para testar a equivalência binária. Exceto pela opção de diferenciar maiúsculas de minúsculas, essa função desconsidera todas as equivalências não binárias e testa todos os pontos de código para igualdade, incluindo pontos de código que não recebem nenhum peso nos esquemas de [classificação](sorting.md) linguística. Observe que as outras funções de comparação mencionadas neste tópico não testam todos os pontos de código para igualdade.
-   [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) (Windows Vista e posterior). Localize uma cadeia de caracteres Unicode em outra cadeia de caracteres Unicode. [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) é semelhante a [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), exceto que identifica uma localidade por nome de localidade em vez de identificador de localidade.
-   [**FindStringOrdinal**](/windows/desktop/api/Libloaderapi/nf-libloaderapi-findstringordinal) (Windows 7 e posterior). Localiza uma cadeia de caracteres Unicode em outra cadeia de caracteres Unicode. O aplicativo deve usar essa função em vez de [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) para todas as comparações não linguísticas.

Como [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) e [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa), [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) avalia as cadeias de caracteres por caractere. No entanto, muitas linguagens têm elementos de vários caracteres, por exemplo, o elemento de dois caracteres "CH" em espanhol tradicional. Como [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) usa a localidade fornecida pelo aplicativo para identificar elementos de vários caracteres e [lstrcmpi](/windows/win32/api/winbase/nf-winbase-lstrcmpia) e [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa) usam a localidade do thread, cadeias de caracteres idênticas podem não ser comparadas como iguais.

O [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) ignora os caracteres indefinidos e, portanto, retorna zero (indicando cadeias iguais) para muitos pares de cadeias de caracteres que são bastante distintos. Uma cadeia de caracteres pode conter valores que não são mapeados para qualquer caractere ou pode conter caracteres com semântica fora do domínio do aplicativo, como caracteres de controle em uma URL. Os aplicativos que usam essa função devem fornecer manipuladores de erro e cadeias de caracteres de teste para certificar-se de que eles são válidos antes de usá-los.

> [!Note]  
> para Windows Vista e posterior, [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex) é semelhante a [**comparestring**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw). Os problemas de segurança são idênticos para essas funções.

 

Problemas de segurança semelhantes se aplicam a funções, como [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring), que fazem comparações implícitas. Dependendo dos sinalizadores definidos, os resultados da chamada de [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring) para pesquisar uma cadeia de caracteres dentro de outra cadeia de caracteres podem ser consideravelmente diferentes.

> [!Note]  
> para o Windows Vista e posterior, o [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex) é semelhante ao [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring). Os problemas de segurança são idênticos para essas funções.

 

## <a name="security-considerations-for-character-sets-in-file-names"></a>Considerações de segurança para conjuntos de caracteres em nomes de arquivos

Windows página de código e conjuntos de caracteres OEM usados em sistemas de idioma japonês contêm o símbolo de iene (¥) em vez de uma barra invertida ( \\ ). Portanto, o caractere de Iene é um caractere proibido para sistemas de arquivos NTFS e FAT. Ao mapear o Unicode para uma página de código de idioma japonês, as funções de conversão mapeiam ambas as barras invertidas (U + 005C) e o símbolo de iene Unicode normal (U + 00A5) para esse mesmo caractere. Por motivos de segurança, os aplicativos normalmente não devem permitir o caractere U + 00A5 em uma cadeia de caracteres Unicode que pode ser convertida para uso como um nome de arquivo FAT.

## <a name="security-considerations-for-internationalized-domain-names"></a>Considerações de segurança para nomes de domínio internacionalizados

Os IDNs (nomes de domínio internacionalizados) são especificados pelo [RFC 3490 do grupo de trabalho de rede: Internacionalizando nomes de domínio em aplicativos (IDNA)](http://www.faqs.org/rfcs/rfc3490.html). O padrão apresenta vários problemas de segurança.

Os glifos que representam determinados caracteres de scripts diferentes podem parecer semelhantes ou mesmo idênticos. Por exemplo, em muitas fontes, A letra cirílica minúscula A ("a") não é diferencial da letra latina minúscula A ("a"). Não há como dizer visualmente que "example.com" e "example.com" são dois nomes de domínio diferentes, um com uma letra latina minúscula no nome, o outro com uma letra cirílica minúscula A. Um site de host inescrupuloso pode usar essa ambiguidade Visual para fingir ser outro site em um ataque de falsificação.

O conjunto de caracteres estendidos que o IDNA permite para IDNs também tem potencial de falsificação dentro de um script específico. Por exemplo, há uma forte semelhança entre o hífen-menos ("-" U + 002D), o hífen ("–" U + 2010), o hífen não separável ("-" U + 2011), a figura Dash ("\u2012" U + 2012), o traço en ("–" U + 2013) e o sinal de subtração ("−" U + 2212).

Problemas semelhantes surgem de determinadas composições de compatibilidade. Por exemplo, o número de caractere Unicode único vinte e uma parada completa ("20.", U + 249B) é convertido em "20". (U + 0032 U + 0030 U + 002E) em uma etapa NamePrep, antes da conversão para Punycode. Em outras palavras, essa composição insere um ponto (parada completa). Essas composições têm potencial de falsificação.

A combinação de scripts diferentes em um IDN não necessariamente indica falsificação ou intenção enganosa. [Relatório técnico \# 36: considerações de segurança de Unicode](https://www.unicode.org/reports/tr36/#international_domain_names) fornece vários exemplos de IDNs razoáveis que contêm uma mistura de scripts, como XML-Документы. com ("Документы" é russo para "Documents").

Ataques de falsificação não são restritos a IDNs. Por exemplo, "rnicrosoft.com" parece muito com "microsoft.com", mas é um nome ASCII. Além disso, um ataque de falsificação pode ser feito por corrupção de um nome. A adição de rótulos extras após um nome de marca conhecido, ou incluindo o nome da marca no caminho de uma URL rotulada como segura, pode confundir usuários iniciantes, independentemente do uso do IDN. Para algumas localidades, os IDNs são necessários e a forma Punycode desses nomes é inaceitável, pois faz com que os nomes pareçam ininteligívels.

Para obter mais informações sobre os problemas de segurança mencionados aqui, além de um grande número de outros problemas relevantes para o IDNA, consulte [relatório técnico \# 36: considerações de segurança de Unicode](https://www.unicode.org/reports/tr36/#international_domain_names). Juntamente com discussões detalhadas sobre problemas de segurança relacionados a IDNA, este relatório oferece sugestões para lidar com IDNs suspeitos em seus aplicativos.

## <a name="security-considerations-for-ansi-functions"></a>Considerações de segurança para funções ANSI

> [!Note]  
> É recomendável usar o Unicode em seus aplicativos globalizados, especialmente os novos, se possível. Você deve usar funções ANSI somente se tiver motivos de substituição para não usar Unicode, por exemplo, conformidade com um protocolo mais antigo que não ofereça suporte a Unicode.

 

Muitas funções NLS (suporte a idioma nacional), como [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) e [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa), têm versões ANSI específicas, nesse caso, **getlocaleinfoa** e **GetCalendarInfoA**, respectivamente. quando seu aplicativo usa a versão ANSI de uma função com um sistema operacional baseado em Unicode, como Windows NT, Windows 2000, Windows XP ou Windows Vista, a função pode falhar ou produzir resultados indefinidos. Se você tiver um motivo convincente para usar funções ANSI com um sistema operacional como esse, verifique se os dados passados pelo seu aplicativo são válidos para ANSI.

## <a name="security-considerations-for-unicode-normalization"></a>Considerações de segurança para normalização de Unicode

Como a normalização Unicode pode alterar a forma de uma cadeia de caracteres, mecanismos de segurança ou algoritmos de validação de caracteres normalmente devem ser implementados após a normalização. Por exemplo, considere um aplicativo com uma interface da Web que aceita um nome de arquivo, mas não aceita um nome de caminho. Um U + FF43 U + FF1A U + FF3C U + FF57 U + FF49 U + FF4E u + FF44 u + FF4F u + FF57 u + FF53 u + 0063 u + 001A u + 003C u + 0077 u + 0069 U + 006E + 0064 & u u + 006F i + 0077 `(c : \ w i n d o w s)` `(c:\windows)` com a normalização de forma 0073. Se um aplicativo testar a presença dos dois pontos e dos caracteres de barra invertida antes de implementar a normalização, o resultado poderá ser o acesso ao arquivo não intencional.

Embora a normalização Unicode seja um elemento em tornar os sistemas operacionais seguros, lembre-se de que a normalização não é uma substituição para uma política de segurança abrangente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conjuntos de caracteres usados em nomes de arquivo](character-sets-used-in-file-names.md)
</dt> <dt>

[Convenções para protótipos de função](conventions-for-function-prototypes.md)
</dt> <dt>

[Lidando com a classificação em seus aplicativos](handling-sorting-in-your-applications.md)
</dt> <dt>

[Tratando IDNs (nomes de domínio internacionalizados)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[Unicode](unicode.md)
</dt> </dl>

 

 
