---
description: Este tópico fornece algumas instruções para lidar com localidades personalizadas em seus aplicativos.
ms.assetid: 2622e2b3-b952-4666-a440-85d73d11c5e0
title: Trabalhando com localidades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab0e59446496ae2985860c0fd6b1bd5bddde084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921203"
---
# <a name="working-with-custom-locales"></a>Trabalhando com localidades personalizadas

Este tópico fornece algumas instruções para lidar com [localidades personalizadas](custom-locales.md) em seus aplicativos. É melhor preparar todo o código-fonte com essas considerações em mente, pois seu aplicativo não controla se as localidades personalizadas estão instaladas no sistema operacional.

## <a name="handle-locale_stime-constant-correctly"></a>Manipular a \_ constante STIME de localidade corretamente

Se você tiver um aplicativo mais antigo que usa [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) para obter o separador de tempo obsoleto indicado pela [localidade \_ STIME](locale-stime-constants.md), o aplicativo poderá falhar ao analisar o formato de hora. Lembre-se de que o caractere que separa horas de minutos é diferente do caractere que separa minutos de segundos.

> [!Note]  
> Ao programar para localidades personalizadas, lembre-se de que elas são incomuns. Praticamente todos os campos disponíveis para NLS têm que lidar com comportamento incomum. Por exemplo, o formato de hora 12H34 ' 12 ' é legítimo e geralmente é compreensível. Ainda assim, muitos aplicativos fazem suposições sobre os separadores de tempo que podem interromper comprimentos de buffer ou campos de exibição.

 

## <a name="distinguish-among-supplemental-locales"></a>Distinguir entre as localidades complementares

Todas as localidades complementares usam a constante [ \_ \_ não especificada de localidade personalizada](locale-custom-constants.md) para o [identificador de localidade](locale-identifiers.md). Como regra, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) não pode distinguir entre localidades complementares, mas [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) pode usar nomes de [localidade](locale-names.md) em vez de identificadores de localidade. Seu aplicativo pode recuperar informações sobre uma localidade complementar específica somente quando essa localidade é a localidade do usuário selecionada no momento. Em seguida, o aplicativo pode chamar [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) e passar o [ \_ \_ padrão de usuário de localidade](locale-user-default.md) de constante como o identificador de localidade.

## <a name="handle-replacement-locales"></a>Manipular localidades de substituição

Para preservar a confiabilidade do Windows, lembre-se de que uma localidade de substituição com suporte do seu aplicativo não pode modificar o identificador de localidade da localidade substituída. Nenhuma localidade de substituição pode modificar as propriedades de classificação do Windows.

Embora uma localidade de substituição possa alterar o calendário padrão, ela deve manter o padrão original em algum lugar na lista de calendários disponíveis. Por exemplo, a localidade tailandesa (Tailândia) usa o calendário budista tailandês como padrão. Um administrador pode criar uma localidade de substituição que usa o calendário gregoriano localizado. No entanto, a lista de calendários disponíveis continua a conter uma entrada para o calendário budista tailandês.

Para localidades de substituição, o aplicativo geralmente deve consultar informações específicas de localidade em vez de tentar um "atalho" com base no conhecimento de uma determinada localidade. Por exemplo, quando [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) recupera a localidade atual como inglês (Estados Unidos), ela pode, na verdade, ser uma localidade de substituição que deve ter permissão para entrar em vigor.

## <a name="customize-calendars"></a>Personalizar calendários

Seus aplicativos podem personalizar os nomes de dia e mês para calendários gregorianos, mas não para calendários não gregorianos. Da mesma forma, o NLS não dá suporte à criação de calendários personalizados definidos pelo usuário. Para obter mais informações, consulte [data e calendário](date-and-calendar.md).

## <a name="handle-sorting-sequences"></a>Processar sequências de classificação

Uma localidade suplementar pode usar qualquer sequência de classificação definida pela Microsoft. Uma localidade de substituição deve usar a mesma sequência de classificação que a localidade que ele substitui. O NLS não oferece suporte à criação de sequências de classificação definidas pelo usuário. Para obter mais informações, consulte [lidando com a classificação em seus aplicativos](handling-sorting-in-your-applications.md).

## <a name="localize-custom-locale-information"></a>Localizar informações de localidade personalizada

O NLS não fornece um mecanismo para localizar informações de localidade personalizadas. Assim, a [localidade constante \_ SLANGUAGE](locale-slanguage.md) ou a [localidade \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md) usada como um identificador de localidade para uma localidade personalizada sempre recupera valores associados à [localidade \_ SNATIVELANGNAME](locale-snative-constants.md) ou à [ \_ SNATIVELANGUAGENAME de localidade](locale-snative-constants.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o suporte ao idioma nacional](using-national-language-support.md)
</dt> <dt>

[Localidades personalizadas](custom-locales.md)
</dt> <dt>

[Data e calendário](date-and-calendar.md)
</dt> <dt>

[Lidando com a classificação em seus aplicativos](handling-sorting-in-your-applications.md)
</dt> </dl>

 

 



