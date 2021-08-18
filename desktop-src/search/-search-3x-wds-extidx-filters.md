---
description: Saiba mais sobre as práticas recomendadas para criar manipuladores de filtro no Windows Search. A pesquisa usa filtros para extrair itens para inclusão em um índice de texto completo.
ms.assetid: 7b86a1b4-c8a9-400d-a9f1-a3b821c0269d
title: Práticas recomendadas para manipuladores de filtro na Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8320cf0f85bf86f7d61df09437271af67d0e4096fc3a917d037914854c9bad3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463695"
---
# <a name="best-practices-for-creating-filter-handlers-in-windows-search"></a>Práticas recomendadas para criar manipuladores de filtro na Windows Search

O Microsoft Windows Search usa filtros para extrair o conteúdo de itens para inclusão em um índice de texto completo. Você pode estender Windows Search para indexar tipos de arquivo novos ou proprietários escrevendo manipuladores de filtro para extrair o conteúdo e manipuladores de propriedades para extrair as propriedades dos arquivos. Os filtros são associados a tipos de arquivo, conforme denotado por extensões de nome de arquivo, tipos MIME ou CLSIDs (identificadores de classe). Embora um filtro possa lidar com vários tipos de arquivo, cada tipo funciona com apenas um filtro.

Este tópico contém as seguintes seções:

-   [Código nativo](#native-code)
-   [Práticas de código seguras para Windows Search](#secure-code-practices-for-windows-search)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="native-code"></a>Código nativo

No Windows 7 e posteriores, os filtros gravados em código gerenciado são explicitamente bloqueados. Os filtros DEVEM ser escritos em código nativo devido a possíveis problemas de versão do CLR com o processo em que vários complementos são executados.

## <a name="secure-code-practices-for-windows-search"></a>Práticas de código seguras para Windows Search

A seguir estão as práticas para escrever aplicativos seguros para uso com Windows Search.

**Para aplicativos de consulta:**

-   Ao escrever clientes de pesquisa, você deve escolher a API que é executado em um contexto de segurança que permita ao usuário o privilégio mínimo. Por exemplo, as páginas ASP podem usar o objeto de consulta IXSSO, que é executado como um processo de usuário.

**Para IFilters e recursos de linguagem:**

-   Se um novo manipulador de filtro para um tipo de arquivo estiver sendo instalado como uma substituição para um registro de filtro existente, o instalador deverá salvar o registro atual e restaurá-lo se o novo manipulador de filtros for desinstalado. Não há nenhum mecanismo para encadear filtros. Portanto, o novo manipulador de filtro é responsável por replicar qualquer funcionalidade necessária do filtro antigo.
-   IFilters, disjuntores de palavras e stemmers para Windows Search são executados no contexto de Segurança Local. Eles devem ser gravados para gerenciar buffers e empilhar corretamente. Todas as cópias de cadeia de caracteres devem ter verificações explícitas para proteger contra estouros de buffer. Você sempre deve verificar o tamanho alocado do buffer e testar o tamanho dos dados em relação ao tamanho do buffer. Estouros de buffer são uma técnica comum para explorar o código que não impõe restrições de tamanho do buffer.
-   [**Os componentes IFilter**](/windows/win32/api/filter/nn-filter-ifilter), de disjuntor de palavras e de stemmer nunca devem chamar a função [ExitProcess Function](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) ou uma API semelhante que encerra um processo e todos os seus threads.
-   Não alocar nem liberar recursos no ponto de entrada DllMain. Isso pode levar a falhas durante testes de estresse de baixo recurso.
-   Codificar todos os objetos para serem thread-safe. Windows A pesquisa chama qualquer instância de um disjuntor de palavras ou um stemmer em um thread por vez, mas pode chamar várias instâncias ao mesmo tempo em vários threads.
-   Evite criar arquivos temporários ou escrever no Registro.
-   Se você usar o Microsoft Visual C++, certifique-se de compilar seu aplicativo usando a **opção /GS.** A **opção /GS** é usada para detectar estouros de buffer. A opção /GS coloca verificações de segurança no código compilado. Para obter mais informações, consulte [DllGetClassObject Function](https://msdn.microsoft.com/library/8dbf701c(vs.71).aspx)GS (Verificação de Segurança de Buffer) na seção Visual C++ Opções do Compilador do  /  SDK da Plataforma.

## <a name="additional-resources"></a>Recursos adicionais

-   O [exemplo IFilterSample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample) demonstra como criar uma classe base IFilter para implementar a interface [**IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)
-   Para uma visão geral do processo de indexação, consulte [O processo de indexação](-search-indexing-process-overview.md).
-   Para uma visão geral dos tipos de arquivo, consulte [Tipos de arquivo](../shell/fa-file-types.md).
-   Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e Registro de Aplicativo.](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo manipuladores de filtro](-search-ifilter-conceptual.md)
</dt> <dt>

[Sobre manipuladores de filtro na Windows Search](-search-ifilter-about.md)
</dt> <dt>

[Retornando propriedades de um manipulador de filtro](-search-ifilter-property-filtering.md)
</dt> <dt>

[Manipuladores de filtros que são Windows](-search-ifilter-implementations.md)
</dt> <dt>

[Implementando manipuladores de filtro na Windows Search](-search-ifilter-constructing-filters.md)
</dt> <dt>

[Registrando manipuladores de filtro](-search-ifilter-registering-filters.md)
</dt> <dt>

[Testando manipuladores de filtro](-search-ifilter-testing-filters.md)
</dt> </dl>

 

 
