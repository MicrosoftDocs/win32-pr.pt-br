---
description: Este tópico inclui instruções para usar as funções NLS em seus aplicativos para recuperar informações de data e hora, bem como dados de duração. Se seu aplicativo precisar manter dados, consulte usando dados de localidade persistente.
ms.assetid: 1880ff8f-110c-4661-8b1f-afe1d8d2a38d
title: Recuperando informações de data e hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f461f12cb1c6324892a415142c159ba570759128e61dd02b53a7cceebccc57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040406"
---
# <a name="retrieving-time-and-date-information"></a>Recuperando informações de data e hora

Este tópico inclui instruções para usar as funções NLS em seus aplicativos para recuperar informações de [data e hora](time-and-date.md) , bem como dados de duração. Se seu aplicativo precisar manter dados, consulte [usando dados de localidade persistente](using-persistent-locale-data.md).

**Windows Vista e posterior:** As funções discutidas neste tópico podem recuperar dados de [localidades personalizadas](custom-locales.md). Em particular, eles podem ser usados para personalizar formatos de data e hora. Por exemplo, é possível ter um formato de hora como "hhHmm'ss '", resultando em cadeias de caracteres de tempo como "12H34 ' 12 ' '".

## <a name="retrieve-time-information"></a>Recuperar informações de tempo

Seu aplicativo pode obter cadeias de caracteres para qualquer momento em um formato apropriado para a localidade atual usando as funções [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) e [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) . Qualquer função verifica cada um dos valores de tempo em uma estrutura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) válida para determinar que está dentro do intervalo de valores apropriado, ignorando as partes de data da estrutura. Se qualquer um dos valores de tempo estiver fora do intervalo correto, a função falhará com o parâmetro de erro de código \_ inválido \_ . A função não retorna nenhum erro para uma cadeia de caracteres de formato inválido, mas simplesmente forma a melhor cadeia de caracteres de tempo possível.

> [!Note]  
> As funções de tempo do NLS não incluem milissegundos como parte de uma cadeia de caracteres de hora formatada.

 

Para obter o formato de hora sem executar nenhuma formatação real, o aplicativo pode usar a função [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) , especificando a constante [ \_ STIMEFORMAT de localidade](locale-stime-constants.md) na chamada.

**Usar marcadores de tempo**

Exemplos de marcadores de tempo são "AM" e "PM" para inglês (Estados Unidos) e "de". e "du". para espanhol (México). Se o tempo \_ NOTIMEMARKER for especificado na chamada para [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) ou [**GetTimeFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex), a função removerá os separadores anteriores e após o marcador de tempo. Se um marcador de tempo existir e o \_ sinalizador NOTIMEMARKER de tempo não estiver definido na chamada, a função localizará o marcador de tempo com base no identificador de localidade especificado.

**Remover separadores que antecedem minutos e segundos**

Seu aplicativo pode chamar [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) ou [**GETTIMEFORMATEX**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) com \_ o tempo NOMINUTESORSECONDS ou o tempo de espera \_ especificado para remover os separadores que antecedem os elementos de minutos e/ou segundos.

**Usar formato de 24 horas**

Se seu aplicativo estiver dando suporte ao formato de 24 horas, ele poderá chamar [**GetTimeFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata) ou [**GETTIMEFORMATEX**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformatex) com o tempo \_ FORCE24HOURFORMAT. A menos que o \_ sinalizador time NOTIMEMARKER seja definido, a função exibe qualquer marcador de tempo existente.

## <a name="retrieve-date-information"></a>Recuperar informações de data

Um aplicativo pode recuperar cadeias de caracteres para qualquer data em um formato apropriado para a localidade atual usando as funções [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) e [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) . Qualquer função verifica cada um dos valores de data ano, mês, dia e dia da semana em uma estrutura [**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) válida, ignorando as partes de tempo da estrutura. O nome do dia, nome do dia abreviado, nome do mês e nome do mês abreviado são todos localizados com base no identificador de localidade. Se o dia da semana estiver incorreto, a função usará o valor correto e não retornará nenhum erro. Se qualquer um dos outros valores de data estiver fora do intervalo correto, a função falhará com o parâmetro de erro de código \_ inválido \_ . A função não retorna nenhum erro para uma cadeia de caracteres de formato inválido, mas simplesmente forma a melhor cadeia de caracteres de data possível.

Se o aplicativo exigir o formato de data para um calendário específico, ele deverá usar [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) ou [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex), passando o [**identificador de calendário**](calendar-identifiers.md)apropriado. Para retornar todos os formatos de data de um calendário específico, o aplicativo pode usar [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)ou [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex).

**Especificar um calendário alternativo**

O aplicativo pode chamar [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) ou [**GETDATEFORMATEX**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) com a data do sinalizador \_ use \_ ALT \_ Calendar para usar o formato padrão para o calendário alternativo especificado. Se não houver nenhum formato padrão para o calendário alternativo, a função usará as substituições do usuário.

Para obter o formato de data para um calendário alternativo, o aplicativo pode usar [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) com a constante [ \_ IOPTIONALCALENDAR de localidade](locale-ioptionalcalendar.md) .

**Especificar tipo de data**

Se o aplicativo quiser usar o formato de data abreviada, ele especificará \_ a data SHORTDATE na chamada para [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) ou [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex). Um formato de data por extenso pode ser obtido especificando \_ a data LONGDATE na chamada de função. Se nenhum sinalizador for especificado e o *lpFormat* for definido como **NULL**, a função usará Date \_ SHORTDATE como o padrão.

Para obter o formato de data abreviada e longa para o calendário de localidade padrão, o aplicativo deve usar a função [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) com a constante de [localidade \_ SSHORTDATE](locale-sshortdate.md) ou [localidade \_ SLONGDATE](locale-slongdate.md) .

**Especificar a imagem do formato de data**

O aplicativo pode especificar uma imagem de formato de data que [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) ou [**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex) usa para formar a cadeia de caracteres de data. Se o formato de data para a localidade especificada for necessário, o aplicativo poderá chamar a função com *lpFormat* definido como **NULL**. Se o parâmetro não estiver definido como **NULL**, a função usará a localidade somente para informações não especificadas na cadeia de caracteres de imagem de formato, por exemplo, os nomes de dia e mês para a localidade.

O aplicativo pode incluir qualquer texto que deva permanecer em sua forma exata entre aspas simples. Uma aspa simples também pode ser usada como um caractere de escape para permitir que a própria marca seja exibida na cadeia de caracteres de data. No entanto, a sequência de escape deve estar entre duas aspas simples. Por exemplo, para exibir a data como "Maio ' 93", a cadeia de caracteres de formato é: "MMMM ' ' ' ' AA".

## <a name="retrieve-duration-information"></a>Recuperar informações de duração

**Windows Vista e posterior:** As funções [**GetDurationFormat**](/windows/desktop/api/Winnls/nf-winnls-getdurationformat) e [**GetDurationFormatEx**](/windows/desktop/api/Winnls/nf-winnls-getdurationformatex) estão disponíveis para obter formatos de duração para localidades, incluindo localidades personalizadas. Para obter o formato de duração padrão para uma localidade, o aplicativo deve usar a função [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) com a constante [ \_ SDURATION de localidade](locale-sduration.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o suporte ao idioma nacional](about-national-language-support.md)
</dt> <dt>

[Data e hora](time-and-date.md)
</dt> <dt>

[Usando dados de localidade persistente](using-persistent-locale-data.md)
</dt> </dl>

 

 
