---
description: O Windows Vista apresenta um grande número de funções que usam nomes de localidade em vez de identificadores de localidade.
ms.assetid: e88c31b2-b1da-40ae-b512-67b8ad409b95
title: Chamando as funções de "nome de localidade"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58c15d2d9fe7721eb162f8c7cf96084bd4afa2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647062"
---
# <a name="calling-the-locale-name-functions"></a>Chamando as funções de "nome de localidade"

O Windows Vista apresenta um grande número de funções que usam [nomes de localidade](locale-names.md) em vez de [identificadores de localidade](locale-identifiers.md). Essas novas funções fornecem um bom suporte para [localidades complementares](custom-locales.md)e várias delas fornecem funcionalidade adicional não disponível nas funções NLS mais antigas. Alguns deles, como as novas funções de enumeração, também representam melhorias de design.

> [!Note]  
> Os aplicativos que se destinam a serem executados somente no Windows Vista e posterior devem usar as funções de "nome de localidade" em preferência às funções NLS que usam identificadores de localidade.

 

A tabela a seguir lista as funções de nome de localidade junto com as funções mais antigas que elas podem substituir.



| Funções usando nomes de localidade                                     | Funções usando identificadores de localidade                                                             |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**CompareStringEx**](/windows/desktop/api/Stringapiset/nf-stringapiset-comparestringex)                       | [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)                                                         |
| [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)             | [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [ **EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) |
| [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)               | [**EnumDateFormats**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa), [ **EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)     |
| [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)               | [**EnumSystemLocales**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesa)                                                 |
| [**EnumTimeFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumtimeformatsex)                   | [**EnumTimeFormats**](/windows/desktop/api/Winnls/nf-winnls-enumtimeformatsa)                                                     |
| [**FindNLSStringEx**](/windows/desktop/api/Winnls/nf-winnls-findnlsstringex)                       | [**FindNLSString**](/windows/desktop/api/Winnls/nf-winnls-findnlsstring)                                                         |
| [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)                   | [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)                                                     |
| [**GetCurrencyFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getcurrencyformatex)               | [**GetCurrencyFormat**](/windows/desktop/api/Winnls/nf-winnls-getcurrencyformata)                                                 |
| [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)                       | [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)                                                         |
| [**GetDurationFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getdurationformatex)               | [**GetDurationFormat**](/windows/desktop/api/Winnls/nf-winnls-getdurationformat)                                                 |
| [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)                       | [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)                                                         |
| [**GetNLSVersionEx**](/windows/desktop/api/Winnls/nf-winnls-getnlsversionex)                       | [**GetNLSVersion**](/windows/desktop/api/Winnls/nf-winnls-getnlsversion)                                                         |
| [**GetNumberFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getnumberformatex)                   | [**GetNumberFormat**](/windows/desktop/api/Winnls/nf-winnls-getnumberformata)                                                     |
| [**GetSystemDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlocalename) | [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid)                                           |
| [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex)                       | [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata)                                                         |
| [**GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename)     | [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid)                                               |
| [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)                   | [**IsValidLocale**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocale)                                                         |
| [**LCMapStringEx**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringex)                           | [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                                                             |



 

## <a name="example"></a>Exemplo

Um exemplo que mostra o uso de várias funções com base em nomes de localidade pode ser encontrado no [exemplo NLS: APIs baseadas em nome](nls--name-based-apis-sample.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o suporte ao idioma nacional](using-national-language-support.md)
</dt> </dl>

 

 
