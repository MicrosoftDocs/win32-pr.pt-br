---
description: O Windows Search usa recursos de idioma como separadores de palavras e lematizadores para quebrar o texto em sua localidade nativa durante a criação do índice e o processamento de consultas.
ms.assetid: 6e8ab091-c22c-4425-b8b9-211d53816304
title: Estendendo recursos de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727f5812d0aee370c96d98f1c57dfffcbea5bc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765101"
---
# <a name="extending-language-resources"></a>Estendendo recursos de idioma

O Windows Search usa recursos de idioma como separadores de palavras e lematizadores para quebrar o texto em sua localidade nativa durante a criação do índice e o processamento de consultas. A Microsoft fornece separadores de palavras e lematizadores para vários idiomas. Esta seção descreve como implementar e usar separadores de palavras e lematizadores personalizados para idiomas e localidades além daqueles fornecidos pela Microsoft.

-   [Noções básicas sobre componentes de recursos de idioma](understanding-language-resource-components.md)
-   [Implementando um separador de palavras e lematizador](implementing-a-word-breaker-and-stemmer.md)
-   [Considerações lingüísticas e Unicode](linguistic-and-unicode-considerations.md)
-   [Solucionando problemas de recursos de idioma e práticas recomendadas](troubleshooting-language-resources.md)

## <a name="additional-resources"></a>Recursos adicionais

-   Para obter uma lista de lanuages com suporte de separadores de palavras, consulte [idiomas com suporte do Windows Search](-search-3x-wds-language-support.md).
-   Se você precisar identificar o idioma de uma parte do texto, poderá usar a detecção automática de idioma (LAD), que está disponível no Windows 7 e posterior. Para obter mais informações, consulte Els ( [Serviços lingüísticos estendidos](../intl/extended-linguistic-services.md) ).
-   Para obter a documentação de referência aplicável, consulte [interfaces de suplemento de dados](-search-data-addins-interfaces-entry-page.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciar o índice](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[Consulta do índice de maneira programática](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Estendendo o índice](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
