---
title: Sobre cadeias de caracteres
description: Este tópico discute as funções de cadeia de caracteres.
ms.assetid: f1799fbf-4619-4b19-998e-b1d2f4c19a35
keywords:
- recursos, cadeias de caracteres
- cadeias de caracteres
- funções de cadeia de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff9fa6c9d93ba2f5c089b52b56816cad74bb61c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105756329"
---
# <a name="about-strings"></a>Sobre cadeias de caracteres

As funções de cadeia de caracteres fornecem aos aplicativos o meio de copiar, comparar, classificar, Formatar e converter cadeias de caracteres, bem como os meios para determinar o tipo de caractere de cada caractere em uma cadeia de caracteres. Todas as funções de cadeia de caracteres dão suporte aos conjuntos de caracteres de byte único, de byte duplo e Unicode se esses conjuntos de caracteres têm suporte no sistema operacional no qual o aplicativo é executado.

**Aviso de segurança:** O uso incorreto de funções de cadeia de caracteres pode causar problemas de segurança para seu aplicativo. Normalmente, isso envolve uma saturação de buffer que pode permitir um ataque de negação de serviço contra seu aplicativo ou a injeção de código executável de um invasor. As funções strsafe permitem a manipulação mais segura de cadeias de caracteres e são recomendadas para maior segurança para seu aplicativo. Para obter mais informações sobre essas funções, consulte [usando as funções strsafe. h](strsafe-ovw.md).

Esta seção aborda os tópicos a seguir.

-   [Comparação com as funções de cadeia de caracteres C Run-Time](#comparison-with-c-run-time-string-functions)
-   [Recursos de cadeia de caracteres](#string-resources)

## <a name="comparison-with-c-run-time-string-functions"></a>Comparação com as funções de cadeia de caracteres C Run-Time

Muitas funções de cadeia de caracteres duplicam ou aprimoram funções de cadeia de caracteres conhecidas da biblioteca CRT (tempo de execução) do C padrão. Muitos dos aprimoramentos permitem que as funções de cadeia de caracteres funcionem com conjuntos de caracteres Unicode ou estendidos. A tabela a seguir mostra as funções do CRT, as funções do Windows (que dão suporte ao Unicode, ao contrário das funções do CRT) e as funções StrSafe.



| Função de cadeia de caracteres CRT                                       | Função de cadeia de caracteres do Windows    | Função StrSafe                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [strcat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019) | [**lstrcat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata) | <dl> <dt>[**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)</dt> <dt>[**StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)</dt> <dt>[**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)</dt> <dt>[**StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)</dt> </dl>         |
| [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp?view=vs-2019) | [**lstrcmp**](/windows/desktop/api/Winbase/nf-winbase-lstrcmpa) | (nenhuma função equivalente)                                                                                                                                                                                                                                                                                                                                                                                  |
| [strcpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019) | [**lstrcpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya) | <dl> <dt>[**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)</dt> <dt>[**StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)</dt> <dt>[**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)</dt> <dt>[**StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)</dt> </dl> |
| [strlen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019) | [**lstrlen**](/windows/desktop/api/Winbase/nf-winbase-lstrlena) | <dl> <dt>[**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)</dt> <dt> [ **StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)</dt> </dl>                                                                                                                                                                                       |



 

A função **strlen** , por exemplo, sempre retorna o número de bytes em uma cadeia de caracteres, mas a função [**lstrlen**](/windows/desktop/api/Winbase/nf-winbase-lstrlena) retorna o número de valores **TCHAR** , que se refere a bytes para versões ANSI dos valores de função ou **WCHAR** para versões Unicode.

As seguintes funções de cadeia de caracteres diferem das funções padrão C, como **ToLower** e **ToUpper** , no que operam em qualquer caractere em um conjunto de caracteres. Usando a função [**CharLower**](/windows/desktop/api/Winuser/nf-winuser-charlowera) , por exemplo, um aplicativo pode converter um U maiúsculo com um trema (ü) para minúsculas (ü). Para obter mais informações sobre conjuntos de caracteres, consulte [conjuntos de caracteres de byte único](/windows/desktop/Intl/single-byte-character-sets).



| Função                               | Descrição                                   |
|----------------------------------------|-----------------------------------------------|
| [**CharLower**](/windows/desktop/api/Winuser/nf-winuser-charlowera)         | Converte um caractere ou uma cadeia de caracteres em minúsculas.  |
| [**CharLowerBuff**](/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa) | Converte uma cadeia de caracteres em minúsculas.     |
| [**CharNext**](/windows/desktop/api/Winuser/nf-winuser-charnexta)           | Move para o próximo caractere em uma cadeia de caracteres.      |
| [**CharPrev**](/windows/desktop/api/Winuser/nf-winuser-charpreva)           | Move para o caractere anterior em uma cadeia de caracteres. |
| [**CharUpper**](/windows/desktop/api/Winuser/nf-winuser-charuppera)         | Converte um caractere ou uma cadeia de caracteres em maiúsculas.  |
| [**CharUpperBuff**](/windows/desktop/api/Winuser/nf-winuser-charupperbuffa) | Converte uma cadeia de caracteres em letras maiúsculas.               |



 

As funções de cadeia de caracteres a seguir fazem determinações sobre um caractere com base na semântica do idioma selecionado pelo usuário. Essas funções são habilitadas para Unicode.



| Função                                         | Descrição                                     |
|--------------------------------------------------|-------------------------------------------------|
| [**IsCharAlpha**](/windows/desktop/api/Winuser/nf-winuser-ischaralphaa)               | Determina se um caractere é alfabético.   |
| [**IsCharAlphaNumeric**](/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica) | Determina se um caractere é alfanumérico. |
| [**IsCharLower**](/windows/desktop/api/Winuser/nf-winuser-ischarlowera)               | Determina se um caractere é minúsculo.    |
| [**IsCharUpper**](/windows/desktop/api/Winuser/nf-winuser-ischaruppera)               | Determina se um caractere é maiúsculo.    |



 

A tabela a seguir mostra as extensões Unicode para as funções CRT (tempo de execução) do C padrão. Conforme mencionado anteriormente, as funções StrSafe permitem a manipulação mais segura de cadeias de caracteres e são recomendadas para maior segurança para seu aplicativo.



| Função CRT padrão                                       | Função de cadeia de caracteres                | Função StrSafe                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [sprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)  | [**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)   | <dl> <dt>[**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)</dt> <dt>[**StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)</dt> <dt>[**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)</dt> <dt>[**StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)</dt> </dl>         |
| [vsprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019) | [**wvsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa) | <dl> <dt>[**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)</dt> <dt>[**StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)</dt> <dt>[**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)</dt> <dt>[**StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)</dt> </dl> |



 

## <a name="string-resources"></a>Recursos de cadeia de caracteres

Um aplicativo que mantém cadeias de caracteres em recursos pode ser traduzido em novas linguagens com esforço mínimo. Em vez de procurar cadeias de caracteres nos módulos de origem, você pode simplesmente converter as cadeias de caracteres no arquivo de recursos e vincular novamente o aplicativo. Além disso, o uso de recursos de cadeia de caracteres simplifica a criação de versões Unicode e não-Unicode do aplicativo dos mesmos arquivos de origem.

A função [**LoadString**](/windows/desktop/api/Winuser/nf-winuser-loadstringa) carrega um recurso de cadeia de caracteres do arquivo executável de um aplicativo. A função [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) carrega um recurso de cadeia de caracteres e interpreta as opções de formatação que podem ser inseridas na cadeia de caracteres.

Os recursos na forma binária são armazenados em formato Unicode. Ao carregar recursos, os aplicativos podem usar a versão Unicode das funções de recurso ([**LoadStringW**](/windows/desktop/api/Winuser/nf-winuser-loadstringa), por exemplo) para obter recursos como dados Unicode.

Para recursos de cadeia de caracteres de 16 bits, 255 caracteres é o comprimento máximo. Para recursos de cadeia de caracteres de 32 bits, 65535 caracteres é o comprimento máximo.

 

 