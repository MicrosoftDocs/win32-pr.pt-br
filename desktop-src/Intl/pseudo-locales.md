---
description: 'Windows Vista e posterior: o NLS define várias pseudovariáveis para uso, além das localidades existentes do Windows.'
ms.assetid: 8ec3038e-da18-47fc-a689-dd9162a41faa
title: Pseudo-Locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad7d4b161440cade65f24fb0157d42958c64d19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780136"
---
# <a name="pseudo-locales"></a>Pseudo-Locales

**Windows Vista e posterior:** O NLS define várias pseudovariáveis para uso, além das localidades existentes do Windows. Use essas pseudo-localidades para testar a localização de seus aplicativos. Para obter detalhes de implementação, consulte [usando Pseudo-Locales para teste de localização](using-pseudo-locales-for-localization-testing.md).

## <a name="supported-pseudo-locales"></a>Pseudo-Locales com suporte

As pseudo-localidades com suporte pelo NLS são:

-   Pseudo-localidade base
-   Pseudo-localidade espelhada (da direita para a esquerda)
-   Leste Asiático – pseudo-localidade do idioma

Escolha a pseudo-localidade específica a ser usada com base em suas atribuições de página de código e nas cadeias de caracteres para localização, por exemplo, nomes de mês, nomes de dias. Os dados de cada pseudo-localidade incluem não apenas as páginas de código relevantes e as cadeias de caracteres de dia e mês para localização, mas também dados para vários outros casos de teste para NLS. Os casos de teste examinam os seguintes tipos de dados:

-   [identificadores de localidade](locale-identifiers.md)de 9 bits. As pseudo-locais oferecem uma boa oportunidade para testar a operação de identificadores de localidade de 9 bits.
-   Cadeias de caracteres de idiomas que devem usar fontes pequenas. Devido a limitações na GDI (Graphics Device Interface), a fonte da interface do usuário para alguns idiomas é menor do que o ideal. As pseudovariáveis incluem várias cadeias de caracteres dessas linguagens, combinadas com cadeias de caracteres de linguagens com mais manipulação de fontes padrão. Você pode usar essas cadeias de caracteres no teste para determinar como uma fonte limitada por GDI é renderizada.
-   Comprimentos de cadeia de caracteres incomuns. Algumas constantes de informações de localidade, por exemplo, a [localidade \_ SLIST](locale-slist.md) e a [localidade \_ ICURRENCY](locale-icurrency.md), têm limites convencionais no tamanho da cadeia de caracteres. As pseudo-localidades dão suporte ao exame de comprimentos de cadeia de caracteres variados.
-   Classificações alternativas. As pseudovariáveis podem ser usadas para testar a funcionalidade de classificação alternativa quando o [identificador da ordem de classificação](sort-order-identifiers.md) alternativa difere do identificador de ordem de classificação base que geralmente está associado à localidade.

## <a name="pseudo-locale-names-and-identifiers"></a>Nomes e identificadores de pseudo-localidade

As pseudo-localidades têm [nomes de localidade](locale-names.md) que são escolhidos do espaço de uso privado para evitar conflitos com possíveis cadeias de caracteres introduzidas nos padrões organização internacional de normalização (iso) 639 e ISO 3166. Cada pseudo-localidade também tem seu próprio identificador de localidade. A tabela a seguir fornece os nomes e identificadores para os pseudo locais definidos.



| Pseudo-localidade       | Nome da localidade | Identificador de localidade |
|---------------------|-------------|-------------------|
| Base                | qps-ploc    | 0501              |
| Espelhado            | qps-plocm   | 09ff              |
| Leste Asiático-idioma | qps-ploca   | 05fe              |



 

## <a name="example"></a>Exemplo

O exemplo a seguir mostra o texto exibido para uma pseudo-localidade base:

\[Шěđлеśđαỳ!!! \] , 8 ōf \[ Μäŕςћ!! \] ōf 2006

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Localidades e idiomas](locales-and-languages.md)
</dt> <dt>

[Identificadores de localidade](locale-identifiers.md)
</dt> <dt>

[Nomes de localidade](locale-names.md)
</dt> <dt>

[Identificadores de ordem de classificação](sort-order-identifiers.md)
</dt> <dt>

[Usando Pseudo-Locales para teste de localização](using-pseudo-locales-for-localization-testing.md)
</dt> </dl>

 

 



