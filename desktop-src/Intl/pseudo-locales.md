---
description: 'Windows Vista e posterior: o NLS define várias pseudo-localidades para uso, além das localidades Windows existentes.'
ms.assetid: 8ec3038e-da18-47fc-a689-dd9162a41faa
title: Pseudo-Locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e099ee2af283c38aff3de7813fec64b5d43c6ac5873549856b27fd224c3e0d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390410"
---
# <a name="pseudo-locales"></a>Pseudo-Locales

**Windows Vista e posterior:** O NLS define várias pseudo-localidades para uso, além das localidades Windows existentes. Use essas pseudo-localidades para testar a localização de seus aplicativos. Para obter detalhes de implementação, [consulte Using Pseudo-Locales for Localization Testing](using-pseudo-locales-for-localization-testing.md).

## <a name="supported-pseudo-locales"></a>Suporte para Pseudo-Locales

As pseudo-localidades com suporte pelo NLS são:

-   Pseudo-localidade base
-   Pseudo-localidade espelhada (da direita para a esquerda)
-   Pseudo-localidade do leste da Ásia

Escolha a pseudo-localidade específica a ser usada com base em suas atribuições de página de código e nas cadeias de caracteres para localização, por exemplo, nomes de mês, nomes de dia. Os dados para cada pseudo-localidade incluem não apenas páginas de código relevantes e cadeias de caracteres de dia e mês para localização, mas também dados para vários outros casos de teste para NLS. Os casos de teste examinam os seguintes tipos de dados:

-   Identificadores de localidade de 9 [bits.](locale-identifiers.md) Pseudo-localidades fornecem uma boa oportunidade para testar a operação de identificadores de localidade de 9 bits.
-   Cadeias de caracteres de linguagens que devem usar fontes pequenas. Devido às limitações na GDI (interface do dispositivo gráfico), a fonte da interface do usuário para algumas linguagens é menor que a ideal. Pseudo-localidades incluem várias cadeias de caracteres dessas linguagens, combinadas com cadeias de caracteres de linguagens com manipulação de fontes mais padrão. Você pode usar essas cadeias de caracteres no teste para determinar como uma fonte limitada por GDI é renderiza.
-   Comprimentos de cadeia de caracteres incomuns. Algumas constantes de informações de localidade, por exemplo, [LOCALE \_ SLIST](locale-slist.md) e [ \_ ICURRENCY LOCALE](locale-icurrency.md), têm limites convencionais no tamanho da cadeia de caracteres. As pseudo-localidades suportam o exame de comprimentos variados de cadeia de caracteres.
-   Classificações alternativas. Pseudo-localidades podem ser usadas para testar a funcionalidade de classificação alternativa quando o identificador de ordem de classificação alternativo difere do [identificador](sort-order-identifiers.md) de ordem de classificação base que geralmente está associado à localidade.

## <a name="pseudo-locale-names-and-identifiers"></a>Nomes e identificadores de pseudo-localidade

As pseudo-localidades [](locale-names.md) têm nomes de localidade escolhidos no espaço de uso privado para evitar conflitos com possíveis cadeias de caracteres introduzidas nos padrões Organização Internacional de Normalização (ISO) 639 e ISO 3166. Cada pseudo-localidade também tem seu próprio identificador de localidade. A tabela a seguir fornece os nomes e identificadores para as pseudo-localidades definidas.



| Pseudo-localidade       | Nome da localidade | Identificador de localidade |
|---------------------|-------------|-------------------|
| Base                | qps-ploc    | 0501              |
| Espelhado            | qps-ltdcm   | 09ff              |
| Idioma do Leste da Ásia | qps-ltdca   | 05fe              |



 

## <a name="example"></a>Exemplo

O exemplo a seguir mostra o texto exibido para uma pseudo-localidade base:

\[ªª(a) !!! !!! , \] 8 ªf \[ Μªª!ªf \] 2006

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

 

 



