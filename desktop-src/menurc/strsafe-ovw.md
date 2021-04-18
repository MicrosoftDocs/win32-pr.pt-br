---
title: Sobre o strsafe. h
description: A manipulação de buffer insatisfatório é incomplicada em muitos problemas de segurança que envolvem saturações de buffer.
ms.assetid: a104a260-1edb-441a-acf8-e2bd3a7d8235
keywords:
- funções de cadeia de caracteres
- Strsafe. h
- Funções strsafe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9b993ccff6d085f3b1eb14c1920c4c633661df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105810882"
---
# <a name="about-strsafeh"></a>Sobre o strsafe. h

A manipulação de buffer insatisfatório é incomplicada em muitos problemas de segurança que envolvem saturações de buffer. As funções definidas em strsafe. h fornecem processamento adicional para a manipulação de buffer adequada em seu código. Por esse motivo, eles devem substituir suas contrapartes C/C++ internas, bem como implementações específicas do Windows. O strsafe. h está disponível na SDK do Windows a partir do Windows XP com Service Pack 2 (SP2).

As vantagens das funções strsafe incluem:

-   O tamanho do buffer de destino é sempre fornecido para a função para garantir que a função não seja gravada após o final do buffer.

-   Os buffers têm a garantia de serem terminados em nulo, mesmo se a operação truncar o resultado pretendido.

-   Todas as funções retornam um valor **HRESULT** , com apenas um possível código de êxito (**S \_ OK**).

-   Cada função está disponível em uma versão de contagem de caracteres ("cch") ou de contagem de bytes ("CB") correspondente.

-   A maioria das funções tem uma versão estendida ("ex") disponível para funcionalidade avançada.

Confira as seções a seguir para obter detalhes.

-   [Funções de contagem de caracteres](#character-count-functions)
-   [Funções de contagem de bytes](#byte-count-functions)
-   [Usando strsafe. h](#using-strsafeh)
-   [Tópicos relacionados](#related-topics)

## <a name="character-count-functions"></a>Funções de contagem de caracteres

As funções a seguir usam uma contagem de caracteres, em vez de uma contagem de bytes.



| Função                                                                                                                                                                                                                      | Substituto                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>[**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)</dt> <dt> [ **StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)</dt> </dl>                 | <dl> <dt>[strcat, wcscat, \_ tcsat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019)</dt> <dt>[**lstrcat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata)</dt> <dt>[**strcat**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatw)</dt> <dt>[**StrCatBuff**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatbuffa)</dt> </dl>                                                                             |
| <dl> <dt>[**StringCchCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)</dt> <dt> [ **StringCchCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)</dt> </dl>             | <dl> <dt>[strncat](/cpp/c-runtime-library/reference/strncat-strncat-l-wcsncat-wcsncat-l-mbsncat-mbsncat-l?view=vs-2019)</dt> <dt> [ **strncat**](/windows/desktop/api/shlwapi/nf-shlwapi-strncata)</dt> </dl>                                                                                                                                                                                                                                                                   |
| <dl> <dt>[**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)</dt> <dt> [ **StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)</dt> </dl>             | <dl> <dt>[strcpy, wcscpy, \_ tcscpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019)</dt> <dt>[**lstrcpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya)</dt> <dt>[**strcpy**](/windows/desktop/api/shlwapi/nf-shlwapi-strcpyw)</dt> </dl>                                                                                                                                                                    |
| <dl> <dt>[**StringCchCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)</dt> <dt> [ **StringCchCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)</dt> </dl>         | <dl> <dt>[strncpy, wcsncpy, \_ tcsncpy](/cpp/c-runtime-library/reference/strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>[**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)</dt> <dt> [ **StringCchGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)</dt> </dl>             | <dl> <dt>[Gets, \_ getws, \_ getts](/cpp/c-runtime-library/gets-getws?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>[**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)</dt> <dt> [ **StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)</dt> </dl>     | <dl> <dt>[sprintf, swprintf, \_ doprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)</dt> <dt>[**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)</dt> <dt>[**wnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wnsprintfa)</dt> <dt>[ \_ snprintf, \_ snwprintf, \_ sntprintf](/cpp/c-runtime-library/reference/snprintf-snprintf-snprintf-l-snwprintf-snwprintf-l?view=vs-2019)</dt> </dl>          |
| <dl> <dt>[**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)</dt> <dt> [ **StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)</dt> </dl> | <dl> <dt>[vsprintf, vswprintf, \_ vstprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019)</dt> <dt>[vsnprintf, \_ vsnwprintf, \_ vsntprintf](/cpp/c-runtime-library/reference/vsnprintf-vsnprintf-vsnprintf-l-vsnwprintf-vsnwprintf-l?view=vs-2019)</dt> <dt>[**wvsprintf wvnsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa)</dt> <dt>[](/windows/desktop/api/shlwapi/nf-shlwapi-wvnsprintfa)</dt> </dl>, |
| <dl> <dt>[**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)</dt> </dl>                                                                                                         | <dl> <dt>[strlen, wcslen, \_ tcslen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="byte-count-functions"></a>Funções de contagem de bytes

As funções a seguir usam uma contagem de bytes em vez de uma contagem de caracteres.



| Função                                                                                                                                                                                                                  | Substituto                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>[**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)</dt> <dt> [ **StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)</dt> </dl>                 | <dl> <dt>[strcat, wcscat, \_ tcsat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019)</dt> <dt>[**lstrcat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata)</dt> <dt>[**strcat**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatw)</dt> <dt>[**StrCatBuff**](/windows/desktop/api/shlwapi/nf-shlwapi-strcatbuffa)</dt> </dl>                                                                            |
| <dl> <dt>[**StringCbCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)</dt> <dt> [ **StringCbCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)</dt> </dl>             | <dl> <dt>[strncat](/cpp/c-runtime-library/reference/strncat-strncat-l-wcsncat-wcsncat-l-mbsncat-mbsncat-l?view=vs-2019)</dt> <dt> [ **strncat**](/windows/desktop/api/shlwapi/nf-shlwapi-strncata)</dt> </dl>                                                                                                                                                                                                                                                                  |
| <dl> <dt>[**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)</dt> <dt> [ **StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)</dt> </dl>             | <dl> <dt>[strcpy, wcscpy, \_ tcscpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019)</dt> <dt>[**lstrcpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya)</dt> <dt>[**strcpy**](/windows/desktop/api/shlwapi/nf-shlwapi-strcpyw)</dt> </dl>                                                                                                                                                                   |
| <dl> <dt>[**StringCbCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)</dt> <dt> [ **StringCbCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)</dt> </dl>         | <dl> <dt>[strncpy, wcsncpy, \_ tcsncpy](/cpp/c-runtime-library/reference/strncpy-strncpy-l-wcsncpy-wcsncpy-l-mbsncpy-mbsncpy-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>[**StringCbGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)</dt> <dt> [ **StringCbGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)</dt> </dl>             | <dl> <dt>[Gets, \_ getws, \_ getts](/cpp/c-runtime-library/gets-getws?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>[**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)</dt> <dt> [ **StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)</dt> </dl>     | <dl> <dt>[sprintf, swprintf, \_ doprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)</dt> <dt>[**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)</dt> <dt>[**wnsprintf**](/windows/desktop/api/shlwapi/nf-shlwapi-wnsprintfa)</dt> <dt>[ \_ snprintf, \_ snwprintf, \_ sntprintf](/cpp/c-runtime-library/reference/snprintf-snprintf-snprintf-l-snwprintf-snwprintf-l?view=vs-2019)</dt> </dl>         |
| <dl> <dt>[**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)</dt> <dt> [ **StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)</dt> </dl> | <dl> <dt>[vsprintf, vswprintf, \_ vstprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019)</dt> <dt>[vsnprintf, \_ vsnwprintf, \_ vsntprintf](/cpp/c-runtime-library/reference/vsnprintf-vsnprintf-vsnprintf-l-vsnwprintf-vsnwprintf-l?view=vs-2019)</dt> <dt>[**wvsprintf wvnsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa)</dt> <dt>[](/windows/desktop/api/shlwapi/nf-shlwapi-wvnsprintfa)</dt> </dl> |
| <dl> <dt>[**StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)</dt> </dl>                                                                                                       | <dl> <dt>[strlen, wcslen, \_ tcslen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019)</dt> </dl>                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="using-strsafeh"></a>Usando strsafe. h

-   Para usar as funções strsafe embutidas, inclua o arquivo de cabeçalho, conforme mostrado aqui, seguindo as instruções **\# include** para todos os outros arquivos de cabeçalho.

    `#include <strsafe.h>`

-   Para usar as funções no formulário biblioteca, inclua a seguinte instrução antes de incluir strsafe. h. No entanto, é recomendável que você use as funções embutidas.

    `#define STRSAFE_LIB`

    > [!Note]  
    > : As funções a seguir devem ser usadas como funções embutidas: [**StringCbGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa), [**StringCbGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa), [**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)e [**StringCchGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa).

     

-   Quando você incluir strsafe. h em seu arquivo, as funções mais antigas substituídas pelas funções strsafe. h serão preteridas. As tentativas de usar essas funções mais antigas resultarão em um erro de compilador informando que você deve usar as funções mais recentes. Se você quiser substituir esse comportamento, inclua a seguinte instrução antes de incluir strsafe. h.

    `#define STRSAFE_NO_DEPRECATE`

-   Para permitir apenas funções de contagem de caracteres, inclua a seguinte instrução antes de incluir strsafe. h.

    `#define STRSAFE_NO_CB_FUNCTIONS`

-   Para permitir apenas funções de contagem de bytes, inclua a seguinte instrução antes de incluir strsafe. h.

    `#define STRSAFE_NO_CCH_FUNCTIONS`

    > [!Note]  
    > Você pode definir **STRSAFE \_ nenhuma \_ \_ função CB** ou **STRSAFE \_ nenhuma \_ \_ função cch**, mas não ambos.

     

-   Algumas funções do strsafe têm versões com reconhecimento de localidade. Por padrão, o cabeçalho não declara essas funções. Para habilitar essas declarações, inclua a seguinte instrução de macro antes de incluir strsafe. h.

    `#define STRSAFE_LOCALE_FUNCTIONS`

-   O tamanho máximo de cadeia de caracteres com suporte é 2.147.483.647 (**STRSAFE \_ Max \_ cch**) caracteres, ANSI ou Unicode.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções strsafe](string-overviews.md)
</dt> </dl>

 

 