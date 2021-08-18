---
description: A maioria dos aplicativos escritos hoje lida com dados de caracteres principalmente como Unicode, usando a codificação UTF-16.
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

A maioria dos aplicativos escritos hoje lida com dados de caracteres principalmente como [Unicode](unicode.md), usando a codificação UTF-16. No entanto, muitos aplicativos herdados continuam a usar conjuntos de caracteres com base em páginas de código. Até mesmo os novos aplicativos às vezes precisam trabalhar com páginas de código, geralmente por um dos seguintes motivos:

-   Para se comunicar com aplicativos herdados.
-   Para se comunicar com servidores de email e de notícias mais antigos, que talvez nem sempre ofereçam suporte a Unicode.
-   para se comunicar com o Console do Windows.

> [!Note]  
> novos aplicativos Windows devem usar [Unicode](unicode.md) para evitar as inconsistências de páginas de código variadas e para facilitar a localização.

 

Cada página de código é representada por um identificador de página de código, por exemplo, 1252, e é manipulada pelas funções de API de conjunto de caracteres e Unicode. Para obter uma lista de identificadores de página de código com suporte, consulte [identificadores de página de código](code-page-identifiers.md). A referência de "páginas de código" no Microsoft [Go Global Developer Center](https://msdn.microsoft.com/goglobal) fornece descrições completas de várias páginas de código.

Windows páginas de código, geralmente chamadas de "páginas de código ANSI", são páginas de código para as quais valores não ASCII (valores maiores que 127) representam caracteres internacionais. essas páginas de código são usadas nativamente no Windows Me e também estão disponíveis no Windows NT e posterior.

> [!Note]  
> originalmente, Windows página de código 1252, a página de código comumente usada para inglês e outros idiomas da europa ocidental, era baseada em um rascunho de American National Standards Institute (ANSI). esse rascunho eventualmente se tornou ISO 8859-1, mas Windows página de código 1252 foi implementada antes que o padrão se tornou final e não é exatamente o mesmo que o ISO 8859-1.

 

muitas Windows funções de API têm versões "A" (ANSI) e "W" (wide, Unicode). a versão "a" manipula o texto com base em páginas de código Windows, enquanto a versão "W" manipula texto Unicode. confira [Windows tipos de dados para cadeias de caracteres](windows-data-types-for-strings.md) e [convenções para protótipos de função](conventions-for-function-prototypes.md).

as páginas de código Windows também são chamadas de "páginas de código ativo" ou "páginas de código ativa do sistema". um sistema operacional Windows sempre tem uma página de código Windows ativa no momento. Todas as [versões ANSI das funções de API](conventions-for-function-prototypes.md) usam a página de código atualmente ativa.

As páginas de código do OEM (fabricante original do equipamento) são páginas de código para as quais valores não ASCII representam o desenho de linha e os caracteres de pontuação. Essas páginas de código foram usadas originalmente para o MS-DOS e ainda são usadas para aplicativos de console. Eles também são usados para os nomes de arquivo não estendidos nos sistemas de arquivos FAT12, FAT16 e FAT32, conforme descrito em [conjuntos de caracteres usados em nomes de arquivos](character-sets-used-in-file-names.md). A página de código OEM usual para inglês é a página de código 437.

para páginas de código Windows e páginas de código OEM, os valores de código 0x00 a 0x7f correspondem ao conjunto de caracteres ASCII de 7 bits. Os valores de código 0x00 a 0x19 e 0x7F sempre representam caracteres de controle padronizados e 0x20 a 0x7E representam caracteres exibíveis padronizados. Os caracteres representados pelos códigos restantes, 0x80 por meio de 0xFF, variam entre os conjuntos de caracteres. Cada conjunto de caracteres inclui diferentes caracteres especiais, normalmente personalizados para um idioma ou grupo de idiomas. Windows página de código 1252 e página de código OEM 437 são geralmente usadas na Estados Unidos.

além das páginas de código Windows e OEM, seus aplicativos podem usar páginas de código não nativas. Os exemplos são páginas de código EBCDIC e Macintosh.

Duas codificações de Unicode (UTF-7 e UTF-8) são implementadas como páginas de código. Assim como outras páginas de código, cada página é conhecida por um identificador numérico e pode ser tratada com muitas das mesmas funções de API de conjunto de caracteres e Unicode.

As páginas de código podem ser páginas SBCS ( [conjunto de caracteres de byte único](single-byte-character-sets.md) ) ou páginas DBCS ( [conjunto de caracteres de byte duplo](double-byte-character-sets.md) ). Em páginas SBCS, cada byte codifica diretamente um único caractere, para que seja possível representar exatamente 256 caracteres distintos (incluindo caracteres de controle, letras, dígitos, pontuação, símbolos e similares). As páginas de código DBCS são usadas para linguagens como japonês e chinês. Nessa página de código, alguns caracteres têm codificações de dois bytes com determinados valores de bytes (sempre valores maiores que 127) servindo como "bytes de Lead". Em vez de codificar caracteres por conta própria, os bytes de Lead podem ser mapeados para um caractere somente em conjunto com um "byte de trilha".

Alguns protocolos herdados exigem o uso de páginas de código SBCS e DBCS. Cada página de código SBCS/DBCS dá suporte a caracteres diferentes, mas nenhuma página de código dá suporte à amplitude completa de caracteres fornecidos pelo Unicode. Cada página de código SBCS/DBCS dá suporte a um subconjunto diferente, codificado de forma diferente.

> [!Note]  
> Os dados convertidos de uma página de código SBCS ou DBCS para outro estão sujeitos a corrupção, pois o mesmo valor de dados em páginas de código diferentes pode codificar um caractere diferente. Os dados convertidos de Unicode para SBCS ou DBCS estão sujeitos à perda de dados, pois uma determinada página de código pode não ser capaz de representar todos os caracteres usados nesses dados Unicode específicos.

 

Além das páginas de código SBCS e DBCS, seus aplicativos disponibilizam as páginas de código de conjunto de caracteres multibyte 52936, 54936, 51949 e 5022x, que usam uma abordagem semelhante à de um DBCS. No entanto, uma página de código de conjunto de caracteres multibyte vai além das codificações de dois bytes de alguns caracteres. O UTF-7 e o UTF-8 usam uma abordagem semelhante para codificar o Unicode com base em bytes de 7 e 8 bits, respectivamente. Para obter mais informações, consulte [Unicode](unicode.md).

Várias funções de conjunto de caracteres e Unicode permitem que seus aplicativos manipulem páginas de código. Um aplicativo pode usar as funções [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) e [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) para obter informações sobre uma página de código. Essas informações incluem o caractere padrão usado quando um caractere em uma cadeia de caracteres convertida não tem nenhuma entrada correspondente na página de código.

um aplicativo pode usar as funções [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) para converter entre cadeias de caracteres com base em páginas de código Windows e em cadeias de caracteres Unicode. Embora seus nomes se refiram a "MultiByte", essas funções funcionam igualmente bem com as páginas de código SBCS, DBCS e conjunto de caracteres MultiByte.

> [!Note]  
> [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) pode perder alguns dados se a página de código fornecida não puder representar todos os caracteres em uma cadeia de caracteres Unicode.

 

seu aplicativo pode converter entre Windows páginas de código e páginas de código OEM usando as funções padrão da biblioteca de tempo de execução C. No entanto, o uso dessas funções apresenta um risco de perda de dados porque os caracteres que podem ser representados por cada página de código não correspondem exatamente.

Seus aplicativos também podem chamar a função [**GetACP**](/windows/desktop/api/Winnls/nf-winnls-getacp) . essa função recupera o identificador da página de código Windows (ANSI) atual.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conjuntos de caracteres](character-sets.md)
</dt> </dl>

 

 



