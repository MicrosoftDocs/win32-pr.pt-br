---
description: SPARENT de localidade \_
ms.assetid: 3fa0bc36-7577-4b5a-b557-8ac42e8594a8
title: LOCALE_SPARENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11383e6fcdd216a1837d9f2f31e70a26821d394c3c56ea614b1df197bbe35c76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105916"
---
# <a name="locale_sparent"></a>SPARENT de localidade \_

**Windows Vista e posterior:** Localidade de fallback, usada pelo carregador de recursos. O número máximo de caracteres permitido para essa cadeia de caracteres é 85, incluindo um caractere nulo de terminação.

As localidades têm uma hierarquia na qual o pai de uma localidade específica é uma localidade neutra. Uma localidade específica é associada a um idioma e a um país/região, enquanto uma localidade neutra é associada a um idioma, mas não está associada a nenhum país/região. A localidade pai é usada para decidir o primeiro fallback a ser tentado quando um recurso para uma localidade específica não está disponível. Por exemplo, a localidade pai para "en-US" (0x0409) é "en" (0x0009). Quando um recurso não está disponível para a localidade "en-US" específica, o carregador de recursos volta a usar o recurso que está disponível para a localidade neutra "en". Consulte [Gerenciamento de idioma da interface do usuário](user-interface-language-management.md) para obter mais detalhes sobre a estratégia de fallback do carregador de recursos.

Esse padrão é consistente para localidades predefinidas. No entanto, a localidade pai não é determinada por qualquer manipulação do nome da localidade. Ou seja, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) e [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) não analisam uma cadeia de caracteres como "en-US" para obter o valor "en". Em vez disso, eles examinam os dados da localidade armazenada. Para localidades predefinidas, o valor segue o padrão esperado, no qual o pai de uma localidade específica é a localidade neutra correspondente e o pai de uma localidade neutra é a localidade invariável. Embora seja recomendável que as localidades personalizadas sigam uma estratégia semelhante em termos de definição de sua localidade pai, isso não é imposto. O aplicativo que implementa uma localidade personalizada pode especificar um pai menos apropriado.

> [!Note]  
> Como nenhuma das funções descritas na [chamada das funções "nome de localidade"](calling-the--locale-name--functions.md) aceita localidades neutras como entradas, essa localidade \_ SPARENT dados é de uso muito limitado. Em particular, nem [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) nem [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) aceita localidades neutras como entradas.

 

 

 



