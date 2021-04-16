---
description: Um nome de localidade é baseado nas convenções de marcação de idioma do RFC 4646 (Windows Vista e posterior) e é representado pela localidade \_ SNAME.
ms.assetid: 221aae7b-3a7c-4995-ae78-50d97de436d8
title: Nomes de localidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9808db94615cba4416c12995b9c969eaaf5a3fee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768739"
---
# <a name="locale-names"></a>Nomes de localidade

Um nome de [localidade](locales-and-languages.md) é baseado nas convenções de marcação de idioma do RFC 4646 (Windows Vista e posterior) e é representado pela [localidade \_ SNAME](locale-sname.md). Em geral, o padrão `<language>-<REGION>` é usado. Aqui, language é um código de linguagem ISO 639 de letras minúsculas. Os códigos de ISO 639-1 são usados quando disponíveis. Caso contrário, os códigos de ISO 639-2/T serão usados. REGIÃO especifica um identificador de país/região em maiúsculas ISO 3166-1. Por exemplo, o nome da localidade para inglês (Estados Unidos) é "en-US" e o nome da localidade para divehi (Maldivass) é "dv-MV".

> [!Note]  
> O [ \_ \_ \_ comprimento máximo do nome de localidade](locale-name-constants.md) da constante fornece o comprimento máximo de um nome de localidade. Ele inclui o espaço para um caractere nulo de terminação.

 

Se a localidade for uma localidade neutra (sem região), o valor de [ \_ SNAME de localidade](locale-sname.md) seguirá o padrão `<language>` . Se for uma localidade neutra para a qual o script é significativo, o padrão será `<language>-<Script>` .

Se uma localidade deve ser diferenciada de outra localidade para o mesmo idioma e região usando um script diferente, o \_ valor de SNAME de localidade segue o padrão `<language>-<Script>-<REGION>` , em que script é um código de script [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html) de letra maiúscula inicial. Por exemplo, o \_ valor de SNAME de localidade para a localidade especificada uzbeque (latino, Uzbequistão) é "uz-Latn-uz". O componente Script não é incluído nos casos em que uma linguagem é comumente gravada em apenas um script.

As ordens de classificação para localidades são designadas usando [identificadores de ordem de classificação](sort-order-identifiers.md), por exemplo, classificar \_ padrão. Para distinguir duas ou mais ordens de classificação para o mesmo idioma e região, o nome da localidade segue o padrão `<language>-<REGION>\_<sort order>` . Se você precisar distinguir o script e a ordem de classificação, o nome seguirá o padrão `<language>-<Script>-<REGION>\_<sort order>` . A ordem de classificação padrão nunca é especificada explicitamente, somente a ordem de classificação alternativa. Por exemplo, húngaro (Hungria) com um \_ padrão de classificação ou o padrão de classificação numérica de \_ húngaro equivalente \_ é designado "Hu-hu". Húngaro (Hungria) com classificação de ordem de classificação \_ \_ técnica húngaro é designado "HU-Hu \_ technl".

Para uma [localidade de substituição](custom-locales.md), o nome da localidade deve ser o mesmo que o nome da localidade que está sendo substituída. Para uma localidade suplementar, o nome da localidade deve seguir o padrão de `<language>-<REGION>-x-<custom>` ou `<language>-<Script>-<REGION>-x-<custom>` , em que `<custom>` é uma cadeia de caracteres alfanumérica específica para a localidade suplementar. Por exemplo, uma localidade suplementar específica para uma empresa chamada fabricam pode ser chamada "en-US-x-fabricam".

Um aplicativo pode recuperar os nomes de localidade atuais usando as funções [**GetSystemDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlocalename) e [**GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename) . Embora cada thread possa recuperar e definir seu próprio identificador de localidade com [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) e defini-lo com [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale), não há funções análogas para obter e definir a localidade por nome.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Localidades e idiomas](locales-and-languages.md)
</dt> <dt>

[Localidades personalizadas](custom-locales.md)
</dt> <dt>

[Identificadores de localidade](locale-identifiers.md)
</dt> <dt>

[Identificadores de ordem de classificação](sort-order-identifiers.md)
</dt> </dl>

 

 



