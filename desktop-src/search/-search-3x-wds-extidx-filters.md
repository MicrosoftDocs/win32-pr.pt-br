---
description: Saiba mais sobre as práticas recomendadas para a criação de manipuladores de filtro no Windows Search. A pesquisa usa filtros para extrair itens para inclusão em um índice de texto completo.
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: Práticas recomendadas para manipuladores de filtro no Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a864cb2651d6236a212f3bf356eed3380869284
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989301"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a>Práticas recomendadas para a criação de manipuladores de filtro no Windows Search

O Microsoft Windows Search usa filtros para extrair o conteúdo de itens para inclusão em um índice de texto completo. Você pode estender o Windows Search para indexar tipos de arquivo novos ou proprietários, escrevendo manipuladores de filtro para extrair o conteúdo e manipuladores de propriedade para extrair as propriedades dos arquivos. Os filtros são associados a tipos de arquivo, como indicado pelas extensões de nome de arquivo, tipos MIME ou identificadores de classe (CLSIDs). Embora um filtro possa lidar com vários tipos de arquivo, cada tipo funciona com apenas um filtro.

Este tópico contém as seguintes seções:

-   [Código nativo](#native-code)
-   [Práticas de código seguro para o Windows Search](#secure-code-practices-for-windows-search)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="native-code"></a>Código nativo

No Windows 7 e posterior, os filtros gravados em código gerenciado são explicitamente bloqueados. Os filtros devem ser escritos em código nativo devido a possíveis problemas de controle de versão do CLR com o processo em que vários suplementos são executados.

## <a name="secure-code-practices-for-windows-search"></a>Práticas de código seguro para o Windows Search

Veja a seguir as práticas para escrever aplicativos seguros para uso com o Windows Search.

**Para aplicativos de consulta:**

-   Ao gravar clientes de pesquisa, você deve escolher a API que é executada em um contexto de segurança que permite ao usuário o privilégio mínimo. Por exemplo, as páginas ASP podem usar o objeto de consulta IXSSO, que é executado como um processo de usuário.

**Para IFilters e recursos de idioma:**

-   Se um novo manipulador de filtro para um tipo de arquivo estiver sendo instalado como uma substituição para um registro de filtro existente, o instalador deverá salvar o registro atual e restaurá-lo se o novo manipulador de filtro for desinstalado. Não há nenhum mecanismo para encadear filtros. Portanto, o novo manipulador de filtro é responsável por replicar qualquer funcionalidade necessária do filtro antigo.
-   IFilters, separadores de palavras e lematizadores para o Windows Search são executados no contexto de segurança local. Eles devem ser gravados para gerenciar buffers e para empilhar corretamente. Todas as cópias de cadeia de caracteres devem ter verificações explícitas para proteção contra estouros de buffer. Você sempre deve verificar o tamanho alocado do buffer e testar o tamanho dos dados em relação ao tamanho do buffer. Saturações de buffer são uma técnica comum para explorar o código que não impõe restrições de tamanho de buffer.
-   [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), separador de palavras e componentes de lematizador devem nunca chamar a função de [função ExitProcess](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) ou API semelhante que encerra um processo e todos os seus threads.
-   Não aloque ou libere recursos no ponto de entrada DllMain. Isso pode levar a falhas durante testes de estresse de recursos baixos.
-   Codifique todos os objetos a serem thread-safe. O Windows Search chama qualquer instância de um separador de palavras ou lematizador em um thread por vez, mas ele pode chamar várias instâncias ao mesmo tempo em vários threads.
-   Evite criar arquivos temporários ou gravar no registro.
-   Se você usar o compilador Microsoft Visual C++, certifique-se de compilar seu aplicativo usando a opção **/GS** . A opção **/GS** é usada para detectar saturações de buffer. A opção/GS coloca as verificações de segurança no código compilado. Para obter mais informações, consulte a [função DllGetClassObject](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)  / **GS** (verificação de segurança do buffer) na seção Opções do compilador Visual C++ do Platform SDK.

## <a name="additional-resources"></a>Recursos adicionais

-   O exemplo [IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) demonstra como criar uma classe base de IFilter para implementar a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
-   Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).
-   Para obter uma visão geral dos tipos de arquivo, consulte [tipos de arquivo](../shell/fa-file-types.md).
-   Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e registro de aplicativo](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo manipuladores de filtro](-search-ifilter-conceptual.md)
</dt> <dt>

[Sobre manipuladores de filtro no Windows Search](-search-ifilter-about.md)
</dt> <dt>

[Retornando Propriedades de um manipulador de filtro](-search-ifilter-property-filtering.md)
</dt> <dt>

[Manipuladores de filtro que acompanham o Windows](-search-ifilter-implementations.md)
</dt> <dt>

[Implementando manipuladores de filtro no Windows Search](-search-ifilter-constructing-filters.md)
</dt> <dt>

[Registrando manipuladores de filtro](-search-ifilter-registering-filters.md)
</dt> <dt>

[Testando manipuladores de filtro](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
