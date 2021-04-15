---
description: Manipuladores de filtro, que são implementações da interface IFilter, digitalizam documentos para texto e propriedades.
ms.assetid: 2ee9ea19-ae03-4f14-8f06-f8aa670e204e
title: Noções básicas sobre manipuladores de filtro no Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49cc1d3e479ae03645665618c60a33bdcfe19ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501478"
---
# <a name="understanding-filter-handlers-in-windows-search"></a>Noções básicas sobre manipuladores de filtro no Windows Search

Manipuladores de filtro, que são implementações da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , digitalizam documentos para texto e propriedades. Os manipuladores de filtro extraem partes de texto desses itens, filtrando a formatação inserida e mantendo as informações sobre a posição do texto. Eles também extraem partes de valores, que são propriedades do documento. O **IFilter** é a base para a criação de aplicativos de nível superior, como indexadores de documentos e visualizadores independentes de aplicativos.

Este tópico é organizado da seguinte maneira:

- [Sobre a interface do IFilter](#about-the-ifilter-interface)
  - [Processo de isolamento](#isolation-process)
  - [DLLs de IFilter](#ifilter-dlls)
  - [Estrutura do IFilter](#ifilter-structure)
  - [Código nativo](#native-code)
- [Encontrando o identificador de classe IFilter](#finding-the-ifilter-class-identifier)
  - [Identificadores de código IFilter:: GetChunk e locale](#ifiltergetchunk-and-locale-code-identifiers)
- [Recursos adicionais](#additional-resources)
- [Tópicos relacionados](#related-topics)

## <a name="about-the-ifilter-interface"></a>Sobre a interface do IFilter

O Microsoft Windows Search usa filtros para extrair o conteúdo de itens para inclusão em um índice de texto completo. Você pode estender o Windows Search para indexar tipos de arquivo novos ou proprietários escrevendo filtros para extrair o conteúdo e os manipuladores de propriedade para extrair as propriedades dos arquivos.

A interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) foi projetada para atender às necessidades específicas de mecanismos de pesquisa de texto completo. Os mecanismos de pesquisa de texto completo, como o Windows Search, chamam os métodos **IFilter** para extrair informações de texto e propriedade e adicioná-las a um índice. O Windows Search interrompe os resultados do método [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) retornado em palavras, normaliza-os e salva-os em um índice. Se estiver disponível, o mecanismo de pesquisa usará o LCID (identificador de código de idioma) de uma parte de texto para executar a quebra e a normalização de palavras específicas ao idioma.

O Windows Search usa três funções, descritas na tabela a seguir, para acessar manipuladores de filtro registrados (implementações da interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ). Essas funções são especialmente úteis ao carregar e associar ao manipulador de filtro de um objeto incorporado.

| Função               | Descrição                                                                                                                                                                                               |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Loadifilter            | Obtém um ponteiro para o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) que é mais adequado para o tipo de conteúdo especificado.                                                                                            |
| BindIFilterFromStorage | Obtém um ponteiro para o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) que é mais adequado para o conteúdo contido em um objeto de [interface IStorage](/windows/win32/api/objidl/nn-objidl-istorage) . |
| BindIFilterFromStream  | Obtém um ponteiro para o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) que é mais adequado para um identificador de classe especificado (CLSID) recuperado de uma variável de fluxo.                                                 |

A interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) tem cinco métodos, descritos na tabela a seguir.

| Método                                                    | Descrição                                                                                                        |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init)          | Inicializa uma sessão de filtragem.                                                                                   |
| [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk)     | Posiciona o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) no início da primeira ou da próxima parte e retorna um descritor. |
| [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext)       | Recupera o texto da parte atual.                                                                             |
| [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue)     | Recupera valores da parte atual.                                                                           |
| [**IFilter:: BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) | Recupera uma interface que representa a parte especificada do objeto. Reservado para uso futuro.                      |

### <a name="isolation-process"></a>Processo de isolamento

O Windows Search executa IFilters no contexto de segurança do sistema local com direitos restritos. Nesse processo de isolamento do host do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , vários direitos são removidos:

- Código restrito
- Todos
- Local
- Interativo
- Usuários Autenticados
- Usuários internos
- SID (identificador de segurança) dos usuários

A remoção desses direitos significa que a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) não tem acesso ao sistema de disco ou à rede ou a nenhuma interface do usuário ou funções da área de transferência. Além disso, o processo de isolamento é executado em um objeto de trabalho que impede que processos filho sejam criados e impõe um limite de 100 MB no conjunto de trabalho. o processo de isolamento de host da interface do **IFilter** aumenta a estabilidade da plataforma de indexação, devido à possibilidade de filtros de terceiros implementados incorretamente.

> [!NOTE]  
> Os manipuladores de filtro devem ser gravados para gerenciar buffers e empilhar corretamente. Todas as cópias de cadeia de caracteres devem ter verificações explícitas para proteção contra estouros de buffer. Você sempre deve verificar o tamanho alocado do buffer. Você deve sempre testar o tamanho dos dados em relação ao tamanho do buffer.

### <a name="ifilter-dlls"></a>DLLs de IFilter

[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) As DLLs implementam a interface **IFilter** para permitir que um cliente extraia informações de valor de texto e propriedade de um tipo de arquivo, classe ou tipo percebido. O processo de filtragem da pesquisa do Windows **SearchFilterHost.exe** é associado ao **IFilter** registrado para a classe, o tipo percebido ou a extensão de nome do item.

### <a name="ifilter-structure"></a>Estrutura do IFilter

Cada [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) é um arquivo dll que implementa um servidor com (Component Object Model em processo) para fornecer os recursos de filtragem especificados. A figura a seguir ilustra o mostra a estrutura geral de uma dll **IFilter** típica. Um exemplo mais complexo poderia implementar mais de uma classe **IFilter** .

![diagrama da estrutura de uma DLL de IFilter típica](images/ifilter-structure.png)

### <a name="native-code"></a>Código nativo

Os filtros devem ser escritos em código nativo devido a problemas de controle de versão do CLR (Common Language Runtime potencial) com o processo em que vários suplementos são executados. No Windows 7 e posterior e posterior, os filtros gravados em código gerenciado são explicitamente bloqueados.

## <a name="finding-the-ifilter-class-identifier"></a>Encontrando o identificador de classe IFilter

A classe da dll do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) é registrada na chave do registro PersistentHandler. O exemplo a seguir, para arquivos HTML, ilustra como encontrar a DLL do **IFilter** para um documento HTML. Este exemplo segue a lógica semelhante à usada pelo sistema para localizar o **IFilter** associado a um item.

1. Verifique se a extensão do tipo de arquivos que a DLL filtra tem um PersistentHandler registrado na entrada do registro \\ HKEY \_ local \_ Machine \\ software \\ classes. Deixe essa chave ser `Value1` . Se essa entrada já existir, pule para a etapa 4 deste procedimento e use essa `Value1` chave. Os valores são do tipo REG \_ sz.

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

2. Como alternativa, se não houver um PersistentHandler registrado para a extensão, localize o CLSID associado ao tipo de documento na entrada do registro \\ HKEY \_ local \_ Machine \\ software \\ classes. Deixe essa chave ser `Value2` .

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                 = Class for WWW HTML files
                CLSID
                   {25336920-03F9-11CF-8FD0-00AA00686F13}
```

3. Determine se um PersistentHandler está registrado para o CLSID. Usando `Value2` determinado na etapa 2, localize o PersistentHandler para a \\ entrada do ' hKey \_ local \_ Machine \\ software \\ classes \\ CLSID \\ value2. Deixe essa chave ser `Value3` .

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                 = Class for WWW HTML files
                PersistentHandler
                   {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. Determine o GUID do manipulador persistente do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Usando `Value1` e `Value3` , localize o GUID do manipulador persistente do **IFilter** para o tipo de documento. O valor na entrada do registro \\ HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID \\ Value1 ou 3 \\ PersistentAddinsRegistered \\ 89BCB740-6119-101A-BCB7-00DD010655AF "/> produz o GUID de PersistentHandler do **IFilter** para esse tipo de documento. Deixe essa chave ser `Value4` . Neste exemplo, o GUID da interface do **IFilter** é 89BCB740-6119-101A-BCB7-00DD010655AF.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {EEC97550-47A9-11CF-B952-00AA0051FE20}
                 = HTML File Persistent Handler
                    Data type         REG_SZ
                        PersistentAddinsRegistered
                        {89BCB740-6119-101A-BCB7-00DD010655AF}

                    Data type         REG_SZ
                        default = {E0CA5340-4534-11CF-B952-00AA0051FE20}
```

> [!NOTE]  
> Neste exemplo, a DLL do [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) para documentos HTML é nlhtml.dll.

### <a name="ifiltergetchunk-and-locale-code-identifiers"></a>Identificadores de código IFilter:: GetChunk e locale

O LCID do texto pode ser alterado em um único arquivo. Por exemplo, o texto de um manual de instrução pode alternar entre inglês (en-US) e espanhol (es) ou o texto pode incluir uma única palavra em um idioma diferente do idioma principal. Em ambos os casos, o [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) deve iniciar uma nova parte sempre que o LCID for alterado. Como o LCID é usado para escolher um separador de palavras apropriado, é muito importante que você o identifique corretamente. Se o **IFilter** não puder determinar a localidade do texto, ele deverá retornar um LCID de zero com a parte. Retornar um LCID de zero faz com que o Windows Search use a tecnologia de detecção automática de idioma (LAD) para determinar a ID de localidade da parte. Se o Windows Search não conseguir encontrar uma correspondência, o padrão será a localidade padrão do sistema (chamando a função de [função GetSystemDefaultLocaleName](/windows/win32/api/winnls/nf-winnls-getsystemdefaultlocalename) ). Para obter mais informações, consulte [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk), [**partes \_ breaktype**](/windows/win32/api/filter/ne-filter-chunk_breaktype), [**chunkstate**](/windows/win32/api/filter/ne-filter-chunkstate)e [**a \_ parte stat**](/windows/win32/api/filter/ns-filter-stat_chunk).

Se você controlar o formato de arquivo e ele não contiver informações de localidade, você deverá adicionar um recurso de usuário para habilitar a identificação de localidade adequada. O uso de um separador de palavras incompatível pode resultar em uma experiência de consulta ruim para o usuário. Para obter mais informações, consulte [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker).

> [!NOTE]  
> Os filtros são associados a tipos de arquivo, como indicado por extensões de nome de arquivo, tipos de MIME ou CLSIDs. Embora um filtro possa lidar com vários tipos de arquivo, cada tipo funciona com apenas um filtro.

## <a name="additional-resources"></a>Recursos adicionais

- O exemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponível no [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample7), demonstra como criar uma classe base IFilter para implementar a interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Para obter uma visão geral do processo de indexação, consulte [o processo de indexação](-search-indexing-process-overview.md).
- Para obter uma visão geral dos tipos de arquivo, consulte [tipos de arquivo](../shell/fa-file-types.md).
- Para consultar atributos de associação de arquivo para um tipo de arquivo, consulte [PerceivedTypes, SystemFileAssociations e registro de aplicativo](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Tópicos relacionados

[Desenvolvendo manipuladores de filtro](-search-ifilter-conceptual.md)

[Práticas recomendadas para a criação de manipuladores de filtro no Windows Search](-search-3x-wds-extidx-filters.md)

[Retornando Propriedades de um manipulador de filtro](-search-ifilter-property-filtering.md)

[Manipuladores de filtro que acompanham o Windows](-search-ifilter-implementations.md)

[Implementando manipuladores de filtro no Windows Search](-search-ifilter-constructing-filters.md)

[Registrando manipuladores de filtro](-search-ifilter-registering-filters.md)

[Testando manipuladores de filtro](-search-ifilter-testing-filters.md)
