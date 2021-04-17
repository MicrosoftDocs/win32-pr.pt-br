---
description: SCONSOLEFALLBACKNAME de localidade \_
ms.assetid: 36465a1c-085f-4f80-ad3d-5be6eaefe943
title: LOCALE_SCONSOLEFALLBACKNAME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09536167c68a4ec9156a1558960c48778019ae97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761831"
---
# <a name="locale_sconsolefallbackname"></a>SCONSOLEFALLBACKNAME de localidade \_

**Windows Vista e posterior:** Localidade preferencial a ser usada para exibição do console. O número máximo de caracteres permitido para essa cadeia de caracteres é 85, incluindo um caractere nulo de terminação.

> [!Note]  
> Em geral, os aplicativos não devem fazer uso direto dos \_ dados de SCONSOLEFALLBACKNAME de localidade. Para determinar quais recursos de idioma usar em uma janela de console, um aplicativo deve chamar [SetThreadUILanguage](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) ou [SetThreadPreferredUILanguages](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages). Essas funções usam os dados de fallback do console como um fator para escolher uma linguagem que seja legível no console, mas não é o único determinante. Em particular, o console é limitado à exibição de caracteres de uma única página de código. Por exemplo, El-GR para grego (Grécia) é um idioma de console válido, mas se a página de código do console atual for Latin-1 (página de código 1252), o console exibirá o texto em grego principalmente como uma série de símbolos de caractere não encontrado.

 

Se o idioma correspondente a essa localidade tiver suporte no console, o valor será o mesmo que para a [localidade \_ SNAME](locale-sname.md), ou seja, a localidade em si poderá ser usada para exibição do console. No entanto, o console do não pode exibir idiomas que podem ser renderizados somente com o [Uniscribe](uniscribe.md). Por exemplo, o console do não pode exibir o árabe ou os vários idiomas índicos. Portanto, o \_ valor de SCONSOLEFALLBACKNAME de localidade para localidades correspondentes a esses idiomas é diferente do valor para a localidade \_ SNAME.

Para localidades predefinidas, se o valor de fallback for diferente do valor para a localidade em si, o valor da localidade neutra será usado. Uma localidade específica é associada a um idioma e a um país/região, enquanto uma localidade neutra é associada a um idioma, mas não está associada a nenhum país/região. Por exemplo, ar-SA retorna para "en", não para "en-US". Essa política de uso de localidades neutras é implementada consistentemente para localidades predefinidas e é altamente recomendável para localidades personalizadas. No entanto, a política não é imposta. Para uma localidade personalizada, seu aplicativo pode usar uma localidade específica em vez de uma localidade neutra como um fallback.

> [!Note]  
> Nenhuma das funções descritas na [chamada das funções "nome de localidade"](calling-the--locale-name--functions.md) aceita localidades neutras como entradas. Assim, \_ os dados de SCONSOLEFALLBACKNAME de localidade são de uso muito limitado. Em particular, nem [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) nem [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) aceita localidades neutras como entradas.

 

 

 



