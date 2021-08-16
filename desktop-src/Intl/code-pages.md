---
description: A maioria dos aplicativos escritos hoje lida com dados de caractere principalmente como Unicode, usando a codificação UTF-16.
ms.assetid: 866f09f4-629e-4097-a974-fbda9389d077
title: Páginas de código
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad589183bbb64a2feb65079a2322dd148598c6c3542320ec2ce851b9de61cfa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754956"
---
# <a name="code-pages"></a>Páginas de código

A maioria dos aplicativos escritos hoje lida com dados de caractere principalmente [como Unicode,](unicode.md)usando a codificação UTF-16. No entanto, muitos aplicativos herdado continuam a usar conjuntos de caracteres com base em páginas de código. Até mesmo novos aplicativos às vezes têm que trabalhar com páginas de código, geralmente por um dos seguintes motivos:

-   Para se comunicar com aplicativos herddos.
-   Para se comunicar com servidores de email e notícias mais antigos, que podem nem sempre dar suporte a Unicode.
-   Para se comunicar com o console Windows.

> [!Note]  
> Novos Windows aplicativos devem usar [Unicode](unicode.md) para evitar inconsistências de páginas de código variadas e para facilitar a localização.

 

Cada página de código é representada por um identificador de página de código, por exemplo, 1252, e é tratada pelas funções de API Unicode e conjunto de caracteres. Para ver uma lista de identificadores de página de código com suporte, consulte [Identificadores de página de código.](code-page-identifiers.md) A referência "Páginas de Código" no Centro de [DesenvolvedorEs Globais do](https://msdn.microsoft.com/goglobal) Microsoft Go fornece descrições completas de muitas páginas de código.

Windows de código, normalmente chamadas de "páginas de código ANSI", são páginas de código para as quais valores não ASCII (valores maiores que 127) representam caracteres internacionais. Essas páginas de código são usadas na Windows Me e também estão disponíveis no Windows NT e posteriores.

> [!Note]  
> Originalmente, Windows página de código 1252, a página de código comumente usada para inglês e outros idiomas da Europa Ocidental, era baseada em um rascunho anSI (American National Standards Institute). Esse rascunho acabou se tornando ISO 8859-1, mas Windows página de código 1252 foi implementada antes do padrão se tornar final e não é exatamente o mesmo que ISO 8859-1.

 

Muitas Windows api têm versões "A" (ANSI) e "W" (wide, Unicode). A versão "A" trata o texto com base Windows páginas de código, enquanto a versão "W" trata o texto Unicode. Consulte [Windows tipos de dados para cadeias de caracteres](windows-data-types-for-strings.md) e [convenções para protótipos de função](conventions-for-function-prototypes.md).

Windows páginas de código também são às vezes conhecidas como "páginas de código ativas" ou "páginas de código ativas do sistema". Um Windows sistema operacional sempre tem uma página de código Windows ativa no momento. Todas [as versões ANSI de funções de API](conventions-for-function-prototypes.md) usam a página de código ativa no momento.

Páginas de código OEM (fabricante original de equipamentos) são páginas de código para as quais valores não ASCII representam caracteres de desenho e pontuação de linha. Essas páginas de código foram originalmente usadas para o MS-DOS e ainda são usadas para aplicativos de console. Eles também são usados para os nomes de arquivo não estendidos nos sistemas de arquivos FAT12, FAT16 e FAT32, conforme descrito em Conjuntos de caracteres usados em nomes [de arquivo](character-sets-used-in-file-names.md). A página de código OEM normal para inglês é a página de código 437.

Para Windows páginas de código e páginas de código OEM, os valores de código 0x00 até 0x7F correspondem ao conjunto de caracteres ASCII de 7 bits. Os valores de 0x00 a 0x19 e 0x7F sempre representam caracteres de controle padronizados e 0x20 por meio 0x7E representam caracteres exibiáveis padronizados. Os caracteres representados pelos códigos restantes, 0x80 até 0xff, variam entre conjuntos de caracteres. Cada conjunto de caracteres inclui diferentes caracteres especiais, normalmente personalizados para um idioma ou grupo de idiomas. Windows de código 1252 e página de código OEM 437 geralmente são usadas no Estados Unidos.

Além de Windows páginas de código OEM e OEM, seus aplicativos podem usar páginas de código não nativas. Exemplos são páginas de código EBCDIC e Macintosh.

Duas codificações de Unicode (UTF-7 e UTF-8) são implementadas como páginas de código. Assim como outras páginas de código, cada página é conhecida por um identificador numérico e pode ser tratada com muitas das mesmas funções de API unicode e conjunto de caracteres.

As páginas de código podem ser páginas SBCS (conjunto de caracteres de [byte](single-byte-character-sets.md) único) ou páginas DBCS [(conjunto](double-byte-character-sets.md) de caracteres de byte duplo). Em páginas SBCS, cada byte codifica diretamente um único caractere, para que seja possível representar exatamente 256 caracteres distintos (incluindo caracteres de controle, letras, dígitos, pontuação, símbolos e assim por diante). As páginas de código DBCS são usadas para idiomas como japonês e chinês. Nessa página de código, alguns caracteres têm codificações de dois bytes com determinados valores de bytes (sempre valores maiores que 127) que servem como "bytes de lead". Em vez de codificar caracteres por conta própria, bytes de lead podem ser mapeados para um caractere somente em conjunto com um "byte à direita".

Alguns protocolos herdadas exigem o uso de páginas de código SBCS e DBCS. Cada página de código SBCS/DBCS dá suporte a caracteres diferentes, mas nenhuma página de código dá suporte à amplitude completa de caracteres fornecidos pelo Unicode. Cada página de código SBCS/DBCS dá suporte a um subconjunto diferente, codificado de forma diferente.

> [!Note]  
> Os dados convertidos de uma página de código SBCS ou DBCS para outra estão sujeitos a corrupção, porque o mesmo valor de dados em páginas de código diferentes pode codificar um caractere diferente. Os dados convertidos de Unicode para SBCS ou DBCS estão sujeitos à perda de dados, porque uma determinada página de código pode não ser capaz de representar todos os caracteres usados nos dados Unicode específicos.

 

Além das páginas de código SBCS e DBCS, seus aplicativos disponibilizam as páginas de código do conjunto de caracteres multibyte 52936, 54936, 51949 e 5022x, que usam uma abordagem semelhante à de um DBCS. No entanto, uma página de código de conjunto de caracteres multibyte vai além das codificações de dois byte de alguns caracteres. UTF-7 e UTF-8 usam uma abordagem semelhante para codificar Unicode com base em bytes de 7 bits e 8 bits, respectivamente. Para obter mais informações, consulte [Unicode](unicode.md).

Várias funções Unicode e conjunto de caracteres permitem que seus aplicativos lidam com páginas de código. Um aplicativo pode usar as [**funções GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) e [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) para obter informações sobre uma página de código. Essas informações incluem o caractere padrão usado quando um caractere em uma cadeia de caracteres convertida não tem nenhuma entrada correspondente na página de código.

Um aplicativo pode usar as funções [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) para converter entre cadeias de caracteres com base em Windows de código e cadeias de caracteres Unicode. Embora seus nomes se refiram a "MultiByte", essas funções funcionam igualmente bem com páginas de código do conjunto de caracteres SBCS, DBCS e multibyte.

> [!Note]  
> [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) poderá perder alguns dados se a página de código fornecida não puder representar todos os caracteres em uma cadeia de caracteres Unicode.

 

Seu aplicativo pode converter entre Windows de código e páginas de código OEM usando as funções de biblioteca de runtime C padrão. No entanto, o uso dessas funções apresenta um risco de perda de dados porque os caracteres que podem ser representados por cada página de código não são exatamente semelhantes.

Seus aplicativos também podem chamar a [**função GetACP.**](/windows/desktop/api/Winnls/nf-winnls-getacp) Essa função recupera o identificador da página de código Windows (ANSI) atual.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conjuntos de caracteres](character-sets.md)
</dt> </dl>

 

 



