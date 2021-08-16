---
description: O termo &\# 0034; language&\# 0034; indica uma coleção de propriedades usadas em comunicação falada e escrita.
ms.assetid: 8214c00d-4ec6-4597-8088-7819a160f0dc
title: Localidades e idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462fc66a3296312de73a472309457e12954b6f30c80857594808350306bf4994
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147149"
---
# <a name="locales-and-languages"></a>Localidades e idiomas

O termo "Language" indica uma coleção de propriedades usadas em comunicação falada e escrita. Cada idioma tem um nome de idioma e um identificador de idioma que indicam a [página de código](code-pages.md) específica (ANSI, dos, Macintosh) usada para representar a [localização geográfica](table-of-geographical-locations.md) do idioma no sistema operacional. Uma linguagem neutra é indicada por um nome como "en" para inglês. Uma linguagem mais específica geograficamente pode ser indicada por um nome que inclui informações de localidade e país/região. Por exemplo, a localidade inglês (Estados Unidos) tem o nome da linguagem "en-US".

Uma "localidade" é uma coleção de informações de preferência do usuário relacionadas à linguagem representada como uma lista de valores. Windows o XP dá suporte a mais de 150 localidades e o Windows Vista dá suporte a aproximadamente 200. Cada localidade é definida por um idioma e uma ordem de classificação e tem um nome de localidade e um identificador de localidade. Um exemplo de um nome de localidade para alemão (Alemanha) é " \_ descatálogo de lista telefônica".

Cada sistema operacional tem pelo menos uma localidade instalada e, muitas vezes, tem muitas localidades das quais o usuário pode selecionar. Cada localidade tem uma variedade de informações associadas a ele, além de seu nome e identificador. Os tipos de informações de localidade são descritos nas [constantes de informações de localidade](locale-information-constants.md).

O sistema operacional atribui uma localidade a cada thread, inicialmente atribuindo a "localidade padrão do sistema", definida pelo [ \_ \_ padrão do sistema de localidade](locale-system-default.md). Essa localidade é definida quando o sistema operacional é instalado ou quando o usuário a seleciona usando a parte de opções regionais e de idiomas do painel de controle. Ao executar um thread em um processo que pertence ao usuário, o sistema operacional atribui a "localidade padrão do usuário" ao thread. Essa localidade é definida por [ \_ \_ padrão de usuário de localidade](locale-user-default.md). Um aplicativo pode substituir o padrão usando a função [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) para definir explicitamente a localidade para um thread.

A implementação de um idioma requer uma localidade correspondente. O sistema operacional implementa um idioma neutro, selecionando os dados para a localidade associada a uma versão específica do idioma, geralmente a localidade mais generalizada.

a partir do Windows Vista, é possível que uma linguagem específica corresponda a uma localidade suplementar, que é um tipo de localidade personalizada. Como as localidades complementares compartilham um único identificador de localidade, seus aplicativos devem lidar com essas localidades e os idiomas correspondentes por nome, em vez de por identificador.

Os conceitos de linguagem estão fortemente relacionados aos conceitos de localidade, mas os dois termos não são intercambiáveis. como regra geral, as funções relacionadas ao [Interface de Usuário Multilíngue](multilingual-user-interface.md) lidam com linguagens, enquanto as funções NLS agem sobre localidades.

Os tópicos a seguir são abordados nesta seção:

-   [Localidades personalizadas](custom-locales.md)
-   [Identificadores de idioma](language-identifiers.md)
-   [Nomes de idiomas](language-names.md)
-   [Identificadores de localidade](locale-identifiers.md)
-   [Nomes de localidade](locale-names.md)
-   [Pseudo-locais](pseudo-locales.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o suporte ao idioma nacional](about-national-language-support.md)
</dt> <dt>

[Páginas de código](code-pages.md)
</dt> <dt>

[Constantes de informações de localidade](locale-information-constants.md)
</dt> <dt>

[Interface do Usuário Multilíngue](multilingual-user-interface.md)
</dt> <dt>

[Tabela de localizações geográficas](table-of-geographical-locations.md)
</dt> <dt>

[Gerenciamento de idioma da interface do usuário](user-interface-language-management.md)
</dt> <dt>

[**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)
</dt> </dl>

 

 



